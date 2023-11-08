# Aggregate

## Aggregations

Elasticsearch is good at analysising documents by using [**Aggreagation**](https://www.elastic.co/guide/en/elasticsearch/reference/current/search-aggregations.html) feature, for example: max, min, , mean or sum value etc. Aggregation has 3 aggregation categories, include: bucket, metrics and pipeline mode.&#x20;

EDQL fully support Elasticsearch Aggregation syntax for quickly statistic documents. and since it's based on Intellij platform, have built a lot of Aggregation templates for quickly write aggregation term, for example: max, min etc.&#x20;

```
POST my-index/_search
{
  "aggs": {
    "m": {
      "max": { // live template
        "field": "f"
      }
    }
  }
}
```

also EDQL support _function_ we can create the custom aggregation function as a aggregation shortcut for usage:

```
function sum(index, field) {
  POST $index/_search
  {
    "size": 0,
    "query": {},
    "aggs": {
      "sum": {
        "sum": {
          "field": $field
        }
      }
    }
  }
}

sum("my-index", "field")
```

## Plot and Visualize

In most time, we not only just want to statistic documents, also need to plot data, especially for time series, buckets or range aggregation result. EDQL support the plot syntax in Query Action, we can easily to plot Aggregation result with the custom chart parameters. also the chart is interactive, can be used to deeper analysis or mark.

> This example aggregation by time with week and month interval, we configure visualization by plot configure, include two line: ff and tt with x axis and y axis, set the chart type as line. after  run this Query Action, we can use the Run Result window to display these charts and interactive include: zoom, selective, filter or marker etc

```
POST my-index/_search
{
  "plot": {
    "data": [
      {
        "x": "ff.buckets.key_as_string",
        "y": "ff.buckets.doc_count",
        "type": "line"
      },
      {
        "x": "tt.buckets.key_as_string",
        "y": "tt.buckets.doc_count",
        "type": "line"
      }
    ]
  },
  "query": {
    "bool": {
    }
  },
  "sort": [
    {
      "create_time": {
        "order": "desc"
      }
    }
  ],
  "size": "0",
  "aggs": {
    "ff": {
      "date_histogram": {
        "field": "update_time",
        "calendar_interval": "week"
      }
    },
    "tt": {
      "date_histogram": {
        "field": "update_time",
        "calendar_interval": "month"
      }
    }
  }
}
```

See more on:

{% content-ref url="../ide-actions/data-browser.md" %}
[data-browser.md](../ide-actions/data-browser.md)
{% endcontent-ref %}
