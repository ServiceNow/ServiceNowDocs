---
title: Creating cases using Threat Analyst Workbench
description: Cases are used to track information about a campaign or threat actor threatening your organization. After a case is created, you can add artifacts that allow you to review and analyze all related information from a single case or case task.
locale: en-US
release: australia
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Threat Analyst Workbench, Use, Threat Intelligence Security Center, Security Operations]
---

# Creating cases using Threat Analyst Workbench

Cases are used to track information about a campaign or threat actor threatening your organization. After a case is created, you can add artifacts that allow you to review and analyze all related information from a single case or case task.

## Before you begin

Role required: sn\_sec\_tisc.analyst, sn\_sec\_tisc.admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Threat Intelligence Security Center**.

2.  Click **Threat Analyst Workbench** icon.

3.  Go to **Case Management** &gt; **All Cases**.

    All the cases are displayed.

4.  Click **New**.

5.  Fill in the fields as appropriate.

<table id="table_mjl_lzv_pzb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Case ID

</td><td>

A unique identifier for the case. This is system generated ID.

</td></tr><tr><td>

Short Description

</td><td>

Summary of the request or issue that is being investigated or a short description.

</td></tr><tr><td>

Description

</td><td>

A detailed description including any relevant information about the case such as background, what analysis is required, outcomes expected.

</td></tr><tr><td>

Case Type

</td><td>

Select the type of case being investigated. The possible options for the investigation are:-   Threat Hunting
-   Request for Information
-   Vulnerability Management Case
-   Compliance Case
-   Incident Response Case
-   Collaboration Case
-   Others


</td></tr><tr><td>

Priority

</td><td>

An assessment of the severity of the request or issue.

</td></tr><tr><td>

Assignment group

</td><td>

The assigned group responsible for working on the case.

</td></tr><tr><td>

Status

</td><td>

The current status of the case.

</td></tr><tr><td>

Assigned to

</td><td>

The Analyst who is responsible for working on a case.

</td></tr><tr><td>

Due Date

</td><td>

The date and time that the task is due to be completed or closed.

</td></tr><tr><td>

Contributors

</td><td>

The list of assignees rolled up from tasks and should be possible to add on top of it.

</td></tr><tr><td>

TLP

</td><td>

Unique value that indicates the Data sensitivity setting per TLP.

</td></tr><tr><td>

Watch list

</td><td>

When a user is added to the watchlist, the person will receive email notifications on changes to status and priority.

</td></tr><tr><td>

Enforce Restriction

</td><td>

Select this check box to modify members of allowed group and allowed members. For more information, see [Enforced Restrictions for case\(s\)](../task/tisc-enforced-restrictions.md).

</td></tr></tbody>
</table>6.  Fill in the fields on the Insights section, as appropriate.

    |Field|Description|
    |-----|-----------|
    |Notes|Any additional notes related to the threat investigation.|
    |Recommendations or Actions|Any recommendations or actions related to the threat investigation.|
    |Analysis and Findings|Enter the analysis and findings related to the threat investigation.|
    |Closure Summary|Add the closure summary of the findings.|

7.  Click **Save**.

    After the record has been saved, you can click the **Import Intelligence** tab to import the threat intelligence data using the **Import Intelligence** feature.

    **Note:** If you are importing and processing data from Case Management, then a unique is associated to the import record.

    ![Import intelligence-Case Management](../image/tisc-import-intelligence-case-management.png)


-   **[Enforced Restrictions for case\(s\)](../task/tisc-enforced-restrictions.md)**  
Use this feature to restrict a case and provide list of groups and users who can access it.
-   **[Associate MITRE Techniques to a Case](../task/tisc-associate-mitre-technique.md)**  
Associate one or more MITRE technique to a case.
-   **[Roll up of MITRE technique associations](../task/tisc-mitre-roll-up.md)**  
Roll up of MITRE technique associations from observables, indicators, objects, and security incidents which are linked or unlinked from a case record.

**Parent Topic:**[Threat Analyst Workbench](threat-analyst-workbench.md)

**Related topics**  


[Workbench Overview](workbench-overview.md)

[Creating case task using Threat Analyst Workbench](../task/tisc-create-case-task.md)

[Working with Investigation Canvas](tisc-investigation-canvases.md)

[Add artifacts to case\(s\) or case task\(s\)](../task/add-artifacts-to-a-case-s.md)

[Run Enrichment Actions within a case](../task/run-enrichment-results.md)

[View Case Reports](../task/view-case-reports.md)

[Create a security incident from a TISC case](../task/tisc-create-si-case.md)

[Upload Secure File Attachments](../task/secure-file-attachments.md)

