---
title: List view
description: The List view in the BCM Configurable Workspace displays BIA, planning, exercise, and crisis event records and their key metrics. You can filter, create, and open records to view all BCM functional components and their metrics.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/governance-risk-compliance/list-view-uib-ws.html
release: australia
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 4
breadcrumb: [BCM Configurable Workspace, Explore, Business Continuity Management, Governance, Risk, and Compliance]
---

# List view

The List view in the BCM Configurable Workspace displays BIA, planning, exercise, and crisis event records and their key metrics. You can filter, create, and open records to view all BCM functional components and their metrics.

Use the List view to check the count and status of the business impact analysis, planning, exercise, and crisis event records. The List view enables you to do the following:

-   Assess potential disruptions to business services or applications.
-   Manage continuity plans and their dependencies.
-   Create and track exercise events.
-   Respond to crisis events with relevant continuity tasks.
-   View issues associated with the plan and event records that are in the **New**, **In progress**, or **Closed** state, and select **New** to create an issue directly from the **Issues** group.
-   View issue remediation tasks in a dedicated **Issue remediation tasks** group, filtered by the **Open** and **Closed** states.
-   View issue triage records in a dedicated **Issue triage** group, filtered by **Unassigned** and **All**.
-   Browse and create recovery teams from a dedicated **Recovery teams** group.

The following image shows a typical List view in the BCM Configurable Workspace.

\[Omitted image "list-view-bcm.png"\] Alt text: List view in BCM UIB Workspace.

The records from each group are listed according to their current state and the record details are configurable. You can create a record by selecting **New**. To view record details, select the record name in the **Name** column.

Use the List view in the BCM Configurable Workspace to complete these business continuity tasks:

-   Assess the impact of a possible disruption on your business services, processes, and applications. For more information on performing a business impact analysis, see [Business impact analysis](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/governance-risk-compliance/bia-uib.md).
-   Create business continuity plans to mitigate the risk at the time of an event. For more information on managing your business continuity planning tasks, see [Business continuity planning](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/governance-risk-compliance/bcp-uib.md).
-   Create an event to exercise the plan in a simulated crisis. For more information on exercising an event, see [Exercises](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/governance-risk-compliance/exercise-management-uib.md).
-   Apply the plan in an actual crisis. For more information on managing a crisis event, see [Crisis events](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/governance-risk-compliance/crisis-management-uib.md).
-   Browse and create issues, and browse issue remediation tasks, without opening a specific plan or event. For more information, see [Issue modules in Business Continuity Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/governance-risk-compliance/bcm-issue-list-modules.md).

For information on managing business continuity tasks in the BCM Configurable Workspace, see [Managing BCM workflow tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/governance-risk-compliance/manage-bcm-with-uib-workspace.md).

## 360° relationship data for records

You can view 360° relationship data for BIAs, plans, exercises, and crisis events. This view shows upstream and downstream dependencies, helping you understand how assets relate to one another. Administrators configure these views using the **360° View Configurations** menu.

The configurations for the 360° view are stored in **360° View Configurations** &gt; **Configure 360° Views**. If you have the BCM administrator role, you can configure the relationships for the records in **360° View Configurations** &gt; **Relationship Registries**.

-   For information on configuring 360° relationship registries and views, see [Configure 360° relationship registries and views](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/governance-risk-compliance/configure-relationship-registries-views.md).
-   For information on how to view 360° relationships of a business impact analysis, see [Visualize 360° relationships for BIAs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/governance-risk-compliance/visualize-360-degree-view-for-bia.md).
-   For information on how to view 360° relationships of a business continuity plan, see [Visualize 360° relationships for the BCP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/governance-risk-compliance/relationship-view-bcp.md).
-   For information on how to view 360° relationships of an exercise or crisis event, see [View 360° relationships for exercises and crises](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/governance-risk-compliance/relationship-view-exercise-crisis.md).

**Related topics**  


[Issue modules in Business Continuity Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/governance-risk-compliance/bcm-issue-list-modules.md)

[Managing BCM workflow tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/governance-risk-compliance/manage-bcm-with-uib-workspace.md)

