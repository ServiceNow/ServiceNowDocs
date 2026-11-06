---
title: CdmQuery - Scoped
description: The CdmQuery script include provides methods that enable you to query the CDM data model tree. It returns a list of node objects that are specific fields/columns in the CDM Node \[sn\_cdm\_node\] table. These values are returned as properties in the object. Every object is a node in the data model.Instantiates a CdmQuery object. You must call this method prior to calling any other CdmQuery methods.Enables you to specify whether decrypted values for encrypted configuration data item \(CDI\) and variable nodes are returned in the results.Enables you to specify whether linked nodes are fully resolved, such that descendant nodes of a referenced node appear under a linked node.Iterates through each of the result nodes and applies the provided function that accepts a CdmNode object.Returns the specified CDM query results.Returns the value of the specified field of the current iterated node result.Enables you to specify whether to fetch the file metadata information for file nodes. The file metadata contains attachment\_id, file\_name, content\_type, and checksum.Iterates to the next node result and returns it if it exists.Executes the specified query against the CDM database or the cache based on the settings, entry node, and filter settings.Specifies the entry node. The CdmQuery API limits its query to the entry node and its descendant nodes. Calling this method is mandatory.Enables you to specify whether to substitute variable references in configuration data item \(CDI\) nodes with the value of the referenced variable node.Enables you to specify whether to retrieve data from the cache, if any, instead of querying the database.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/api-reference/server-api-reference/CdmQueryScopedAPI.html
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 20
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# CdmQuery- Scoped

The CdmQuery script include provides methods that enable you to query the CDM data model tree. It returns a list of node objects that are specific fields/columns in the CDM Node \[sn\_cdm\_node\] table. These values are returned as properties in the object. Every object is a node in the data model.

This script include is fluent which means most of its methods support chaining and return a CdmQuery object. The methods within this script include are classified into different types. You must specify them in a particular order within a call, based on their type. All methods except the result methods are chainable.

**Note:** This documentation only covers the usage of the CdmQuery script include in querying snapshot data, therefore, only methods necessary for this process are currently documented. Querying snapshot data is needed when writing PaCE policy scripts for data validation and CDM exporter scripts for data export.

Method types:

