---
title: Activate ServiceNow Otto plugin on Sales CRM Mobile
description: Activate the plugin and ServiceNow Otto tab required for AI conversational interface on Sales CRM Mobile application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/activate-servicenow-otto-plugin-sales-crm-mobile.html
release: brazil
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Configure Sales CRM Mobile, Configure, Sales Customer Relationship Management]
---

# Activate ServiceNow Otto plugin on Sales CRM Mobile

Activate the plugin and ServiceNow Otto tab required for AI conversational interface on Sales CRM Mobile application.

## Before you begin

Role required: admin

## Procedure

1.  Activate the ServiceNow Otto for Sales Automation plugin \(**sn\_som\_gen\_ai**\).

    For more information, see [Activate a plugin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/t_ActivateAPlugin.md).

2.  Navigate to **All** &gt; **sys\_sg\_button\_instance.list**.

    The Function instances page appears.

3.  Filter the record by entering **Sales CRM** in the **Name** field.

4.  Select the **Sales CRM - Agent Chat Prominent Action** record.

    The Sales CRM - Agent Chat Prominent Action function form is displayed.

5.  Select the **Active** option.

6.  Select **Update**.

    The Sales CRM - Agent plugin is installed and the ServiceNow Otto is available on the Sales CRM Mobile application.


## Result

Activate the chat launcher to use ServiceNow Otto on the Sales CRM Mobile application.

**Parent Topic:**[Configure Sales CRM Mobile Application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/configure-sales-crm-mobile.md)

**Related topics**  


[Configure Sales CRM Mobile Application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/configure-sales-crm-mobile.md)

[Activate ServiceNow Otto AI Interface](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/activate-servicenow-otto-chat-sales-crm-mobile.md)

[Use ServiceNow Otto on Sales CRM Mobile](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/servicenow-otto-sales-crm-mobile.md)

