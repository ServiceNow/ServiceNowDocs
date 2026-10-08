---
title: Configure Service Graph Connector for BlueCat using SGC Central
description: Use the playbook in SGC Central to set up the Service Graph Connector for BlueCat and pull BlueCat data into your CMDB.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/service-graph-connectors/sgcc-configure-bluecat.html
release: brazil
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [BlueCat, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Configure Service Graph Connector for BlueCat using SGC Central

Use the playbook in SGC Central to set up the Service Graph Connector for BlueCat and pull BlueCat data into your CMDB.

## Before you begin

Install Service Graph Connector for BlueCat from the ServiceNow Store. For ServiceNow Store installation steps, see [Install a ServiceNow Store application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/installing-applications-in-application-manager.md).

## About this task

The playbook experience for onboarding connectors is activated with SGC Central in the CMDB Workspace. To configure the SGC Central application, see [Configuring SGC Central](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/sgcc-configuring.md) and for more information on how to interact with a playbook, see Interact with Playbook.

## Procedure

1.  Navigate to **Workspaces** &gt; **CMDB Workspace**.

2.  In the CMDB Workspace, select **SGC Central**.

3.  On the Overview page, select **Create connection**.

4.  On the Create connection window, select the BlueCat connector type, and then select **Create connection**.

5.  Complete the initial prerequisites when setting up a connection for the first time.

    **Note:** This step is required only during the first-time setup. See [Perform initial setup tasks when creating a connection in SGC Central](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/sgcc-first-time-setup.md).

6.  Enter connection details and test the connection for importing BlueCat data.

    1.  In the **Setup** stage, select **Create and test connection**.

    2.  On the form, fill in the fields.

    3.  Select **Create and test connection**.

    4.  After the test completes, select **Continue**.

7.  Set the configuration properties for the connection.

    1.  In the **Setup** stage, select **Set configuration properties**.

    2.  Fill in the property details.

    3.  Select **Continue**.

8.  Configure the import schedule.

    1.  In the **Setup** stage, select **Configure import schedule**.

    2.  Select the import schedule for your connection, set it to **Active**, and fill in the run schedule details.

    3.  Select **Save**, then **Continue**.

9.  Select **Confirm connection creation** to verify the connection.


## What to do next

Select **View all connections** to review the connection details.

You can manage connections from the SGC Central view of the CMDB Workspace. For more information, see [Managing connections added for Service Graph Connectors in SGC Central](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/sgcc-managing-connection.md).

