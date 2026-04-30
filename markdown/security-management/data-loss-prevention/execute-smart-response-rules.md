---
title: Execute Smart Response Rules
description: Use this feature to execute Smart Response Rules for the Symantec DLP incidents.
locale: en-US
release: zurich
product: Data Loss Prevention
classification: data-loss-prevention
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Symantec Integration for Data Loss Prevention Incident Response, Integrate, Data Loss Prevention Incident Response, Security Operations]
---

# Execute Smart Response Rules

Use this feature to execute Smart Response Rules for the Symantec DLP incidents.

## Before you begin

You need to configure the Smart Response Rules by following procedure explained here in this section, [Configure Smart Response Rules](config-smart-response-rules.md).

Role required: sn\_dlir.admin

**Note:**

The response options on the workspace will be available for the end user or analyst or manager based on the configuration mentioned in the section [Configure response option for your DLP incidents](../../data-loss-prevention/task/configure-response-option-mapping.md).

## Procedure

1.  Navigate to **All** &gt; **DLP** &gt; **DLP User Workspace**.

2.  Open any Symantec DLP incident.

3.  Click **Respond**.

4.  Select the response option from the Response drop down list.

    The response options will be visible based on the configuration of the **Incident Response Option Rule** and **Response Option Mappings**.

5.  Click **Submit**.

    **Note:** You can also configure the approval rule\(s\) for the Response Options by following the procedure explained in the [Create Approval Rules](../../data-loss-prevention/task/configure-approval-rules.md) section. When an approval rule is configured for the Smart Response Rule, the approval flow will be triggered first and after receiving all the approvals, the Smart Response Option flow will be triggered. The state of the DLP Incident will be updated as per the target state of the Response Option mapping after successful run of response option.


**Parent Topic:**[Symantec Integration for Data Loss Prevention Incident Response](../concept/symantec-dlp-integration.md)

