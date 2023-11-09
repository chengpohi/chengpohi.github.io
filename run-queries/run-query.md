# Run Query

EDQL (Elasticsearch Data Query Language) feature in Intellij provides convenient ways to execute queries and manage Elasticsearch resources. Additionally, you can convert queries written in EDQL to Java code for further integration and customization. Let's explore these features in more detail:

## Run Query Action:

To execute an individual request, you can simply click the right icon of the request or use the Run shortcut when the cursor is positioned on the request action block. This action runs the selected request and returns the corresponding response. It is a quick and easy way to execute single queries within your EDQL script.

## Run Script:

When an EDQL script contains multiple request actions, you can run all of them together. To do this, ensure that the cursor is not positioned on any specific request action block and use the Run shortcut. This action executes all the requests in the script sequentially, and the responses are returned and displayed in separate tabs. It allows you to conveniently analyze and compare the results of multiple queries.

## Export:

The export feature provides options for exporting query results. The "Export Query Result" functionality allows you to save the results of a query in various formats, such as CSV or JSON. This is useful for sharing or further analyzing the query results outside of Intellij.

## Scroll Export by Query:

When dealing with large result sets, the scroll export feature is beneficial. It enables you to export query results in smaller batches, making the process more efficient and manageable. This helps prevent overwhelming system resources and ensures smoother execution of exports.

## Query Conversion to Java:

In addition to running queries in EDQL, Intellij also offers the capability to convert EDQL queries to Java code. This is useful if you want to incorporate and customize your queries within Java applications. By converting the queries to Java, you can take advantage of the Elasticsearch Java API and its features.

To convert an EDQL query to Java, you can use the appropriate code generation or conversion tools available in Intellij. These tools typically provide options to automatically generate Java code that corresponds to your EDQL query. Once the conversion is complete, you can integrate the generated Java code into your Java application, allowing for seamless interaction with Elasticsearch.

## Manage:

The manage section in Intellij provides various functionalities for managing Elasticsearch resources. Some of the key features available include:

* Create Index: This action allows you to create a new index in Elasticsearch, specifying the desired settings and mappings.
* Delete Index: Use this action to remove an existing index from Elasticsearch.
* Export Data: Export data from Elasticsearch to an external file or destination.
* Import Data: Import data from external sources into Elasticsearch.
* Create Template: Define templates that specify mappings and settings for new indices.
* Create Alias: Create an alias, which is an alternate name for an index or a group of indices.
* Create Script: Develop custom scripts for advanced data processing and transformations.
* Create Pipeline: Define an ingest pipeline for preprocessing data before indexing.
* Reindex: Perform data reindexing from one index to another, potentially applying transformations or filtering.
* Rebuild: Optimize indices by rebuilding them, refreshing and optimizing them for improved performance.
* Templates, Tasks, Ingests, Plugins, Plot: These sections provide additional management functionalities for templates, tasks, ingest pipelines, plugins, and plotting, respectively.

The EDQL run query feature in Intellij, along with the ability to convert queries to Java, provides a comprehensive set of tools for executing and managing Elasticsearch queries. Whether you prefer working with EDQL or integrating queries into Java applications, Intellij offers the flexibility and functionality to streamline your Elasticsearch workflows.
