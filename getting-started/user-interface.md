# User Interface

<figure><img src="/.gitbook/assets/image.png" alt=""><figcaption></figcaption></figure>

## Dock Manager

The EDQL Dock Manager is an integral part of the Intellij IDE user interface, positioned by default on the right side of the screen. It provides a user-friendly interface for efficiently managing connections and script files within the EDQL environment.

With the EDQL Dock Manager, you can effortlessly organize and navigate through your connections, establishing seamless communication with your Elasticsearch clusters. Additionally, it allows you to conveniently manage and access your script files, ensuring easy retrieval and modification as needed.

### Dock Toolbar

The Dock Toolbar is a user-friendly feature located within the EDQL environment, designed to streamline connection and query management. Here are the key functionalities offered by the toolbar:

*   New Connection

    Create a new Elasticsearch connection, allowing you to establish communication with your Elasticsearch clusters effortlessly.
*   Duplicate Connection

    Duplicate an existing Elasticsearch connection, facilitating the replication of connection settings for convenience and efficiency.
*   Query Console

    Create a new query in the selected connection, enabling you to execute Elasticsearch queries and retrieve data seamlessly.
*   Plot

    Plot data from the selected connection, providing visualization capabilities for deeper insights and analysis.
*   Edit

    Modify connection settings, index configurations, and EDQL scripts to fine-tune your Elasticsearch querying experience.
*   Delete

    Remove connections, indexes, or EDQL elements that are no longer needed, helping you maintain a clean and organized workspace.
*   Configuration

    Access and configure connection settings, ensuring optimal performance and compatibility with your Elasticsearch setup.

### Connection Node

Once a new connection is added in the EDQL Dock Manager, it is displayed as a connection node. Double-clicking on the connection node reveals a list of related information for that specific connection:

*   Indices

    Lists all selected indices. Double-clicking on an index allows you to run queries specifically on that index.
*   Nodes

    Displays all selected connection's nodes.
*   Aliases

    Provides a list of aliases associated with the selected connection, allowing you to view or edit alias details.
*   Templates

    Lists all selected connection's templates, enabling you to view or edit template details.
*   Tasks

    list all selected connection's tasks for view
*   Scripts

    Provides a list of scripts associated with the selected connection, allowing you to view or edit script details.
*   Ingests

    Lists all selected connection's ingests, enabling you to view or edit ingest details.
*   Transforms

    Displays all selected connection's transforms, allowing you to view or edit transform details.
*   Plugins

    Provides details of all selected connection's plugins for easy viewing.
*   ILMs

    Lists all selected connection's index lifecycle management (ILM) settings for easy viewing.
*   EDQLs

    Displays all selected connection's EDQL scripts, allowing you to view, edit, and run them.
*   Charts

    Provides a list of charts associated with the selected connection for easy viewing. By default, it includes the ClusterStats chart.
*   Favroite functions

    Lists all selected connection's favorite functions.

### EDQLs Node

Global EDQLs file node.

### Charts Node

Global Charts file node.

### Documents Node

Elasticsearch documentation in local.

## Run Result Panel

When you execute a query using EDQL, the run result panel conveniently appears at the bottom of the window, providing you with instant access to the query results. This dedicated panel offers a clear and organized view of the outcome of your query execution.

By displaying the run results in the bottom panel, you can easily review and analyze the returned data, ensuring a smooth and efficient workflow within the EDQL environment. The intuitive placement of the run result panel allows for seamless interaction and quick reference to the query execution outcomes.

### Running Details Panel

Show the executed details: start, finished and usage time.

### Data Panel

Show the query response: Table view, JSON view or Plot view.

### Explain\&Profile Panel

Show the query explain\&profile info, it's JSON structural view.
