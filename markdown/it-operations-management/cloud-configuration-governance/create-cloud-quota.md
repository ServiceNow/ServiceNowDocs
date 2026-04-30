---
title: Create a cloud quota definition
description: A cloud quota definition specifies the limitations on a resource block. You can use templates or manually create different types of configurations for each quota definition.
locale: en-US
release: zurich
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Quotas and resource order controls, Cloud Admin Portal, Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Cloud Accelerate, IT Operations Management]
---

# Create a cloud quota definition

A cloud quota definition specifies the limitations on a resource block. You can use templates or manually create different types of configurations for each quota definition.

## Before you begin

Role required: sn\_cmp.cloud\_governor

## Procedure

1.  In the Cloud Admin Portal, navigate to **Govern** &gt; **Quota**.

2.  Click **New**.

3.  On the form, fill in the fields.

<table id="table_ww1_zms_yy"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Quota Definition

</td><td>

A unique identifier for the quota definition. Typically it is the `resource name_count` or `resource name_size`. For example: Network\_Count, VM\_Count, or StorageVolume\_Size.

</td></tr><tr><td>

Quota Type

</td><td>

Type of quota restriction to set:-   Count
-   Size


</td></tr><tr><td>

Resource Name

</td><td>

The Resource Block type to apply the quota to. Select from the lookup list. For example, select Cloud Resource for any template-based cloud resource. For more information, see [Resource blocks in Cloud Provisioning and Governance](../concept/resource-blocks.md).

</td></tr><tr><td>

Calculation Unit

</td><td>

The unit this quota is calculated in:-   GB
-   Single


</td></tr><tr><td>

CI Class

</td><td>

The CMDB CI class to be selected from the lookup list.

</td></tr><tr><td>

Attribute

</td><td>

The column name from the underlying CI type on the [resource block](../concept/resource-blocks.md) that holds the value to restrict with the quota. For example, if your quota limits the CPU count on a virtual server, the table of the underlying CI type is cmdb\_ci\_vm\_instance. The **cpus** column holds that CPU data. So you would enter `cpus`.You can also enter `instance`.

</td></tr><tr><td>

Template\[optional\]

</td><td>

The table name of a resource type, for example Hardware Type \[cmdb\_ci\_compute\_template\] or Image \[cmdb\_ci\_os\_template\].

</td></tr><tr><td>

Template Attribute\[optional\]

</td><td>

A column from the table you specified in the Template field. This it the attribute on which the quota is set. For example, if you selected the \[cmdb\_ci\_compute\_template\] template and you want to put a quota on the virtual CPUs, you would enter `vcpus`. That column stores the virtual CPU count for all records in the \[cmdb\_ci\_compute\_template\] table.

</td></tr></tbody>
</table>4.  Right-click the header and select **Save**.

    The Quota Configurations, Default Quotas, and Cloud Template Resources related lists appear.

5.  In the Quota Configurations related list, click **New**.

6.  On the form, fill in the fields:

    |Field|Description|
    |-----|-----------|
    |Group Name|A unique name for the configuration group.|
    |Group Maximum Limit|The maximum limit for the group's quota.|
    |Quota Definition Type|The quota definition name.|
    |Per User Limit|The maximum quota limit for each user in the group.|

7.  Click **Submit**.

8.  You can specify optional default quotas that will be set on the resource block by clicking **New** in the Default Quotas related list, and then filling in the form.

    |Field|Description|
    |-----|-----------|
    |Group Maximum Limit|The maximum quota limit for the group.|
    |Quota Definition|The quota definition for which you are setting the default values.|
    |Per User Limit|The quota limit applicable to each user in this group.|

9.  Click **Submit**.

10. Map catalog item to which the quota you defined applies by clicking **New** in the Cloud Template Resources related list.

    **Note:** If you do not map quota to a catalog, quota is not calculated for that catalog.

11. On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Domain|The domain to which this quota applies.|
    |Quota Definition|The name of the quota definition you are applying.|
    |Catalog Item|The catalog item or cloud resource you are mapping to the quota.|

12. Click **Submit**.


## Result

You have specified the cloud quota definitions and quota limits for users and user groups.

**Parent Topic:**[Quotas and resource order controls](../concept/quotas.md)

**Related topics**  


[Resource blocks in Cloud Provisioning and Governance](../concept/resource-blocks.md)

