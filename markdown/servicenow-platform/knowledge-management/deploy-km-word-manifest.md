---
title: Deploy Knowledge Management - Add-in for Microsoft Word
description: Deploy the Knowledge Management - Add-in for Microsoft Word for authoring knowledge articles from within the Microsoft Word.
locale: en-US
release: zurich
product: Knowledge Management
classification: knowledge-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure Knowledge Management - Add-in for Microsoft Word, Configuring Knowledge Management, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Deploy Knowledge Management - Add-in for Microsoft Word

Deploy the Knowledge Management - Add-in for Microsoft Word for authoring knowledge articles from within the Microsoft Word.

## Before you begin

In addition to having one of the following roles on the ServiceNow instance, you must be an Office365 administrator to deploy the Knowledge Management - Add-in for Microsoft Word.

Role required: admin, sn\_outlook\_addin.outlook\_addin\_setup

## Procedure

1.  Navigate to **All** &gt; **ServiceNow Add-Ins for Office** &gt; **Office Add-In-Manifests**.

2.  In the Add-In Name column, click **Knowledge Management**.

3.  Click **Download Manifest** to download the add-in manifest file to your desktop.

    **Note:** For releases prior to the Paris Patch 3 release, the downloaded manifest reports validation errors in Office 365. For more information about resolving such errors, see the [Enabling Knowledge MS-Word add-in fails validation \[KB0858357\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0858357) article in the HI knowledge base.

4.  Deploy the Knowledge Management- Add-in for Microsoft Word.

    For more information, see [Deploy add-ins in the admin center](https://docs.microsoft.com/en-us/microsoft-365/admin/manage/manage-deployment-of-add-ins?view=o365-worldwide).


**Related topics**  


[Import a Word document to a knowledge base](import-word-platform.md)

[Import a Word document to a knowledge base using Knowledge Management v3](t_ImportADocument.md)

