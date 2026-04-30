---
title: Create case task using Threat Analyst Workbench
description: Create case tasks to associate with case\(s\).
locale: en-US
release: xanadu
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Threat Analyst Workbench, Use, Threat Intelligence Security Center, Security Operations]
---

# Create case task using Threat Analyst Workbench

Create case tasks to associate with case\(s\).

## Before you begin

Role required: sn\_sec\_tisc.analyst, sn\_sec\_tisc.admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Threat Intelligence Security Center**.

2.  Click **Threat Analyst Workbench** icon.

3.  Go to **Case Task Management** &gt; **All Cases Tasks**.

    All the case tasks are displayed.

4.  Click **New**.

5.  Fill in the fields as appropriate.

    |Field|Description|
    |-----|-----------|
    |Task ID|A unique identifier for the case task. This is system generated ID.|
    |Short Description|Summary of the request or issue that is being investigated or a short description.|
    |Description|A detailed description including any relevant information about the case task such as background, what analysis is required, outcomes expected.|
    |Parent Case ID|Select the parent case ID from the lookup.|
    |Priority|An assessment of the severity of the request or issue.|
    |Assignment group|The assigned group responsible for working on the case task.|
    |Status|The current status of the case task.|
    |Assigned to|The Analyst who is responsible for working on a case task.|
    |Due Date|The date and time that the case task is due to be completed or closed.|
    |TLP|Unique value that indicates the Data sensitivity setting per TLP.|
    |Enforce Restriction|As an sn\_sec\_tisc\_admin, select this check box to modify members of allowed group and allowed members. For more information, see [Enforced Restrictions for case\(s\)](tisc-enforced-restrictions.md).|

6.  Fill in the fields on the Insights section, as appropriate.

    |Field|Description|
    |-----|-----------|
    |Notes|Any additional notes related to the threat investigation.|
    |Closure|Add the closure summary of the findings.|

7.  Click **Save**.

    Your case task will be associated with your case.

    **Note:** After saving the case task, you can add tags and taxonomies to the task. For more information, see [Creating Taxonomies](../concept/create-taxonomies.md).


**Parent Topic:**[Threat Analyst Workbench](../concept/threat-analyst-workbench.md)

**Related topics**  


[Workbench Overview](../concept/workbench-overview.md)

[Creating cases using Threat Analyst Workbench](../concept/create-cases-using-threat-analyst-workbench.md)

[Working with Investigation Canvases](../concept/tisc-investigation-canvases.md)

[Add artifacts to case\(s\) or case task\(s\)](add-artifacts-to-a-case-s.md)

[Run Enrichment Actions within a case](run-enrichment-results.md)

[View Case Reports](view-case-reports.md)

[Create a security incident from a TISC case](tisc-create-si-case.md)

[Upload Secure File Attachments](secure-file-attachments.md)

