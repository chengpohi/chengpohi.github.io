---
description: with script syntax, support abstract and create common functions
---

# Script Syntax

## Variable

In **edql** we can define variable to control the context logics, if we need to query multi indexes with same query conditions, we can use variable as a **Query DSL Block** for these multiple actions, example:

```
function extractCodes() {
  POST my-index/_search
  {
    "size": 0,
    "aggs": {
      "t": {
        "terms": {
          "field": "title.keyword"
        }
      }
    }
  }
}
var p = jq(extractCodes(), "$.aggregations.t.buckets[*].key")
for (i in $p) {
  POST my-index/_search
  {
    "query": {
      "bool": {
        "must": [
          {
            "term": {
              "title.keyword": $i
            }
          }
        ]
      }
    },
  }
}
```

we define p variable for title keywords and extract it as array by **jq**, in for loop we iterate all keywords

## Function

**Function** is used to **abstract** the common logics and for building custom library for your own projects. such as data dictionary, common query logics for quickly query data and locate data issues.

### System Function

**System Function** is edql already defined functions for supporting file IO etc. example:

*   readJSON

    ```
    local p = readJSON("filename")
        
    ```

    read json file from file path
*   writeJSON

    ```
    writeJSON($p, "filename")
        
    ```

    write variable to file path
*   jq

    ```
    jq({"name": "edql"}, "$.name")
        
    ```

    used to extract json value as json type variable
* **TODO** readExcel
* **TODO** writeExcel

### Define Function

**Define Function** this is for user abstract common query logics, example:

```
function extractCodes() {
  POST my-index/_search
  {
    "size": 0,
    "aggs": {
      "t": {
        "terms": {
          "field": "title.keyword"
        }
      }
    }
  }
}
```

quickly aggregation current my index title keywords

## Import

## For Loop

## Comment

## Terms
