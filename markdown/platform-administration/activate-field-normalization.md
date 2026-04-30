---
title: Activate Field Normalization
description: Activate the Field Normalization \[com.snc.field\_normalization\] plugin to install demo data and activate related plugins if they are not already active.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Field normalization and transformation, Field administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Activate Field Normalization

Activate the Field Normalization \[com.snc.field\_normalization\] plugin to install demo data and activate related plugins if they are not already active.

## Before you begin

Role required: admin.

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the plugin using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/xanadu-platform-administration/page/administer/plugins/task/find-components.html).


-   **[Installed with field normalization](../reference/r_InstalledWithFieldNormalization.md#)**  
Several components are installed with Field Normalization.

**Parent Topic:**[Field normalization and transformation](../concept/c_FieldNormalization.md)

**Related topics**  


[List of plugins \(Xanadu\)](../../plugins/reference/list-of-plugins.md#)

