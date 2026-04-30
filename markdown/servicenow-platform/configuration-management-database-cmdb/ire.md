---
title: Identification and Reconciliation engine \(IRE\)
description: IRE is an underlying key component in Identification and Reconciliation, providing a centralized framework to perform identification and reconciliation processes across different data sources. IRE uses identification rules, reconciliation rules, and IRE data source rules when processing incoming data before inserting that data to the CMDB.
locale: en-US
release: zurich
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 12
breadcrumb: [Components and process, Explore, CMDB Identification and Reconciliation \(IRE\), Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Identification and Reconciliation engine \(IRE\)

IRE is an underlying key component in Identification and Reconciliation, providing a centralized framework to perform identification and reconciliation processes across different data sources. IRE uses identification rules, reconciliation rules, and IRE data source rules when processing incoming data before inserting that data to the CMDB.

IRE processes help maintain data integrity in the CMDB.

-   IRE prevents duplicate CIs by uniquely identifying CIs.​
-   IRE reconciles CI attributes by allowing only authoritative data sources to write to CMDB.

ServiceNow® applications such as Service Mapping, horizontal discovery, and pattern discovery, use APIs to apply identification and reconciliation processes. You can also apply IRE processes to data imported by import sets. When using other data sources including third-party data sources, you can leverage REST or scriptable IRE APIs to perform identification and reconciliation.​

Additional information:

-   About properties that affect some functions of IRE: See [Properties](../reference/properties-id-reconciliation.md).
-   About using IRE APIs: See [IdentificationEngine - Scoped](https://www.servicenow.com/docs/access?context=IdentificationEngineScopedAPI&version=zurich&pubname=zurich-api-reference&ft:locale=en-US).
-   About enabling debugging and checking on issues with a payload: See [How to log the payload sent to IRE and check the issues with the payload \[KB0750382\]](https://support.servicenow.com/kb_view_customer.do?sysparm_article=KB0750382).
-   About the steps that IRE performs illustrating how IRE works, such as validating the payload, applying reconciliation, and committing the data to the CMDB: See [\[CMDB - IRE\] How the CMDB Identification and Reconciliation Engine works when passing a CI \(as payload\) to the createOrUpdateCI\(\) \[KB0750386\]](https://support.servicenow.com/kb_view_customer.do?sysparm_article=KB0750386).
-   About how to run a payload through IRE: See [\[CMDB IRE\] How to run the CI identification on demand using the payload \[KB0750383\]](https://support.servicenow.com/kb_view_customer.do?sysparm_article=KB0750383).

## CI identification

The CMDB identification process relies on identification rules to uniquely identify CIs. When possible, CIs can also be uniquely identified using **source\_name** and **source\_native\_key** values provided in the **sys\_object\_source\_info** section of the payload, and the Source \[sys\_object\_source\] table. If identification is successful using that method, then it is not necessary to apply matching algorithms that rely on identification rules, which is a slower identification method.

You can configure the system to prioritize the use of IRE identification rules, even when **source\_name** and **source\_native\_key** are provided and can be used for unique identification. For more information about using the **glide.identification\_engine.skip\_sys\_object\_source\_matching** system property to manage this behavior, see [Properties](../reference/properties-id-reconciliation.md).

A unique CI identifier can be provided in the optional **sys\_object\_source\_info** object in the IRE payload.

```
{
  "items": [
    {
      "className": "cmdb_ci_win_server",
      "values": {
        "name": "SAMLABVM52"
      },
      "sys_object_source_info": {
            "source_native_key": "16777219",
            "source_name": "SCCM",
            "source_feed": "SCCM Computer Identity",
            "source_recency_timestamp": "2019-08-26 13:00:00"
      }
     }
    ]
  }
```

Identification processes rely on [CIs dependency classification](c_CMDBClassifications.md) to uniquely identify CIs. For example, to identify a Tomcat CI which is a dependent CI. Assuming a Windows Server CI \(independent class\) which is running a Tomcat application \(dependent class\). Relying on 'config file path' to uniquely identify the Tomcat CI, isn't sufficient because the Tomcat application can run on multiple machines with identical paths. The identification engine won't be able to choose a CI to update. Dependent relationships force the identification process to first identify the Windows Server host on which the Tomcat application is running, and only then, in the context of the host, to uniquely identify the Tomcat application itself.

## Payload items identification

IRE generates identifier keys for all payload items in an incoming payload and then uses those keys when trying to match partial and incoming payloads. An identifier key is based either on:

-   Combination of the **source\_name** and **source\_native\_key** values from the **sys\_object\_source\_info** object.
-   Identification criterion attributes.

IRE stores the identifier keys associated with partial items in the CMDB IRE Partial Payloads Index \[cmdb\_ire\_partial\_payloads\_index\] table, and then uses those keys to try to match with identifier keys of incoming payloads.

## Timestamps in key attributes

To help resolve conflicting attribute values, IRE uses timestamps in the following attributes to identify records that are older than the current record and therefore can be ignored:

-   Most recent discovery \(**last\_discovered**\) and Discovery source \(**discovery\_source**\):

    Most recent discovery \(**last\_discovered**\) is the timestamp of when the CI was last discovered. IRE always updates CIs’ **last\_discovered** and **discovery\_source** attributes during payload processing, even when no other CI attributes are updated. When **last\_discovered** is provided in the payload, IRE updates the CI with the provided value only if the **last\_discovered** time in the payload is newer than the one in the CMDB. If **last\_discovered** is not provided in the payload, IRE updates the **last\_discovered** attribute with the current timestamp.

    You can use the [glide.identification\_engine.skip\_updating\_source\_last\_discovered\_if\_older](../reference/properties-id-reconciliation.md) and the [glide.identification\_engine.ire\_message\_listener\_skip\_updating\_source\_last\_discovered\_to\_now](../reference/properties-id-reconciliation.md) system properties to modify this default behaviour.

-   First discovered \(**first\_discovered**\) is the timestamp of when the CI was first created.

    -   When the CI is first created: If a value is provided in the payload, IRE inserts that value. Otherwise, IRE inserts the current timestamp.
    -   In subsequent updates: If a value is provided, IRE updates the CI with the provided value. Otherwise, the attribute is not updated.

You can also use the following system properties to modify how IRE uses the **source\_recency\_timestamp** value in a payload to update the **last\_scan** attribute in the Source \[sys\_object\_source\] table:

-   [glide.identification\_engine.skip\_updating\_last\_scan\_if\_older](../reference/properties-id-reconciliation.md)
-   [glide.identification\_engine.ire\_message\_listener\_skip\_updating\_last\_scan\_to\_now](../reference/properties-id-reconciliation.md)

## Enhanced IRE features

The [CreateOrUpdateCIEnhanced\(\)](https://www.servicenow.com/docs/access?context=IdentificationEngineScopedAPI&version=zurich&pubname=zurich-api-reference&ft:locale=en-US)​​ and [identifyCIEnhanced](https://www.servicenow.com/docs/access?context=c_IdentEngineScriptAPI&version=zurich&pubname=zurich-api-reference&ft:locale=en-US) scriptable APIs provides the functionality for the following enhanced IRE features, which can be enabled or disabled as needed:

-   **Partial payloads**

    IRE isolates items for which data sources did not provide enough information to uniquely identify the CI and therefore processing cannot continue. Some of these items are identified as partial items, which get stored for potential later processing. Other items are identified as incomplete items, which get stored for logging purposes only.

    For example: SCCM has multiple feeds such as a disk feed and a computer feed. The disk feed might have complete information about the disk but insufficient information about the computer CI that it depends on.

    API option: **partial\_payloads** which is enabled by default. When **partial\_payloads** is enabled, **partial\_commits** and **deduplicate\_payloads** are automatically enabled regardless of their setting in options.

-   **Partial commits**

    Errors in some items do not prevent committing the rest of the items in a payload. Therefore, when a payload contains items with errors, IRE still commits the remaining valid items in the payload. In this situation, some of the uncommitted items are saved as partial payloads and other uncommitted items are saved as incomplete payloads.

    API option: **partial\_commits** which is enabled by default.

-   **Deduplicate payload items**

    IRE deduplicates duplicate items within the payload, merging those duplicates into a single payload item for processing.

    API option: **deduplicate\_payloads** which is enabled by default.

-   **Generate summary**

    IRE generates summaries in the output payload with processing details such as the number of updates per class.

    API option: **generate\_summary** which is disabled by default.


## Partial items

A payload item is determined to be a partial item if it doesn't contain the necessary data for unique identification and if it has one of the following errors. Unique identification requires that the payload item has the **sys\_object\_source\_info** section with **source\_name** and **source\_native\_key** values, or the full set of the identification criterion attributes specified for the CI class, or both.

IRE errors for a partial item:

-   MISSING\_MATCHING\_ATTRIBUTES –— Item does not have identification criterion attributes to use at least one identifier entry for matching.​
-   REQUIRED\_ATTRIBUTE\_EMPTY –— Unable to create a CI because a required attribute is missing​.
-   MISSING\_DEPENDENCY –— Dependent CI is missing a dependency relation which is specified in the payload​.
-   INSERT\_NOT\_ALLOWED\_FOR\_SOURCE –— An IRE data source rule prevents the specified data sources from creating CIs of the specified class.

For more details about IRE error messages, see [IRE error messages](../reference/id-engine-error-messages.md).

If processing fails because payload items are determined to be partial items, then the partial items are saved as partial payloads in the CMDB IRE Partial Payloads \[cmdb\_ire\_partial\_payloads\] table in JSON format for later potential processing.​ IRE uses identifier keys to attempt to match incoming payloads with stored partial payloads.

If later, a data source sends the data that was missing in the partial item, IRE matches the incoming payload with the stored partial payloads. IRE then merges any matching partial payloads with the incoming payload. To resolve any conflicting attributes, IRE uses either **source\_recency\_timestamp** \(when **source\_native\_key** and **source\_name** are identical\), or static reconciliation rules specified for the class. The result is a complete and valid payload which IRE then processes to create or update the respective CIs.

Partial payloads older than 90 days are deleted from the CMDB IRE Partial Payloads \[cmdb\_ire\_partial\_payloads\] table.

Sample of a partial payload:

```
Disk feed:
{
  "items": [
    {
      "className": "cmdb_ci_computer",
      "sys_object_source_info": {
            "source_native_key": "Server001",
            "source_name": "SCCM",
            "source_feed": "DISK_FEED",
            "source_recency_timestamp": "2019-08-26 13:00:00"
      }
    },
    {
      "className": "cmdb_ci_disk",
      "values": {
        "name": "disk1"
      }
    }
  ],
  "relations": [{
              "parent": 0,
              "child": 1,
              "type": "Contains::Contained by"}
              ]
}
```

The computer item in the above payload does not have any attributes and therefore IRE can't process it. However, **source\_name** and `source_native_key` are provided making it a partial item. Because the computer item is partial, the disk item that depends on the computer item, is a partial item too.

Sample of a subsequent payload that completes the previous partial payload by providing the missing details:

```
Server/Computer feed:
 {
  "items": [
    {
      "className": "cmdb_ci_linux_server",
      "values": { "name": 'linux001',
                "ip_address": "100.126.38.19",
                "mac_address": "DSWER4587" },
      "sys_object_source_info": {
            "source_native_key": "Server001",
            "source_name": "SCCM",
            "source_feed": "COMPUTER_IDENTITY",
            "source_recency_timestamp": "2019-08-26 14:00:00"
      }
    }
  ]
}
```

The computer in the partial payload and the server in the new payload match because they have identical **source\_name** and **source\_native\_key**. Therefore, the partial payload and the new payload are merged, the operation is committed, and the partial payload is deleted from the Partial Payloads table.

There is a limit on the number of items per partial payload, which is set by the [glide.identification\_engine.partial\_payload\_items\_max\_size](../reference/properties-id-reconciliation.md) property \(1000 by default\). Storing associated relationships, references, and dependent items, in one partial payload, can result in reaching that limit, in which case, the payload is split into multiple partial payloads.

For more information about partial payloads, see [CreateOrUpdateCIEnhanced\(\)](https://www.servicenow.com/docs/access?context=IdentificationEngineScopedAPI&version=zurich&pubname=zurich-api-reference&ft:locale=en-US)​​.

## Incomplete items

A payload item is determined to be an incomplete item if:

-   It does not contain all the data necessary for unique identification
-   It has an error that is not associated with a partial item

Unique identification is not possible if neither **source\_name** and **source\_native\_key** within the **sys\_object\_source\_info** object, nor the full set of identification criterion attributes specified for the CI class, is provided.

Incomplete items are saved as incomplete payloads in the CMDB IRE Incomplete Payloads \[cmdb\_ire\_incomplete\_payloads\] table in JSON format. Incomplete items are stored for the purpose of logging payloads with irrecoverable errors, and are never processed again.

## Adding relationships

Add relationships by using either indices, or the optional JSON internal\_id element.

Use the **relations** object in the payload to add or update relationships by referring to **internal\_ids** of items. Relationships can be created using main items and related items in the payload. For example:

-   Relation \(parent Index, child Index, Relation Type\)
-   Relation \(parent Internal Id, child Internal Id, Relation Type\)​

For more information and for code samples, see [CreateOrUpdateCIEnhanced\(\)](https://www.servicenow.com/docs/access?context=IdentificationEngineScopedAPI&version=zurich&pubname=zurich-api-reference&ft:locale=en-US)​​.

## Adding references between payload items

Add references between two payload items by using the optional JSON **internal\_id** element, which uniquely identifies payload items.

Use the **referenceItems** block to add or update references. You can add references between any two items, including main items, lookup items, and related items, in a single payload.

For more information and for code samples, see [CreateOrUpdateCIEnhanced\(\)](https://www.servicenow.com/docs/access?context=IdentificationEngineScopedAPI&version=zurich&pubname=zurich-api-reference&ft:locale=en-US)​​.

## CI reclassification

Use the **updateWithoutUpgrade**, **updateWithoutDowngrade**, and **updateWithoutSwitch** flags in the settings block in a payload, to prevent unintentional updates to CIs' class. These flags prevent upgrading, downgrading, or switching the class of a CI that multiple data sources unintentionally might attempt while updating the same CI. For more information and for code samples, see [CreateOrUpdateCIEnhanced\(\)](https://www.servicenow.com/docs/access?context=IdentificationEngineScopedAPI&version=zurich&pubname=zurich-api-reference&ft:locale=en-US)​​.

Reclassification flags have precedence over any other system settings for [Configure CI reclassification during IRE processing](c_CIReclassification.md#).

## Adding custom before and after scripts

Use the [IntegrationHub ETL](integrationhub-etl.md) to [add custom Java scripts for a data source of a CMDB integration application](../task/add-scripts-integration-datasource.md). Those scripts provide access to the IRE input and output payloads, while processing CMDB integrations.

Before scripts provide access to a batch of input payloads that will be sent to IRE. Using a custom before script lets you:

-   Skip a payload in the batch by setting the **status** to `SKIPPED`. Optionally, provide a reason for skipping the payload which will appear as a comment on the respective import set row table.
-   Modify the input payload.
-   Write other custom logic inside the script that uses the IRE payload.

After scripts provide access to the IRE input and output payloads. Using a custom after script lets you:

-   Easily compare the input and output payloads and identify the different operations that IRE performed on each CI.
-   Access the sys\_ids of the CIs that IRE created or updated.
-   Write other custom logic inside the script that uses the IRE output payload.

