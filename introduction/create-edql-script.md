---
description: Connect Elasticsearch and Query by EDQL
---

# Connect Elasticsearch and Query

## Connect to Elasticsearch

Connect to Elasticsearch by using EDQL Dock Manage default **on the Intellij right side**. In the EDQL Dock Manager, you can **add new connection to connect Elasticsearch and Test connection**.

View more on:

{% content-ref url="../ide-actions/dock-manager.md" %}
[dock-manager.md](../ide-actions/dock-manager.md)
{% endcontent-ref %}

## Query Console

After create and test a connection of Elasticsearch, you can create new query console on the Dock Toolbar with terminal icon

### Query by Visual Editor

After EDQL file is created, we can use the **Visual Editor** to configure an query action, since the common query conditions are annoying and boring.  Visual Editor is a powerful tool to visual query conditions and configurations, example: term match, range query, wildcard query and size, explan etc.

![](../.gitbook/assets/configure-by-dashboard.gif)

## EDQL Script

EDQL is based on **Intellij**, for different use cases there are two places to save new edql script:

* store on EDQL dock manager
* store on current project directory

### New EDQL by Dock Manager

EDQL manager dashboard is used to manage the EDQL files, it will share cross projects, so we can use this place to store the EDQL files that will be used anywhere.

it will auto fill the HOST, Timeout and Authorization with a simple EDQL Action, the EDQL file will be stored in the Manager like the Scratches files.

![](../.gitbook/assets/new-edql-by-manager.gif)

### New EDQL by New file

it will automatically load the EDQL file template, include: HOST, Timeout , Authorization and with a simple EDQL Query Action. this file will be stored on the current directory

![](../.gitbook/assets/new-edql-by-file.gif)

## Configurations

### HOST

HOST is target to Elasticsearch/Opensearch cluster **master host endpoint or gateway**

```
HOST http://127.0.0.1:9200
```

### KIBANA\_HOST

In some cases we can't directly connect to Elasticsearch Cluster host, only **Kibana** is exposed to use, in this case we can configure the KIBANA\_HOST to proxy query from Elasticsearch

```
KIBANA_HOST http://localhost:5601/
```

### Timeout

Timeout is used to configure every action request timeout, like query, write and delete etc

> **Caution**: this only limit the request timeout, not this action execute time.

```
Timeout 3000
```

### Authorization

If Elasticsearch/Opensearch cluster has configured **Authorization**, we need to configure the Authorization to connect Elasticsearch Cluster

> basic authorization, elastic cloud authorization, AWS credentials

#### Authorization header

```
HOST http://127.0.0.1:9200
Authorization "Bear xxx"
```

#### Basic Username and Password

```
HOST http://127.0.0.1:9200
Username "u"
Password "p"
```

#### ApiKey Credential

```
HOST http://127.0.0.1:9200
ApiKeyId "a"
ApiKeySecret "c"
```

#### AWS Credential

> aws has another configuration of aws region

```
HOST http://127.0.0.1:9200
AWSRegion "us-east"
ApiKeyId "c"
ApiKeySecret "c"
ApiSessionToken "c"
```

### Query Action

Elasticsearch query action include 4 parts:

* Query Methods: GET, POST, DELETE and PUT
* Query Index: the index name for query
* Query Type: _search,_ mapping
* Query Body: the JSON body for query conditions

```
POST my-index/_search

#OR

GET my-index/_mapping

#OR

GET _cluster/stats
```

### Query DSL Body

Query DSL body is same as the offcial Query DSL block: [QueryDSL](https://www.elastic.co/guide/en/elasticsearch/reference/current/query-dsl.html), it's a **JSON** format with the query configurations. since EDQL is based on Intellij, it supports autocomplete, format and live templates, example: qbm, range, wildcard etc.

```
POST my-index/_search
{
  "query": {
    "bool": {
      "must": [
        {
          "term": {
            "title.keyword": "DGS10"
          }
        }
      ]
    }
  }
}
```

![](../.gitbook/assets/new-visual.gif)
