---
title: Disable Document Viewer
description: Disable Document Viewer at the instance level to disable it or at table level to disable it for specific tables within the instance.
locale: en-US
release: australia
product: Document Management Services
classification: document-management-services
topic_type: task
last_updated: "2023-08-03"
reading_time_minutes: 1
breadcrumb: [Document Viewer, Document Services, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Disable Document Viewer

Disable Document Viewer at the instance level to disable it or at table level to disable it for specific tables within the instance.

## Before you begin

Ensure the Add a system property \(com.snc.documentviewer.enable\_document\_viewer\) exists in your instance.

Role required: admin

## Procedure

1.  Disable Document Viewer at the instance level or for specific tables.

<table id="choicetable_ehk_xyh_43b"><thead><tr><th align="left" id="d366613e67">

Option

</th><th align="left" id="d366613e70">

Description

</th></tr></thead><tbody><tr><td id="d366613e76">

**Disable Document Viewer at the instance level**

</td><td>

1.  Search for `sys_properties.list` in the navigation filter.
2.  Set the system property **com.snc.documentviewer.enable\_document\_viewer** value to **false**.
3.  Click **Update**.


</td></tr><tr><td id="d366613e109">

**Disable Document Viewer at the table level**

</td><td>

1.  Navigate to **System Definition**→ **Dictionary**.
2.  Open the table and click **New** under the **Attributes** tab.
3.  Search for `Use Document Viewer` in the **Attribute** field.
4.  Enter `false` in the **Value** field.
5.  Click **Submit**.


</td></tr></tbody>
</table>
**Related topics**  


[Enable Document Viewer](enable-document-viewer.md)

