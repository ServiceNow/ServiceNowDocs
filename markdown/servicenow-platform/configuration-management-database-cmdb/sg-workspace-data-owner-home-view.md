---
title: Data Owner Home view in Service Graph Workspace
description: Data Owner Home view in Service Graph Workspace provides a filtered view for data owner users who own, manage, or support CIs. It provides those users with a simple method to browse their CIs, view health, related activity associated with their CIs, understand what their CIs support, and access to actions they're authorized to use for their CIs.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Explore, Service Graph Workspace, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Data Owner Home view in Service Graph Workspace

Data Owner Home view in Service Graph Workspace provides a filtered view for data owner users who own, manage, or support CIs. It provides those users with a simple method to browse their CIs, view health, related activity associated with their CIs, understand what their CIs support, and access to actions they're authorized to use for their CIs.

## Access

Navigate to **Workspaces** &gt; **Service Graph Workspace**, and then, in the navigation panel, select the Data Owner Home icon.

Role required: sn\_cmdb\_editor or sn\_cmdb\_admin

The Data Owner Home view shows users CIs that they own or manage, related health, related records, and related services and offerings. This view also provides AI-assisted insights, recommended actions, and important notifications. Service instance owners can view and manage their Service Instances.

As a data owner, you can view the following types of information:

-   Health of your CIs
-   Data sources used to populate your CIs
-   Tasks assigned to you with respect to your CIs
-   Insights, actions and tools available which are relevant to your CIs

Data owners can view their data in tabs and panels as described in this topic.

## CMDB data

Shows CMDB data details.

-   **Data sources and updates:**

    Provides summaries of related data sources, CI health, and tasks associated with the CIs, in the following cards:Counts of the data sources used to populate the CIs in the view, new and updated records and data ingestion issues affecting the CIs:

    -   Data sources: Total number of data sources used to update the user’s CIs, derived from the **Discovery source** field values.
    -   Data ingestion issues: Count of errors reported in Service Graph Connector log files, filtered to count only serious errors. Data is collected on a daily, weekly? schedule?
    -   New CIs: Count of CIs created in the last 24 hours, owned or managed by the logged-in data owner.
    -   Updated CIs: Count of CIs updated in the last 24 hours, owned or managed by the logged-in data owner.
-   **Health:**

    Shows the following health counts for CIs:

    -   Completeness: Number of CIs missing required attributes, and number of CIs missing recommended attributes \(counting unique CIs\)
    -   Correctness: Number of duplicate CIs, number of orphan CIs, and number of stale CIs
    -   Compliance: Number of CIs with audit failures
-   **CI list view**

    A list of the CIs associated with a selected card and filtered according to the filter settings on the page.


## Related activity

Shows cards for open incidents, changes, and problems, providing summaries from the Incident, Change Request, and Problem tables, and summaries from other tables related to the data owner CIs.

## Actions &amp; Insights

A panel providing a set of recommended actions and insights related to the a list of CIs and the user’s association with those CIs. This panel contains the following cards:

-   **Actions**

    Open tasks that are associated with the CIs in the list.

-   **Health**

    Details about the overall health score for owned CIs. The card shows a breakdown of counts by the main health KPIs:

    -   Completeness: Number of CIs missing mandatory fields, \# of CIs missing recommended fields
    -   Correctness: Number of stale, orphan &amp; duplicate CIs
    -   Compliance: Number of non-compliant CIs
    If the CMDB Health Dashboard jobs aren't running then health scores aren't available. In which case, a notification appears to inform your that health scores aren't available until you activate those jobs.

-   **Related activity summary**

    Lists related items, Incident, Change Request, and Problem by default, based on the user role and on records in the Explore CI Related Item Configurations \[sn\_cmdb\_ws\_explore\_ci\_related\_item\_config\] table. For each related item in the view, there is a summary for the related table.

-   **Recommended tools**

    Provides links to tools that are relevant to the data owner, such as Unified Map.

-   **Data Ingestion**

    Available to users with the sn\_cmdb\_admin role \(i.e. CMDB Administrators\).


## Use the Data Owner Home view

You can perform the following actions on the Data Owner Home view:

-   Filter the data that shows in the CMDB data cards, by:
    -   Association: Select **CIs I own** to show only those CIs that you own \(CIs in which **owned\_by** is equal to the data owner user\). Select **CIs I manage** to show only those CIs that you manage or that are managed by a group that you're a member of \(CIs in which **managed\_by** is equal to one of the groups that the data owner user belongs to\). Or, select **All association types** to show both types.
    -   Classes: Select a CI class derived from the CIs specified by the association filter, or **All classes**. This filter is applied on top of the association filter.
-   Personalize the list of the CIs included in the view. You can specify conditions that limit which CIs are included, you can sort and group the list, and select a CI from the list to show it in CI Form. For more information about CI Form, see [Manage CI details using CI Form in Service Graph Workspace](ci-form-sg-workspace.md).
-   Select related items to open a list view of the associated records.
-   Select the Related items settings icon in the Related activity tab and select and arrange which related items categories appear in the cards in the Related activity tab.
-   Select **CMDB Health Settings** in the Health card on the CMDB data tab to configure CMDB Health preferences. For more information, see [Configuring CMDB Health](c_CMDBHealthSetupandConfig.md).
-   Select a tool in the Recommended tools card in the Insights &amp; Actions pane.
-   In the CIs list, select an action such as Edit, Export, New, or select the More Actions icon and then select **Personalize fields**.
-   An Administrator can configure which related items appear in the Related activity summary card in the Actions &amp; Insights panel.

    A user with the sn\_cmdb\_ws.config\_editor role can access the Explore CI Related Item Configurations \[sn\_cmdb\_ws\_explore\_ci\_related\_item\_config\] table to delete, update, or add records for other related items such as alerts.


