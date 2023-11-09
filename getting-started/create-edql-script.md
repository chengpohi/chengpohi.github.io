---
description: Connection Elasticsearch and Query by EDQL
---

# Connection and Query

## Connection

Connect to Elasticsearch by using EDQL Dock Manage default **on the Intellij right side**. In the EDQL Dock Manager, you can **add new connection to connect Elasticsearch and Test connection**.

![](../.gitbook/assets/new-connection.gif)

View more on:

{% content-ref url="../configuration/configure-connection.md" %}
[configure-connection.md](../configuration/configure-connection.md)
{% endcontent-ref %}

## Authorization

### Authorization Token

Use authorization token to connect Elasticsearch cluster, such as basic token, bearer token or custom token

### Username & Password

Basic username, password

### AWS

Use aws region, api key id, api key secret to connect aws Elasticsearch, also you can custom AWS profile to use

### General ApiKey

Use general api key to connect Elasticsearch cluster, such as Elastic cloud

### SSH Tunnel

Use an SSH tunnel to encrypt a connection between a client and a server to connect Server, Or make connections inside same VPC(Virtual Private Cloud), Example: connect aws server in the same VPC.

<figure><img src="../.gitbook/assets/ssh-tunnel.png" alt=""><figcaption></figcaption></figure>

### HTTP Proxy

Use HTTP Proxy to connect Elasticsearch with http proxy

## Query Console

After creating and testing a connection of Elasticsearch, You can create a new query console on the Dock Toolbar with terminal icon

![](../.gitbook/assets/query-console.gif)

## Query by Visual Editor

After EDQL file is created, we can use the **Visual Editor** to configure a query action, since the common query conditions are annoying and boring. Visual Editor is a powerful tool for visual query conditions and configurations, example: term match, range query, wildcard query and size, explain etc.

![](../.gitbook/assets/configure-by-dashboard.gif)

![](../.gitbook/assets/new-visual.gif)