-   entry method: This method specifies the entry node. CdmQuery limits its query to the entry node and its descendant nodes. Specifying the entry node is mandatory.

    [CdmQuery - snapshotId\(String snapshotSysID\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/server-api-reference/CdmQueryScopedAPI.md)

-   query method: This method executes the specified query.

    [CdmQuery - query\(\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/server-api-reference/CdmQueryScopedAPI.md)

-   result methods: These methods return a specific set of results data.
    -   [CdmQuery - forEach\(Function function\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/server-api-reference/CdmQueryScopedAPI.md)
    -   [CdmQuery - getTree\(Boolean simpleTree, Boolean prettify\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/server-api-reference/CdmQueryScopedAPI.md)
    -   [CdmQuery - getValue\(String fieldName\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/server-api-reference/CdmQueryScopedAPI.md)
    -   [CdmQuery - next\(\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/server-api-reference/CdmQueryScopedAPI.md)
-   setting methods: These methods modify the behavior of CdmQuery\(\).
    -   [CdmQuery - decryptPassword\(Boolean decrypt\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/server-api-reference/CdmQueryScopedAPI.md)
    -   [CdmQuery - followIncludes\(Boolean followIncludes\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/server-api-reference/CdmQueryScopedAPI.md)
    -   [CdmQuery - includeFileMetadata\(\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/server-api-reference/CdmQueryScopedAPI.md)
    -   [CdmQuery - substituteVariable\(Boolean substitute\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/server-api-reference/CdmQueryScopedAPI.md)
    -   [CdmQuery - useCache\(Boolean useCache\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/server-api-reference/CdmQueryScopedAPI.md)

The snapshotId\(\) and query\(\) methods are mandatory. You must add filter and setting methods before the query\(\) method, but after the snapshotId\(\) method. The order in which you add filter and setting methods is not important, unless they are conflicting, in which case the latest relevant method prevails. You must add any result methods, such as getTree\(\) to fetch the result, after the query\(\) method.

For example:

```
var primarySnapshot = new sn_cdm.CdmQuery()
  .snapshotId("1a2fe2e6c3a27010cc0a259d7640dd59")
  .decryptPassword(true)
  .includeFileMetadata()
  .query()
  .getTree(true, false);
```

This API runs in the `sn_cdm` namespace and you must have the sn\_cdm.cdm\_viewer or sn\_cdm.cdm\_secrets roles to access its various methods.

**Parent Topic:**[Server API reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/server-api-reference/api-server.md)

## CdmQuery - CdmQuery\(\)

Instantiates a CdmQuery object. You must call this method prior to calling any other CdmQuery methods.

|Name|Type|Description|
|----|----|-----------|
|None| ||

The following code examples shows how to call the CdmQuery method to instantiate a CdmQuery object in the sn\_cdm namespace.

```
var primarySnapshot = new sn_cdm.CdmQuery()
.snapshotId("snapshot_id")
.decryptPassword(true)
.query()
.getTree();
```

## CdmQuery - decryptPassword\(Boolean decrypt\)

Enables you to specify whether decrypted values for encrypted configuration data item \(CDI\) and variable nodes are returned in the results.

An error is thrown if the user does not have the required sn\_cdm.cdm\_secrets role.

<table id="table_lwv_kkz_5wb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

decrypt

</td><td>

Boolean

</td><td>

Optional. Flag that indicates whether to return decrypted values for the CDI and variable nodes.Valid values:

-   true: Return decrypted values for the CDI and variable nodes.
-   false: Return encrypted values for the CDI and variable nodes.

Default: false

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

The following code example shows how to query a snapshot and return decrypted values for the encrypted CDI and variable nodes. The user running the script must have the sn\_cdm.cdm\_secrets role.

```
var primarySnapshot = new sn_cdm.CdmQuery()
  .snapshotId("snapshot_sys_id")
  .decryptPassword(true)
  .query()
  .getTree(true, true);

gs.info(primarySnapshot);
```

Return results:

```
{
  "Development_1": {
    "vars": {},
    "services": {
      "vars": {},
      "paymentComponent": {
        "applicationSLA": "24x7",
        "paymentService": {
          "database": {
            "backup": {
              "dbServer": "db23.paymentx.be"
            },
            "dbIpAddress": "10.20.40.50",
            "dbName": "paymentX_dev2",
            "dbPort": "8050",
            "dbServer": "db22.paymentx.be",
            "dbUserName": "exampleDbUser",
            "dbPassword": "exampleDbPassword"
          }
        }
      }
    }
  }
}
```

The following code example shows how to query a snapshot and return masked values for the encrypted configuration data item \(CDI\) and variable nodes.

```
var primarySnapshot = new sn_cdm.CdmQuery()
  .snapshotId("snapshot_sys_id")
  .decryptPassword(false)
  .query()
  .getTree(true, true);

gs.info(primarySnapshot);
```

Return results \(decrypt=false\):

```
{
  "Deployable_1": {
    "vars": {},
    "linked_node": {
      "vars": {},
      "component_1": {
        "applicationSLA": "24x7",
        "component_2": {
          "database": {
            "backup": {
              "dbServer": "backup.example.com"
            },
            "dbIpAddress": "192.0.2.10",
            "dbName": "exampleDb",
            "dbPort": "5000",
            "dbServer": "db.example.com",
            "dbUserName": "exampleDbUser",
            "dbPassword": "*******"
          }
        }
      }
    }
  }
}
```

## CdmQuery - followIncludes\(Boolean followIncludes\)

Enables you to specify whether linked nodes are fully resolved, such that descendant nodes of a referenced node appear under a linked node.

<table id="table_ebw_4xz_5wb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

followIncludes

</td><td>

Boolean

</td><td>

Optional. Flag that indicates whether linked nodes are fully resolved.Valid values:

-   true: Linked nodes are fully resolved.
-   false: Linked nodes aren't fully resolved.

Default: true

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

The following code example shows how to query a snapshot and fully resolve linked nodes \(`followIncludes = true`\). The descendant nodes of each referenced node appear under the linked node.

```
var primarySnapshot = new sn_cdm.CdmQuery()
  .snapshotId("snapshot_sys_id")
  .followIncludes(true)
  .query()
  .getTree(false, true);
```

Example return data:

```
{
  "sys_id": "sys_id_1",
  "type": "sn_cdm_node_deployable",
  "main_id": "main_id_1",
  "name": "Deployable_1",
  "node_path": "node_path_1",
  "effective_path": "effective_path_1",
  "main_id_encoded": "encoded_id_1",
  "node_classifier": "/application/deployables/env:Environment",
  "status": "valid",
  "level": "2",
  "children": [
    {
      "sys_id": "sys_id_2",
      "type": "sn_cdm_node_folder",
      "main_id": "main_id_2",
      "name": "vars",
      "node_path": "node_path_2",
      "effective_path": "effective_path_2",
      "main_id_encoded": "encoded_id_2",
      "node_classifier": "/application/deployables/env:Environment/vars",
      "status": "valid",
      "level": "3",
      "children": [],
      "hasParent": true
    },
    {
      "sys_id": "sys_id_3",
      "type": "sn_cdm_node_linked",
      "main_id": "main_id_3",
      "name": "linked_node",
      "node_path": "node_path_3",
      "effective_path": "effective_path_3",
      "main_id_encoded": "encoded_id_3",
      "node_classifier": "/application/deployables/env:Environment",
      "status": "valid",
      "level": "3",
      "children": [
        {
          "sys_id": "sys_id_4",
          "type": "sn_cdm_node_folder",
          "main_id": "main_id_4",
          "name": "vars",
          "node_path": "node_path_4",
          "effective_path": "effective_path_4",
          "main_id_encoded": "encoded_id_4",
          "node_classifier": "/application/collections/vars",
          "status": "valid",
          "level": "3",
          "children": [],
          "hasParent": true
        },
        {
          "sys_id": "sys_id_5",
          "type": "sn_cdm_node_component",
          "main_id": "main_id_5",
          "name": "component_1",
          "node_path": "node_path_5",
          "effective_path": "effective_path_5",
          "main_id_encoded": "encoded_id_5",
          "node_classifier": "/application/deployables/env:Environment",
          "status": "valid",
          "level": "4",
          "children": [
            {
              "sys_id": "sys_id_6",
              "type": "sn_cdm_node_cdi",
              "main_id": "main_id_6",
              "name": "applicationSLA",
              "node_path": "node_path_6",
              "value": "24x7",
              "effective_path": "effective_path_6",
              "main_id_encoded": "encoded_id_6",
              "node_classifier": "/application/components",
              "status": "valid",
              "level": "3",
              "children": [],
              "hasParent": true
            },
            {
              "sys_id": "sys_id_7",
              "type": "sn_cdm_node_component",
              "main_id": "main_id_7",
              "name": "component_2",
              "node_path": "node_path_7",
              "effective_path": "effective_path_7",
              "main_id_encoded": "encoded_id_7",
              "node_classifier": "/application/deployables/env:Environment",
              "status": "valid",
              "level": "5",
              "children": [
                {
                  "sys_id": "sys_id_8",
                  "type": "sn_cdm_node_component",
                  "main_id": "main_id_8",
                  "name": "database",
                  "node_path": "node_path_8",
                  "effective_path": "effective_path_8",
                  "main_id_encoded": "encoded_id_8",
                  "node_classifier": "/application/deployables/env:Environment",
                  "status": "valid",
                  "level": "6",
                  "children": [
                    {
                      "sys_id": "sys_id_9",
                      "type": "sn_cdm_node_component",
                      "main_id": "main_id_9",
                      "name": "backup",
                      "node_path": "node_path_9",
                      "effective_path": "effective_path_9",
                      "main_id_encoded": "encoded_id_9",
                      "node_classifier": "/application/components",
                      "status": "valid",
                      "level": "5",
                      "children": [
                        {
                          "sys_id": "sys_id_10",
                          "type": "sn_cdm_node_cdi",
                          "main_id": "main_id_10",
                          "name": "dbServer",
                          "node_path": "node_path_10",
                          "value": "backup.example.com",
                          "effective_path": "effective_path_10",
                          "main_id_encoded": "encoded_id_10",
                          "node_classifier": "/application/components",
                          "status": "valid",
                          "level": "6",
                          "children": [],
                          "hasParent": true
                        }
                      ],
                      "hasParent": true
                    },
                    {
                      "sys_id": "sys_id_11",
                      "type": "sn_cdm_node_cdi",
                      "main_id": "main_id_11",
                      "name": "dbIpAddress",
                      "node_path": "node_path_11",
                      "value": "192.0.2.10",
                      "effective_path": "effective_path_11",
                      "main_id_encoded": "encoded_id_11",
                      "node_classifier": "/application/components",
                      "status": "valid",
                      "level": "5",
                      "children": [],
                      "hasParent": true
                    },
                    {
                      "sys_id": "sys_id_12",
                      "type": "sn_cdm_node_cdi",
                      "main_id": "main_id_12",
                      "name": "dbName",
                      "node_path": "node_path_12",
                      "value": "exampleDb",
                      "effective_path": "effective_path_12",
                      "main_id_encoded": "encoded_id_12",
                      "node_classifier": "/application/components",
                      "status": "valid",
                      "level": "5",
                      "children": [],
                      "hasParent": true
                    },
                    {
                      "sys_id": "sys_id_13",
                      "type": "sn_cdm_node_cdi",
                      "main_id": "main_id_13",
                      "name": "dbPort",
                      "node_path": "node_path_13",
                      "value": "5000",
                      "effective_path": "effective_path_13",
                      "main_id_encoded": "encoded_id_13",
                      "node_classifier": "/application/components",
                      "status": "valid",
                      "level": "5",
                      "children": [],
                      "hasParent": true
                    },
                    {
                      "sys_id": "sys_id_14",
                      "type": "sn_cdm_node_cdi",
                      "main_id": "main_id_14",
                      "name": "dbServer",
                      "node_path": "node_path_14",
                      "value": "db.example.com",
                      "effective_path": "effective_path_14",
                      "main_id_encoded": "encoded_id_14",
                      "node_classifier": "/application/components",
                      "status": "valid",
                      "level": "5",
                      "children": [],
                      "hasParent": true
                    },
                    {
                      "sys_id": "sys_id_15",
                      "type": "sn_cdm_node_cdi",
                      "main_id": "main_id_15",
                      "name": "dbUserName",
                      "node_path": "node_path_15",
                      "value": "exampleDbUser",
                      "effective_path": "effective_path_15",
                      "main_id_encoded": "encoded_id_15",
                      "node_classifier": "/application/components",
                      "status": "valid",
                      "level": "5",
                      "children": [],
                      "hasParent": true
                    },
                    {
                      "sys_id": "sys_id_16",
                      "type": "sn_cdm_node_cdi",
                      "main_id": "main_id_16",
                      "name": "dbPassword",
                      "node_path": "node_path_16",
                      "secure_value": "ENCRYPTED_VALUE_PLACEHOLDER",
                      "effective_path": "effective_path_16",
                      "main_id_encoded": "encoded_id_16",
                      "node_classifier": "/application/deployables/env:Environment",
                      "status": "valid",
                      "level": "7",
                      "masked_value": "*******",
                      "children": [],
                      "hasParent": true
                    }
                  ],
                  "hasParent": true
                }
              ],
              "hasParent": true
            }
          ],
          "hasParent": true
        }
      ],
      "hasParent": true
    }
  ]
}
```

The following code example shows how to query a snapshot without fully resolving linked nodes \(`followIncludes = false`\). Only a subset of the referenced node’s descendants appear under the linked node.

```
var primarySnapshot = new sn_cdm.CdmQuery()
  .snapshotId("snapshot_sys_id")
  .followIncludes(false)
  .query()
  .getTree(false, true);
```

Example return data:

```
{
  "sys_id": "sys_id_1",
  "type": "sn_cdm_node_deployable",
  "main_id": "main_id_1",
  "name": "Deployable_1",
  "node_path": "node_path_1",
  "effective_path": "effective_path_1",
  "main_id_encoded": "encoded_id_1",
  "node_classifier": "/application/deployables/env:Environment",
  "status": "valid",
  "level": "2",
  "children": [
    {
      "sys_id": "sys_id_2",
      "type": "sn_cdm_node_folder",
      "main_id": "main_id_2",
      "name": "vars",
      "node_path": "node_path_2",
      "effective_path": "effective_path_2",
      "main_id_encoded": "encoded_id_2",
      "node_classifier": "/application/deployables/env:Environment/vars",
      "status": "valid",
      "level": "3",
      "children": [],
      "hasParent": true
    },
    {
      "sys_id": "sys_id_3",
      "type": "sn_cdm_node_linked",
      "main_id": "main_id_3",
      "name": "linked_node",
      "node_path": "node_path_3",
      "effective_path": "effective_path_3",
      "main_id_encoded": "encoded_id_3",
      "node_classifier": "/application/deployables/env:Environment",
      "status": "valid",
      "level": "3",
      "children": [
        {
          "sys_id": "sys_id_5",
          "type": "sn_cdm_node_component",
          "main_id": "main_id_5",
          "name": "component_1",
          "node_path": "node_path_5",
          "effective_path": "effective_path_5",
          "main_id_encoded": "encoded_id_5",
          "node_classifier": "/application/deployables/env:Environment",
          "status": "valid",
          "level": "4",
          "children": [
            {
              "sys_id": "sys_id_7",
              "type": "sn_cdm_node_component",
              "main_id": "main_id_7",
              "name": "component_2",
              "node_path": "node_path_7",
              "effective_path": "effective_path_7",
              "main_id_encoded": "encoded_id_7",
              "node_classifier": "/application/deployables/env:Environment",
              "status": "valid",
              "level": "5",
              "children": [
                {
                  "sys_id": "sys_id_8",
                  "type": "sn_cdm_node_component",
                  "main_id": "main_id_8",
                  "name": "database",
                  "node_path": "node_path_8",
                  "effective_path": "effective_path_8",
                  "main_id_encoded": "encoded_id_8",
                  "node_classifier": "/application/deployables/env:Environment",
                  "status": "valid",
                  "level": "6",
                  "children": [
                    {
                      "sys_id": "sys_id_16",
                      "type": "sn_cdm_node_cdi",
                      "main_id": "main_id_16",
                      "name": "dbPassword",
                      "node_path": "node_path_16",
                      "secure_value": "ENCRYPTED_VALUE_PLACEHOLDER",
                      "effective_path": "effective_path_16",
                      "main_id_encoded": "encoded_id_16",
                      "node_classifier": "/application/deployables/env:Environment",
                      "status": "valid",
                      "level": "7",
                      "masked_value": "*******",
                      "children": [],
                      "hasParent": true
                    }
                  ],
                  "hasParent": true
                }
              ],
              "hasParent": true
            }
          ],
          "hasParent": true
        }
      ],
      "hasParent": true
    }
  ]
}
```

## CdmQuery - forEach\(Function function\)

Iterates through each of the result nodes and applies the provided function that accepts a CdmNode object.

|Name|Type|Description|
|----|----|-----------|
|function|Function|Function to apply to the CdmNode object.|

|Type|Description|
|----|-----------|
|None| |

The following code example shows how to call the forEach\(\) method to apply a function to each node in the query results. The function logs the name and value of each node.

```
var cdmQuery = new sn_cdm.CdmQuery()
  .snapshotId("snapshot_sys_id")
  .query();

cdmQuery.forEach(function (node) {
  gs.info("Node - {0}:{1}", [node.getValue("name"), node.getValue("value")]);
});
```

## CdmQuery - getTree\(Boolean simpleTree, Boolean prettify\)

Returns the specified CDM query results.

You can specify the level and format of the content to return by setting the associated flags within the call. The default is to return a formatted string containing the node metadata and its child nodes, and where the entry node is the top node.

<table id="table_pfp_ywf_vwb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

simpleTree

</td><td>

Boolean

</td><td>

Optional. Flag that indicates the level of content to return.Valid values:

-   true: Returns a simplified JSON object of hierarchical key-values pairs, excluding all node metadata.
-   false: Returns a JSON object containing the node metadata and all its child nodes, and specifies where the entry node is the top node.

Default: false

</td></tr><tr><td>

prettify

</td><td>

Boolean

</td><td>

Optional. Flag that indicates whether to return a formatted string instead of a JSON object.Valid values:

-   true: Return the content in a JSON object.
-   false: Return the content as a formatted string. Only use this option in UI and exporters as it adds new line and escape characters to the response.

Default: false

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|CdmQuery|CdmQuery object containing the specified query information.|

The following code example shows how to call the getTree\(\) method using the default settings and log the result as a string. The result contains the node metadata and all child nodes, with the entry node as the top node.

```
var primarySnapshot = new sn_cdm.CdmQuery()
  .snapshotId("snapshot_sys_id")
  .query()
  .getTree();

gs.info(JSON.stringify(primarySnapshot));
```

Return results \(single-line string\):

```
{"sys_id":"sys_id_1","type":"sn_cdm_node_deployable","main_id":"main_id_1","name":"Deployable_1","node_path":"node_path_1","effective_path":"effective_path_1","main_id_encoded":"encoded_id_1","node_classifier":"/application/deployables/env:Environment","status":"valid","level":"2","children":[{"sys_id":"sys_id_2","type":"sn_cdm_node_folder","main_id":"main_id_2","name":"vars","node_path":"node_path_2","effective_path":"effective_path_2","main_id_encoded":"encoded_id_2","node_classifier":"/application/deployables/env:Environment/vars","status":"valid","level":"3","children":[],"hasParent":true},{"sys_id":"sys_id_3","type":"sn_cdm_node_linked","main_id":"main_id_3","name":"linked_node","node_path":"node_path_3","effective_path":"effective_path_3","main_id_encoded":"encoded_id_3","node_classifier":"/application/deployables/env:Environment","status":"valid","level":"3","children":[{"sys_id":"sys_id_4","type":"sn_cdm_node_folder","main_id":"main_id_4","name":"vars","node_path":"node_path_4","effective_path":"effective_path_4","main_id_encoded":"encoded_id_4","node_classifier":"/application/collections/vars","status":"valid","level":"3","children":[],"hasParent":true},{"sys_id":"sys_id_5","type":"sn_cdm_node_component","main_id":"main_id_5","name":"component_1","node_path":"node_path_5","effective_path":"effective_path_5","main_id_encoded":"encoded_id_5","node_classifier":"/application/deployables/env:Environment","status":"valid","level":"4","children":[{"sys_id":"sys_id_6","type":"sn_cdm_node_cdi","main_id":"main_id_6","name":"applicationSLA","node_path":"node_path_6","value":"24x7","effective_path":"effective_path_6","main_id_encoded":"encoded_id_6","node_classifier":"/application/components","status":"valid","level":"3","children":[],"hasParent":true},{"sys_id":"sys_id_7","type":"sn_cdm_node_component","main_id":"main_id_7","name":"component_2","node_path":"node_path_7","effective_path":"effective_path_7","main_id_encoded":"encoded_id_7","node_classifier":"/application/deployables/env:Environment","status":"valid","level":"5","children":[{"sys_id":"sys_id_8","type":"sn_cdm_node_component","main_id":"main_id_8","name":"database","node_path":"node_path_8","effective_path":"effective_path_8","main_id_encoded":"encoded_id_8","node_classifier":"/application/deployables/env:Environment","status":"valid","level":"6","children":[{"sys_id":"sys_id_9","type":"sn_cdm_node_component","main_id":"main_id_9","name":"backup","node_path":"node_path_9","effective_path":"effective_path_9","main_id_encoded":"encoded_id_9","node_classifier":"/application/components","status":"valid","level":"5","children":[{"sys_id":"sys_id_10","type":"sn_cdm_node_cdi","main_id":"main_id_10","name":"dbServer","node_path":"node_path_10","value":"backup.example.com","effective_path":"effective_path_10","main_id_encoded":"encoded_id_10","node_classifier":"/application/components","status":"valid","level":"6","children":[],"hasParent":true}],"hasParent":true},{"sys_id":"sys_id_11","type":"sn_cdm_node_cdi","main_id":"main_id_11","name":"dbIpAddress","node_path":"node_path_11","value":"192.0.2.10","effective_path":"effective_path_11","main_id_encoded":"encoded_id_11","node_classifier":"/application/components","status":"valid","level":"5","children":[],"hasParent":true},{"sys_id":"sys_id_12","type":"sn_cdm_node_cdi","main_id":"main_id_12","name":"dbName","node_path":"node_path_12","value":"exampleDb","effective_path":"effective_path_12","main_id_encoded":"encoded_id_12","node_classifier":"/application/components","status":"valid","level":"5","children":[],"hasParent":true},{"sys_id":"sys_id_13","type":"sn_cdm_node_cdi","main_id":"main_id_13","name":"dbPort","node_path":"node_path_13","value":"5000","effective_path":"effective_path_13","main_id_encoded":"encoded_id_13","node_classifier":"/application/components","status":"valid","level":"5","children":[],"hasParent":true},{"sys_id":"sys_id_14","type":"sn_cdm_node_cdi","main_id":"main_id_14","name":"dbServer","node_path":"node_path_14","value":"db.example.com","effective_path":"effective_path_14","main_id_encoded":"encoded_id_14","node_classifier":"/application/components","status":"valid","level":"5","children":[],"hasParent":true},{"sys_id":"sys_id_15","type":"sn_cdm_node_cdi","main_id":"main_id_15","name":"dbUserName","node_path":"node_path_15","value":"exampleDbUser","effective_path":"effective_path_15","main_id_encoded":"encoded_id_15","node_classifier":"/application/components","status":"valid","level":"5","children":[],"hasParent":true},{"sys_id":"sys_id_16","type":"sn_cdm_node_cdi","main_id":"main_id_16","name":"dbPassword","node_path":"node_path_16","secure_value":"ENCRYPTED_VALUE_PLACEHOLDER","effective_path":"effective_path_16","main_id_encoded":"encoded_id_16","node_classifier":"/application/deployables/env:Environment","status":"valid","level":"7","masked_value":"*******","children":[],"hasParent":true}],"hasParent":true}],"hasParent":true}],"hasParent":true}],"hasParent":true}]}
```

The following code example shows how to call the getTree\(\) method to return a simplified JSON object of hierarchical key-values pairs.

```
var primarySnapshot = new sn_cdm.CdmQuery()
  .snapshotId("snapshot_sys_id")
  .query()
  .getTree(true, true);

gs.info(JSON.stringify(primarySnapshot));
```

Return results:

```
{
  "Deployable_1": {
    "vars": {},
    "linked_node": {
      "vars": {},
      "component_1": {
        "applicationSLA": "24x7",
        "component_2": {
          "database": {
            "backup": {
              "dbServer": "backup.example.com"
            },
            "dbIpAddress": "192.0.2.10",
            "dbName": "exampleDb",
            "dbPort": "5000",
            "dbServer": "db.example.com",
            "dbUserName": "exampleDbUser",
            "dbPassword": "*******"
          }
        }
      }
    }
  }
}
```

The following code example shows how to call the getTree\(\) method to return a JSON object containing the node metadata and all child nodes, with the entry node as the top node.

```
var primarySnapshot = new sn_cdm.CdmQuery()
  .snapshotId("snapshot_sys_id")
  .query()
  .getTree(false, true);

gs.info(JSON.stringify(primarySnapshot));
```

Results:

```
{
  "sys_id": "sys_id_1",
  "type": "sn_cdm_node_deployable",
  "main_id": "main_id_1",
  "name": "Deployable_1",
  "node_path": "node_path_1",
  "effective_path": "effective_path_1",
  "main_id_encoded": "encoded_id_1",
  "node_classifier": "/application/deployables/env:Environment",
  "status": "valid",
  "level": "2",
  "children": [
    {
      "sys_id": "sys_id_2",
      "type": "sn_cdm_node_folder",
      "main_id": "main_id_2",
      "name": "vars",
      "node_path": "node_path_2",
      "effective_path": "effective_path_2",
      "main_id_encoded": "encoded_id_2",
      "node_classifier": "/application/deployables/env:Environment/vars",
      "status": "valid",
      "level": "3",
      "children": [],
      "hasParent": true
    },
    {
      "sys_id": "sys_id_3",
      "type": "sn_cdm_node_linked",
      "main_id": "main_id_3",
      "name": "linked_node",
      "node_path": "node_path_3",
      "effective_path": "effective_path_3",
      "main_id_encoded": "encoded_id_3",
      "node_classifier": "/application/deployables/env:Environment",
      "status": "valid",
      "level": "3",
      "children": [
        {
          "sys_id": "sys_id_4",
          "type": "sn_cdm_node_folder",
          "main_id": "main_id_4",
          "name": "vars",
          "node_path": "node_path_4",
          "effective_path": "effective_path_4",
          "main_id_encoded": "encoded_id_4",
          "node_classifier": "/application/collections/vars",
          "status": "valid",
          "level": "3",
          "children": [],
          "hasParent": true
        },
        {
          "sys_id": "sys_id_5",
          "type": "sn_cdm_node_component",
          "main_id": "main_id_5",
          "name": "component_1",
          "node_path": "node_path_5",
          "effective_path": "effective_path_5",
          "main_id_encoded": "encoded_id_5",
          "node_classifier": "/application/deployables/env:Environment",
          "status": "valid",
          "level": "4",
          "children": [
            {
              "sys_id": "sys_id_6",
              "type": "sn_cdm_node_cdi",
              "main_id": "main_id_6",
              "name": "applicationSLA",
              "node_path": "node_path_6",
              "value": "24x7",
              "effective_path": "effective_path_6",
              "main_id_encoded": "encoded_id_6",
              "node_classifier": "/application/components",
              "status": "valid",
              "level": "3",
              "children": [],
              "hasParent": true
            },
            {
              "sys_id": "sys_id_7",
              "type": "sn_cdm_node_component",
              "main_id": "main_id_7",
              "name": "component_2",
              "node_path": "node_path_7",
              "effective_path": "effective_path_7",
              "main_id_encoded": "encoded_id_7",
              "node_classifier": "/application/deployables/env:Environment",
              "status": "valid",
              "level": "5",
              "children": [
                {
                  "sys_id": "sys_id_8",
                  "type": "sn_cdm_node_component",
                  "main_id": "main_id_8",
                  "name": "database",
                  "node_path": "node_path_8",
                  "effective_path": "effective_path_8",
                  "main_id_encoded": "encoded_id_8",
                  "node_classifier": "/application/deployables/env:Environment",
                  "status": "valid",
                  "level": "6",
                  "children": [
                    {
                      "sys_id": "sys_id_9",
                      "type": "sn_cdm_node_component",
                      "main_id": "main_id_9",
                      "name": "backup",
                      "node_path": "node_path_9",
                      "effective_path": "effective_path_9",
                      "main_id_encoded": "encoded_id_9",
                      "node_classifier": "/application/components",
                      "status": "valid",
                      "level": "5",
                      "children": [
                        {
                          "sys_id": "sys_id_10",
                          "type": "sn_cdm_node_cdi",
                          "main_id": "main_id_10",
                          "name": "dbServer",
                          "node_path": "node_path_10",
                          "value": "backup.example.com",
                          "effective_path": "effective_path_10",
                          "main_id_encoded": "encoded_id_10",
                          "node_classifier": "/application/components",
                          "status": "valid",
                          "level": "6",
                          "children": [],
                          "hasParent": true
                        }
                      ],
                      "hasParent": true
                    },
                    {
                      "sys_id": "sys_id_11",
                      "type": "sn_cdm_node_cdi",
                      "main_id": "main_id_11",
                      "name": "dbIpAddress",
                      "node_path": "node_path_11",
                      "value": "192.0.2.10",
                      "effective_path": "effective_path_11",
                      "main_id_encoded": "encoded_id_11",
                      "node_classifier": "/application/components",
                      "status": "valid",
                      "level": "5",
                      "children": [],
                      "hasParent": true
                    },
                    {
                      "sys_id": "sys_id_12",
                      "type": "sn_cdm_node_cdi",
                      "main_id": "main_id_12",
                      "name": "dbName",
                      "node_path": "node_path_12",
                      "value": "exampleDb",
                      "effective_path": "effective_path_12",
                      "main_id_encoded": "encoded_id_12",
                      "node_classifier": "/application/components",
                      "status": "valid",
                      "level": "5",
                      "children": [],
                      "hasParent": true
                    },
                    {
                      "sys_id": "sys_id_13",
                      "type": "sn_cdm_node_cdi",
                      "main_id": "main_id_13",
                      "name": "dbPort",
                      "node_path": "node_path_13",
                      "value": "5000",
                      "effective_path": "effective_path_13",
                      "main_id_encoded": "encoded_id_13",
                      "node_classifier": "/application/components",
                      "status": "valid",
                      "level": "5",
                      "children": [],
                      "hasParent": true
                    },
                    {
                      "sys_id": "sys_id_14",
                      "type": "sn_cdm_node_cdi",
                      "main_id": "main_id_14",
                      "name": "dbServer",
                      "node_path": "node_path_14",
                      "value": "db.example.com",
                      "effective_path": "effective_path_14",
                      "main_id_encoded": "encoded_id_14",
                      "node_classifier": "/application/components",
                      "status": "valid",
                      "level": "5",
                      "children": [],
                      "hasParent": true
                    },
                    {
                      "sys_id": "sys_id_15",
                      "type": "sn_cdm_node_cdi",
                      "main_id": "main_id_15",
                      "name": "dbUserName",
                      "node_path": "node_path_15",
                      "value": "exampleDbUser",
                      "effective_path": "effective_path_15",
                      "main_id_encoded": "encoded_id_15",
                      "node_classifier": "/application/components",
                      "status": "valid",
                      "level": "5",
                      "children": [],
                      "hasParent": true
                    },
                    {
                      "sys_id": "sys_id_16",
                      "type": "sn_cdm_node_cdi",
                      "main_id": "main_id_16",
                      "name": "dbPassword",
                      "node_path": "node_path_16",
                      "secure_value": "ENCRYPTED_VALUE_PLACEHOLDER",
                      "effective_path": "effective_path_16",
                      "main_id_encoded": "encoded_id_16",
                      "node_classifier": "/application/deployables/env:Environment",
                      "status": "valid",
                      "level": "7",
                      "masked_value": "*******",
                      "children": [],
                      "hasParent": true
                    }
                  ],
                  "hasParent": true
                }
              ],
              "hasParent": true
            }
          ],
          "hasParent": true
        }
      ],
      "hasParent": true
    }
  ]
}
```

## CdmQuery - getValue\(String fieldName\)

Returns the value of the specified field of the current iterated node result.

|Name|Type|Description|
|----|----|-----------|
|fieldName|String|Name of the field with the snapshot record to return.|

|Type|Description|
|----|-----------|
|None| |

The following code example shows how to use the getValue\(\) method to get the name and type of each node in the query results. The example iterates through the nodes with the next\(\) method. For CDI and variable nodes, it also gets the node value.

```
var cdmQuery = new sn_cdm.CdmQuery()
  .snapshotId("snapshot_sys_id")
  .decryptPassword(true)
  .query();

var output = [];
while (cdmQuery.next()) {
  var name = cdmQuery.getValue('name');
  var type = cdmQuery.getValue('type');

  if (type == 'sn_cdm_node_cdi' || type == 'sn_cdm_node_variable') {
    var value = cdmQuery.getValue('value');
    output.push(gs.getMessage("{0} : {1} [{2}]", [name, value, type]));
  } else {
    output.push(gs.getMessage("{0} [{1}]", [name, type]));
  }
}
```

Return values:

```
[
  "deployable_name [sn_cdm_node_deployable]",
  "vars [sn_cdm_node_folder]",
  "service_password : examplePassword [sn_cdm_node_variable]",
  "linked_node [sn_cdm_node_linked]",
  "vars [sn_cdm_node_folder]",
  "component_1 [sn_cdm_node_component]",
  "user_name : exampleUser [sn_cdm_node_cdi]",
  "user_password : examplePassword [sn_cdm_node_cdi]"
]
```

## CdmQuery - includeFileMetadata\(\)

Enables you to specify whether to fetch the file metadata information for file nodes. The file metadata contains attachment\_id, file\_name, content\_type, and checksum.

**Note:** Metadata is only returned for non-simple trees. For additional information on this type of data return, see [CdmQuery - getTree\(Boolean simpleTree, Boolean prettify\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/server-api-reference/CdmQueryScopedAPI.md).

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|None| |

The following code example shows how to call the includeFileMetadata\(\) method to return file metadata for file nodes in the query results. The metadata includes the attachment ID, file name, content type, and checksum.

```
var cdmQuery = new sn_cdm.CdmQuery()
  .snapshotId("snapshot_sys_id")
  .includeFileMetadata()
  .query()
  .getTree(false, true);
```

Returns:

```
{
  "sys_id": "sys_id_1",
  "type": "sn_cdm_node_deployable",
  "main_id": "main_id_1",
  "name": "Deployable_1",
  "node_path": "node_path_1",
  "effective_path": "effective_path_1",
  "main_id_encoded": "encoded_id_1",
  "node_classifier": "/application/deployables/env:Environment",
  "status": "valid",
  "level": "2",
  "children": [
    {
      "sys_id": "sys_id_2",
      "type": "sn_cdm_node_folder",
      "main_id": "main_id_2",
      "name": "vars",
      "node_path": "node_path_2",
      "effective_path": "effective_path_2",
      "main_id_encoded": "encoded_id_2",
      "node_classifier": "/application/deployables/env:Environment/vars",
      "status": "valid",
      "level": "3",
      "children": [],
      "hasParent": true
    },
    {
      "sys_id": "sys_id_3",
      "type": "sn_cdm_node_file",
      "main_id": "main_id_3",
      "name": "config_file.xml",
      "node_path": "node_path_3",
      "value": "file: https://instance.example.com/sys_attachment.do?sys_id=attachment_sys_id",
      "effective_path": "effective_path_3",
      "main_id_encoded": "encoded_id_3",
      "node_classifier": "/application/deployables/env:Environment",
      "status": "valid",
      "level": "3",
      "file_metadata": {
        "attachment_id": "attachment_sys_id",
        "file_name": "config_file.xml",
        "content_type": "application/xml",
        "checksum": "CHECKSUM_PLACEHOLDER"
      },
      "children": [],
      "hasParent": true
    }
  ]
}
```

## CdmQuery - next\(\)

Iterates to the next node result and returns it if it exists.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_ncd_1hh_vwb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

CdmQuery

</td><td>

If available, the CdmQuery object of the next node.If no additional nodes are available it returns a null or undefined.

</td></tr></tbody>
</table>The following code example shows how to use the next\(\) method to iterate through each node in the query results. The example outputs the name and type of each node. For CDI and variable nodes, it also outputs the node value.

```
var cdmQuery = new sn_cdm.CdmQuery()
  .snapshotId("snapshot_sys_id")
  .decryptPassword(true)
  .query();

var output = [];
while (cdmQuery.next()) {
  var name = cdmQuery.getValue('name');
  var type = cdmQuery.getValue('type');

  if (type == 'sn_cdm_node_cdi' || type == 'sn_cdm_node_variable') {
    var value = cdmQuery.getValue('value');
    output.push(gs.getMessage("{0} : {1} [{2}]", [name, value, type]));
  } else {
    output.push(gs.getMessage("{0} [{1}]", [name, type]));
  }
}
```

Return results:

```
[
  "deployable_name [sn_cdm_node_deployable]",
  "vars [sn_cdm_node_folder]",
  "service_password : examplePassword [sn_cdm_node_variable]",
  "linked_node [sn_cdm_node_linked]",
  "vars [sn_cdm_node_folder]",
  "component_1 [sn_cdm_node_component]",
  "user_name : exampleUser [sn_cdm_node_cdi]",
  "user_password : examplePassword [sn_cdm_node_cdi]"
]
```

## CdmQuery - query\(\)

Executes the specified query against the CDM database or the cache based on the settings, entry node, and filter settings.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|CdmQuery|CdmQuery object.|

The following code example shows how to call the query\(\) method to run the query against a snapshot. The example also returns decrypted values for encrypted nodes and returns the results as a tree.

```
var primarySnapshot = new sn_cdm.CdmQuery()
  .snapshotId("snapshot_sys_id")
  .decryptPassword(true)
  .query()
  .getTree();
```

Return results:

```
{
  "_decryptPassword": true,
  "sys_id": "sys_id_1",
  "type": "sn_cdm_node_deployable",
  "main_id": "main_id_1",
  "name": "deployable_name",
  "node_path": "node_path_1",
  "effective_path": "effective_path_1",
  "main_id_encoded": "encoded_id_1",
  "node_classifier": "/application/deployables/dep:deployable_name",
  "status": "valid",
  "children": [
    {
      "_decryptPassword": true,
      "sys_id": "sys_id_2",
      "type": "sn_cdm_node_folder",
      "main_id": "main_id_2",
      "name": "vars",
      "node_path": "node_path_2",
      "effective_path": "effective_path_2",
      "main_id_encoded": "encoded_id_2",
      "node_classifier": "/application/deployables/dep:deployable_name/vars",
      "status": "valid",
      "children": [
        {
          "_decryptPassword": true,
          "sys_id": "sys_id_3",
          "type": "sn_cdm_node_variable",
          "main_id": "main_id_3",
          "name": "service_password",
          "node_path": "node_path_3",
          "value": "examplePassword",
          "effective_path": "effective_path_3",
          "main_id_encoded": "encoded_id_3",
          "node_classifier": "/application/deployables/dep:deployable_name/vars",
          "status": "valid",
          "children": [],
          "hasParent": true
        }
      ],
      "hasParent": true
    },
    {
      "_decryptPassword": true,
      "sys_id": "sys_id_4",
      "type": "sn_cdm_node_linked",
      "main_id": "main_id_4",
      "name": "linked_node",
      "node_path": "node_path_4",
      "effective_path": "effective_path_4",
      "main_id_encoded": "encoded_id_4",
      "node_classifier": "/application/deployables/dep:deployable_name",
      "status": "valid",
      "children": [
        {
          "_decryptPassword": true,
          "sys_id": "sys_id_5",
          "type": "sn_cdm_node_folder",
          "main_id": "main_id_5",
          "name": "vars",
          "node_path": "node_path_5",
          "effective_path": "effective_path_5",
          "main_id_encoded": "encoded_id_5",
          "node_classifier": "/application/collections/vars",
          "status": "valid",
          "children": [],
          "hasParent": true
        },
        {
          "_decryptPassword": true,
          "sys_id": "sys_id_6",
          "type": "sn_cdm_node_component",
          "main_id": "main_id_6",
          "name": "component_1",
          "node_path": "node_path_6",
          "effective_path": "effective_path_6",
          "main_id_encoded": "encoded_id_6",
          "node_classifier": "/application/deployables/dep:deployable_name",
          "status": "valid",
          "children": [
            {
              "_decryptPassword": true,
              "sys_id": "sys_id_7",
              "type": "sn_cdm_node_cdi",
              "main_id": "main_id_7",
              "name": "user_name",
              "node_path": "node_path_7",
              "value": "exampleUser",
              "effective_path": "effective_path_7",
              "main_id_encoded": "encoded_id_7",
              "node_classifier": "/application/deployables/dep:deployable_name",
              "status": "valid",
              "children": [],
              "hasParent": true
            },
            {
              "_decryptPassword": true,
              "sys_id": "sys_id_8",
              "type": "sn_cdm_node_cdi",
              "main_id": "main_id_8",
              "name": "user_password",
              "node_path": "node_path_8",
              "value": "examplePassword",
              "effective_path": "effective_path_8",
              "main_id_encoded": "encoded_id_8",
              "node_classifier": "/application/deployables/dep:deployable_name",
              "status": "valid",
              "children": [],
              "hasParent": true
            }
          ],
          "hasParent": true
        }
      ],
      "hasParent": true
    }
  ],
  "hasParent": false
}
```

## CdmQuery - snapshotId\(String snapshotSysID\)

Specifies the entry node. The CdmQuery API limits its query to the entry node and its descendant nodes. Calling this method is mandatory.

<table id="table_vhw_cbz_5wb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

snapshotSysId

</td><td>

String

</td><td>

Sys\_id of the deployable snapshot to query.Internally it sets the sys\_id of the changeset and the sys\_id of the deployable node.

Table: CDM Snapshot \[sn\_cdm\_snapshot\]

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

The following code example shows how to call the snapshotId\(\) method to specify the snapshot to query. The query is limited to the entry node of that snapshot and its descendant nodes.

```
var primarySnapshot = new sn_cdm.CdmQuery()
  .snapshotId("snapshot_sys_id")
  .decryptPassword(true)
  .query()
  .getTree();
```

Return results:

```
{
  "_decryptPassword": true,
  "sys_id": "sys_id_1",
  "type": "sn_cdm_node_deployable",
  "main_id": "main_id_1",
  "name": "deployable_name",
  "node_path": "node_path_1",
  "effective_path": "effective_path_1",
  "main_id_encoded": "encoded_id_1",
  "node_classifier": "/application/deployables/dep:deployable_name",
  "status": "valid",
  "children": [
    {
      "_decryptPassword": true,
      "sys_id": "sys_id_2",
      "type": "sn_cdm_node_folder",
      "main_id": "main_id_2",
      "name": "vars",
      "node_path": "node_path_2",
      "effective_path": "effective_path_2",
      "main_id_encoded": "encoded_id_2",
      "node_classifier": "/application/deployables/dep:deployable_name/vars",
      "status": "valid",
      "children": [
        {
          "_decryptPassword": true,
          "sys_id": "sys_id_3",
          "type": "sn_cdm_node_variable",
          "main_id": "main_id_3",
          "name": "service_password",
          "node_path": "node_path_3",
          "value": "examplePassword",
          "effective_path": "effective_path_3",
          "main_id_encoded": "encoded_id_3",
          "node_classifier": "/application/deployables/dep:deployable_name/vars",
          "status": "valid",
          "children": [],
          "hasParent": true
        }
      ],
      "hasParent": true
    },
    {
      "_decryptPassword": true,
      "sys_id": "sys_id_4",
      "type": "sn_cdm_node_linked",
      "main_id": "main_id_4",
      "name": "linked_node",
      "node_path": "node_path_4",
      "effective_path": "effective_path_4",
      "main_id_encoded": "encoded_id_4",
      "node_classifier": "/application/deployables/dep:deployable_name",
      "status": "valid",
      "children": [
        {
          "_decryptPassword": true,
          "sys_id": "sys_id_5",
          "type": "sn_cdm_node_folder",
          "main_id": "main_id_5",
          "name": "vars",
          "node_path": "node_path_5",
          "effective_path": "effective_path_5",
          "main_id_encoded": "encoded_id_5",
          "node_classifier": "/application/collections/vars",
          "status": "valid",
          "children": [],
          "hasParent": true
        },
        {
          "_decryptPassword": true,
          "sys_id": "sys_id_6",
          "type": "sn_cdm_node_component",
          "main_id": "main_id_6",
          "name": "component_1",
          "node_path": "node_path_6",
          "effective_path": "effective_path_6",
          "main_id_encoded": "encoded_id_6",
          "node_classifier": "/application/deployables/dep:deployable_name",
          "status": "valid",
          "children": [
            {
              "_decryptPassword": true,
              "sys_id": "sys_id_7",
              "type": "sn_cdm_node_cdi",
              "main_id": "main_id_7",
              "name": "user_name",
              "node_path": "node_path_7",
              "value": "exampleUser",
              "effective_path": "effective_path_7",
              "main_id_encoded": "encoded_id_7",
              "node_classifier": "/application/deployables/dep:deployable_name",
              "status": "valid",
              "children": [],
              "hasParent": true
            },
            {
              "_decryptPassword": true,
              "sys_id": "sys_id_8",
              "type": "sn_cdm_node_cdi",
              "main_id": "main_id_8",
              "name": "user_password",
              "node_path": "node_path_8",
              "value": "examplePassword",
              "effective_path": "effective_path_8",
              "main_id_encoded": "encoded_id_8",
              "node_classifier": "/application/deployables/dep:deployable_name",
              "status": "valid",
              "children": [],
              "hasParent": true
            }
          ],
          "hasParent": true
        }
      ],
      "hasParent": true
    }
  ],
  "hasParent": false
}
```

## CdmQuery - substituteVariable\(Boolean substitute\)

Enables you to specify whether to substitute variable references in configuration data item \(CDI\) nodes with the value of the referenced variable node.

<table id="table_r4r_1rz_5wb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

substitute

</td><td>

Boolean

</td><td>

Optional. Flag that indicates whether to substitute variable references in CDI nodes with the value of the referenced variable node.Valid values:

-   true: Substitute variable references in CDI nodes with the value of the referenced variable node.
-   false: Do not substitute variable references in CDI nodes with the value of the referenced variable node.

Default: true

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

### SUBSTITUTEVARIABLE=false

The following code example shows how to turn off substitution of variable references in CDI nodes. Values that reference other nodes are returned as references, shown between @@ delimiters.

```
var primarySnapshot = new sn_cdm.CdmQuery()
  .snapshotId("snapshot_sys_id")
  .substituteVariable(false)
  .query()
  .getTree(true, true);

gs.info(primarySnapshot);
```

Example return results:

```
{
  "service_name": {
    "featureToggles": {
      "featureA": "enabled",
      "featureB": "enabled",
      "featureC": "enabled",
      "featureD": "disabled",
      "featureE": "enabled"
    },
    "vars": {
      "service": {
        "database": {
          "dbName": "exampleDb",
          "dbUserName": "exampleDbUser",
          "dbPassword": "exampleDbPassword",
          "dbServer": "db.example.com",
          "dbPort": "5000",
          "dbIpAddress": "192.0.2.10",
          "backup": {
            "dbServer": "backup.example.com"
          }
        }
      },
      "applicationSLA": "24x7"
    },
    "settings": {
      "idSetting": "example_id",
      "listSettingA": "1,2,3",
      "listSettingB": "1,2,3",
      "listSettingC": "1,2,3",
      "listSettingD": "1",
      "listSettingE": "1,2,3",
      "dbIPAddress": "@@service/database/dbIpAddress@@",
      "dbPort": "@@service/database/dbPort@@",
      "dbConnectionString": "@@service/database/dbUserName@@:@@service/database/dbPassword@@ @@service/database/dbServer@@:@@service/database/dbPort@@ @@service/database/dbName@@",
      "dbConnectionStringBackup": "@@service/database/dbUserName@@:@@service/database/dbPassword@@ @@service/database/backup/dbServer@@ @@service/database/dbName@@",
      "optionA": "enabled",
      "optionB": "disabled",
      "optionC": "enabled"
    }
  }
}
```

### SUBSTITUTEVARIABLE=true

The following code example shows how to turn on substitution of variable references in CDI nodes. Each reference is replaced with the value of the referenced variable node, as shown in the return results for the same snapshot.

```
var primarySnapshot = new sn_cdm.CdmQuery()
  .snapshotId("snapshot_sys_id")
  .substituteVariable(true)
  .query()
  .getTree(true, true);

gs.info(primarySnapshot);
```

Example return results:

```
{
  "service_name": {
    "featureToggles": {
      "featureA": "enabled",
      "featureB": "enabled",
      "featureC": "enabled",
      "featureD": "disabled",
      "featureE": "enabled"
    },
    "vars": {
      "service": {
        "database": {
          "dbName": "exampleDb",
          "dbUserName": "exampleDbUser",
          "dbPassword": "exampleDbPassword",
          "dbServer": "db.example.com",
          "dbPort": "5000",
          "dbIpAddress": "192.0.2.10",
          "backup": {
            "dbServer": "backup.example.com"
          }
        }
      },
      "applicationSLA": "24x7"
    },
    "settings": {
      "idSetting": "example_id",
      "listSettingA": "1,2,3",
      "listSettingB": "1,2,3",
      "listSettingC": "1,2,3",
      "listSettingD": "1",
      "listSettingE": "1,2,3",
      "dbIPAddress": "192.0.2.10",
      "dbPort": "5000",
      "dbConnectionString": "exampleDbUser:exampleDbPassword db.example.com:5000 exampleDb",
      "dbConnectionStringBackup": "exampleDbUser:exampleDbPassword backup.example.com exampleDb",
      "optionA": "enabled",
      "optionB": "disabled",
      "optionC": "enabled"
    }
  }
}
```

## CdmQuery - useCache\(Boolean useCache\)

Enables you to specify whether to retrieve data from the cache, if any, instead of querying the database.

<table id="table_wr1_p5z_5wb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

useCache

</td><td>

Boolean

</td><td>

Optional. Flag that indicates whether to retrieve data from the cache, if any, instead of querying the database.Valid values:

-   true: Retrieve data from the cache.
-   false: Query the database to retrieve the data.

Default: true

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

The following code example shows how to turn off the cache so that the query retrieves data from the database instead.

```
var cdmQuery = new sn_cdm.CdmQuery()
  .snapshotId("snapshot_sys_id")
  .decryptPassword(true)
  .useCache(false)
  .query();
```

