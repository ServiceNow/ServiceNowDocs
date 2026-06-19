---
title: Create a connection administrator
description: Create a connection admin who can create zero copy connections in Workflow Data Fabric Hub.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/integrate-applications/workflow-data-fabric-hub/create-connection-admin-wdf.html
release: zurich
product: Workflow Data Fabric Hub
classification: workflow-data-fabric-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure, Workflow Data Fabric Hub, Workflow Data Fabric]
---

# Create a connection administrator

Create a connection admin who can create zero copy connections in Workflow Data Fabric Hub.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **User Administration** &gt; **Users**.

2.  Select an existing user.

3.  Update the user's role assignment by selecting **Edit** in the Roles related list.

4.  Add the df\_connection\_admin role.

5.  Select **Update**.


## Result

The user is now a connection admin in Workflow Data Fabric Hub. As a connection admin, the user can perform the following tasks:

-   Browse available primary and community connectors on the **Available connectors** tab.
-   Select a connector and create a zero copy connection to an external data source.
-   Define who can access the connection and create data fabric tables by assigning the df\_data\_steward role to an existing role.

See [Managing zero copy connections in Workflow Data Fabric Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/workflow-data-fabric-hub/managing-connections-wdf.md).

**Parent Topic:**[Configuring Workflow Data Fabric Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/workflow-data-fabric-hub/configuring-wdf.md)

