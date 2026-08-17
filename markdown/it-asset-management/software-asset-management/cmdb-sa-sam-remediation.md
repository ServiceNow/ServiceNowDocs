---
title: Improving CMDB data quality for SAM
description: The Remediation actions panel available for a chart in the CMDB success advisor dashboard for Software Asset Management \(SAM\) suggests targeted actions to improve the overall quality of your Configuration Management Database \(CMDB\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/software-asset-management/cmdb-sa-sam-remediation.html
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2026-07-22"
reading_time_minutes: 1
keywords: [SAM remediation actions panel, improve SAM data quality, stale CI remediation, duplicate CI remediation, software asset data quality issues]
breadcrumb: [Use SAM advisor, Software Asset Management, IT Asset Management, Asset Management]
---

# Improving CMDB data quality for SAM

The Remediation actions panel available for a chart in the CMDB success advisor dashboard for Software Asset Management \(SAM\) suggests targeted actions to improve the overall quality of your Configuration Management Database \(CMDB\).

\[Omitted image "cmdb-sa-sam-remediation-actions.png"\] Alt text: Example actions in the remediation actions panel shown for installs on duplicate CIs.

When remediation actions are available for a chart, the Remediation actions panel appears on the KPI Details page.

You can perform the actions suggested within the Remediation actions panel to address SAM data quality issues in the CMDB. These actions help improve the accuracy, consistency, and usability of configuration items \(CIs\), promoting better alignment with SAM.

The Remediation actions panel:

-   Improves CMDB data quality through guided actions
-   Suggests context-aware actions
-   Supports quick, informed remediation steps
-   Focuses attention on meaningful tasks
-   Appears only when actionable insights are available

## Accessing the Remediation actions panel

To open the Remediation actions panel, select a segment or count on a chart in the CMDB success advisor dashboard for SAM. The KPI Details page opens. If remediation actions are available for the selected data, the panel appears on the details page suggesting various remediation actions.

## Available remediation actions

The Remediation actions panel provides relevant suggestions and actions based on the information in the selected chart. The remediation actions are available for the improvement of the following issues:

-   **Stale CIs**

    Selecting a segment on the **CIs not updated** chart displays a suggestion to review the retire policies for the CI classes associated with the listed CIs. Reviewing these policies enables you to maintain an accurate representation of your software asset environment.

-   **Duplicate CIs**

    Selecting a segment on the **Installs on Duplicate CIs** chart displays a suggestion to review the open de-duplication tasks for the affected CIs. Reviewing these tasks enables you to avoid data fragmentation and promote a single source of truth for software install data.


