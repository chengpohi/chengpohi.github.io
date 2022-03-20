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

{% hint style="info" %}
**Good to know:** your product docs aren't just a reference of all your features! use them to encourage folks to perform certain actions and discover the value in your product.
{% endhint %}

### Fundamentals: Dive a little deeper

Learn the fundamentals of MyProduct to get a deeper understanding of our main features:

{% content-ref url="language-specification/basic-glossary.md" %}
[basic-glossary.md](language-specification/basic-glossary.md)
{% endcontent-ref %}

{% content-ref url="language-specification/basic-syntax.md" %}
[basic-syntax.md](language-specification/basic-syntax.md)
{% endcontent-ref %}

{% content-ref url="language-specification/advance-syntax.md" %}
[advance-syntax.md](language-specification/advance-syntax.md)
{% endcontent-ref %}

{% content-ref url="broken-reference" %}
[Broken link](broken-reference)
{% endcontent-ref %}

{% hint style="info" %}
**Good to know:** Splitting your product into fundamental concepts, objects, or areas can be a great way to let readers deep dive into the concepts that matter most to them. Combine guides with this approach to 'fundamentals' and you're well on your way to great documentation!
{% endhint %}
