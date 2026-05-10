---
title: Create a remote task definition in Service Exchange for Providers
description: As a provider, create remote task definitions \(RTD\) that trigger the assignment of a remote task.
locale: en-US
release: australia
product: Service Exchange
classification: service-exchange
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 9
breadcrumb: [Configure for providers, Service Exchange for Providers, Service Exchange]
---

# Create a remote task definition in Service Exchange for Providers

As a provider, create remote task definitions \(RTD\) that trigger the assignment of a remote task.

## Before you begin

Role required: admin

## About this task

Before you can create a remote task, you must first create an RTD. A remote task is generated based on the RTD you define. To learn more about how RTD and remote task works, see [Remote tasks](../concept/service-bridge-v2-remote-task-overview.md).

## Procedure

1.  Navigate to **All** &gt; **Service Exchange Provider** &gt; **Administration** &gt; **Remote Task Definitions**.

2.  Select **New**.

3.  On the form, fill in the fields.

<table id="table_r2f_zkw_d5b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the remote task definition record.

</td></tr><tr><td>

Application

</td><td>

This is a read-only field and is set by default based on the application scope.

</td></tr><tr><td>

State

</td><td>

Shows the status of the remote task definition. When you create a remote task definition, this field is set to the **Draft** state. **Note:** This field is automatically updated when you Publish, Archive, or Retire a remote task definition.

</td></tr><tr><td>

Provider table

</td><td>

Any task table that you select from the list. For example, you can choose a case table or an incident table.

</td></tr><tr><td>

Consumer table

</td><td>

Any task table that you select from the list. For example, you can choose a case table or an incident table.

</td></tr><tr><td>

Compatibility

</td><td>

This field is populated by default. It shows the Service Exchange version that is being used by the provider. If the consumer is using a compatible Service Exchange version, data can be synced between the provider and consumer instances. But if the consumer isn’t using a compatible version, any new remote task definitions can’t be activated until the corresponding Service Exchange version is upgraded.

</td></tr><tr><td>

Send attachments

</td><td>

If this check box is selected, if an attachment is added on the parent record, it’s sent to the remote task.**Note:** When data, such as an attachment or task, is shared with another instance through Service Exchange, it becomes part of that instance’s data. Service Exchange does not delete data on remote instances; the receiving instance must handle the deletion if required.

</td></tr><tr><td>

Short description

</td><td>

Brief information about this remote task definition.

</td></tr><tr><td>

Description

</td><td>

More detailed information about this remote task definition.

</td></tr></tbody>
</table>4.  Select **Submit**.

5.  Open this new Remote task definition record.

6.  On the **Inbound fields** related tab, select **New**.

    Starting from Service Exchange version 2.2.x, an inbound field record is created with the source and target fields set as comments. This record enables comment-to-comment mappings for your RTD.

7.  On the form, fill in the fields.

    The inbound fields enable you to receive data from the consumer's instance when a remote task is created or updated.

    **Note:** If the inbound field values are updated, the updated information is shown in a work note on the parent record.

<table id="table_lkx_vzd_25b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Field label

</td><td>

Field label that appears on the remote task form.

</td></tr><tr><td>

Field name

</td><td>

Field name that is used in the remote task flow and script.

</td></tr><tr><td>

Max length

</td><td>

Maximum length of the source field name.

</td></tr><tr><td>

Sync when

</td><td>

Enables you to specify when a target field on the remote task's parent record is directly updated. You can select:-   **Insert:** Updates the target field on the remote task's parent record only when the remote task is initially inserted.
-   **Insert or Update**: Updates the target field on the remote task's parent record every time the remote task is updated.
-   **Never**: The inbound field never updates a target field on the remote task's parent record directly. For example, you can use this field for state mapping where a flow is used to convert the incoming value before updating the target field.
**Note:** Irrespective of the option you select here, whenever an inbound field is updated, the changes are reflected in a worknote on parent record.

</td></tr><tr><td>

Source Mapping tab

</td><td>

This tab is not displayed if you have selected the **Virtual** check box to define a virtual field mapping.

</td></tr><tr><td>

Source table \(read-only\)

</td><td>

The Consumer table that you selected while creating the remote task definition.

</td></tr><tr><td>

Source field

</td><td>

Field from the source table that is sent to another ServiceNow instance.Source fields allow for [Dot-walking to data in related tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/c_DotWalking.md), which is useful when reference data is not available between ServiceNow instances. For example, you can create multiple inbound mappings for change incidents \(CIs\) to include the name, class, IP address, and asset tag.

</td></tr><tr><td>

Target Mapping tab

</td><td>

Displayed only in the following conditions:-   Sync when: You select **Insert** or **Insert or update**.
-   Virtual: You select this check box to enable virtual field mapping.


</td></tr><tr><td>

Target table \(read-only\)

</td><td>

The Provider table that you selected while creating the remote task definition.

</td></tr><tr><td>

Target field

</td><td>

Field from the target table that is sent to another ServiceNow instance.**Note:** If you are defining a virtual field mapping, the field you select in the target table is not present in the source table.

</td></tr><tr><td>

Active

</td><td>

This field is enabled by default.

</td></tr><tr><td>

Virtual

</td><td>

Select this check box to enable virtual inbound field mapping. A virtual field is a field that is present in the target table but does not exist in the source table.

 When a source table doesn’t contain a field that exists on a target table, the field is configured as a virtual field. The values specified for the virtual field are passed from the source instance to the target instance. The consumer can create a remote task to sync data and update the value of the virtual field in the associated target task record.

 The target field can be updated either by using the Virtual Inbound option described in the [Create a transform in Service Exchange](service-bridge-v2-create-transform.md) or by using the `updateVirtualField` API.

