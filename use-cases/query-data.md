# Query

## Search Documents

Elasticsearch is a powerful search engine and has complex and features query syntax for search and analysis data. but the query syntax it's complex and have a hard curve to learn. EDQL is try to improve learn curve with supporting primitive Elasticsearch query syntax and IDE support(highlight, autocomplete, document etc).

We can just copy the query demo from Elasticsearch document website, paste to EDQL script and run for quickly verify the result.  Also we can try to test Elasticsearch new features by using EDQL script.

Since EDQL is a script file, we can create EDQL scripts for daily search and search shortcuts. and these scripts can be shared by projects and team, help other people for quickly search from Elasticsearch without extra effort.

With search result can be displayed compact data table, it's easy to filter data, highlight data and  modify data.

Also EDQL has a powerful Visual Editor, it can help quickly to search data by configure queries without writing code, the Visual Editor has the Layout mode, we can just run queries to search data, for example: team share EDQL scripts for search data

## Export Documents

In some cases we want to export Elasticsearch documents for analysis or sharing, EDQL support two modes export Elasticsearch data, for now both modes only support download as CSV file

### Export Search Result-Set

Export search result-set is for when run the EDQL query action, want to export current data table, the export data only limit the EDQL query action return current result size determined by query action: "size" parameter

### Export by Query

Export by query is based on Visual Editor, it default will use scroll download the query action whole data, when start downloading you can configure the scroll size. it will download whole data that match the query action, it maybe take a long time to export determined by the query hits. EDQL also has support to cancel the long time exporting on progress bar
