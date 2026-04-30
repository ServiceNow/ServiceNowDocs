---
title: Activating e-signature
description: You can activate the e-signature plugin \(com.snc.esign\) if you have the admin role. This plugin includes demo data and activates related plugins if they are not already active.
locale: en-US
release: zurich
product: e-Signature
classification: e-signature
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [E-signature, Manage people and work capabilities, Extend ServiceNow AI Platform capabilities]
---

# Activating e-signature

You can activate the e-signature plugin \(com.snc.esign\) if you have the admin role. This plugin includes demo data and activates related plugins if they are not already active.

## Before you begin

Role required: admin

## About this task

E-signature activates these related plugins if they are not already active.

<table id="table_wxd_nj4_pgb"><thead><tr><th>

Plugin

</th><th>

Description

</th></tr></thead><tbody><tr><td>

ServiceNow document viewer\[com.snc.documentviewer\]

</td><td>

Document viewer is a platform feature that will enable users to view enterprise class documents inline within the platform attachment instead of downloading it to the local device and then opening the documents with a locally installed viewer.

</td></tr><tr><td>

Managed documents\[com.snc.document\_management\]

</td><td>

Managed Documents application. To enable the ability to publish to the knowledge base, activate the knowledge document plugin.

</td></tr><tr><td>

Signature pad\[com.snc.signaturepad\]

</td><td>

Provides a tool to allow a digital signature in a .pdf document. The Human Resources application uses this with various documents.

</td></tr></tbody>
</table>## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the plugin using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated Admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/zurich-platform-administration/page/administer/plugins/task/find-components.html).


**Parent Topic:**[E-signature](../concept/e-signature.md)

