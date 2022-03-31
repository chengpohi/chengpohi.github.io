---
description: 'Elasticsearch cluster: observerlity and management settings, index and tasks'
---

# Manage Cluster

Elasticsearch Cluster has many [metrics](https://www.elastic.co/guide/en/elasticsearch/reference/current/cluster.html) need to observe all the time, Example we often need to check whether cluster health, index stats or tasks background running.&#x20;

EDQL has provided full features to manage Elasticsearch cluster by interactive action include: cluster, nodes, index, tasks etc. so we can simplily observe Elasticsearch metrics by EDQL without any extra effort.

## Index Manage

Elasticsearch index with EDQL is very simple, all actions are interactive with Actions.

### Indices

List of all indices of Elasticsearch, this action will query indices and display index details as table, include:

* name
* documents
* size

### Create Index

EDQL has built an ui of create index table, we can configure new index by seting field name, field type and nest field type(properties or field), for nest field we can use "a.b" for nest field path. when executing the index creation, EDQL will automatically expand nest field path as nest document

Also EDQL support creating index by copying from another index, we can use **copy from index action** to import other index mapping

By default EDQL create index action use default index type \_doc, if want specify other type, you need set the custom index type on index type field

After creating index successfu, the create index table will be closed and redirect to Indices table, if create failed, such as index name duplicate or name is illegal, the error popup dialog will show up

### Delete Index

When using **Indices** table we can use delete action for deleting index with selected index

### Modify Index

When using Indices table we can modify an existed index by using modify action, modify action will open a new table dialog with all indiex fields will be displayed, in the modify table dialog we can add new fields, since Elasticsearch cannot support modify exist fields

### Reindex

EDQL support reindex index by using Reindex action, so if need to switch new index, we can use this action for quickly reindex data to new index.

### Import Index

In some times, maybe need to index data into index, EDQL support import an csv data with header, it will use header as field name, index line by line as documents into Elasticsearch index

### Templates

Templates action display Elasticsearch all templates in a table. for manage Templates, **TODO**

### Snapshots

Snapshots action display Elasticsearch all snapshots in a table. for manage snapshots, **TODO**

## Cluster

### Health

### Stats

### State

### Nodes

### Tasks



