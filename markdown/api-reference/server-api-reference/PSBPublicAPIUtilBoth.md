---
title: sb - Scoped, Global
description: The sb script include provides methods that enable you to perform operations on Service Exchange configuration records.Validates that the specified GlideRecord is a valid Service Exchange configuration record and verifies that the record is in the "inactive" state. If this validation passes, archives the specified configuration record, leaving all other versions of the same configuration record untouched.Validates that the specified GlideRecord is a valid Service Exchange configuration record and verifies that the record is in the "published" state. If this validation passes, creates a new version of the specified configuration record and sets the state field to "draft".Validates that the specified GlideRecord is a valid Service Exchange configuration record and verifies that the record is in the "draft" state. If this validation passes, publishes the draft version of the configuration record.Validates that the specified GlideRecord is a valid Service Exchange configuration record and verifies that the record is in a valid state. If this validation passes, retires the specified version of the configuration record along with all other revisions of that same configuration record. Populates virtual fields in a task table on a target instance when using Service Exchange remote tasks.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 8
keywords: [Service Bridge, ServiceBridge, PSBPublicAPIUtil, Service Bridge API]
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# sb - Scoped, Global

The sb script include provides methods that enable you to perform operations on Service Exchange configuration records.

There are three types of Service Exchange configuration records that you can perform operations on using this script include:

-   Foundation Data Sync \(FDS\)
-   Remote Record Producers \(RRP\)
-   Remote Task Definition \(RTD\)

You can perform any of the following Service Exchange operations on these configuration records:

-   Checkout: Creates a draft version of a specified configuration record. Any published version is still available for customer use.
-   Publish: Publishes the draft version of a specified configuration record and makes it available for customer use.
-   Archive: Archives an inactive version of a specified configuration record and makes it unavailable to customers.
-   Retire: Retires all versions of a specified configuration record and makes them unavailable to customers.
-   Update virtual field: Populates virtual fields in a task table on a target instance when using Service Exchange remote tasks.

For additional information on Service Exchange configuration records, see Create configuration revisions.

To access this API, the Service Exchange for Providers application \(sn\_sb\_pro\) and the Service Exchange Base \(sn\_sb\) plugins must be installed on your instance.

You call the methods in this API using the sb script include. The code for these methods, however, resides in the PSBPublicAPIUtil script include.

When calling these methods from global scope, use the following syntax:

```
sb.checkout(glideRecord);
sb.publish(glideRecord);
sb.archive(glideRecord);
sb.retire(glideRecord);
```

When calling them from a scoped application, use this syntax:

```
global.sb.checkout(glideRecord);
global.sb.publish(glideRecord);
global.sb.archive(glideRecord);
global.sb.retire(glideRecord);
```

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## sb - archive\(glideRecord\)

Validates that the specified GlideRecord is a valid Service Exchange configuration record and verifies that the record is in the "inactive" state. If this validation passes, archives the specified configuration record, leaving all other versions of the same configuration record untouched.

For additional information on configuration revisions and their associated states, see Create configuration revisions.

<table id="table_wlx_2cn_zbc" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

glideRecord

</td><td>

GlideRecord

</td><td>

Configuration record to archive.This record can be one of the following:

-   Foundation Data Sync \(FDS\): Records located in the Foundation Data Provider Offering \[sn\_fds\_pro\_offering\] table.
-   Remote Record Producers \(RRP\): Records located in the Remote record producer \[sn\_sb\_pro\_remote\_record\_producer\] table.
-   Remote Task Definition \(RTD\): Records located in the Remote task definition \[sn\_sb\_pro\_remote\_task\_def\] table.

</td></tr></tbody>
</table><table id="table_xlx_2cn_zbc" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the configuration record was archived.Possible values:

-   true: Configuration record was archived.
-   false: Error occurred; configuration record wasn't archived.

</td></tr></tbody>
</table>The following code example shows how to call this method from global scope on an FDS configuration record.

