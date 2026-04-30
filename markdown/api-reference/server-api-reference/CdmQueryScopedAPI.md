---
title: CdmQuery - Scoped
description: The CdmQuery script include provides methods that enable you to query the CDM data model tree. It returns a list of node objects that are specific fields/columns in the CDM Node \[sn\_cdm\_node\] table. These values are returned as properties in the object. Every object is a node in the data model.Instantiates a CdmQuery object. You must call this method prior to calling any other CdmQuery methods.Enables you to specify whether decrypted values for encrypted configuration data item \(CDI\) and variable nodes are returned in the results.Enables you to specify whether linked nodes are fully resolved, such that descendant nodes of a referenced node appear under a linked node.Iterates through each of the result nodes and applies the provided function that accepts a CdmNode object.Returns the specified CDM query results.Returns the value of the specified field of the current iterated node result.Enables you to specify whether to fetch the file metadata information for file nodes. The file metadata contains attachment\_id, file\_name, content\_type, and checksum.Iterates to the next node result and returns it if it exists.Executes the specified query against the CDM database or the cache based on the settings, entry node, and filter settings.Specifies the entry node. The CdmQuery API limits its query to the entry node and its descendant nodes. Calling this method is mandatory.Enables you to specify whether to substitute variable references in configuration data item \(CDI\) nodes with the value of the referenced variable node.Enables you to specify whether to retrieve data from the cache, if any, instead of querying the database.
locale: en-US
release: yokohama
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 19
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# CdmQuery- Scoped

The CdmQuery script include provides methods that enable you to query the CDM data model tree. It returns a list of node objects that are specific fields/columns in the CDM Node \[sn\_cdm\_node\] table. These values are returned as properties in the object. Every object is a node in the data model.

This script include is fluent which means most of its methods support chaining and return a CdmQuery object. The methods within this script include are classified into different types. You must specify them in a particular order within a call, based on their type. All methods except the result methods are chainable.

**Note:** This documentation only covers the usage of the CdmQuery script include in querying snapshot data, therefore, only methods necessary for this process are currently documented. Querying snapshot data is needed when writing PaCE policy scripts for data validation and CDM exporter scripts for data export.

Method types:

