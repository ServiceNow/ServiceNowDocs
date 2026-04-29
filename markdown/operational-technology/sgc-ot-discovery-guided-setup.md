---
title: Service Graph Connector for OT Discovery guided setup
description: Use the Guided Setup for the Service Graph Connector \(SGC\) for ServiceNow OT Discovery to lead you through the connection, configuration, and integration steps.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Service Graph Connector for ServiceNow Operational Technology\(OT\) Discovery, Operational Technology Native Discovery components, Operational Technology Discovery, Operational Technology]
---

# Service Graph Connector for OT Discovery guided setup

Use the Guided Setup for the Service Graph Connector \(SGC\) for ServiceNow OT Discovery to lead you through the connection, configuration, and integration steps.

## Before you begin

Review the [Service Graph Connector prerequisites and settings](../concept/sgc-prereq-settings.md) section before beginning.

Role required: admin

## Procedure

1.  From your ServiceNow Instance, use the **All** menu to search for the Guided Setup page.

2.  Enter into the filter `Service Graph Connector` and scroll down the menu to find ServiceNow OT Discovery.

3.  Select **Setup**.

4.  The Service Graph Connector for ServiceNow OT Discovery Guided Setup page opens.

5.  On the Guided Setup page, select **Get started**.

    This opens the page with each task for downloading the OT components as well as steps to configure connections, integrations, and imports for the Service Graph Connector.

6.  In the first section, select **Download &amp; Deploy OT Discovery**.

    This opens the **Download &amp; Deploy OT Discovery** page.

7.  Select **Configure**.

8.  Read the EULA and then download the packages for the Discovery Console for OT, the Discovery Sensor for OT, and the OT Discovery Collector.

9.  Choose the Collector package that matches your machine's OS \(Windows or Linux\).

    Install these packages after you have configured the settings and connections for the Service Graph Connector.

10. Return to the previous page and select **Mark as complete**.

11. Return to the Service Graph Connector Guided Setup page.

    **Note:** Setting the table permissions allows you to have multiple connections across multiple Consoles. This depends on your deployment choice of the Discovery Console for OT.

12. The next section is **Configure table permissions**.

13. In the **Configure table permissions** section, select **Scheduled data import**.

    This opens the **Configure table permissions** page.

14. Next to the **Scheduled data import** task, select **Configure**.

    The **Scheduled data import** table opens.

15. In the table, select the **Application Access** tab.

    Verify that the Can Read, Can Create, and Can Update options are checked.

16. Select **Update**.

17. Return to the Configure table permissions page and select **Mark as complete** next to the **Scheduled data import** task.

18. Select **Configure** next to the **Data source** task.

    The **Data source** table displays.

19. Select the **Application Access** tab.

    Verify that Can Read, Can Create, and Can Update options are checked.

20. Select **Update** or **Save**,

21. Return to the **Configure table permissions** page and select **Mark as complete** next to the **Data source** task.

22. Return to the Guided Setup page.

    **Note:** These settings give you flexibility in how you setup your OT system. The Service Graph Connector for OT Discovery supports multiple-connections to multiple consoles \(this depends on the deployment choice made for the Consoles\). These settings give you the ability to create multiple data source objects, console objects, and multiple schedules from which to pull data.


## What to do next

The next step in the Guided Setup is [Configure the OT Discovery connections &amp; credentials](configure-the-ot-discovery-connections-credentials.md).

