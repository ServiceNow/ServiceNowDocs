---
title: Create remote record producers in a remote catalog in Service Exchange for Providers
description: Create remote record producers as part of creating a Remote Catalog in Service Exchange for Providers.
locale: en-US
release: yokohama
product: Service Bridge
classification: service-bridge
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Remote record producers in Service Exchange, Create remote catalogs in Service Exchange for providers, Installing and configuring Service Exchange for Providers, Service Exchange for Providers, Service Exchange]
---

# Create remote record producers in a remote catalog in Service Exchange for Providers

Create remote record producers as part of creating a Remote Catalog in Service Exchange for Providers.

## Before you begin

-   Ensure that the catalog scope is set to Global.
-   Role required: admin, sn\_sb.admin

**Note:** Users without the admin role must be granted a catalog admin role to modify and publish remote record producers.

## Procedure

1.  Navigate to **All** &gt; **Service Exchange Provider** &gt; **Administration** &gt; **Remote Catalog Items**.

2.  Click **New**.

3.  On the form, fill in the fields.

<table id="table_uzj_fds_jmb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the remote record producer.

</td></tr><tr><td>

Application

</td><td>

This is a read only field and is set by default based on the application scope.

</td></tr><tr><td>

State

</td><td>

Shows the status of the remote record producer. When you create a remote record producer, this field is set to the **Draft** state. **Note:** This field is automatically updated when you Publish, Archive, or Retire a remote record producer.

</td></tr><tr><td>

Table name

</td><td>

Table name is Provider Task. This is a read only field.

</td></tr><tr><td>

Flow

</td><td>

Choose one of the default Service Exchange flows provided or create your own flow if required.

</td></tr><tr><td>

Active

</td><td>

This is a read only field and is enabled based on the Publish, Retire, Archive, or Delete actions.

</td></tr><tr><td>

Persona

</td><td>

Catalog personas that you want to assign to this record producer.

</td></tr><tr><td>

Compatibility

</td><td>

This field is populated by default. It shows the Service Exchange version that is being used by the provider. If the consumer is using a compatible Service Exchange version, data can be synced between the provider and consumer instances. But if the consumer is not using a compatible version, any new entitlements cannot be activated until the corresponding Service Exchange version is upgraded.

</td></tr><tr><td>

Short Description

</td><td>

Short description for the record producer.

</td></tr><tr><td>

Description

</td><td>

Detailed description for the record producer.

</td></tr></tbody>
</table>4.  Click the link next to the Icon field to attach a picture.

5.  Click the link next to the Picture field to attach a picture.

    **Note:** You can also delete the picture if it is no longer required.

6.  Click **Submit**.

7.  Add at least one variable.

    See [Create variables for remote record producers in Service Exchange for Providers](service-bridge-v2-assign-variables-ser-defn.md).

8.  Add a consumer criteria.

9.  Click **Publish** to publish the remote record producer and make it available in the provider and consumer instances.


## What to do next

You can create multiple configuration revisions of this published remote record producer. For details on how to create a configuration revision, see [Create configuration revisions](../concept/service-bridge-v2-create-config-rev.md). You can also perform the following operations:

-   Archive a configuration revision: See [Archive a configuration revision](../concept/service-bridge-v2-create-config-rev.md#section_zjw_2qc_sbc)
-   Copy a configuration revision: See [Copy a configuration revision](../concept/service-bridge-v2-create-config-rev.md#section_gst_43n_tbc).
-   Retire a configuration: [Retire a configuration](../concept/service-bridge-v2-create-config-rev.md#section_x1w_dqc_sbc).
-   Delete a configuration: See [Delete a configuration](../concept/service-bridge-v2-create-config-rev.md#section_igy_2jn_tbc).

