---
description: Elasticsearch GUI Client and Intellij Elasticsearch Plugin
---

# What is EDQL?

[Elasticsearch Query - EDQL ](https://plugins.jetbrains.com/plugin/16364-elasticsearch-query--edql/)is a very useful Elasticsearch GUI client for query and manage Elasticsearch or Opesearch cluster. Just run [Elasticsearch Query - EDQL](https://plugins.jetbrains.com/plugin/16364-elasticsearch-query--edql/versions) plugin with the one-click install on Intellij. Since it is script language, you can not only build your own query templates with function, variable, libraries, but also can do many types of simple or complex Elasticsearch queries with it. and EDQL is full compatible with official DSL API for all Elasticsearch versions, so it's easy for quick start.

{% embed url="https://plugins.jetbrains.com/embeddable/card/16364" %}
Install EDQL
{% endembed %}

## Core Features

1. Easy to Use: query by official DSL syntax
2. Visual query editor: visual query conditions and contexts
3. Manage query documents: add, delete, update and search document
4. Export query documents: download current query results or scroll download by query DSL
5. Query visualization: query documents as table, plot aggregations(line, bar, pie chart)
6. Multi authorizations support: Auth header, Basic Auth, Api Key and AWS Opensearch ApiKey
7. Support Elasticseaerch and AWS Opensearch connection
8. Manage Elasticsearch and Opensearch cluster: create index, add index and import documents etc
9. Intellij IDE language operations support: go to declaration, find usages, extract, autocomplete, highlight, live templates, folding/unfolding
10. Intellij IDE run support: run single request or run multiple requests
11. Program easily: Transfer/convert Query DSL to Java request cod
12. Script syntax: variable, function, iteration, collection, type

## Getting Started

Quickly review an Elasticsearch query example:&#x20;

* Query from localhost with port _9200_&#x20;
* Query index _**myindex**_ with custom source fields

```
#elasticsearch host
HOST http://localhost:9200
Authorization "Basic xxx"
local myindex = "myindex"
#display fields
local fields = [
  "a",
  "b",
  "c"
]
POST $myindex/_search
{
  "_source": $fields,
  "query": {
    "match_all": {}
  }
}
```

![](.gitbook/assets/new-demo.gif)

### Guides: Jump right in

Follow our handy guides to get started on the basics as quickly as possible:

{% content-ref url="guides/install-edql-on-intellij.md" %}
[install-edql-on-intellij.md](guides/install-edql-on-intellij.md)
{% endcontent-ref %}

{% content-ref url="guides/create-edql-script.md" %}
[create-edql-script.md](guides/create-edql-script.md)
{% endcontent-ref %}

{% content-ref url="guides/run-edql-request.md" %}
[run-edql-request.md](guides/run-edql-request.md)
{% endcontent-ref %}

### Use cases with EDQL

EDQL is not only target for query also can help solve multi scenarios problems, you could find use cases by:

{% content-ref url="use-cases/query-data.md" %}
[query-data.md](use-cases/query-data.md)
{% endcontent-ref %}

{% content-ref url="use-cases/analysis-data.md" %}
[analysis-data.md](use-cases/analysis-data.md)
{% endcontent-ref %}

{% content-ref url="use-cases/manage-cluster.md" %}
[manage-cluster.md](use-cases/manage-cluster.md)
{% endcontent-ref %}



### Explore More about EDQL Syntax

EDQL is a full features of script with compatible Elasticsearch Query DSL, and also support: function, variable, collection, type and iteration etc. explore more :

{% content-ref url="syntax/basic-syntax.md" %}
[basic-syntax.md](syntax/basic-syntax.md)
{% endcontent-ref %}

{% content-ref url="syntax/script-syntax.md" %}
[script-syntax.md](syntax/script-syntax.md)
{% endcontent-ref %}

{% content-ref url="syntax/glossary.md" %}
[glossary.md](syntax/glossary.md)
{% endcontent-ref %}
