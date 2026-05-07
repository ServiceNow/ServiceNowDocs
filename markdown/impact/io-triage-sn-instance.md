---
title: Triage a ServiceNow instance
description: Perform a triage on a ServiceNow instance to gather point-in-time telemetry data for troubleshooting using Instance Observer. The triage feature gives a summary of ongoing operations at the time of its execution.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Monitoring instance health with Instance Observer, Platform Health, Using Impact, Impact]
---

# Triage a ServiceNow instance

Perform a triage on a ServiceNow instance to gather point-in-time telemetry data for troubleshooting using Instance Observer. The triage feature gives a summary of ongoing operations at the time of its execution.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **Instance Observer** &gt; **Triage**.

2.  From the Instance Observer Dashboard page, select the **Triage** tab.

3.  Select the **Instance** you want to triage.

4.  If the instance is not listed, select the **Update instance default settings** link.

    In the Update instance management settings page, select ![configure icon.](../image/io-popular-configured-icon.png) that works as toggle on and off within the Instance Telemetry pages.

    Instrumentation or telemetry data is available for production and sub-production instances. Caution must be exercised in interpreting the content of the sub-production data with the awareness of any active customizations or other development activities that might be happening.

5.  Select the **Node Type** to triage the instance.

    The production nodes are categorized as **All**, **Generic**, **Worker**, and **UI** nodes. You must select at least one node.

6.  Select **Triage**.

    The triage feature gives a summary of ongoing operations at the time of its execution. The triaged data displays the **Triaged Date** and **Node Status**, which is primary always.

    The triaged data appears in the form of widgets in 6 sections such as **Transactions**, **Jobs**, **Servlets**, **Schedulers**, **Semaphore Sets**, **Update Sets**. The Node type appears in each of the sections as **Type**, except **Update Sets** as this operates at the instance level and not at the node level.

    Most of the charts display data broken down by age. Whereas, Schedulers chart breaks down the data by worker nodes.

    To know more about each of the sections, see [Triaged instance data](../concept/io-triage.md).

    ![Instance Observer triage page.](../image/io-triage-phase-2.png)

7.  Select **View Details** in the Transactions section that takes you to the Transactions page to view its exclusive details.

    The **Triaged Date** and **Node Status** information is available here as well. The Type column gives you the node type information in the transactions section.

    ![View details in transactions section.](../image/io-transactions-view-det.png)

    You can filter \(![hamburger icon.](../../../common/image/icon_menu3lines.png)\) the columns with conditions to view transactions that you want and sort \(![descending sorting icon.](../../../reuse/icons/product-icons/sort-descending-outline-24.svg)\) each of the columns in ascending or descending order.

8.  Select the Transaction number for a node to view the details.

    **Note:** You will be able to view the details only when the transaction is complete, and it may take awhile.

9.  Select **Back to Triage** to navigate back to the Triage main page.

10. Select **View Details** in each section to view the respective details of **Jobs**, **Servlets**, **Schedulers**, and **Semaphore Sets**.

11. Select **History** to view the triage history in a slider view and click the **Created on** link that takes you to Triage History page.

12. Select **Download Triage File** to view all the sections of triaged details, downloaded in an excel format.


-   **[Triaged instance data](../concept/io-triage.md)**  
You can triage your instance to get instant information on transactions, jobs, nodes utilization, semaphores, schedulers and update sets. Minimal use of this feature is recommended as use of this consumes resources on your instance.

**Parent Topic:**[Monitoring instance health with Instance Observer](../concept/io-overview.md)

