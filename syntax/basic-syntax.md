---
description: basic EDQL syntax for help quickly use EDQL
---

# Basic Syntax

## Connection

When firstly prepare to query from **Elasticsearch**, we need to configure how to connect the **Elasticsearch cluster**

### Authorization

If the **Elasticsearch Cluster** needs **authorization** to connect, configure authorization, there are three ways to achieve
that.

#### Authorization Header

If **Elasticsearch Cluster** supports http basic **Authorization** header, we can configure **Authorization** header
directly by:

```
Authorization "Basic <token>"
```

The **token** should compute by base64 with username and password, see
more: [HTTP/REST clients and security](https://www.elastic.co/guide/en/elasticsearch/reference/current/security-clients-integrations.html)
and [Elasticsearch Token Service tokens](https://www.elastic.co/guide/en/elasticsearch/client/java-rest/current/\_other\_authentication\_methods.html#\_elasticsearch\_token\_service\_tokens)

#### Basic Username and Password

For if you don’t want use **Authorization** header, you can directly use the reserverd words **Username** and **Password
** to configure the **Authorization**:

```
Username "username"
Password "password"
```

see
more: [Basic Authentication](https://www.elastic.co/guide/en/elasticsearch/client/java-rest/current/\_basic\_authentication.html)

#### ApiKeyId and ApiKeySecret

If you are using the **Elastic Cloud**, you can use the **ApiKeyId** and **ApiKeySecret** to connect Elastic Cloud by:

```
ApiKeyId ""
ApiKeySecret ""
```

see
more: [ApiKeySecret](https://www.elastic.co/guide/en/elasticsearch/client/java-rest/current/\_other\_authentication\_methods.html#\_elasticsearch\_api\_keys)

#### AWS IAM: ApiKeyId, ApiKeySecret and ApiSessionToken

If you are using the **AWS Opensearch**, you can use the **AWSRegion** to activate aws credential:

```
AWSRegion "us-east" # if want to use system env or default aws credential, just only set AWSRegion
ApiKeyId ""
ApiKeySecret ""
ApiSessionToken ""
```

### Timeout

**Timeout** is used to control the query actions timeout for **Elasticsearch Cluster**, it will apply to every action in
current context. set **Timeout** by:

```
Timeout 1000
```

this will set timeout for action 1 second.

## Query Actions

**Query Actions** is same
with [Elasticsearch REST APIs](https://www.elastic.co/guide/en/elasticsearch/reference/current/rest-apis.html), but in
edql context defined it as **Query Actions**. so we can copy from **Elascticsearch** offical sample requests and execute
these directly. such as:

```
POST my-index/_search
{
  "query": {
    "bool": {
      "filter": [
      ]
    }
  }
}
```

query from **my-index** with **bool** query and **filter**.

why called it as **REST Actions** not **REST APIS**? since have enhanced the apis such as variables and functions etc,
maybe call it as **Action** maybe better.

## Query DSL: JSON Block

**Query DSL JSON Block** is the same as **Elasticsearch** query DSL definition, we can write these query contexts in the
current block. such as **bool** query, **aggregation** etc. Example:

```
POST my-index/_search
{
  "query": {
    "bool": {
      "must": [

      ]
    }
  },
  "aggs": {
    "maxValue": {
      "max": {
        "field": "value"
      }
    }
  }
}
```

