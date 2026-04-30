---
title: Default DevOps Config exporters
description: The DevOps Config Exporter content pack contains a set of default DevOps Config exporters of data that can be used as input for further deployment and provisioning activities.
locale: en-US
release: yokohama
product: DevOps \(Family\)
classification: devops-family
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Reference, DevOps Config, IT Service Management]
---

# Default DevOps Config exporters

The DevOps Config Exporter content pack contains a set of default DevOps Config exporters of data that can be used as input for further deployment and provisioning activities.

**Important:** DevOps Config is now deprecated and no longer supported or available for new activation.

DevOps Config exporters allow other tools to consume the data from deployable snapshots.

**Note:** You cannot modify default exporters. However, you can make a copy of the exporter and customize your copy.

These exporters are contained in the DevOps Config Exporter content pack.

-   returnAllData-now
-   returnAllData\_noVars-now
-   returnDataforNodeName-now
-   returnDataForNodeNames-now
-   returnDataForPath-now
-   returnNodeListForLevel-now
-   returnNodeListForPath-now
-   returnValueForKeyAtNodeName-now
-   returnValueForKeyPath-now
-   returnValueForUniqueKeyName-now

## Return all data \(returnAllData-now\)

Returns the full content of the snapshot without any filtering or modifications, including the var system folder.

**Note:** The exporter fails if the application/deployable is not in Active state \(deleted\).

-   **Arguments**
    -   appName - Application name
    -   deployableName - Deployable name
    -   requestedFormat - Requested format \(json/yaml/xml/ini/raw\)
-   **Special logic**

    None.

-   **Error handling**

    None.


## Return all data except vars \(returnAllData\_noVars-now\)

Returns all of the configuration data for the deployable, except deployable name and variables.

Response does not include:

-   `vars` folder at the deployable level
-   `vars` folder at each of the included collections
-   Deployable name at the root level of the response

**Note:** This exporter does not work for deleted applications/deployables.

-   **Arguments**

    Arguments \(can be provided on the command line, or entered interactively in run mode\).

    -   appName - Application name
    -   deployableName - Deployable name
    -   requestedFormat - Requested format \(json/yaml/xml/ini/raw\)
-   **Special logic**

    None.

-   **Error handling**

    None.


## Return data for a node name \(returnDataforNodeName-now\)

Returns the subset of the snapshot data for a given node name, which is provided as an argument. The argument value must be passed as string text.

-   **Arguments**
    -   appName - Application name
    -   deployableName - Deployable name
    -   requestedFormat - Requested format \(json/yaml/xml/ini/raw\)
    -   nodeName - Node name \(string, in quotes\)
    -   includeNodeInOutput - \(string, default is true\)
-   **Special logic**
    -   If nodeName is empty, all data is returned.
    -   If includeNodeInOutput is false, the node data is returned excluding the node name.
-   **Error handling**
    -   If the nodeName is not unique, `multiple instances of nodeName found`.
    -   If the nodeName is not found, `node not found: <nodeName>`.
    -   If includeNodeInOutput is false and node data is a key-value pair, an error is returned.

## Return data for list of nodes \(returnDataForNodeNames-now\)

Returns the full data from the snapshot for a list of nodes. Same as `Return data for a node name` but returns a nested JSON with configuration data for a list of given node names \(including any child nodes\).

-   **Arguments**
    -   appName - Application name
    -   deployableName - Deployable name
    -   requestedFormat - Requested format \(json/yaml/xml/ini/raw\)
    -   nodeNames - Node names \(string, in quotes, comma-separated\)
-   **Special logic**

    If nodeNamesList is empty, returns all config data.

-   **Error handling**

    None.

-   **Response details**

    \{“node1”:\{“contentKey”:”contentValue”\},”node2”:\{ “error”:”nodeName not found”\}\}.

-   **Error handling**
    -   In case the nodeName is not unique the exporter returns an error response stating “multiple instances of nodeName found” for that specific nodeName. Other nodeNames contain the data
    -   If a nodeName is not found it should contain error message for that node

## Return data for path \(returnDataForPath-now\)

Returns all of the configuration data for a given node path in the snapshot.

-   **Arguments**
    -   appName - Application name
    -   deployableName - Deployable name
    -   requestedFormat - Requested format \(json/yaml/xml/ini/raw\)
    -   nodePath - Node path \(string, in quotes\)