```
var grConfig = new GlideRecord('sn_fds_pro_offering’’'); // Configuration table that contains the desired record 
grConfig.get('0ed11101ff6aca10c1befe258c4fd99e'); // Sys_id of the configuration record to publish
var isExecuted = sb.archive(grConfig);
```

## sb - checkout\(glideRecord\)

Validates that the specified GlideRecord is a valid Service Exchange configuration record and verifies that the record is in the "published" state. If this validation passes, creates a new version of the specified configuration record and sets the state field to "draft".

<table id="table_x5b_yxm_zbc" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

glideRecord

</td><td>

GlideRecord

</td><td>

Configuration record to checkout.This record can be one of the following:

-   Foundation Data Sync \(FDS\): Records located in the Foundation Data Provider Offering \[sn\_fds\_pro\_offering\] table.
-   Remote Record Producers \(RRP\): Records located in the Remote record producer \[sn\_sb\_pro\_remote\_record\_producer\] table.
-   Remote Task Definition \(RTD\): Records located in the Remote task definition \[sn\_sb\_pro\_remote\_task\_def\] table.

</td></tr></tbody>
</table><table id="table_y5b_yxm_zbc" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

GlideRecord

</td><td>

If successful, returns the newly created configuration record with the state field set to "draft".If an error occurred, returns null.

</td></tr></tbody>
</table>The following code example shows how to call this method from the global scope on an RTD configuration record.

```
var grConfig = new GlideRecord('sn_sb_pro_remote_task_def'); // Configuration table that contains the desired record 
grConfig.get('0ed11101ff6aca10c1befe258c4fd99e'); // Sys_id of the configuration record to checkout
var checkoutGr = sb.checkout(grConfig);
```

## sb - publish\(glideRecord\)

Validates that the specified GlideRecord is a valid Service Exchange configuration record and verifies that the record is in the "draft" state. If this validation passes, publishes the draft version of the configuration record.

<table id="table_mqz_mbn_zbc" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

glideRecord

</td><td>

GlideRecord

</td><td>

Configuration record to publish.This record can be one of the following:

-   Foundation Data Sync \(FDS\): Records located in the Foundation Data Provider Offering \[sn\_fds\_pro\_offering\] table.
-   Remote Record Producers \(RRP\): Records located in the Remote record producer \[sn\_sb\_pro\_remote\_record\_producer\] table.
-   Remote Task Definition \(RTD\): Records located in the Remote task definition \[sn\_sb\_pro\_remote\_task\_def\] table.

</td></tr></tbody>
</table><table id="table_nqz_mbn_zbc" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the configuration record was published.Possible values:

-   true: Configuration record was published.
-   false: Error occurred; configuration record wasn't published.

</td></tr></tbody>
</table>The following code example shows how to call this method from global scope on an RRP configuration record.

```
var grConfig = new GlideRecord('sn_sb_pro_remote_record_producer’'); // Configuration table that contains the desired record 
grConfig.get('0ed11101ff6aca10c1befe258c4fd99e'); // Sys_id of the configuration record to publish
var isExecuted = sb.publish(grConfig);
```

## sb - retire\(glideRecord\)

Validates that the specified GlideRecord is a valid Service Exchange configuration record and verifies that the record is in a valid state. If this validation passes, retires the specified version of the configuration record along with all other revisions of that same configuration record.

For additional information on configuration revisions and their associated states, see Create configuration revisions.

<table id="table_kqj_hcn_zbc" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

glideRecord

</td><td>

GlideRecord

</td><td>

Configuration record to retire.This record can be one of the following:

-   Foundation Data Sync \(FDS\): Records located in the Foundation Data Provider Offering \[sn\_fds\_pro\_offering\] table.
-   Remote Record Producers \(RRP\): Records located in the Remote record producer \[sn\_sb\_pro\_remote\_record\_producer\] table.
-   Remote Task Definition \(RTD\): Records located in the Remote task definition \[sn\_sb\_pro\_remote\_task\_def\] table.

</td></tr></tbody>
</table><table id="table_lqj_hcn_zbc" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the configuration record was retired.Possible values:

-   true: Configuration record was retired.
-   false: Error occurred; configuration record wasn't retired.

