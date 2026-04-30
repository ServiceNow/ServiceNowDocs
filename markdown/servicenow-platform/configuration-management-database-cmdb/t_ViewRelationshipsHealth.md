---
title: View relationships health
description: View health scores for relationship health such as orphan, stale, and duplicate relationships, in the Relationship Health Dashboard.
locale: en-US
release: zurich
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [CMDB Health, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# View relationships health

View health scores for relationship health such as orphan, stale, and duplicate relationships, in the Relationship Health Dashboard.

## Before you begin

The CMDB Health Dashboard - Relationship Compliance Processor dashboard job must run to generate data for these reports.

**Note:** As a general guideline, activate this job only if you need the relationship reports as this job can affect performance.

Role required: sn\_cmdb\_editor, asset, or itil

## About this task

The Relationship Health Dashboard shows various scorecards for health indicators of CI relationships in your CMDB. It contains donut reports for duplicate, orphan or stale relationships, broken down by relationship type. You can drill down these charts for further details.

The warning that max failure is reached icon, indicates that the maximum failure threshold for the metric has been reached. The tests for the metric are halted for this cycle, and all associated aggregated summaries show 0%. Review the scorecard rules which might be ineffective, or the CMDB might be in an unstable state.

CMDB Health reports for the following metrics:

-   **Duplicate relationship**

    Relationships that have identical parent, child, and relationship type.

-   **Orphan relationship**

    A relationship that is missing parent, child, or relationship type.

-   **Stale relationship**

    A relationship in which one of the CIs is stale. For a stale CI — its associated relationships are also stale.


In addition, the following relationship compliance reports with breakdown by relationship types, are available:

-   **Relationships not compliant with all relationship rules**

    Relationships that do not comply with any [relationship governance](../concept/relationship-governance.md) rule, including suggested relationships and dependent relationship rules.

-   **Relationships not compliant with suggested relationships**

    [Suggested CI relationships](../reference/r_SuggestedRelationshipModel.md) are used as rules to test if relationships comply with specified suggested relationships.

-   **Relationships not compliant with containment rules**

    Containment rules are used to test if relationships comply with specified containment relationships.

-   **Relationships not compliant with hosting rules**

    Hosting rules are used to test if relationships comply with specified hosting relationships.


For each of the compliance reports, testing a relationship requires a rule \(suggested relationship, hosting rule, or containment rule\) in which the parent and child CI classes match the parent and child CI classes in the tested relationship. If the relationship types in the rule and in the tested relationship don't match, then the relationship isn't in compliance. If an applicable rule isn't found, then the relationship is considered to be in compliance. Rules apply to the classes specified in the rule, and also to descendant classes. Therefore, when testing a relationship, rules that apply to ascendant parents of the CIs in the tested relationship are used. If there are multiple rules that match the parent and the child CI classes of the tested relationship, then the tested relationship needs to satisfy only one of these rules to be in compliance.

## Procedure

1.  Navigate to **Workspaces** &gt; **CMDB Workspace**.

2.  Select **Home** in the CMDB Workspace menu bar and then, in the Quick links section select the **Relationship Health Dashboard** link.

3.  Examine the donut reports and the charts in the Relationship health overview and Relationship compliance overview sections on the dashboard.

    Report results are grouped by relationship type, and you can drill down for further details:

    -   Point to a donut report to show more details about compliant and non-compliant relationships.
    -   Point to a bar in a bar chart to show more details for the bar.
    -   Select a bar in a bar chart to drill down to a list view of all the associated relationships that aren't compliant. The list view includes the **Failure Description** field which lists only a single rule that the relationship didn't comply with, even if there are additional rules that the relationship fails to comply with.

## What to do next

For troubleshooting information, see the [How to identify and delete duplicate CMDB CI Relationship records, or ones that have orphan or missing parent/child relationships \[KB0780988\]](https://support.servicenow.com/kb_view_customer.do?sysparm_article=KB0780988) knowledge base article.

**Parent Topic:**[CMDB Health](../concept/c_CMDBHealth.md)

**Related topics**  


[Exploring CMDB Health](../concept/exploring-cmdb-health-parent.md)

[CMDB Health experience in CMDB Workspace and in Service Graph Workspace](../concept/cmdb-health-exp-cmdb-workspace.md)

[View CMDB Health Dashboard](../concept/c_MonitorCMDBHealth.md)

[View CI health](t_ViewCIHealth.md)

[Create a CMDB remediation rule](t_CreateCMDBRemediationRule.md)

[CMDB Health process tracking and troubleshooting](../concept/c_CMDBHealthTroubleshooting.md)

[CMDB Health reference](../concept/cmdb-health-ref-parent.md)

[Enable and configure a CMDB Health Dashboard job](t_EnableCMDBHealthDashboardJob.md)