</td></tr></tbody>
</table>8.  Click **Submit**.

9.  On the **Outbound fields** related tab, click **New**.

    Starting from Service Exchange version 2.2.x, an outbound field record is created with the source and target fields set as comments. This record enables comment-to-comment mappings for your RTD.

10. On the form, fill in the fields.

    The outbound fields enable you to send data to the consumer's instance when a remote task is created or updated.

<table id="table_jfg_wzd_25b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Field label

</td><td>

Name of the field label that appears on the remote task form.

</td></tr><tr><td>

Field name

</td><td>

Field name that is used in the remote task flow and script.

</td></tr><tr><td>

Max length

</td><td>

Maximum length of the field name.

</td></tr><tr><td>

Sync when suggestion

</td><td>

Enables you \(the provider\) to suggest to the consumer when a target field on the remote task's parent record should be directly updated. The consumer can change this setting before activating the definition-   **Insert:** Updates the target field on the remote task's parent record only when the remote task is initially inserted.
-   **Insert or Update**: Updates the target field on the remote task's parent record every time the remote task is updated.
-   **Never**: The inbound field never updates a target field on the remote task's parent record directly. For example, you can use this field for state mapping where a flow is used to convert the incoming value before updating the target field.


</td></tr><tr><td>

Sync pre-existing entries

</td><td>

Option to enable synchronization of all existing comments to the target task when a connection is established. If enabled, any comments made prior to the connection gets included in the sync process when a remote task is created.**Note:** This feature is available from Service Exchange version 2.2.x.

</td></tr><tr><td>

Source Mapping tab

</td><td>

This tab is not displayed if you have selected the **Virtual** check box to define a virtual field mapping.

</td></tr><tr><td>

Source table \(read-only\)

</td><td>

The Provider table that you selected while creating the remote task definition.

</td></tr><tr><td>

Source field

</td><td>

Field from the source table that is sent to another ServiceNow instance.Source fields allow for [Dot-walking to data in related tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/c_DotWalking.md), which is useful when reference data is not available between ServiceNow instances. For example, you can create multiple inbound mappings for change incidents \(CIs\) to include the name, class, IP address, and asset tag.

 **Note:** From Service Exchange version 2.2.x, you can create

</td></tr><tr><td>

Target Mapping tab

</td><td>

Displayed only in the following conditions:-   Sync when: You select **Insert** or **Insert or update**.
-   Virtual: You select this check box to enable virtual field mapping.


</td></tr><tr><td>

Target table \(read-only\)

</td><td>

The Consumer table that you selected while creating the remote task definition.

</td></tr><tr><td>

Target field

</td><td>

Field from the target table that is sent to another ServiceNow instance.**Note:** If you are defining a virtual field mapping, the field you select in the target table is not present in the source table.

</td></tr><tr><td>

Active

</td><td>

This field is enabled by default.

</td></tr><tr><td>

Virtual

</td><td>

Select this check box to enable virtual inbound field mapping. A virtual field is a field that is present in the target table but does not exist in the source table.

 When a source table doesn’t contain a field that exists on a target table, the field is configured as a virtual field. The values specified for the virtual field are passed from the source instance to the target instance.

 The target field can be updated either by using the Virtual Outbound option described in the [Create a transform in Service Exchange](service-bridge-v2-create-transform.md) or by using the `updateVirtualField API`.

</td></tr></tbody>
</table>11. Click **Submit**.

12. On the **Consumer criteria** related tab, click **New**.

13. On the form, fill in the fields.

    Consumer criteria enable you to manage which consumers can use these remote task definitions.

    |Field|Description|
    |-----|-----------|
    |Consumer condition|Customer company or account that you want this remote task definition to be entitled to.|
    |Remote task definition|Name of this remote task definition record. This name is auto-filled.|

    For more details on consumer criteria, see [Creating entitlements in Service Exchange for Providers](../concept/service-bridge-v2-entitlements.md).

14. Click **Publish**.

    Remote task variables are automatically created when you publish a remote task definition. These variables are the data variables for the inbound fields displayed and can be accessed on the remote tasks.


## Result

A remote task definition record is created on your instance. This record is also synchronized with your customer's instance and is now pending activation on your consumer's instance. If the **Auto activate remote task definition** field has been enabled by the consumer, the remote task definition is automatically activated on your consumer's instance.

## What to do next

You can create multiple configuration revisions of this published remote task definition. For details on how to create a configuration revision, see [Create configuration revisions](../concept/service-bridge-v2-create-config-rev.md). You can also perform the following operations:

-   Archive a configuration revision: See [Archive a configuration revision](../concept/service-bridge-v2-create-config-rev.md#section_zjw_2qc_sbc)
-   Copy a configuration revision: See [Copy a configuration revision](../concept/service-bridge-v2-create-config-rev.md#section_gst_43n_tbc).
-   Retire a configuration: [Retire a configuration](../concept/service-bridge-v2-create-config-rev.md#section_x1w_dqc_sbc).
-   Delete a configuration: See [Delete a configuration](../concept/service-bridge-v2-create-config-rev.md#section_igy_2jn_tbc).

**Related topics**  


[Remote tasks](../concept/service-bridge-v2-remote-task-overview.md)

