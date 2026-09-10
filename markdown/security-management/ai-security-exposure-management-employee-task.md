---
title: Resolve tasks for AI assets in Employee Center
description: Resolve the finding or request an exception from Employee Center AI posture findings.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/ai-security-exposure-management-employee-task.html
release: australia
topic_type: task
last_updated: "2026-09-03"
reading_time_minutes: 2
keywords: [AI posture finding, AI Security Exposure Management, Employee Center, assignment rule, exception request]
breadcrumb: [Using Employee Center AI asset remediation, AI Security Exposure Management, Use, Unified Security Exposure Management, Security Operations]
---

# Resolve tasks for AI assets in Employee Center

Resolve the finding or request an exception from Employee Center AI posture findings.

## Before you begin

The AI Security Exposure Management application and at least one AI posture-finding integration must be activated. Employee Center must be deployed in the instance.

Only the Zenity AI exposure integration is currently supported for import of AI posture findings.

Roles required: sn\_vul.vulnerability\_admin, sn\_sec\_ai.vulnerability\_admin, admin

## Procedure

1.  To configure the workflow, navigate to the USEM workspace and select the administration module \(gear icon\).

2.  Select the **Advanced settings** card.

    This card is visible only if you have the sn\_vul.vulnerability\_admin, sn\_sec\_ai.vulnerability\_admin, or admin role.

3.  In the left navigation, select **AI Security Exposure Management**.

4.  Activate AI exposure tasks by configuring the following properties.

    -   **sn\_sec\_ai.create\_employee\_tasks\_ai\_posture** - Toggle that enables the creation of employee tasks for AI posture findings.
    -   **sn\_sec\_ai.employee\_task\_filter\_ai\_posture** - Filter that is evaluated against incoming posture findings.
    Only the Zenity AI exposure integration is currently supported for import of AI posture findings.

5.  Verify that AI posture findings are processed correctly.

    When an AI posture finding is imported, the finding is checked against the filter in the **sn\_sec\_ai.employee\_task\_filter\_ai\_posture** property.

    If the finding is determined to be eligible, the owner metadata is retrieved from the Discovered AI Asset. If the imported owner metadata can be correlated with a sys\_user record, for example, the emails align, an AI exposure task is created and assigned to the correlated sys\_user.

    **Note:**

    If you want to further limit which posture findings are eligible, you can update the sn\_sec\_ai.employee\_task\_filter\_ai\_posture system property. However, the admin role is required to update system properties.

6.  As a user, navigate to Employee Center to review your assigned AI exposure tasks.

7.  Select **My Tasks**.

8.  Open the task associated with the posture finding.

9.  Review the issue summary, the affected agent, tool, or prompt, the severity, the source tool, and the recommended remediation steps.

10. Take action on the task by resolving the finding or requesting an exception.

    -   To fix the issue yourself, correct the configuration in the source platform, such as Microsoft Copilot Studio, then select **Resolve** on the task.
    -   To request an exception instead, select **Request exception**, enter a justification in the **Justification** field, then submit the request.

## Result

Selecting **Resolve** sets the finding to Resolved. Selecting **Request exception** creates an exception request on the finding and routes it through the existing USEM exception approval workflow. The employee can see the request status reflected on the task.

## What to do next

The finding moves through the following states based on the task outcome and the next integration run with the source AI security tool.

|Current state|Trigger|Resulting state|
|-------------|-------|---------------|
|Open|The owner opens the assigned task in Employee Center.|In progress|
|In progress|The owner selects **Resolve**.|Resolved|
|In progress|The owner requests an exception, and the request is approved.|Deferred|
|In progress|The owner requests an exception, and the request is rejected.|Open \(the task remains actionable\)|
|Resolved|The next integration run confirms the finding is no longer present.|Closed|
|Resolved|The next integration run finds the issue still present.|Open \(the task reopens and the owner is notified\)|

**Parent Topic:**[Using AI remediation workflows with Employee Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/ai-security-exposure-employee-workflow.md)

