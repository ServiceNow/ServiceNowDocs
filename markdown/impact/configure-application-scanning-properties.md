---
title: Configure application scanning properties
description: The Scan Engine provides options to configure application scanning and enhance governance over Team Dev push approval. Configure which applications are scanned, the parameters applications must have to satisfy Team Dev approval, and whether developers can use Suite Scans for faster, focused validation.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/impact/configure-application-scanning-properties.html
release: australia
topic_type: task
last_updated: "2026-08-17"
reading_time_minutes: 2
keywords: [application scanning, Team Dev, Suite Scan, scan engine, push approval]
breadcrumb: [Configure Scan Engine parameters, Activate Scan Engine and review settings, Run Impact Guided Setup, Configuring Impact, Impact]
---

# Configure application scanning properties

The Scan Engine provides options to configure application scanning and enhance governance over Team Dev push approval. Configure which applications are scanned, the parameters applications must have to satisfy Team Dev approval, and whether developers can use Suite Scans for faster, focused validation.

## Before you begin

Applications are scanned in Team Dev workflows during the following scenarios:

-   On-demand scan before push approval
-   Team Dev review process with automatic scanning
-   Application validation for governance rules

Role required: scan\_engine\_admin

## About this task

Set filter conditions that align with your Team Dev governance requirements. Different applications may require different criteria based on their risk profile and deployment targets.

## Procedure

1.  Navigate to **ALL** &gt; **Impact** &gt; **Configuration** &gt; **Scan Engine Properties**.

2.  Select the **Dev Team** tab.

3.  In the **Table for application scanning condition** field, verify the table reference.

    This field specifies which table the scan condition builder references. By default, this is the Custom Applications \[x\_snc\_sys\_app\_app\] table and is typically not changed.

4.  Configure the application scanning condition using the condition builder.

    The Scan Engine uses these defined conditions to determine which applications to include in scans. By default, conditions are set to filter out system applications and include only active, custom applications.

    You can add and configure additional filter conditions by selecting **Add filter condition**. You can also add and configure OR clauses by selecting **Add OR clause**.

    **Tip:** You can append filter conditions and OR clauses to existing conditions by selecting the AND or OR options next to them.

5.  Select the **Enable Team Dev push approval enforcement** check box to require applications to meet approval conditions before push.

    When enabled, applications must meet the conditions specified in the **Conditions for Team Dev push approval** field.

    **Warning:** Team Dev reviewers may be blocked from approving pushes until scanning validation is satisfied.

6.  Configure the conditions for Team Dev push approval using the condition builder.

    Typical criteria include:

    -   Finding severity limits
    -   Restricted module rules
    -   Definition suite alignment
    -   Custom governance conditions
7.  Configure additional application scanning options.

<table><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Enforce completion criteria for application scans

</td><td>

-   When selected, applications must meet the conditions specified in the **Conditions for completing application scans** field.
-   Distinct from Team Dev push approval enforcement.
-   Allows different completion criteria from approval criteria for flexible governance.


</td></tr><tr><td>

Conditions for completing application scans

</td><td>

-   Conditions used to determine if an application scan is complete or resolved for internal tracking.
-   Typically used to mark an application as scanned and passed for compliance or tracking purposes.
-   Separate from Team Dev approval.


</td></tr><tr><td>

Allow Suite Scan for applications

</td><td>

-   Suite Scan runs only selected definitions for faster validation.
-   Full Scan runs all active definitions for comprehensive validation.
-   When selected, developers can choose between Full scan and Suite scan.
-   When cleared, only Full scans are available.
-   Enable for faster, focused validation. Clear for comprehensive validation.


</td></tr></tbody>
</table>8.  Select **Save**.


**Parent Topic:**[Configure Scan Engine parameters](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/configure-scan-engine-properties.md)

**Related topics**  


[Customize Scan Engine definition suites](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/create-scan-engine-definition-suites.md)

[Initiate application scans](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/initiating-on-demand-scans-scan-engine.md)

[Configure update set scanning properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/update-set-scanning-properties2.md)

