# What is EDQL?

[EDQL](https://plugins.jetbrains.com/plugin/16364-elasticsearch-query--edql/) is an Intellij Plugin for Query Elasticsearch, it’s fully compatible with Elasticsearch Query DSL syntax. It’s powerful for management ES documents and visualize views. such as: query result, aggregation result, export result, plot etc. Since it works as script language, you can build your own query templates with function, variable, library by using productivity Intellij IDE.&#x20;

## Core Features:

1. Query Elasticsearch with Query DSL
2. Manage query result, including: add, delete, update document
3. Visualize query result as compact table and table functions
4. Plot aggregation result: line chart
5. Download/Export query result by CSV, Raw JSON, Images
6. Elasticsearch Host bind and Authorization bind
7. Fully Intellij operations support: go to declaration, find usages, extract, autocomplete, highlight, live templates, folding/unfolding
8. Intellij Run Configurations: run single request or run multiple requests
9. Transfer/convert query DSL to Java request code
10. Shell script syntax: variable, function, iteration, collect, type

## Getting Started

**Got 2 minutes?** Quickly Review an Example:

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

Use cases with EDQL

With EDQL can help solve multi scenarios problem, you could find use cases by:

{% content-ref url="use-cases/query-data.md" %}
[query-data.md](use-cases/query-data.md)
{% endcontent-ref %}

{% content-ref url="use-cases/analysis-data.md" %}
[analysis-data.md](use-cases/analysis-data.md)
{% endcontent-ref %}

{% content-ref url="use-cases/manage-cluster.md" %}
[manage-cluster.md](use-cases/manage-cluster.md)
{% endcontent-ref %}
