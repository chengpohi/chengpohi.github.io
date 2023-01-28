---
description: Supercharge Elasticsearch query performance and manage Elasticsearch cluster.
---

# EDQL: Elasticsearch GUI Client by Intellij Plugin

[EDQL](https://plugins.jetbrains.com/plugin/16364-elasticsearch-query--edql/) is a query and management tool for Elasticsearch based on Intellij plugin platform. It has a simple graphical user interface for manage Elasticsearch clusters and query from Elasticsearch. &#x20;

{% hint style="info" %}
EDQL is cross platform since it's based on intellij, so we can use it on windows, linux or macos.
{% endhint %}

**The most important EDQL is full compatible with official Query DSL**, It means we can copy query DSL from tutorial and run without any extra effort. also EDQL has visual editor for quickly write query dsl with interactive UI.

> Elasticsearch Query DSL is complex, although we can use SQL or simple DSL directly query Elasticsearch, but in some time if we want to aggs data, further analysis or share Query DSL, it's hard to achieve.

**It** has powerful script engine: support function, variable and iteration etc. with intelligent Intellij you can easily write query DSL(autocomplete, refactor, live templates, extract etc).

For analysis aggregations, **EDQL** support plotting these aggregation results in intellij(find more: [visualize.md](ide-actions/visualize.md "mention")).

{% embed url="https://plugins.jetbrains.com/embeddable/card/16364" %}
Install It
{% endembed %}

## Feature Overview

<details>

<summary>Query</summary>

Query directly with official Query DSL without any other extra effort. so can quickly verify query conditions and examine data

</details>

<details>

<summary>Data Viewer</summary>

View query result as table mode, JSON mode, search, highlight, fields selection etc. and  modify, delete, new and export(scroll) documents on Data Viewer.

</details>

<details>

<summary>Management</summary>

Manage Elasticsearch connections: add, delete and modify connection, view index, templates, tasks and nodes etc. also can modify index and create new index.

</details>

<details>

<summary>Script Function</summary>

Works like a script with function, variable or iteration etc, so can quickly create your own query template or library for handling common use cases

</details>

## Getting Started

### 1. Connect to Elasticsearch

Connect to Elasticsearch by using EDQL Dock Manager, it's default **on the Intellij right side**. In the EDQL Dock Manager, you can **add a new connection to connect Elasticsearch and Test connectivity**.

![](.gitbook/assets/new-connection.gif)

### 2. Start New Query Console

After create and test a connection of Elasticsearch, you can create new query console on the Dock Toolbar with terminal icon:

```
POST myindex/_search
{
  "query": {
    "match_all": {}
  }
}
```

or

```
var myindex = "myindex"
#fields
var fields = [
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

> Query index _**myindex**_ with custom source fields

<figure><img src=".gitbook/assets/new-query-demo (1).gif" alt=""><figcaption></figcaption></figure>

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
