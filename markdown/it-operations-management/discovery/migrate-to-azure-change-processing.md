---
title: Migrate to Azure change processing
description: Migrate to Azure change processing to improve the change processing performance of the ServiceNow AI Platform and take advantage of the simplified setup.
locale: en-US
release: yokohama
product: Discovery
classification: discovery
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Azure change processing, Discovery for Microsoft Azure Cloud, Discovery for cloud environment, Discovery, ITOM Visibility, IT Operations Management]
---

# Migrate to Azure change processing

Migrate to Azure change processing to improve the change processing performance of the ServiceNow AI Platform and take advantage of the simplified setup.

## Before you begin

-   Ensure that the latest version of Discovery and Service Mapping Patterns store app is installed on the ServiceNow AI Platform.
-   Ensure that Microsoft Azure alert-driven discovery is configured on the ServiceNow AI Platform.
-   Ensure that the Cloud Events \[sn\_cmp\_cloud\_event\] table doesn’t contain any event in ready state.
-   Ensure that the scope is set to Global.
-   Ensure that at least one active MID Server is available.

Role required: discovery\_admin or sn\_cmp.cloud\_admin

## About this task

If you are using the Microsoft Azure alert-driven discovery and the ServiceNow AI Platform receives a huge number of alerts from the Azure cloud, it may take a significant amount of time to process the alerts and update the Configuration Management Database \(CMDB\). Migrate to the Azure change processing to overcome the performance issues. For more information on the Azure change processing, see [Azure change processing](../concept/azure-change-processing.md).

## Procedure

1.  Navigate to **All** &gt; **Pattern Designer** &gt; **Configure Azure Change Processing**.

2.  Select Retrieve Azure alert configurations to retrieve the list of all the active Azure alert configurations.

3.  Select **Disable Azure alert configurations**.

    The ServiceNow AI Platform deactivates the Azure alert configurations and removes the webhooks from the Azure portal.

4.  Select the accounts for which you want to configure Azure change processing.

    1.  From the **Service Accounts without ‘pull-based’ change processing** list, select the accounts for which you want to configure Azure change processing.

    2.  Add the selected accounts to the **Service Accounts with ‘pull-based’ change processing** list.

        **Note:** When you enable Azure change processing for an Azure management group, it is also enabled for all the subscriptions in the management group.

5.  Select **OK**.


## Result

The migration script marks the Azure configurations module as deprecated. In the Cloud Discovery. The Azure Alert Configurations page is hidden in the Cloud Discovery Workspace.

**Related topics**  


[https://support.servicenow.com/kb?id=kb\_article\_view&amp;sysparm\_article=KB1705862](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1705862)

