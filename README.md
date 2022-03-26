# What is EDQL?

[Elasticsearch Query - EDQL ](https://plugins.jetbrains.com/plugin/16364-elasticsearch-query--edql/)is a very useful GUI client for query and manage Elasticsearch or AWS Opensearch cluster. Just run [Elasticsearch Query - EDQL](https://plugins.jetbrains.com/plugin/16364-elasticsearch-query--edql/versions) with the one-click install on IntelliJ. Since it is script language, you can not only build your own query templates with function, variable, libraries, but also can do many types of simple or complex Elasticsearch queries with it. and EDQL is full compatible with official DSL API for all Elasticsearch versions, so it's easy for quick start.

## Core Features

1. Easy to Use: query by official DSL syntax
2. Visual query editor: visual query conditions and contexts
3. Manage query documents: add, delete, update and search document
4. Export query documents: download current query results or scroll download by query DSL
5. Query visualization: query documents as table, plot aggregations(line, bar, pie chart)
6. Multi authorizations support: Auth header, Basic Auth, Api Key and AWS Opensearch ApiKey
7. Support Elasticseaerch and AWS Opensearch connection
8. Manage Elasticsearch and Opensearch cluster: create index, add index and import data etc
9. Intellij IDE language operations support: go to declaration, find usages, extract, autocomplete, highlight, live templates, folding/unfolding
10. Intellij IDE run support: run single request or run multiple requests
11. Program easily: Transfer/convert Query DSL to Java request cod
12. Script syntax: variable, function, iteration, collection, type

## Getting Started

Quickly Review an Query Example:&#x20;

* Query from localhost cluster with port _9200_&#x20;
* Query index _myindex_ with custom source fields

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

### Explore More about EDQL Syntax

EDQL is a full features of script and compatible with Elasticsearch Query DSL block, include: function, variable, iteration etc., explore more :

{% content-ref url="language-specification/glossary.md" %}
[glossary.md](language-specification/glossary.md)
{% endcontent-ref %}

{% content-ref url="language-specification/basic-syntax.md" %}
[basic-syntax.md](language-specification/basic-syntax.md)
{% endcontent-ref %}

{% content-ref url="language-specification/script-syntax.md" %}
[script-syntax.md](language-specification/script-syntax.md)
{% endcontent-ref %}

### Use cases with EDQL

With EDQL can help solve multi scenarios problems, you could find use cases by:

{% content-ref url="use-cases/query-data.md" %}
[query-data.md](use-cases/query-data.md)
{% endcontent-ref %}

{% content-ref url="use-cases/analysis-data.md" %}
[analysis-data.md](use-cases/analysis-data.md)
{% endcontent-ref %}

{% content-ref url="use-cases/manage-cluster.md" %}
[manage-cluster.md](use-cases/manage-cluster.md)
{% endcontent-ref %}
