---
description: >-
  Search documents from Elasticsearch: filter, highlight, modify and export
  result set
---

# Query

## Search Documents

Elasticsearch is a powerful search engine and has complex and features [query dsl syntax](https://www.elastic.co/guide/en/elasticsearch/reference/current/query-dsl.html) for search and analysis documents. but the query syntax it's complex and have a hard curve to learn. EDQL is try to improve learn curve with supporting primitive Elasticsearch query syntax and IDE support(highlight, autocomplete, document etc).

We can just copy the query demo from Elasticsearch document website, paste to EDQL script and run for quickly verify the result.  Also we can try to test Elasticsearch new features by using EDQL script.

Since EDQL is a script file, we can create EDQL scripts for daily search and search shortcuts. and these scripts can be shared by projects and team, help other people for quickly search from Elasticsearch without extra effort.

With search result can be displayed compact data table, it's easy to filter document, highlight document and  modify document.

Also EDQL has a powerful Visual Editor, it can help quickly to search document by configure queries without writing code, the Visual Editor has the Layout mode, we can just run queries to search document, for example: team share EDQL scripts for search document

## Export Documents

In some cases we want to download Elasticsearch documents for analysis or sharing, EDQL support two modes download Elasticsearch documents, for now both modes only support download as CSV file

### Download Search Result-Set

Download search result-set is for when run the EDQL query action, want to download current documents table, the download documents only limit the EDQL query action return current result size determined by query action: "size" parameter

### Download by Query

Download by query is based on Visual Editor, it default will use scroll download the query action whole documents, when start downloading you can configure the scroll size. it will download whole documents that match the query action, it maybe take a long time to export determined by the query hits. EDQL also has support to cancel the long time downloading on progress bar with **Cancel** button



## EDQL syntax could find on:

{% content-ref url="../language-specification/basic-syntax.md" %}
[basic-syntax.md](../language-specification/basic-syntax.md)
{% endcontent-ref %}
