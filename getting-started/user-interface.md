# User Interface

## Dock Manager

**EDQL Dock Manager** default on the right side of intellij. and it is used to manage connections and
script files.

### Dock Toolbar

- New Connection

  create a new Elasticsearch connection
- Duplicate Connection

  duplicate Elasticsearch connection
- Query Console

  create new query in selected connection
- Plot

  plot in selected connection
- Edit

  edit connection, index, edql etc
- Delete

  delete connection, index, edql etc
- Configuration

  configure connection

### Connection Node

After new connection, the added connection will display connection name as connection node, after double click will list
all related infos:

- Indices

  list all selected indices, and double click index to run
- Nodes

  list all selected connection's nodes
- Aliases

  list all selected connection's aliases for view or edit details
- Templates

  list all selected connection's templates for view or edit details
- Tasks

  list all selected connection's tasks for view

- Scripts

  list all selected connection's scripts for view or edit details
- Ingests

  list all selected connection's ingests for view or edit details
- Transforms

  list all selected connection's transforms for view or edit details
- Plugins

  list all selected connection's plugins for view details
- ILMS

  list all selected connection's ilms for view details
- EDQLS

  list all selected connection's EDQLs for view, edit and run
- Charts

  list all selected connection's charts for view, it defaults includes ClusterStats chart
- Favroite functions

  list all selected connection's favorite function

### EDQLs Node

Global EDQLs file node.

### Charts Node

Global Charts file node.

### Documents Node

Elasticsearch documentation in local.

## Run Result Panel

After running a query by EDQL, the run result panel will display on the window bottom.

### Running Details Panel

Show the executed details: start, finished and usage time.

### Data Panel

Show the query response: Table view, JSON view or Plot view.

### Explain&Profile Panel

Show the query explain&profile info, it's JSON structural view.