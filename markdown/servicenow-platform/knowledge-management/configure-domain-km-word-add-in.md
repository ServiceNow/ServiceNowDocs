---
title: Configure the security for Knowledge Management add-in for Microsoft Word
description: Use the sn\_km\_word.glide.knowman.word.xframe property to specify all the parent domains in the Microsoft Word Online application in which Knowledge Management - Add-in for Microsoft Word is embedded.
locale: en-US
release: zurich
product: Knowledge Management
classification: knowledge-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure Knowledge Management - Add-in for Microsoft Word, Configuring Knowledge Management, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Configure the security for Knowledge Management add-in for Microsoft Word

Use the **sn\_km\_word.glide.knowman.word.xframe** property to specify all the parent domains in the Microsoft Word Online application in which Knowledge Management - Add-in for Microsoft Word is embedded.

## Before you begin

Ensure that you have activated the Knowledge Management - Add-in for Microsoft Word plugin and the application scope is set to Knowledge Management - Add-in for Microsoft Word.

Role required: admin

## About this task

The domains you specify for the Microsoft Word application in the **sn\_km\_word.glide.knowman.word.xframe** property are used for setting the [x-frame-options](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/X-Frame-Options#Syntax) and [content-security-policy](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Content-Security-Policy) headers. These settings securely display the Knowledge Management add-in for Microsoft Word in the online version of Microsoft Word documents.

**Note:** If you don't set the **sn\_km\_word.glide.knowman.word.xframe** correctly, the Knowledge Management - Add-in for Microsoft Word fails to load in the Word document. For more information about resolving such errors, see the [Knowledge Word Office Manifest fails validation \[KB0860916\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0860916) article in the HI knowledge base.

## Procedure

1.  In the navigation filter, enter `sys_properties.list`.

2.  Search for the **sn\_km\_word.glide.knowman.word.xframe** property.

3.  In the **Value** field, enter a domain.

    For multiple entries, separate the domains with commas.

    For example, to enter the Microsoft SharePoint and Microsoft OneDrive domains: `https://*sitename*.sharepoint.com,https://*sitename*-my.sharepoint.com,https://word-edit.officeapps.live.com`

4.  Click **Update**.