-   **Special logic**

    If nodePath is empty, return the whole content \(similar to all config data\).

-   **Error handling**

    If nodePath is not found, the last node name that was not found is stated `path not found: <nodeName>`.


## Return node list for level \(returnNodeListForLevel-now\)

Returns a list of names of nodes that are children of root node at specified level \(depth\) in the snapshot. For example, level 1 is a direct child of root node, level 2 is a grandchild, etc.

-   **Arguments**
    -   appName - Application name
    -   deployableName - Deployable name
    -   requestedFormat - Requested format \(json/yaml/xml/ini/raw\)
    -   ExcludeVarsNode \[true\|false\] - Exclude the vars node from the result \(true or false, default is true\)
    -   nodeLevel - Level of the node \(integer, default is 0\)
-   **Special logic**

    If no level is specified, then exporter returns the value for level 0 \(for example, the deployable root node name\).

-   **Error handling**

    None.

-   **Response details**

    \[“node1, “node2”, “node3”\]


## Return node list for path \(returnNodeListForPath-now\)

Returns the list of nodes for a given node path in the snapshot \(not taking into account sub-nodes\).

-   **Arguments**
    -   appName - Application name
    -   deployableName - Deployable name
    -   requestedFormat - Requested format \(json/yaml/xml/ini/raw\)
    -   ExcludeVarsNode \[true\|false\] - Exclude the vars node from the result \(true or false, default is true\)
    -   nodePath - Path to follow with list of nodes separated by pathSeparator \(string, in quotes\)
    -   pathSeparator - Character to separate list of nodePaths \(string, default is ‘,’\)
-   **Special logic**

    None.

-   **Error handling**

    None.

-   **Response details**

    \[“node1, “node2”, “node3”\]


## Return value for key within a node \(returnValueForKeyAtNodeName-now\)

Returns the value of a specific key that is part of a node in the snapshot. The key can either be directly defined to the node, or lower in the data model to one of the children of the node.

The difference between this exporter and `export value for unique keyName` is that the key name only needs to be unique within the subtree of the node.

Key/node combination is expected to be unique in the snapshot. If the key/node combination is found more than once, there is an error.

-   **Arguments**
    -   appName - Application name
    -   deployableName - Deployable name
    -   requestedFormat - Requested format \(json/yaml/xml/ini/raw\)
    -   keyName - Key name \(string, in quotes\)
    -   nodeName - Node name \(string, in quotes\)
-   **Special logic**

    None.

-   **Error Handling**

    If keyName nodeName combination is not found an empty response is returned.


## Return value for keyPath \(returnValueForKeyPath-now\)

Returns the value of a specific key in a specific path.

-   **Arguments**
    -   appName - Application name
    -   deployableName - Deployable name
    -   requestedFormat - Requested format \(json/yaml/xml/ini/raw\)
    -   keyPath - List of node names with key name at the end separated by pathSeparator \(string, in quotes\)
    -   pathSeparator - Character to separate list of keyPaths \(string, default is ‘,’\)
-   **Special logic**

    None.

-   **Error handling**
    -   If the keyPath is not provided, `no keyPath argument provided`.
    -   If the keyPath is not found, states the last node name not found `path not found: <path>/<nodeName>`.
    -   If the keyPath is found and is a node \(not a key\), `keyPath provided is a node and not a key`.

## Return value for unique keyName \(returnValueForUniqueKeyName-now\)

Returns the value of a specific key based on its name in the snapshot. Unlike `export value for key within a node`, the key is expected to be unique across the snapshot data model. Multiple keys are supported.

**Note:** Formats xml and ini are not supported for this exporter.

-   **Arguments**
    -   appName - Application name
    -   deployableName - Deployable name
    -   requestedFormat - Requested format \(json/yaml/raw\)
    -   keyName - Key name \(data array\)
-   **Special logic**

    If the key is present multiple times in the snapshot, the exporter returns the first value found \(returns error\).

-   **Error handling**
    -   If the keyName is not provided, `no keyName argument provided`.
    -   If the key is not found, `key not found: <keyName>`.

**Parent Topic:**[DevOps Config reference](devops-config-reference.md)

