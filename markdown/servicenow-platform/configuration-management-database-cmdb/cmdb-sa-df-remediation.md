---
title: Improving CMDB data quality for Data Foundations
description: The Remediation actions panel available for a chart in the CMDB success advisor dashboard for Data Foundations suggests targeted actions to address Data Foundations data quality issues and improve the overall quality of your Configuration Management Database \(CMDB\).
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Use Data Foundations advisor, CMDB success advisor, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Improving CMDB data quality for Data Foundations

The Remediation actions panel available for a chart in the CMDB success advisor dashboard for Data Foundations suggests targeted actions to address Data Foundations data quality issues and improve the overall quality of your Configuration Management Database \(CMDB\).

![Example actions in the remediation actions panel shown for CIs not updated in the last 90 days.](../image/cmdb-sa-df-remediation-actions.png "Remediation actions panel")

When remediation actions are available for a chart, the Remediation actions panel appears on the KPI Details page.

You can perform the actions suggested within the Remediation actions panel to address Data Foundations data quality issues in the CMDB. These actions help improve the accuracy, consistency, and usability of configuration items \(CIs\), promoting better alignment with Data Foundations.

The Remediation actions panel:

-   Improves CMDB data quality through guided actions
-   Suggests context-aware actions
-   Supports quick, informed remediation steps
-   Focuses attention on meaningful tasks
-   Appears only when actionable insights are available

## Accessing the Remediation actions panel

To open the Remediation actions panel, select a segment or count on a chart in the CMDB success advisor dashboard for Data Foundations. The KPI Details page opens. If the remediation actions are available for the selected data, the panel appears on the details page suggesting various remediation actions.

## Available remediation actions

The Remediation actions panel provides relevant suggestions and actions based on the information in the selected chart. For example, if the chart shows CIs that weren't updated recently, the panel suggests reviewing retirement policies.

The remediation actions are available for the improvement of the following issues:

-   **CIs with invalid or unpopulated names**

    Identify and correct CIs in your principal classes that lack a valid name. Accurate names are required to correctly reference data to the right configuration item.

-   **CIs missing location**

    Resolve CIs in your principal classes that have no location assigned. Location data supports incident routing, asset tracking, and compliance reporting across your organization.

-   **CIs missing managed by group**

    Assign a managed by group to CIs in your principal classes that are missing ownership. Ownership data is critical for routing incidents, changes, and service requests to the correct team.

-   **Stale CIs**

    Remove or update CIs in your principal classes that have not been updated or discovered for an extended period. Stale records reduce trust in the CMDB and can cause incorrect assignments.

-   **Duplicate CIs**

    Remove or merge duplicate records within your principal classes. Duplicates can cause split incident history and routing errors in workflows.


## Data Foundations specific remediation tips

-   For stale CIs in principal classes: check whether a Discovery schedule is running against the affected network segment or cloud account. Stale data often means a Discovery job is failing or out of scope.
-   For duplicate CIs: review the CMDB Identification and Reconciliation \(IRE\) rules for the affected CI class. Duplicates often signal that IRE rules need updating.
-   For missing location or owner: consider using a CMDB enrichment rule to auto-populate these fields from related records. For example, derive location from IP subnet.