-   entry method: This method specifies the entry node. CdmQuery limits its query to the entry node and its descendant nodes. Specifying the entry node is mandatory.

    [CdmQuery - snapshotId\(String snapshotSysID\)](CdmQueryScopedAPI.md#)

-   query method: This method executes the specified query.

    [CdmQuery - query\(\)](CdmQueryScopedAPI.md#)

-   result methods: These methods return a specific set of results data.
    -   [CdmQuery - forEach\(Function function\)](CdmQueryScopedAPI.md#)
    -   [CdmQuery - getTree\(Boolean simpleTree, Boolean prettify\)](CdmQueryScopedAPI.md#)
    -   [CdmQuery - getValue\(String fieldName\)](CdmQueryScopedAPI.md#)
    -   [CdmQuery - next\(\)](CdmQueryScopedAPI.md#)
-   setting methods: These methods modify the behavior of CdmQuery\(\).
    -   [CdmQuery - decryptPassword\(Boolean decrypt\)](CdmQueryScopedAPI.md#)
    -   [CdmQuery - followIncludes\(Boolean followIncludes\)](CdmQueryScopedAPI.md#)
    -   [CdmQuery - includeFileMetadata\(\)](CdmQueryScopedAPI.md#)
    -   [CdmQuery - substituteVariable\(Boolean substitute\)](CdmQueryScopedAPI.md#)
    -   [CdmQuery - useCache\(Boolean useCache\)](CdmQueryScopedAPI.md#)

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

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## CdmQuery - CdmQuery\(\)

Instantiates a CdmQuery object. You must call this method prior to calling any other CdmQuery methods.

|Name|Type|Description|
|----|----|-----------|
|None| ||

The following code examples shows how to call the CdmQuery method to instantiate a CdmQuery object in the sn\_cdm namespace.

```
var primarySnapshot = new sn_cdm.CdmQuery()
.snapshotId("1a2fe2e6c3a27010cc0a259d7640dd59")
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

The following code example shows how to call the CdmQuery\(\) API and specify to return encrypted values for the CDI and variable nodes.

```
var primarySnapshot = new sn_cdm.CdmQuery()
.snapshotId("9f12a80047352150fd6ce977746d4364")
.decryptPassword(false)
.query()
.getTree(true,true);

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
            "dbUserName": "root",
            "dbPassword": "*******"
          }
        }
      }
    }
  }
}
```

The following code example shows how to call the CdmQuery\(\) API and specify to return decrypted values for the CDI and variable nodes.

```
var primarySnapshot = new sn_cdm.CdmQuery()
.snapshotId("9f12a80047352150fd6ce977746d4364")
.decryptPassword(true)
.query()
.getTree(true,true);

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
            "dbUserName": "root",
            "dbPassword": "dev1-password"
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
-   false: Linked nodes are not fully resolved.

Default: true

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

The following code example shows how to return data that is fully resolved, **followIncludes** = true.

```
var primarySnapshot = new sn_cdm.CdmQuery()
  .snapshotId("9f12a80047352150fd6ce977746d4364")
  .followIncludes(true)
  .query()
  .getTree(false, true);
```

Example return data:

```
{
  "sys_id": "62a0a0cc47f12150fd6ce977746d431a",
  "type": "sn_cdm_node_deployable",
  "main_id": "111673",
  "name": "Development_1",
  "node_path": "!K<+!K<0!K<1",
  "effective_path": "!K<+!K<0!K<1",
  "main_id_encoded": "K<1",
  "node_classifier": "/application/deployables/env:Development",
  "status": "valid",
  "level": "2",
  "children": [
    {
      "sys_id": "2aa0a0cc47f12150fd6ce977746d431a",
      "type": "sn_cdm_node_folder",
      "main_id": "111674",
      "name": "vars",
      "node_path": "!K<+!K<0!K<1!K<2",
      "effective_path": "!K<+!K<0!K<1!K<2",
      "main_id_encoded": "K<2",
      "node_classifier": "/application/deployables/env:Development/vars",
      "status": "valid",
      "level": "3",
      "children": [],
      "hasParent": true
    },
    {
      "sys_id": "2ca1600047352150fd6ce977746d4391",
      "type": "sn_cdm_node_linked",
      "main_id": "111693",
      "name": "services",
      "node_path": "!K<+!K<0!K<1!K<G",
      "effective_path": "!K<+!K<0!K<1!K<G",
      "main_id_encoded": "K<G",
      "node_classifier": "/application/deployables/env:Development",
      "status": "valid",
      "level": "3",
      "children": [
        {
          "sys_id": "2bb0e0cc47f12150fd6ce977746d43e2",
          "type": "sn_cdm_node_folder",
          "main_id": "111680",
          "name": "vars",
          "node_path": "!K<+!K</!K<7!K<8",
          "effective_path": "!K<+!K<0!K<1!K<G!K<8",
          "main_id_encoded": "K<8",
          "node_classifier": "/application/collections/vars",
          "status": "valid",
          "level": "3",
          "children": [],
          "hasParent": true
        },
        {
          "sys_id": "ccf1640047352150fd6ce977746d438b",
          "type": "sn_cdm_node_component",
          "main_id": "111697",
          "name": "paymentComponent",
          "node_path": "!K<+!K<0!K<1!K<G!K<K",
          "effective_path": "!K<+!K<0!K<1!K<G!K<K",
          "main_id_encoded": "K<K",
          "node_classifier": "/application/deployables/env:Development",
          "status": "valid",
          "level": "4",
          "children": [
            {
              "sys_id": "7fd064cc47f12150fd6ce977746d4372",
              "type": "sn_cdm_node_cdi",
              "main_id": "111682",
              "name": "applicationSLA",
              "node_path": "!K<+!K<,!K<9!K<:",
              "value": "24x7",
              "effective_path": "!K<+!K<0!K<1!K<G!K<K!K<:",
              "main_id_encoded": "K<:",
              "node_classifier": "/application/components",
              "status": "valid",
              "level": "3",
              "children": [],
              "hasParent": true
            },
            {
              "sys_id": "44f1a40047352150fd6ce977746d43dc",
              "type": "sn_cdm_node_component",
              "main_id": "111698",
              "name": "paymentService",
              "node_path": "!K<+!K<0!K<1!K<G!K<K!K<L",
              "effective_path": "!K<+!K<0!K<1!K<G!K<K!K<L",
              "main_id_encoded": "K<L",
              "node_classifier": "/application/deployables/env:Development",
              "status": "valid",
              "level": "5",
              "children": [
                {
                  "sys_id": "8cf1a40047352150fd6ce977746d43dc",
                  "type": "sn_cdm_node_component",
                  "main_id": "111699",
                  "name": "database",
                  "node_path": "!K<+!K<0!K<1!K<G!K<K!K<L!K<M",
                  "effective_path": "!K<+!K<0!K<1!K<G!K<K!K<L!K<M",
                  "main_id_encoded": "K<M",
                  "node_classifier": "/application/deployables/env:Development",
                  "status": "valid",
                  "level": "6",
                  "children": [
                    {
                      "sys_id": "b3d064cc47f12150fd6ce977746d4374",
                      "type": "sn_cdm_node_component",
                      "main_id": "111685",
                      "name": "backup",
                      "node_path": "!K<+!K<,!K<9!K<;!K<<!K<?",
                      "effective_path": "!K<+!K<0!K<1!K<G!K<K!K<L!K<M!K<?",
                      "main_id_encoded": "K<?",
                      "node_classifier": "/application/components",
                      "status": "valid",
                      "level": "5",
                      "children": [
                        {
                          "sys_id": "7bd064cc47f12150fd6ce977746d4374",
                          "type": "sn_cdm_node_cdi",
                          "main_id": "111686",
                          "name": "dbServer",
                          "node_path": "!K<+!K<,!K<9!K<;!K<<!K<?!K<@",
                          "value": "db23.paymentx.be",
                          "effective_path": "!K<+!K<0!K<1!K<G!K<K!K<L!K<M!K<?!K<@",
                          "main_id_encoded": "K<@",
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
                      "sys_id": "33d064cc47f12150fd6ce977746d4375",
                      "type": "sn_cdm_node_cdi",
                      "main_id": "111687",
                      "name": "dbIpAddress",
                      "node_path": "!K<+!K<,!K<9!K<;!K<<!K<A",
                      "value": "10.20.40.50",
                      "effective_path": "!K<+!K<0!K<1!K<G!K<K!K<L!K<M!K<A",
                      "main_id_encoded": "K<A",
                      "node_classifier": "/application/components",
                      "status": "valid",
                      "level": "5",
                      "children": [],
                      "hasParent": true
                    },
                    {
                      "sys_id": "f7d064cc47f12150fd6ce977746d4375",
                      "type": "sn_cdm_node_cdi",
                      "main_id": "111688",
                      "name": "dbName",
                      "node_path": "!K<+!K<,!K<9!K<;!K<<!K<B",
                      "value": "paymentX_dev2",
                      "effective_path": "!K<+!K<0!K<1!K<G!K<K!K<L!K<M!K<B",
                      "main_id_encoded": "K<B",
                      "node_classifier": "/application/components",
                      "status": "valid",
                      "level": "5",
                      "children": [],
                      "hasParent": true
                    },
                    {
                      "sys_id": "77d064cc47f12150fd6ce977746d4376",
                      "type": "sn_cdm_node_cdi",
                      "main_id": "111690",
                      "name": "dbPort",
                      "node_path": "!K<+!K<,!K<9!K<;!K<<!K<D",
                      "value": "8050",
                      "effective_path": "!K<+!K<0!K<1!K<G!K<K!K<L!K<M!K<D",
                      "main_id_encoded": "K<D",
                      "node_classifier": "/application/components",
                      "status": "valid",
                      "level": "5",
                      "children": [],
                      "hasParent": true
                    },
                    {
                      "sys_id": "3fd064cc47f12150fd6ce977746d4376",
                      "type": "sn_cdm_node_cdi",
                      "main_id": "111691",
                      "name": "dbServer",
                      "node_path": "!K<+!K<,!K<9!K<;!K<<!K<E",
                      "value": "db22.paymentx.be",
                      "effective_path": "!K<+!K<0!K<1!K<G!K<K!K<L!K<M!K<E",
                      "main_id_encoded": "K<E",
                      "node_classifier": "/application/components",
                      "status": "valid",
                      "level": "5",
                      "children": [],
                      "hasParent": true
                    },
                    {
                      "sys_id": "f3d064cc47f12150fd6ce977746d4377",
                      "type": "sn_cdm_node_cdi",
                      "main_id": "111692",
                      "name": "dbUserName",
                      "node_path": "!K<+!K<,!K<9!K<;!K<<!K<F",
                      "value": "root",
                      "effective_path": "!K<+!K<0!K<1!K<G!K<K!K<L!K<M!K<F",
                      "main_id_encoded": "K<F",
                      "node_classifier": "/application/components",
                      "status": "valid",
                      "level": "5",
                      "children": [],
                      "hasParent": true
                    },
                    {
                      "sys_id": "c4f1a40047352150fd6ce977746d43dd",
                      "type": "sn_cdm_node_cdi",
                      "main_id": "111700",
                      "name": "dbPassword",
                      "node_path": "!K<+!K<0!K<1!K<G!K<K!K<L!K<M!K<N",
                      "secure_value": "﷞﷟﷒dac329a2476c6110fd6ce977746d43e1﷬﷔1﷬﷭w8YJ85PO5byT5YNmeG_HwQ==WrNQP39n-PWKFs_VXFSjr3TJsGxS1ESKpyl4PUE=﷮﷯",
                      "effective_path": "!K<+!K<0!K<1!K<G!K<K!K<L!K<M!K<N",
                      "main_id_encoded": "K<N",
                      "node_classifier": "/application/deployables/env:Development",
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

The following code example shows how to return data that is not fully resolved, **followIncludes** = false.

```
var primarySnapshot = new sn_cdm.CdmQuery()
  .snapshotId("9f12a80047352150fd6ce977746d4364")
  .followIncludes(false)
  .query()
  .getTree(false, true);
```

Example return data:

```
{
  "sys_id": "62a0a0cc47f12150fd6ce977746d431a",
  "type": "sn_cdm_node_deployable",
  "main_id": "111673",
  "name": "Development_1",
  "node_path": "!K<+!K<0!K<1",
  "effective_path": "!K<+!K<0!K<1",
  "main_id_encoded": "K<1",
  "node_classifier": "/application/deployables/env:Development",
  "status": "valid",
  "level": "2",
  "children": [
    {
      "sys_id": "2aa0a0cc47f12150fd6ce977746d431a",
      "type": "sn_cdm_node_folder",
      "main_id": "111674",
      "name": "vars",
      "node_path": "!K<+!K<0!K<1!K<2",
      "effective_path": "!K<+!K<0!K<1!K<2",
      "main_id_encoded": "K<2",
      "node_classifier": "/application/deployables/env:Development/vars",
      "status": "valid",
      "level": "3",
      "children": [],
      "hasParent": true
    },
    {
      "sys_id": "2ca1600047352150fd6ce977746d4391",
      "type": "sn_cdm_node_linked",
      "main_id": "111693",
      "name": "services",
      "node_path": "!K<+!K<0!K<1!K<G",
      "effective_path": "!K<+!K<0!K<1!K<G",
      "main_id_encoded": "K<G",
      "node_classifier": "/application/deployables/env:Development",
      "status": "valid",
      "level": "3",
      "children": [
        {
          "sys_id": "ccf1640047352150fd6ce977746d438b",
          "type": "sn_cdm_node_component",
          "main_id": "111697",
          "name": "paymentComponent",
          "node_path": "!K<+!K<0!K<1!K<G!K<K",
          "effective_path": "!K<+!K<0!K<1!K<G!K<K",
          "main_id_encoded": "K<K",
          "node_classifier": "/application/deployables/env:Development",
          "status": "valid",
          "level": "4",
          "children": [
            {
              "sys_id": "44f1a40047352150fd6ce977746d43dc",
              "type": "sn_cdm_node_component",
              "main_id": "111698",
              "name": "paymentService",
              "node_path": "!K<+!K<0!K<1!K<G!K<K!K<L",
              "effective_path": "!K<+!K<0!K<1!K<G!K<K!K<L",
              "main_id_encoded": "K<L",
              "node_classifier": "/application/deployables/env:Development",
              "status": "valid",
              "level": "5",
              "children": [
                {
                  "sys_id": "8cf1a40047352150fd6ce977746d43dc",
                  "type": "sn_cdm_node_component",
                  "main_id": "111699",
                  "name": "database",
                  "node_path": "!K<+!K<0!K<1!K<G!K<K!K<L!K<M",
                  "effective_path": "!K<+!K<0!K<1!K<G!K<K!K<L!K<M",
                  "main_id_encoded": "K<M",
                  "node_classifier": "/application/deployables/env:Development",
                  "status": "valid",
                  "level": "6",
                  "children": [
                    {
                      "sys_id": "c4f1a40047352150fd6ce977746d43dd",
                      "type": "sn_cdm_node_cdi",
                      "main_id": "111700",
                      "name": "dbPassword",
                      "node_path": "!K<+!K<0!K<1!K<G!K<K!K<L!K<M!K<N",
                      "secure_value": "﷞﷟﷒dac329a2476c6110fd6ce977746d43e1﷬﷔1﷬﷭w8YJ85PO5byT5YNmeG_HwQ==WrNQP39n-PWKFs_VXFSjr3TJsGxS1ESKpyl4PUE=﷮﷯",
                      "effective_path": "!K<+!K<0!K<1!K<G!K<K!K<L!K<M!K<N",
                      "main_id_encoded": "K<N",
                      "node_classifier": "/application/deployables/env:Development",
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

This code example shows how to call the forEach\(\) method.

```
CdmQuery.forEach(function (node) {
  gs.info("Node - {0}:{1} ", [node.getValue("name"), node.getValue("value")]);
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

The following code example shows how to call the getTree\(\) method using the default settings. This returns a formatted string containing the node metadata and all its child nodes.

```
var primarySnapshot = new sn_cdm.CdmQuery()
  .snapshotId("9f12a80047352150fd6ce977746d4364")
  .query()
  .getTree();

gs.info(JSON.stringify(primarySnapshot));
```

Return results:

```
{"sys_id":"62a0a0cc47f12150fd6ce977746d431a","type":"sn_cdm_node_deployable","main_id":"111673","name":"Development_1","node_path":"!K<+!K<0!K<1","effective_path":"!K<+!K<0!K<1","main_id_encoded":"K<1","node_classifier":"/application/deployables/env:Development","status":"valid","level":"2","children":[{"sys_id":"2aa0a0cc47f12150fd6ce977746d431a","type":"sn_cdm_node_folder","main_id":"111674","name":"vars","node_path":"!K<+!K<0!K<1!K<2","effective_path":"!K<+!K<0!K<1!K<2","main_id_encoded":"K<2","node_classifier":"/application/deployables/env:Development/vars","status":"valid","level":"3","children":[],"hasParent":true},{"sys_id":"2ca1600047352150fd6ce977746d4391","type":"sn_cdm_node_linked","main_id":"111693","name":"services","node_path":"!K<+!K<0!K<1!K<G","effective_path":"!K<+!K<0!K<1!K<G","main_id_encoded":"K<G","node_classifier":"/application/deployables/env:Development","status":"valid","level":"3","children":[{"sys_id":"2bb0e0cc47f12150fd6ce977746d43e2","type":"sn_cdm_node_folder","main_id":"111680","name":"vars","node_path":"!K<+!K</!K<7!K<8","effective_path":"!K<+!K<0!K<1!K<G!K<8","main_id_encoded":"K<8","node_classifier":"/application/collections/vars","status":"valid","level":"3","children":[],"hasParent":true},{"sys_id":"ccf1640047352150fd6ce977746d438b","type":"sn_cdm_node_component","main_id":"111697","name":"paymentComponent","node_path":"!K<+!K<0!K<1!K<G!K<K","effective_path":"!K<+!K<0!K<1!K<G!K<K","main_id_encoded":"K<K","node_classifier":"/application/deployables/env:Development","status":"valid","level":"4","children":[{"sys_id":"7fd064cc47f12150fd6ce977746d4372","type":"sn_cdm_node_cdi","main_id":"111682","name":"applicationSLA","node_path":"!K<+!K<,!K<9!K<:","value":"24x7","effective_path":"!K<+!K<0!K<1!K<G!K<K!K<:","main_id_encoded":"K<:","node_classifier":"/application/components","status":"valid","level":"3","children":[],"hasParent":true},{"sys_id":"44f1a40047352150fd6ce977746d43dc","type":"sn_cdm_node_component","main_id":"111698","name":"paymentService","node_path":"!K<+!K<0!K<1!K<G!K<K!K<L","effective_path":"!K<+!K<0!K<1!K<G!K<K!K<L","main_id_encoded":"K<L","node_classifier":"/application/deployables/env:Development","status":"valid","level":"5","children":[{"sys_id":"8cf1a40047352150fd6ce977746d43dc","type":"sn_cdm_node_component","main_id":"111699","name":"database","node_path":"!K<+!K<0!K<1!K<G!K<K!K<L!K<M","effective_path":"!K<+!K<0!K<1!K<G!K<K!K<L!K<M","main_id_encoded":"K<M","node_classifier":"/application/deployables/env:Development","status":"valid","level":"6","children":[{"sys_id":"b3d064cc47f12150fd6ce977746d4374","type":"sn_cdm_node_component","main_id":"111685","name":"backup","node_path":"!K<+!K<,!K<9!K<;!K<<!K<?","effective_path":"!K<+!K<0!K<1!K<G!K<K!K<L!K<M!K<?","main_id_encoded":"K<?","node_classifier":"/application/components","status":"valid","level":"5","children":[{"sys_id":"7bd064cc47f12150fd6ce977746d4374","type":"sn_cdm_node_cdi","main_id":"111686","name":"dbServer","node_path":"!K<+!K<,!K<9!K<;!K<<!K<?!K<@","value":"db23.paymentx.be","effective_path":"!K<+!K<0!K<1!K<G!K<K!K<L!K<M!K<?!K<@","main_id_encoded":"K<@","node_classifier":"/application/components","status":"valid","level":"6","children":[],"hasParent":true}],"hasParent":true},{"sys_id":"33d064cc47f12150fd6ce977746d4375","type":"sn_cdm_node_cdi","main_id":"111687","name":"dbIpAddress","node_path":"!K<+!K<,!K<9!K<;!K<<!K<A","value":"10.20.40.50","effective_path":"!K<+!K<0!K<1!K<G!K<K!K<L!K<M!K<A","main_id_encoded":"K<A","node_classifier":"/application/components","status":"valid","level":"5","children":[],"hasParent":true},{"sys_id":"f7d064cc47f12150fd6ce977746d4375","type":"sn_cdm_node_cdi","main_id":"111688","name":"dbName","node_path":"!K<+!K<,!K<9!K<;!K<<!K<B","value":"paymentX_dev2","effective_path":"!K<+!K<0!K<1!K<G!K<K!K<L!K<M!K<B","main_id_encoded":"K<B","node_classifier":"/application/components","status":"valid","level":"5","children":[],"hasParent":true},{"sys_id":"77d064cc47f12150fd6ce977746d4376","type":"sn_cdm_node_cdi","main_id":"111690","name":"dbPort","node_path":"!K<+!K<,!K<9!K<;!K<<!K<D","value":"8050","effective_path":"!K<+!K<0!K<1!K<G!K<K!K<L!K<M!K<D","main_id_encoded":"K<D","node_classifier":"/application/components","status":"valid","level":"5","children":[],"hasParent":true},{"sys_id":"3fd064cc47f12150fd6ce977746d4376","type":"sn_cdm_node_cdi","main_id":"111691","name":"dbServer","node_path":"!K<+!K<,!K<9!K<;!K<<!K<E","value":"db22.paymentx.be","effective_path":"!K<+!K<0!K<1!K<G!K<K!K<L!K<M!K<E","main_id_encoded":"K<E","node_classifier":"/application/components","status":"valid","level":"5","children":[],"hasParent":true},{"sys_id":"f3d064cc47f12150fd6ce977746d4377","type":"sn_cdm_node_cdi","main_id":"111692","name":"dbUserName","node_path":"!K<+!K<,!K<9!K<;!K<<!K<F","value":"root","effective_path":"!K<+!K<0!K<1!K<G!K<K!K<L!K<M!K<F","main_id_encoded":"K<F","node_classifier":"/application/components","status":"valid","level":"5","children":[],"hasParent":true},{"sys_id":"c4f1a40047352150fd6ce977746d43dd","type":"sn_cdm_node_cdi","main_id":"111700","name":"dbPassword","node_path":"!K<+!K<0!K<1!K<G!K<K!K<L!K<M!K<N","secure_value":"﷞﷟﷒dac329a2476c6110fd6ce977746d43e1﷬﷔1﷬﷭w8YJ85PO5byT5YNmeG_HwQ==WrNQP39n-PWKFs_VXFSjr3TJsGxS1ESKpyl4PUE=﷮﷯","effective_path":"!K<+!K<0!K<1!K<G!K<K!K<L!K<M!K<N","main_id_encoded":"K<N","node_classifier":"/application/deployables/env:Development","status":"valid","level":"7","masked_value":"*******","children":[],"hasParent":true}],"hasParent":true}],"hasParent":true}],"hasParent":true}],"hasParent":true}]}

```

The following code example shows how to call the getTree\(\) method to return a simplified JSON object of hierarchical key-values pairs.

```
var primarySnapshot = new sn_cdm.CdmQuery()
  .snapshotId("9f12a80047352150fd6ce977746d4364")
  .query()
  .getTree(true, true);

gs.info(JSON.stringify(primarySnapshot));
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
            "dbUserName": "root",
            "dbPassword": "*******"
          }
        }
      }
    }
  }
}
```

The following code example shows how to call the getTree\(\) method to return a JSON object containing the node metadata and all its child nodes.

```
var primarySnapshot = new sn_cdm.CdmQuery()
  .snapshotId("9f12a80047352150fd6ce977746d4364")
  .query()
  .getTree(false, true);

gs.info(JSON.stringify(primarySnapshot));
```

Return results:

```
{
  "sys_id": "62a0a0cc47f12150fd6ce977746d431a",
  "type": "sn_cdm_node_deployable",
  "main_id": "111673",
  "name": "Development_1",
  "node_path": "!K<+!K<0!K<1",
  "effective_path": "!K<+!K<0!K<1",
  "main_id_encoded": "K<1",
  "node_classifier": "/application/deployables/env:Development",
  "status": "valid",
  "level": "2",
  "children": [
    {
      "sys_id": "2aa0a0cc47f12150fd6ce977746d431a",
      "type": "sn_cdm_node_folder",
      "main_id": "111674",
      "name": "vars",
      "node_path": "!K<+!K<0!K<1!K<2",
      "effective_path": "!K<+!K<0!K<1!K<2",
      "main_id_encoded": "K<2",
      "node_classifier": "/application/deployables/env:Development/vars",
      "status": "valid",
      "level": "3",
      "children": [],
      "hasParent": true
    },
    {
      "sys_id": "2ca1600047352150fd6ce977746d4391",
      "type": "sn_cdm_node_linked",
      "main_id": "111693",
      "name": "services",
      "node_path": "!K<+!K<0!K<1!K<G",
      "effective_path": "!K<+!K<0!K<1!K<G",
      "main_id_encoded": "K<G",
      "node_classifier": "/application/deployables/env:Development",
      "status": "valid",
      "level": "3",
      "children": [
        {
          "sys_id": "2bb0e0cc47f12150fd6ce977746d43e2",
          "type": "sn_cdm_node_folder",
          "main_id": "111680",
          "name": "vars",
          "node_path": "!K<+!K</!K<7!K<8",
          "effective_path": "!K<+!K<0!K<1!K<G!K<8",
          "main_id_encoded": "K<8",
          "node_classifier": "/application/collections/vars",
          "status": "valid",
          "level": "3",
          "children": [],
          "hasParent": true
        },
        {
          "sys_id": "ccf1640047352150fd6ce977746d438b",
          "type": "sn_cdm_node_component",
          "main_id": "111697",
          "name": "paymentComponent",
          "node_path": "!K<+!K<0!K<1!K<G!K<K",
          "effective_path": "!K<+!K<0!K<1!K<G!K<K",
          "main_id_encoded": "K<K",
          "node_classifier": "/application/deployables/env:Development",
          "status": "valid",
          "level": "4",
          "children": [
            {
              "sys_id": "7fd064cc47f12150fd6ce977746d4372",
              "type": "sn_cdm_node_cdi",
              "main_id": "111682",
              "name": "applicationSLA",
              "node_path": "!K<+!K<,!K<9!K<:",
              "value": "24x7",
              "effective_path": "!K<+!K<0!K<1!K<G!K<K!K<:",
              "main_id_encoded": "K<:",
              "node_classifier": "/application/components",
              "status": "valid",
              "level": "3",
              "children": [],
              "hasParent": true
            },
            {
              "sys_id": "44f1a40047352150fd6ce977746d43dc",
              "type": "sn_cdm_node_component",
              "main_id": "111698",
              "name": "paymentService",
              "node_path": "!K<+!K<0!K<1!K<G!K<K!K<L",
              "effective_path": "!K<+!K<0!K<1!K<G!K<K!K<L",
              "main_id_encoded": "K<L",
              "node_classifier": "/application/deployables/env:Development",
              "status": "valid",
              "level": "5",
              "children": [
                {
                  "sys_id": "8cf1a40047352150fd6ce977746d43dc",
                  "type": "sn_cdm_node_component",
                  "main_id": "111699",
                  "name": "database",
                  "node_path": "!K<+!K<0!K<1!K<G!K<K!K<L!K<M",
                  "effective_path": "!K<+!K<0!K<1!K<G!K<K!K<L!K<M",
                  "main_id_encoded": "K<M",
                  "node_classifier": "/application/deployables/env:Development",
                  "status": "valid",
                  "level": "6",
                  "children": [
                    {
                      "sys_id": "b3d064cc47f12150fd6ce977746d4374",
                      "type": "sn_cdm_node_component",
                      "main_id": "111685",
                      "name": "backup",
                      "node_path": "!K<+!K<,!K<9!K<;!K<<!K<?",
                      "effective_path": "!K<+!K<0!K<1!K<G!K<K!K<L!K<M!K<?",
                      "main_id_encoded": "K<?",
                      "node_classifier": "/application/components",
                      "status": "valid",
                      "level": "5",
                      "children": [
                        {
                          "sys_id": "7bd064cc47f12150fd6ce977746d4374",
                          "type": "sn_cdm_node_cdi",
                          "main_id": "111686",
                          "name": "dbServer",
                          "node_path": "!K<+!K<,!K<9!K<;!K<<!K<?!K<@",
                          "value": "db23.paymentx.be",
                          "effective_path": "!K<+!K<0!K<1!K<G!K<K!K<L!K<M!K<?!K<@",
                          "main_id_encoded": "K<@",
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
                      "sys_id": "33d064cc47f12150fd6ce977746d4375",
                      "type": "sn_cdm_node_cdi",
                      "main_id": "111687",
                      "name": "dbIpAddress",
                      "node_path": "!K<+!K<,!K<9!K<;!K<<!K<A",
                      "value": "10.20.40.50",
                      "effective_path": "!K<+!K<0!K<1!K<G!K<K!K<L!K<M!K<A",
                      "main_id_encoded": "K<A",
                      "node_classifier": "/application/components",
                      "status": "valid",
                      "level": "5",
                      "children": [],
                      "hasParent": true
                    },
                    {
                      "sys_id": "f7d064cc47f12150fd6ce977746d4375",
                      "type": "sn_cdm_node_cdi",
                      "main_id": "111688",
                      "name": "dbName",
                      "node_path": "!K<+!K<,!K<9!K<;!K<<!K<B",
                      "value": "paymentX_dev2",
                      "effective_path": "!K<+!K<0!K<1!K<G!K<K!K<L!K<M!K<B",
                      "main_id_encoded": "K<B",
                      "node_classifier": "/application/components",
                      "status": "valid",
                      "level": "5",
                      "children": [],
                      "hasParent": true
                    },
                    {
                      "sys_id": "77d064cc47f12150fd6ce977746d4376",
                      "type": "sn_cdm_node_cdi",
                      "main_id": "111690",
                      "name": "dbPort",
                      "node_path": "!K<+!K<,!K<9!K<;!K<<!K<D",
                      "value": "8050",
                      "effective_path": "!K<+!K<0!K<1!K<G!K<K!K<L!K<M!K<D",
                      "main_id_encoded": "K<D",
                      "node_classifier": "/application/components",
                      "status": "valid",
                      "level": "5",
                      "children": [],
                      "hasParent": true
                    },
                    {
                      "sys_id": "3fd064cc47f12150fd6ce977746d4376",
                      "type": "sn_cdm_node_cdi",
                      "main_id": "111691",
                      "name": "dbServer",
                      "node_path": "!K<+!K<,!K<9!K<;!K<<!K<E",
                      "value": "db22.paymentx.be",
                      "effective_path": "!K<+!K<0!K<1!K<G!K<K!K<L!K<M!K<E",
                      "main_id_encoded": "K<E",
                      "node_classifier": "/application/components",
                      "status": "valid",
                      "level": "5",
                      "children": [],
                      "hasParent": true
                    },
                    {
                      "sys_id": "f3d064cc47f12150fd6ce977746d4377",
                      "type": "sn_cdm_node_cdi",
                      "main_id": "111692",
                      "name": "dbUserName",
                      "node_path": "!K<+!K<,!K<9!K<;!K<<!K<F",
                      "value": "root",
                      "effective_path": "!K<+!K<0!K<1!K<G!K<K!K<L!K<M!K<F",
                      "main_id_encoded": "K<F",
                      "node_classifier": "/application/components",
                      "status": "valid",
                      "level": "5",
                      "children": [],
                      "hasParent": true
                    },
                    {
                      "sys_id": "c4f1a40047352150fd6ce977746d43dd",
                      "type": "sn_cdm_node_cdi",
                      "main_id": "111700",
                      "name": "dbPassword",
                      "node_path": "!K<+!K<0!K<1!K<G!K<K!K<L!K<M!K<N",
                      "secure_value": "﷞﷟﷒dac329a2476c6110fd6ce977746d43e1﷬﷔1﷬﷭w8YJ85PO5byT5YNmeG_HwQ==WrNQP39n-PWKFs_VXFSjr3TJsGxS1ESKpyl4PUE=﷮﷯",
                      "effective_path": "!K<+!K<0!K<1!K<G!K<K!K<L!K<M!K<N",
                      "main_id_encoded": "K<N",
                      "node_classifier": "/application/deployables/env:Development",
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

The following code example shows how to use the getValue\(\) method to extract required data.

```
var cdmQuery = new sn_cdm.CdmQuery()
  .snapshotId("1a2fe2e6c3a27010cc0a259d7640dd59")
  .decryptPassword(true)
  .query();  

var output = [];
  while(cdmQuery.next()) {
    var name = cdmQuery.getValue('name');
    var type = cdmQuery.getValue('type');

    if (type == 'sg_cdm_node_cdi' || type == 'sg_cdm_node_variable') {
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
  "test_login_service [sg_cdm_node_deployable]",
  "vars [sg_cdm_node_folder]",
  "service_password : service12345 [sg_cdm_node_variable]",
  "login_service [sg_cdm_node_linked]",
  "vars [sg_cdm_node_folder]",
  "core_component [sg_cdm_node_component]",
  "user_name : admin [sg_cdm_node_cdi]",
  "user_password : service12345 [sg_cdm_node_cdi]"
]
```

## CdmQuery - includeFileMetadata\(\)

Enables you to specify whether to fetch the file metadata information for file nodes. The file metadata contains attachment\_id, file\_name, content\_type, and checksum.

**Note:** Metadata is only returned for non-simple trees. For additional information on this type of data return, see [CdmQuery - getTree\(Boolean simpleTree, Boolean prettify\)](CdmQueryScopedAPI.md#).

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|None| |

The following code example shows how to call the CdmQuery\(\) API and return file metadata information.

```
var cdmQuery = new CdmQuery()
.snapshotId("20c365a2476c6110fd6ce977746d4336")
.includeFileMetadata()
.query()
.getTree(false, true);
```

Returns:

```
{
  "sys_id": "62a0a0cc47f12150fd6ce977746d431a",
  "type": "sn_cdm_node_deployable",
  "main_id": "111673",
  "name": "Development_1",
  "node_path": "!K<+!K<0!K<1",
  "effective_path": "!K<+!K<0!K<1",
  "main_id_encoded": "K<1",
  "node_classifier": "/application/deployables/env:Development",
  "status": "valid",
  "level": "2",
  "children": [
    {
      "sys_id": "2aa0a0cc47f12150fd6ce977746d431a",
      "type": "sn_cdm_node_folder",
      "main_id": "111674",
      "name": "vars",
      "node_path": "!K<+!K<0!K<1!K<2",
      "effective_path": "!K<+!K<0!K<1!K<2",
      "main_id_encoded": "K<2",
      "node_classifier": "/application/deployables/env:Development/vars",
      "status": "valid",
      "level": "3",
      "children": [],
      "hasParent": true
    },
    {
      "sys_id": "b83eb65fffdf6110f0ccffffffffff7d",
      "type": "sn_cdm_node_file",
      "main_id": "111675",
      "name": "deploy_config.xml",
      "node_path": "!K<+!K<0!K<1!K<G",
      "value": "file: http://instance.servicenow.com/sys_attachment.do?sys_id=bc3eb65fffdf6110f0ccffffffffff7d",
      "effective_path": "!K<+!K<0!K<1!K<G",
      "main_id_encoded": "V",
      "node_classifier": "/application/deployables/env:Development",
      "status": "valid",
      "level": "3",
      "file_metadata": {
        "attachment_id": "bc3eb65fffdf6110f0ccffffffffff7d",
        "file_name": "deploy_config.xml",
        "content_type": "application/xml",
        "checksum": "UbWkF5HZOQTQ89bFrqyFBg=="
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
</table>The following code example shows how the next\(\) method to iterate through the available node.

```
var cdmQuery = new sn_cdm.CdmQuery()
  .snapshotId("1a2fe2e6c3a27010cc0a259d7640dd59")
  .decryptPassword(true)
  .query(); 

var output = [];
while(cdmQuery.next()) {
  var name = cdmQuery.getValue('name');
  var type = cdmQuery.getValue('type');
    if (type == 'sg_cdm_node_cdi' || type == 'sg_cdm_node_variable') {
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
  "test_login_service [sg_cdm_node_deployable]",
  "vars [sg_cdm_node_folder]",
  "service_password : service12345 [sg_cdm_node_variable]",
  "login_service [sg_cdm_node_linked]",
  "vars [sg_cdm_node_folder]",
  "core_component [sg_cdm_node_component]",
  "user_name : username [sg_cdm_node_cdi]",
  "user_password : service12345 [sg_cdm_node_cdi]" 
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

The following code example shows how to call the CdmQuery\(\) API and specify the deployable snapshot to query.

```
var primarySnapshot = new sn_cdm.CdmQuery()
.snapshotId("1a2fe2e6c3a27010cc0a259d7640dd59")
.decryptPassword(true)
.query()
.getTree();
```

Return results:

```
{ 
  "_decryptPassword": true,
  "sys_id": "d73d6666c3a27010cc0a259d7640dde7",
  "type": "sg_cdm_node_deployable",
  "main_id": "731",
  "name": "test_login_service",
  "node_path": "!1+!1/!10",
  "effective_path": "!1+!1/!10",
  "main_id_encoded": "10",
  "node_classifier": "/application/deployables/dep:test_login_service", 
  "status": "valid", 
  "children": [
    {
      "_decryptPassword": true,
      "sys_id": "9f3d6666c3a27010cc0a259d7640dde7",
      "type": "sg_cdm_node_folder",
      "main_id": "732",
      "name": "vars",
      "node_path": "!1+!1/!10!11",
      "effective_path": "!1+!1/!10!11",
      "main_id_encoded": "11",
      "node_classifier": "/application/deployables/dep:test_login_service/vars",
      "status": "valid",
      "children": [
        {
          "_decryptPassword": true,
          "sys_id": "49dd2e66c3a27010cc0a259d7640ddf9",
          "type": "sg_cdm_node_variable", 
          "main_id": "741",
          "name": "service_password",
          "node_path": "!1+!1/!10!11!1:",
          "value": "service12345",
          "effective_path": "!1+!1/!10!11!1:",
          "main_id_encoded": "1:",
          "node_classifier": "/application/deployables/dep:test_login_service/vars",
          "status": "valid",
          "children": [],
          "hasParent": true 
        }
      ], 
      "hasParent": true 
    }, 
    {
      "_decryptPassword": true,
      "sys_id": "26bd2e66c3a27010cc0a259d7640dd74",
      "type": "sg_cdm_node_linked",
      "main_id": "740",
      "name": "login_service",
      "node_path": "!1+!1/!10!19",
      "effective_path": "!1+!1/!10!19",
      "main_id_encoded": "19",
      "node_classifier": "/application/deployables/dep:test_login_service",
      "status": "valid",
      "children": [
        {
          "_decryptPassword": true,
          "sys_id": "eeadea66c3a27010cc0a259d7640dd8c",
          "type": "sg_cdm_node_folder",
          "main_id": "738",
          "name": "vars",
          "node_path": "!1+!1.!16!17",
          "effective_path": "!1+!1/!10!19!17",
          "main_id_encoded": "17",
          "node_classifier": "/application/collections/vars",
          "status": "valid",
          "children": [],
          "hasParent": true 
        },
        { 
          "_decryptPassword": true,
          "sys_id": "da1f22e6c3a27010cc0a259d7640dda2",
          "type": "sg_cdm_node_component",
          "main_id": "742",
          "name": "core_component",
          "node_path": "!1+!1/!10!19!1;",
          "effective_path": "!1+!1/!10!19!1;",
          "main_id_encoded": "1;",
          "node_classifier": "/application/deployables/dep:test_login_service",
          "status": "valid",
          "children": [
            { 
              "_decryptPassword": true,
              "sys_id": "921f22e6c3a27010cc0a259d7640dda3",
              "type": "sg_cdm_node_cdi",
              "main_id": "743",
              "name": "user_name",
              "node_path": "!1+!1/!10!19!1;!1<",
              "value": "admin",
              "effective_path": "!1+!1/!10!19!1;!1<",
              "main_id_encoded": "1<",
              "node_classifier": "/application/deployables/dep:test_login_service",
              "status": "valid",
              "children": [],
              "hasParent": true
            },
            { 
              "_decryptPassword": true,
              "sys_id": "5a1f22e6c3a27010cc0a259d7640dda3",
              "type": "sg_cdm_node_cdi",
              "main_id": "744",
              "name": "user_password",
              "node_path": "!1+!1/!10!19!1;!1?",
              "value": "service12345",
              "effective_path": "!1+!1/!10!19!1;!1?",
              "main_id_encoded": "1?",
              "node_classifier": "/application/deployables/dep:test_login_service",
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

The following code example shows how to call the CdmQuery\(\) API and specify the deployable snapshot to query.

```
var primarySnapshot = new sn_cdm.CdmQuery()
.snapshotId("1a2fe2e6c3a27010cc0a259d7640dd59")
.decryptPassword(true)
.query()
.getTree();
```

Return results:

```
{ 
  "_decryptPassword": true,
  "sys_id": "d73d6666c3a27010cc0a259d7640dde7",
  "type": "sg_cdm_node_deployable",
  "main_id": "731",
  "name": "test_login_service",
  "node_path": "!1+!1/!10",
  "effective_path": "!1+!1/!10",
  "main_id_encoded": "10",
  "node_classifier": "/application/deployables/dep:test_login_service", 
  "status": "valid", 
  "children": [
    {
      "_decryptPassword": true,
      "sys_id": "9f3d6666c3a27010cc0a259d7640dde7",
      "type": "sg_cdm_node_folder",
      "main_id": "732",
      "name": "vars",
      "node_path": "!1+!1/!10!11",
      "effective_path": "!1+!1/!10!11",
      "main_id_encoded": "11",
      "node_classifier": "/application/deployables/dep:test_login_service/vars",
      "status": "valid",
      "children": [
        {
          "_decryptPassword": true,
          "sys_id": "49dd2e66c3a27010cc0a259d7640ddf9",
          "type": "sg_cdm_node_variable", 
          "main_id": "741",
          "name": "service_password",
          "node_path": "!1+!1/!10!11!1:",
          "value": "service12345",
          "effective_path": "!1+!1/!10!11!1:",
          "main_id_encoded": "1:",
          "node_classifier": "/application/deployables/dep:test_login_service/vars",
          "status": "valid",
          "children": [],
          "hasParent": true 
        }
      ], 
      "hasParent": true 
    }, 
    {
      "_decryptPassword": true,
      "sys_id": "26bd2e66c3a27010cc0a259d7640dd74",
      "type": "sg_cdm_node_linked",
      "main_id": "740",
      "name": "login_service",
      "node_path": "!1+!1/!10!19",
      "effective_path": "!1+!1/!10!19",
      "main_id_encoded": "19",
      "node_classifier": "/application/deployables/dep:test_login_service",
      "status": "valid",
      "children": [
        {
          "_decryptPassword": true,
          "sys_id": "eeadea66c3a27010cc0a259d7640dd8c",
          "type": "sg_cdm_node_folder",
          "main_id": "738",
          "name": "vars",
          "node_path": "!1+!1.!16!17",
          "effective_path": "!1+!1/!10!19!17",
          "main_id_encoded": "17",
          "node_classifier": "/application/collections/vars",
          "status": "valid",
          "children": [],
          "hasParent": true 
        },
        { 
          "_decryptPassword": true,
          "sys_id": "da1f22e6c3a27010cc0a259d7640dda2",
          "type": "sg_cdm_node_component",
          "main_id": "742",
          "name": "core_component",
          "node_path": "!1+!1/!10!19!1;",
          "effective_path": "!1+!1/!10!19!1;",
          "main_id_encoded": "1;",
          "node_classifier": "/application/deployables/dep:test_login_service",
          "status": "valid",
          "children": [
            { 
              "_decryptPassword": true,
              "sys_id": "921f22e6c3a27010cc0a259d7640dda3",
              "type": "sg_cdm_node_cdi",
              "main_id": "743",
              "name": "user_name",
              "node_path": "!1+!1/!10!19!1;!1<",
              "value": "admin",
              "effective_path": "!1+!1/!10!19!1;!1<",
              "main_id_encoded": "1<",
              "node_classifier": "/application/deployables/dep:test_login_service",
              "status": "valid",
              "children": [],
              "hasParent": true
            },
            { 
              "_decryptPassword": true,
              "sys_id": "5a1f22e6c3a27010cc0a259d7640dda3",
              "type": "sg_cdm_node_cdi",
              "main_id": "744",
              "name": "user_password",
              "node_path": "!1+!1/!10!19!1;!1?",
              "value": "service12345",
              "effective_path": "!1+!1/!10!19!1;!1?",
              "main_id_encoded": "1?",
              "node_classifier": "/application/deployables/dep:test_login_service",
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

The following code examples shows how to turn off substitution of variable references in CDI nodes.

```
var primarySnapshot = new sn_cdm.CdmQuery()
.snapshotId("20c365a2476c6110fd6ce977746d4336")
.substituteVariable(false)
.query()
.getTree(true, true);

gs.info(primarySnapshot);
```

Example return results:

```
{
  "paymentService-V1.1": {
    "featureToggles": {
      "paymentRefund": "enabled",
      "myPreferredPaymentMethods": "enabled",
      "invoicePrinting": "enabled",
      "payOnDelivery": "disabled",
      "payByVoucher": "enabled"
    },
    "vars": {
      "paymentService": {
        "database": {
          "dbName": "paymentX_dev2",
          "dbUserName": "root",
          "dbPassword": "admin123",
          "dbServer": "db22.paymentx.be",
          "dbPort": "8050",
          "dbIpAddress": "10.20.40.50",
          "backup": {
            "dbServer": "db23.paymentx.be"
          }
        }
      },
      "applicationSLA": "24x7"
    },
    "settings": {
      "merchantId": "10334",
      "paymentMethods": "1,3,5,6",
      "allowed.billing.countries": "74,76,88,136,139,176,197",
      "creditcards.cacf.type.ids": "43,44,45,46,48,49,50",
      "creditcards.oney.type.ids": "33,34,35",
      "included.availabilityids": "999",
      "included.warrantiestypeids.cacf": "19002,19005,19006,19009,19010,19011,19014,19016",
      "dbIPAddress": "@@paymentService/database/dbIpAddress@@",
      "dbPort": "@@paymentService/database/dbPort@@",
      "dbConnectionString": "@@paymentService/database/dbUserName@@:@@paymentService/database/dbPassword@@ @@paymentService/database/dbServer@@:@@paymentService/database/dbPort@@ @@paymentService/database/dbName@@",
      "dbConnectionStringBackup": "@@paymentService/database/dbUserName@@:@@paymentService/database/dbPassword@@ @@paymentService/database/backup/dbServer@@ @@paymentService/database/dbName@@",
      "paypal": "enabled",
      "applePay": "disabled",
      "ogone": "enabled"
    }
  }
}
```

The following code examples shows how to turn on substitution of variable references in CDI nodes and the associated return results for the same record.

```
var primarySnapshot = new sn_cdm.CdmQuery()
.snapshotId("20c365a2476c6110fd6ce977746d4336")
.substituteVariable(true)
.query()
.getTree(false, true);

gs.info(primarySnapshot);
```

Example return results:

```
{
  "paymentService-V1.1": {
    "featureToggles": {
      "paymentRefund": "enabled",
      "myPreferredPaymentMethods": "enabled",
      "invoicePrinting": "enabled",
      "payOnDelivery": "disabled",
      "payByVoucher": "enabled"
    },
    "vars": {
      "paymentService": {
        "database": {
          "dbName": "paymentX_dev2",
          "dbUserName": "root",
          "dbPassword": "admin123",
          "dbServer": "db22.paymentx.be",
          "dbPort": "8050",
          "dbIpAddress": "10.20.40.50",
          "backup": {
            "dbServer": "db23.paymentx.be"
          }
        }
      },
      "applicationSLA": "24x7"
    },
    "settings": {
      "merchantId": "10334",
      "paymentMethods": "1,3,5,6",
      "allowed.billing.countries": "74,76,88,136,139,176,197",
      "creditcards.cacf.type.ids": "43,44,45,46,48,49,50",
      "creditcards.oney.type.ids": "33,34,35",
      "included.availabilityids": "999",
      "included.warrantiestypeids.cacf": "19002,19005,19006,19009,19010,19011,19014,19016",
      "dbIPAddress": "10.20.40.50",
      "dbPort": "8050",
      "dbConnectionString": "root:admin123 db22.paymentx.be:8050 paymentX_dev2",
      "dbConnectionStringBackup": "root:admin123 db23.paymentx.be paymentX_dev2",
      "paypal": "enabled",
      "applePay": "disabled",
      "ogone": "enabled"
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

The following code examples shows how to turn off using the cache to obtain data.

```
var cdmQuery = new sn_cdm.CdmQuery()
  .snapshotId("1a2fe2e6c3a27010cc0a259d7640dd59")
  .decryptPassword(true)
  .useCache(false)
  .query();
```

