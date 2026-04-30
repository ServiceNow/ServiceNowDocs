---
title: Tags for cloud resources
description: Tags categorize cloud resources to provide richer and more detailed tracking and billing report data.Cloud Administrators can create custom tags in addition to the default tags to categorize cloud resources.Configure user-defined tags to view and analyze billing data using custom tags existing on provisioned resources.
locale: en-US
release: zurich
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Cloud Admin Portal, Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Cloud Accelerate, IT Operations Management]
---

# Tags for cloud resources

Tags categorize cloud resources to provide richer and more detailed tracking and billing report data.

Create tags to enable Cloud Provisioning and Governance to automatically categorize cloud resources after they are provisioned. Each tag associates a specific `key:value` pair with a requested cloud resource, such as `Application=HRMS`.

After the cloud resource is provisioned, the key:value information in tags become part of the resource's metadata and are saved along with all other parameters about the resource. Because a cloud resource can have multiple tags, you can view cost items from multiple perspectives.

## Tag definitions

Tag definitions are records that associate a tag name with a value type. These value types are available:

<table id="table_db3_vzx_vy"><thead><tr><th>

Value type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Variable

</td><td>

A value that user enters or selects from a choice list. This value is stored as a service catalog variable. If a table is associated with a variable tag, the values in the field marked as the **Display** field are displayed to the user when they request the instance. In most cases, this is the Name field. For example, the names of the business services in the Service table display to the user. If no table is specified in the tag definition, the user is presented with a text field.

</td></tr><tr><td>

Script

</td><td>

A script that obtains a value from the instance, such as the current time on the instance. The script must obtain the value via the base-system API and return the value to the `answer` variable. For example, to obtain the current time on the instance, the script would be:```
answer = new GlideDateTime().getValue();
```

</td></tr></tbody>
</table>## Default tags

These tags are provided by default.

**Important:** Do not deactivate the default tags, as this action will delete all the corresponding catalog item variables.

|Label|Name|Value type|Table that provides choices|
|-----|----|----------|---------------------------|
|Application|application|variable|Application \[cmdb\_ci\_appl\]|
|Business Service|business\_service|variable|Service \[cmdb\_ci\_service\]|
|Cost Center|cost\_center|variable|Cost Center \[cmn\_cost\_center\]|
|Project|project|variable|n/a|
|ServiceNow instance|sn\_instance|script|n/a|
|Stack|stack|variable|Stack \[sn\_cmp\_stack\]|
|Time Provisioned|time\_provisioned|script|n/a|
|User|user|order field|User \[sys\_user\]|
|User Group|user\_group|variable|Group \[sys\_user\_group\]|

Cloud administrators can also create custom tags to suit the specific needs of the organization. For example, you can create a Location tag can to track the location of the resource.

## AWS tags

Tags generated for Amazon Web Services \(AWS\) resources are sent to AWS and are also available from your AWS console.

**Related topics**  


[View tagged resources on the Tag dashboard](cloud-dashboards.md#)

## Create a custom tag for cloud resources

Cloud Administrators can create custom tags in addition to the default tags to categorize cloud resources.

### Before you begin

Role required: sn\_cmp.cloud\_admin

### About this task

If a resource was provisioned prior to the existence of a particular tag, then that tag must be manually added to the record for that resource.

### Procedure

1.  In the Cloud Admin Portal, navigate to **Analyze** &gt; **Tag** &gt; **Tag Management** &gt; **Tag Definitions**.

2.  Select **New**.

3.  On the form, fill in the fields.

<table id="table_rlb_d1w_sy"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Label

</td><td>

Name to display on screen for the cloud user.

</td></tr><tr><td>

Name

</td><td>

Name of the key. The name is stored in all tables, along with the value.

</td></tr><tr><td>

Value type

</td><td>

The [type of value](cloud-tagging.md#table_db3_vzx_vy) for this tag.

</td></tr><tr><td>

Variable name

</td><td>

The name of the variable. This option appears if you select the **Variable** value type.

</td></tr><tr><td>

Table\[optional\]

</td><td>

The table that provides the choices for the **Variable** value type field. Select a table from the system. If you do not select a table, cloud users are presented with an empty text field for the variable.

</td></tr><tr><td>

Order field

</td><td>

The field on the request form. Click the down arrow next to **Click to select**, and then select the field from the Orders \[sn\_cmp\_order\] table.

</td></tr><tr><td>

Active

</td><td>

An indicator that specifies if the tag is in use. Select this option to apply the tag to all new requests.

</td></tr></tbody>
</table>
**Related topics**  


[View tagged resources on the Tag dashboard](cloud-dashboards.md#)

## Group billing data using custom tags from provisioned resources

Configure user-defined tags to view and analyze billing data using custom tags existing on provisioned resources.

### Before you begin

-   Perform cloud discovery in Cloud Provisioning and Governance for provisioned resources.
-   Run a billing download job for the associated service account.

Role required: Resource Policy Contributor role in Azure Service account and sn\_cmp.cloud\_admin in the instance.

### About this task

Provisioned resources with existing tags are discovered as part of Cloud discovery. Existing tags are considered user-defined tags in Tag Management. By default, the imported \(user-defined\) tags are not displayed in the Billing dashboard, restricting you from filtering and analyzing billing data using imported \(user-defined\) tags.

**Important:** Starting with the Rome release, billing and budgeting features are no longer supported for Cloud Provisioning and Governance running on a non-domain-separated instance. However, if you are using Cloud Provisioning and Governance on a domain-separated instance, there is no change in functionality for the billing and budgeting features.

### Procedure

1.  In the **Cloud Admin portal**, navigate to **Analyze** &gt; **Tag** &gt; **Tag Management**.

    The **Tag Definitions** list displays discovered resources provisioned with existing tags labeled as User-defined.

2.  Open a tag record of type **User-defined**.

3.  In the Tag Definition form, change the tag from User-defined to ServiceNow \(Custom\):

    1.  In the **Tag type** field, select **ServiceNow \(Custom\)**.

    2.  Copy the **Label** field value to the **Variable** field.

    3.  Select the **Active** and **Visible** check boxes.

    4.  Select **Update**.

4.  Repeat Steps 2 and 3 for all the user-defined tags that you wish to enable in the Billing Dashboard.

5.  Perform Cloud Discovery again to view updated ServiceNow \(Custom\) tags.

    For more information, see [Cloud Discovery](../../discovery/concept/discovery-manager.md#).

6.  Run the Billing schedule.

    1.  In the **Cloud Admin Portal**, navigate to **Analyze** &gt; **Billing** &gt; **Billing Schedule**.

    2.  Create a schedule or open an existing schedule.

    3.  Select **Execute Now**.

    4.  On the **Retrieve Billing Data** dialog box that appears, select a date range and then click **Download**.

    The ServiceNow \(Custom\) tags now show up in the Tags field on the Billing Dashboard.


### What to do next

[View cloud costs on the Billing dashboard](cloud-dashboards.md#).

