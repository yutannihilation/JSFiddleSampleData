This is test data for [JSFiddle Github API](http://doc.jsfiddle.net/use/github_response.html#github-response).

A sample dataset in `datasets` package is converted as JSON format by following commands:

```R
library(xts)
library(jsonlite)

data_xts <- as.xts(nhtemp)
data_df <- data.frame(date = time(data_xts), value=coredata(data_xts))
cat(toJSON(data_df, pretty = TRUE), file = "demo.response.json")
```