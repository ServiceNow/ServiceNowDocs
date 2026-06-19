---
title: Service Graph Connector for ServiceNow OT Discovery Guided Setup
description: Use the Guided Setup for the Service Graph Connector for ServiceNow OT Discovery to lead you through the installation, connection, configuration, and integration steps for the OT Discovery environment.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/operational-technology/sgc-ot-discovery-guided-setup.html
release: australia
product: Operational Technology
classification: operational-technology
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Service Graph Connector for ServiceNow Operational Technology \(OT\) Discovery, Operational Technology Native Discovery components, Operational Technology Discovery, Operational Technology]
---

# Service Graph Connector for ServiceNow OT Discovery Guided Setup

Use the Guided Setup for the Service Graph Connector for ServiceNow OT Discovery to lead you through the installation, connection, configuration, and integration steps for the OT Discovery environment.

## Before you begin

Review the [Service Graph Connector for ServiceNow Operational Technology \(OT\) Discovery prerequisites and settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/operational-technology/sgc-prereq-settings.md) section before beginning.

Role required: admin

## Procedure

1.  From your ServiceNow instance, navigate the **All** menu.

2.  Enter `Service Graph Connector` into the filter and scroll down the menu to find ServiceNow OT Discovery.

3.  Select **Setup**.

4.  The Service Graph Connector for ServiceNow OT Discovery Guided Setup page opens.

5.  On the Guided Setup page, select **Get started**.

    This opens the page with each task for downloading the OT devices as well as steps to configure connections, integrations, and imports for the Service Graph Connector.

6.  In the first section, select **Download &amp; Deploy OT Discovery**.

    This opens the **Download &amp; Deploy OT Discovery** page.

7.  Select **Configure**.

8.  Read the EULA and then download the packages for the Console, Sensor, and Collector.

9.  Choose the OT Discovery Collector OS package that matches your machine's OS.

    **Note:** If you have a closed network, download the Sensor package and the containerized versions of the Console and Collector packages. When ready, in stall the Console first, install the Sensor after that and, finally, install the Collector. See [Air-gapped networks and OT Discovery installation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/operational-technology/air-gapped-networks-installation.md) for more information.

10. Return to the previous page and select **Mark as complete**.

11. Go back to the Service Graph Connector Guided Setup page.

12. The next section is **Configure table permissions**.

    **Note:** Setting the table permissions allows you to have multiple connections across multiple consoles. This depends on your deployment choice of the Discovery Console for OT.

    1.  In the Configure table permissions section, select **Scheduled data import**.

        This opens the Configure table permissions page.

    2.  Next to the **Scheduled data import** task, select **Configure**.

    3.  The Scheduled data import table opens.

    4.  In the table, select the **Application Access** tab.

    5.  Confirm that the Can Read, Can Create, and Can Update options are checked.

    6.  Select **Update**.

    7.  Return to the Configure table permissions page and select **Mark as complete** next to the **Scheduled data import** task.

    8.  Select **Configure** next to the **Data source** task.

    9.  The Data source table displays.

    10. Select the **Application Access** tab.

    11. Confirm that Can Read, Can Create, and Can Update options are checked.

    12. Select **Update** or **Save**,

    13. Return to the Configure table permissions page and select **Mark as complete** next to the **Data source** task.

    14. Return to the Guided Setup page.

    **Note:** These settings give you flexibility in how you setup your system. The Service Graph Connector for ServiceNow OT Discovery supports multiple-connections to multiple consoles. This depends on the deployment choice made for the Consoles. These settings give you the ability to create multiple data source objects, console objects, and multiple schedules from which to pull data.


## What to do next

The next step in the Guided Setup is [Configure the OT Discovery connections &amp; credentials](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/operational-technology/configure-the-ot-discovery-connections-credentials.md).