</td></tr></tbody>
</table>The following code example shows how to call this method from global scope on an RTD configuration record.

```
var grConfig = new GlideRecord('sn_sb_pro_remote_task_def'); // Configuration table that contains the desired record 
grConfig.get('0ed11101ff6aca10c1befe258c4fd99e'); // Sys_id of the configuration record to checkout
var isExecuted = sb.retire(grConfig);
```

## sb - updateVirtualField\(GlideRecord remoteTaskGr, String virtualField, String virtualValue, String virtualDisplayValue\)

Populates virtual fields in a task table on a target instance when using Service Exchange remote tasks.

A virtual field is a field that exists in a target task table but doesn’t exist in the source task table. You use this method to pass the values for a virtual field from the source instance to the target instance. This method stores the specified values for the virtual field as JSON in the form section of the specified remote task. This remote task is then synced to the target instance where the values are stored in the mapped field in the target task table.

Virtual fields are defined in remote task definitions. Remote task definitions contain inbound and outbound mapping tables that map fields between task tables in source and target instances. When a source table doesn’t contain a field that exists on a target table, the field is configured in the remote task definition as a virtual field. The consumer can then use either Service Exchange transforms or this method to update the values of these virtual fields in the associated target task record.

The following section describes an example use case on how to implement virtual fields and then use the updateVirtualField\(\) method to populate values in the virtual field. In this example, the two task tables that are bound together by a remote task definition are the provider Case table and the consumer Incident table. When an incident record is created or updated on the consumer instance, it’s configured to sync with the provider Case table. The Affected Instances field in the Case table is a required field but doesn’t exist in the Incident table. To handle this situation, the Affected Instances field must be defined as a virtual field in the inbound mapping of the associated remote task definition.

1.  The provider creates a remote task definition for the provider Case table and the consumer Incident table.
2.  On the **Inbound fields** tab in the **Related links** of the remote task definition, the provider maps the fields between the Incident table and the Case table.

    When defining the Affected Instances field, the provider selects the **Virtual** check box and then selects **Affected Instances** from the **Target field** on the **Target mapping** tab.

    **Note:** When defining a virtual field, no source field is defined as it doesn’t exist.

3.  The provider then publishes the remote task definition, which is synced to the consumer instance.
4.  The consumer creates a remote task for the Incident table. A JSON payload that holds all values for the mapped fields, including the information on virtual fields, is included on a form section in the remote task.
5.  The consumer instance calls the updateVirtualField\(\) method, such as in a business rule that runs when records in the Incident table are updated, to set the values of the Affected Instances field in the remote task.

    **Note:** Even though you can populate data in the target table at any time, required fields configured as virtual fields must be populated in the remote task before the remote task is sent to the producer instance.

6.  The remote task is synced to the provider instance and creates a Case record on the provider instance.

For information on how to create a remote task definition, see Create a remote task definition in Service Exchange for Providers.

For information on how to create a Service Exchange transform, see Transform data with the Service Exchange transform framework.

**Warning:** You should only call this method in a before business rule as it updates the remote task that it is called on. If you call this method in an after business rule, you must include strict conditions that prevent the update of the virtual field on the remote task from triggering the business rule as this can cause an infinite loop.

|Name|Type|Description|
|----|----|-----------|
|remoteTaskGr|GlideRecord|GlideRecord object of the remote task for which to set the specified virtual field values.|
|virtualField|String|**Field name** of the virtual field for which to update the associate information. Defined on the **Outbound fields** related tab of the associated remote task definition.|
|virtualValue|String|Value to set for this field on the target instance.|
|virtualDisplayValue|String|Display value to set for this field on the target instance|

|Type|Description|
|----|-----------|
|None| |

The following example shows how to call this method.

```
var remoteTaskGr = new GlideRecord("");
/** Remote Task table name,
** Table name vary based on which instance the script is being executed.
**/

remoteTaskGr.get(""); // Remote Task record sys_id

global.sb.updateVirtualField(remoteTaskGr,"<virtual outbound field name>", "<value to set on target field>", "<display value to set on target field>");

```

