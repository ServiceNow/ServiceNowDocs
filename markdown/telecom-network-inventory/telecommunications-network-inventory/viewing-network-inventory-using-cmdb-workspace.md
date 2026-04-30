---
title: Viewing your network inventory configuration items with CMDB Workspace or Service Graph Workspace
description: You can use CMDB Workspace to search and explore the CMDB, examine its health and recent activity, and access various dashboards and tools to support the tasks in your organization.
locale: en-US
release: zurich
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 6
breadcrumb: [Use, Telecommunications Network Inventory]
---

# Viewing your network inventory configuration items with CMDB Workspace or Service Graph Workspace

You can use CMDB Workspace to search and explore the CMDB, examine its health and recent activity, and access various dashboards and tools to support the tasks in your organization.

## Prerequisites for Service Graph Workspace or CMDB Workspace

-   Plugins: You must activate the following plugins before you can use CMDB Workspace:
    -   CMDB CSDM Support \(com.snc.cmdb.csdm\)
    -   CMDB Activation \(com.snc.cmdb.csdm.activation\)
-   Roles: To access CMDB Workspace, you must, at a minimum, have one of the following roles:

    -   sn\_cmdb\_admin
    -   sn\_cmdb\_editor
    -   sn\_cmdb\_user
    **Note:** In CMDB Workspace, some dashboards and list views require specific roles in addition to the key admin, editor, or user roles. Depending on which role is assigned to you, you might only have access to some of the features that are available in the CMDB Workspace or Service Graph Workspace

    .

-   Features: CMDB Workspace provides access to a wide range of applications and features. However, to provide meaningful reports, overviews, and trends, you must set up and configure some of those features so that CMDB Workspace can use the data that is generated.

## Accessing CMDB Workspace

After you install the app from the ServiceNow Store, navigate to **Workspaces** &gt; **CMDB Workspace or Service Graph Workspace**.

## CI searches

Specify up to five conditions to search for the configuration items \(network asset CI\) of a class. These conditions are based on the attributes for a selected class. In the results list, click a network asset CI to see the details about the network asset CI, including a time line, health overview, and attributes for the network asset CI.

For more information, see the CI Details page section.

## CI overview

Get an overview of the network asset CIs in CMDB that are grouped by common class categories as **Applications**, **Cloud**, and **Server**.

Select a class group to see all the classes that are included in the group, and then select the class whose network asset CIs you want to see.

In the Results list, you can click a network asset CI to see an overview page with a time line, health overview, and attributes for the network asset CI. For more information, see the CI Details page section.

## CMDB health

Get the metrics for the network asset CIs and see the health of the relationships. Click the percentage numbers to navigate to the CMDB Health and CMDB Relationship Health dashboards where you can see the following information:

-   The overall percentage number represents the health of all network asset CIs as an aggregation of all three key performance indicators \(KPIs\), which are correctness, compliance, and completeness. Each network asset CI contains submetrics.
-   The relationship percentage number represents the overall health of the relationships as an aggregation of the orphan, duplicate, and stale relationship KPIs.

## 7-day activity trends

CMDB Workspace includes the following charts that provide an overview of the activity in the CMDB for the last seven days:

-   **CI Activity in Last 7 Days**

    See a chart that shows the metrics that are related to the network asset CIs. For example, you can see the metrics for the number of new network asset CIs, updated network asset CIs, and duplicate network asset CIs.

-   **Application Service Activity in 7 Days**

    See a chart that shows the metrics that are related to the application services. For example, you can see the total number of Application Services, new Application Services, updated Application Services, and the number of Application Services with outages.


## CIs managed by me

See a list of network asset CIs that you manage, grouped by the network asset CI class. Network asset CIs appear in this list if you are a member of the group that is assigned to the network asset CI's **Managed by Group** attribute.

## Quick links

See a list of the links to the CMDB dashboards and tools:

**Note:** Links are conditionally available based on the installation of applications, active plugins, and your assigned role. If a link doesn't appear, make sure that all the requirements for the link are met.

-   CI Class Manager: You can view, create, or edit the basic class definitions and class settings for Identification and Reconciliation \(IRE\) and CMDB Health.
-   CMDB Health Dashboard: You can view the health reports and configure the health KPIs and metrics that the network asset CIs are evaluated by in the CMDB Health dashboards.

## CI details page

When you drill down to a network asset CI record, you can see the following details for the network asset CI:

-   CI Timeline - Last 14 days: A time line of the network asset CI activities, such as change requests.
-   CI Health: A summary of the health of the network asset CI that shows the related items such as critical incidents, incomplete attributes, and stale relationships for the network asset CI.
-   Details: Network asset CI attributes, grouped into categories such as Key attributes, Asset attributes, Discovery attributes, Operational attributes, and More attributes.

    **Note:** You can configure the appearance of the attributes by using the **CMDB - Workspace** or Service Graph Workspace form view for a network asset CI class.

-   Activity: An activity stream to track what's changed in the network asset CI record.
-   Infrastructure Relationships: A list of the infrastructure network asset CIs that are related to the network asset CI.
-   Service Relationships: A list of business applications, service offerings, and application services that the network asset CI may be related to.

On the CI details page, you can do the following actions:

-   To open Dependency Views and to get a graphic infrastructure view of the network asset CI record, click **Open Dependency View**.
-   To open the Multisource Data Report Builder and track how the CMDB is populated by the various discovery sources at the network asset CI attribute level of the network asset CI record, click **View Multisource Data**.
-   To save your changes to the attributes for the network asset CI record, click **Save**.


## CI error message

The following table helps you to understand the CI error message that appears during the CI deletion and the solution that you can use to resolve the error:

<table id="table_jlb_snm_wtb"><thead><tr><th>

Error

</th><th>

Resolution

</th></tr></thead><tbody><tr><td>

**The current operation ended in state: ERROR. Detail: Operation\(Delete All TNI CI Hierarchy./end\) failed with error: Error: The CI "XXXX/XXXX/Copper Link/000118" cannot be deleted since there is a related CI "XXXX/XXXX/PON Access Path/100Mbps/000030" \(sys\_script\_include.989afcd1cb330110202b2c52f8076d7e.script; line 52\)**

</td><td>

Delete the child or related CI \(Configuration Item\) to delete the parent CI.1.  Click the related or the child CI under **Related Templates**.
2.  Click **Delete**.

However, an Admin can always customize the deletion action. To learn more, see [Customizing deletion action](../task/customizing-deletion-action.md).

</td></tr></tbody>
</table>-   **[Customizing deletion action](../task/customizing-deletion-action.md)**  
Customizing deletion action enables you to create your own process of the deletion.

**Parent Topic:**[Using Telecommunications Network Inventory](using-telecom-network-inventory.md)

