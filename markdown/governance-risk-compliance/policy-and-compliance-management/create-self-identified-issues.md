---
title: Report self-identified issues via the Service Portal
description: Your employees and business users within your company can self-identify an issue and submit it via the ServiceNow Service Portal. Following submission, a triage issue is automatically created.
locale: en-US
release: zurich
product: Policy and Compliance Management
classification: policy-and-compliance-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Manage issues, Classic UI, Use, Policy and Compliance Management, Governance, Risk, and Compliance]
---

# Report self-identified issues via the Service Portal

Your employees and business users within your company can self-identify an issue and submit it via the ServiceNow® Service Portal. Following submission, a triage issue is automatically created.

## Before you begin

You must download the GRC: Advanced Core application before you can use the Issue Triage featuring within Policy and Compliance Management. For more information, see [Download a GRC application from the ServiceNow Store for the first time](../../grc-common/task/download-grc-first-time.md).

Role required: sn\_compliance.user, sn\_grc.business\_user

## About this task

There are multiple methods you can use to report an issue using the Service Portal. For example, you can click the **Request Something** button on the Service Portal home page, select the **Governance, Risk, and Compliance** category, and then click **Report Issue**. An alternate, and perhaps simpler, method is described here.

## Procedure

1.  Open the Service Portal.

    1.  In your instance URL, type sp after your instance name.

    2.  Press the Return key.

    ![Service Portal](../image/service-portal1.png "Service Portal home page")

2.  In the screen header, navigate to **GRC** &gt; **My Issues** to view issues already assigned to you.

    ![My issues](../image/my-issues.png "My issues")

3.  Click **Report an Issue**.

    ![Report an issue](../image/sp-report-issue.png "Report an issue")

4.  Answer the questions presented.

    Additional questions may appear depending on the answers you provide. For example, if your response to the **What type of issue is this?** field is **Incident or loss event**, additional questions relating to the incident or loss event are presented to you. Or if you select **Non-compliance to a policy** at that field, you are asked for the affected policy and what you consider to be the root cause of the issue.

5.  When you have completed all of the questions, click **Submit**.

    The request is submitted, and an issue triage record is created. This kicks off the [issue triage](triage-issue.md) process.

    **Note:** You can control the options displayed in the Service Portal **GRC** option menu by returning to your instance and navigating to **Policy and Compliance** &gt; **Issue Triage** &gt; **Administration** &gt; **Properties**, and setting the **sn\_grc\_advanced.enable\_my\_issues\_hide\_my\_reported\_issues** property.

    If it is set to **Yes**, the **GRC** &gt; **My Issues** menu option is available, and the **My Reported Issues** option is hidden. You can use the **My Issues** menu option to create risk or compliance issues that must be triaged before being released as actual issues.

    If the property is set to **No**, the **GRC** &gt; **My Reported Issues** menu option is available, and the **My Issues** option is hidden. You can use the **My Reported Issues** menu option to create actual risk or compliance issues directly from the Service Portal.


-   **[Triage a self-identified issue](triage-issue.md)**  
After an issue has been identified and submitted by employees or business users via the Service Portal, the issue triage process begins. The actual problem is identified and assigned to the appropriate owner for prioritization and resolution.

**Parent Topic:**[Manage issues in Policy and Compliance Management](../concept/manage-issues.md)

