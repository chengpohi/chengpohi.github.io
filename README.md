---
icon: home
description: Elasticsearch GUI on Intellij Plugin
---

# EDQL: Elasticsearch GUI on Intellij Plugin

[EDQL](https://plugins.jetbrains.com/plugin/16364-elasticsearch-query--edql/) is a management and query tool based on Intellij plugin platform for Elasticsearch. It has a simple graphical user interface for manage Elasticsearch clusters and query from Elasticsearch. &#x20;

**It is full compatible with official Query DSL**, can just copy query DSL and run on EDQL without any extra effort. also EDQL has visual editor for quickly write query conditions with interactive UI.

**It** has powerful script engine: support function, variable and iteration etc. with smart Intellij you can easily write query DSL(refactor, extract etc).

{% hint style="info" %}
EDQL is cross platform since it's based on cross platform
{% endhint %}

**It's full compatible with official Query DSL**, just copy query DSL and run on EDQL without any extra effort. also EDQL has visual editor for quickly write query conditions with interactive UI.

> Elasticsearch Query DSL is complex, although we can use SQL or simple DSL directly query Elasticsearch, but in some time if we want to aggs data, further analysis or share Query DSL, it's hard to achieve.

**It** has powerful script engine: support function, variable and iteration etc. with intelligent Intellij you can easily write query DSL(autocomplete, refactor, live templates, extract etc).

For analysis aggregations, **EDQL** support plotting these aggregation results in intellij(find more: [visualize.md](ide-actions/visualize.md "mention")).

{% embed url="https://plugins.jetbrains.com/embeddable/card/16364" %}

## Feature Overview

<details>

<summary>Query</summary>

Query directly with official Query DSL without any other extra effort. so can quickly verify query conditions and examine data

</details>

<details>

<summary>Data Viewer</summary>

management

</details>

<details>

<summary>Management</summary>

plot

</details>

<details>

<summary>Script Function</summary>



</details>



## Getting Started

Quick start on EDQL

### Create Connection by EDQL Dock Manager

## Create EDQL Query Console

Query index _**myindex**_ with custom source fields

```
local myindex = "myindex"
#fields
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

![](<.gitbook/assets/new-demo (1).gif>)

### Guides: Jump right in

Follow our handy guides to get started on the basics as quickly as possible:

{% content-ref url="introduction/install-edql-on-intellij.md" %}
[install-edql-on-intellij.md](introduction/install-edql-on-intellij.md)
{% endcontent-ref %}

{% content-ref url="introduction/create-edql-script.md" %}
[create-edql-script.md](introduction/create-edql-script.md)
{% endcontent-ref %}

{% content-ref url="introduction/run-edql-request.md" %}
[run-edql-request.md](introduction/run-edql-request.md)
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
