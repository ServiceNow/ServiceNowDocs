---
title: Manage issues
description: You can measure the effectiveness of your company's risk management program by how quickly and completely it identifies and reacts to risk and compliance issues.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/governance-risk-compliance/grc-common-functions/manage-issues-common-core.html
release: zurich
product: GRC Common Functions
classification: grc-common-functions
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Common GRC features, Governance, Risk, and Compliance]
---

# Manage issues

You can measure the effectiveness of your company's risk management program by how quickly and completely it identifies and reacts to risk and compliance issues.

Issues can be submitted using two methods, depending on the type of user involved:

-   Employees and business users within your company can [self-identify an issue and submit it via the ServiceNow® Service Portal.](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/policy-and-compliance-management/create-self-identified-issues.md) Following submission, a triage issue is automatically created and the issue triage process begins.
-   GRC users can [manually create an issue](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/audit-management/t_CreateAnIssue.md) from within their instance to document audit observations and remediations, and compliance and risk issues.

**Note:** Various types of issues can also be automatically generated under the following conditions \(these types of issues are not triaged\):

-   Control issue: Created when a control attestation is completed, indicating that the control is not implemented, or when an indicator fails.
-   Control test issue: Created when a control test is closed complete with the control effectiveness set to **Ineffective**.

## Goals of issue management

The goals of issue management include:

-   Eliminating noise​.

-   Consolidating duplicate issues​.

-   Focusing on issues that expose the organization to the greatest risk.

-   Identifying and prioritizing remediation actions​.

-   Identifying new issues across the business operations​.

-   Analyzing operational weakness in policies, processes, and controls​.


## Issue management workflow and life cycle

By remediating issues, controls can be kept compliant, and risk can be mitigated​. The Issue Management workflow and life cycle are illustrated and described here.

\[Omitted image "issue-management-workflow.png"\] Alt text: Issue Management Workflow

<table id="table_exh_nm3_b4b"><thead><tr><th>

Stage

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Issue intake

</td><td>

As described earlier, issues can be submitted using two methods, depending on the type of user involved:-   Employees and business users within your company can self-identify an issue and submit it via the ServiceNow® Service Portal. Following submission, a triage issue is automatically created and the [issue triage process](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/policy-and-compliance-management/triage-issue.md) begins.
-   GRC users can [manually create an issue](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/audit-management/t_CreateAnIssue.md) from within their instance. These types of issues are not triaged.

</td></tr><tr><td>

Investigate the issue

</td><td>

During the investigation phase, it is determined whether the issue requires additional study. If a triage is being performed, the triage issue is assigned to a triage team for analysis. The triage team may request more information from the issue creator. The team can also optionally send the issue to the compliance manager, risk manager, or triage manager with a triage result.

</td></tr><tr><td>

Remediate the issue

</td><td>

After the team has confirmed the issue, the necessary steps to remediate it are performed. If a triage was performed, the triage issue is converted into an actual issue or risk event. The team may also decide to track the issue as a recommendation or close it as a non-issue.

</td></tr><tr><td>

Review and monitor the issue

</td><td>

Prior to closing the issue, the policy owner reviews and approves it. The review also allows the organization to:-   track past due tasks
-   benchmark issue timelines
-   identify where losses could have been mitigated
-   reduce gaps in the future

</td></tr></tbody>
</table>-   **[Issues in the Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/grc-common-functions/issues-in-workspace.md)**  
You can track all your issues or one specific issue from the Workspace. Issues are listed under the **Issues** module in the list view of the Workspace.
-   **[Group issues in the Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/grc-common-functions/issue-grouping-in-workspaces.md)**  
Group issues within your workspaces to organize and manage related issues. Grouping similar issues can streamline your workflow and save time.

**Parent Topic:**[Common Governance, Risk, and Compliance features](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/grc-common-functions/common-grc-features.md)

