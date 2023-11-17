---
description: Intellij IDE support for EDQL DSL editor
---

# DSL Editor

##

<figure><img src="../.gitbook/assets/image (1) (1).png" alt=""><figcaption></figcaption></figure>

## File Template

## Live Templates

**EDQL** plugin already defined the common used Live Templates for intelligence, easily and quickly to write the request action or query conditions, so when input the below keyword, the Live Template will automatically expand.

Defined Live Templates:

*   search

    ```
    POST $EXPR$/_search
    {
      "query": {
        "bool": {
          "must": [
          ]
        }
      }
    }
        
    ```
*   term

    ```
    {
      "term": {
        "$EXPR$": "$V$"
      }
    },
        
    ```
*   clusterHealth

    ```
    GET _cluster/health
        
    ```
*   clusterStats

    ```
    GET _cluster/stats
        
    ```
*   catIndices

    ```
    GET _cat/indices?v
        
    ```
*   catHealth

    ```
    GET _cat/health?v
        
    ```
*   catNodes

    ```
    GET _cat/nodes?v
        
    ```
*   aggs

    ```
    "aggs": {
      "$E$": {
        $P$
      }
    }
        
    ```
*   term

    ```
    {
      "term": {
        "$EXPR$": "$V$"
      }
    },
        
    ```
*   terms

    ```
    {
      "terms": {
        "$EXPR$": [$V$]
      }
    }
        
    ```
*   bool

    ```
    "bool": {
      $EXPR$
    }
        
    ```
*   avg

    ```
    "aggregations": {
      "$P1$": {
        "avg": {
          "field": "$EXPR$"
       }
      }
    }
        
    ```
*   count

    ```
    GET $E$/_count
        
    ```
*   from

    ```
    "from": $EXPR$,
        
    ```
*   size

    ```
    "size": $EXPR$,
        
    ```
*   qbm

    ```
    {
      "query": {
        "bool": {
          "must": [
            $EXPR$
          ]
        }
      }
    }
        
    ```
*   qbf

    ```
    {
      "query": {
        "bool": {
          "filter": [
            $EXPR$
          ]
        }
      }
    }
        
    ```
*   script

    ```
    {
      "script": {
         "script": "$EXPR$"
      }
    },
        
    ```
*   range

    ```
    {
      "range": {
       "$EXPR$": {
        "gt": $E$,
        "lt": $A$,
       }
      }
    },
        
    ```
*   wildcard

    ```
    {
      "wildcard": {
        "$EXPR$": {
            "value": "*$K$*",
            "boost": 1.0,
        }
      }
    }
        
    ```
*   regexp

    ```
    {
      "regexp" : {
         "$EXPR$" : {
            "value" : "$V$",
          }
      }
    }
        
    ```
*   profile

    ```
    "profile": true,
        
    ```
*   explain

    ```
    "explain": true,
        
    ```
*   mapping

    ```
    GET $E$/_mapping
        
    ```
*   from

    ```
    "from": $EXPR$,
        
    ```
*   field

    ```
    "field": "$EXPR$"
        
    ```
*   sort

    ```
    "sort": [
      {
        "$EXPR$": {
          "order": "$F1$"
        }
      }
    ]
        
    ```
*   exists

    ```
    "exists": {
      "field": "$EXPR$"
    }
        
    ```
*   createIndex

    ```
    PUT /$EXPR$
    {
      "settings": {
      },
      "mappings": {
        "properties": {
            $A$
        }
      }
    }
        
    ```
*   getNodes

    ```
    GET /_nodes
        
    ```
*   source

    ```
    "_source": ["$EXPR$"],
        
    ```
*   tasks

    ```
    GET /_tasks
        
    ```
*   notEmpty

    ```
    {
      "regexp": {
        "$EXPR$": {
          "value": ".+",
        }
      }
    }
        
    ```
*   mustNot

    ```
    "must_not" : [
      $EXPR$
    ],
        
    ```
*   must

    ```
    "must" : [
      $EXPR$
    ],
        
    ```
*   filter

    ```
    "filter" : [
      $EXPR$
    ],
        
    ```
*   should

    ```
    "should" : [
      $EXPR$
    ],
        
    ```

## Highlight

**Highlight** includes two parts for edql, for now it supports:

1. highlight for reservered words
   * HOST
   * Authorization
   * local
   * …
2. highlight for key characters
   * brackets
   * number
   * comment
   * colon
   * …

**TODO**: In next step will try to support semantics hilightling

## Autocomplete

**Autocomplete** includes two ways autocomplete for edql:

1.  Keywords autocomplete

    Usually include the reserved words and keywords for edql, example: HOST, Authorization, POST, GET, DELETE, PUT, local etc
2.  Live Templates autocomplete

    Live Templates are defined for autocomplete the query dsl, example: qbm, qbf, size, terms, term, queryString, search etc

**TODO**: autocomplete auto integrates with the current dsl, such as remove extra bracket

## Refactor

**Refactor** is an import way for coding, for now edql supports: rename variable, rename function name

## Format

**Format** support to format **Query DSL** blocks, includes: function, variable, JSON block, array block etc. it’s a simple way to make code is clean
