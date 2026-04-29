---
title: Enable Azure change processing
description: Configure the Azure change processing to collect resource change information from the Microsoft Azure cloud and use it to update the Configuration Management Database \(CMDB\).
locale: en-US
release: australia
product: Discovery
classification: discovery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Azure change processing, Discovery for Microsoft Azure, Discovery for cloud environment, Discovery, ITOM Visibility, IT Operations Management]
---

# Enable Azure change processing

Configure the Azure change processing to collect resource change information from the Microsoft Azure cloud and use it to update the Configuration Management Database \(CMDB\).

## Before you begin

-   Ensure that the latest version of Discovery and Service Mapping Patterns store app is installed on the ServiceNow AI Platform.
-   Ensure that Microsoft Azure alert-driven discovery isn’t configured on the ServiceNow AI Platform.

Role required: discovery\_admin or sn\_cmp.cloud\_admin

## About this task

For information about the resources which are supported by Azure change processing, see [Azure change processing](../concept/azure-change-processing.md).

## Procedure

1.  Navigate to **All** &gt; **Pattern Designer** &gt; **Configure Azure Change Processing**.

2.  Select the accounts which you want to sync Azure change processing for.

    1.  Select the accounts from the **Service Accounts without ‘pull-based’ change processing** list.

    2.  Add the selected accounts to the **Service Accounts with ‘pull-based’ change processing** list.

        **Note:** When you enable Azure change processing for an Azure management group, it is also enabled for all the subscriptions in the management group.

3.  Select **OK**.


**Related topics**  


[https://support.servicenow.com/kb?id=kb\_article\_view&amp;sysparm\_article=KB1705862](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1705862)

