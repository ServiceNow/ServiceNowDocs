---
title: Exception Management Overview
description: When your organization can't comply with a published finding or security policy, standard, or guideline, you can request an exception. Exception management entails requesting, reviewing, approving, or rejecting exceptions to a finding or remediation task \(RT\) that can’t be remediated.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-08-01"
reading_time_minutes: 3
breadcrumb: [Use, Unified Security Exposure Management, Security Operations]
---

# Exception Management Overview

When your organization can't comply with a published finding or security policy, standard, or guideline, you can request an exception. Exception management entails requesting, reviewing, approving, or rejecting exceptions to a finding or remediation task \(RT\) that can’t be remediated.

Some findings might not have an existing patch, fix, or solution. When an exception is approved, it also means that you're accepting a risk because you're acknowledging and agreeing to the consequences of not remediating the finding.

Exception Management provides administrators the ability to handle, configure, and review exception cases within the Security Exposure Management Administration Console. You can navigate to Exception Management from the **Workspaces** &gt; **Security Exposure Management Workspace** &gt; **Administration** &gt; **Exception Management**.

In the Exception Management landing page, you can view the exception management configurations for all the four apps- Vulnerability response, Configuration compliance, Application Vulnerability Response, and Container Vulnerability Response. You can create a new questionnaire or to design your own questionnaire using the templates available in the smart assessment workspace to help review the exception requests for the Vulnerability Manager, Business Unit Head, or Service Owners.

You can personalize the columns and rows with the help of the setting icon on the right.

## The Life-cycle of an exception

-   **Definition of an exception**

    An exception is a request to defer the remediation of a finding or remediation task for a specified period. For example, as a remediation owner, you can request an exception if a patch isn’t available for a machine.

-   **Requesting an exception**

    As the remediation owner, you can ask for an exemption for a finding or remediation task using the exception management process. After the exception approver approves this request, the finding or remediation task moves to a **Deferred** state.

-   **Approving an exception request**

    Findings or remediation tasks that can't be remediated immediately are reviewed by a vulnerability manager or business analyst, assessed for risk, and approved for deferral until they can be remediated. Approval rules for Exception Management are determined based on the configured approvers and approver levels. Once the required approvals are obtained, the request state transitions according to the type of request. If defined, Exception requests can follow a multi-level approval workflow. If no approver is configured for a specific request type, the request can’t be submitted. Approvals are typically carried out by the Vulnerability Manager or by Business Users who have been assigned the appropriate Approver role.


-   **Tracking an exception request**

    After raising the exception, you can track its status by using the **Change Approvals** tab of the finding or remediation task. If an action is taken on a remediation task, you can't track the status of the individual findings in that remediation task.

-   **Expiry of an exception request**

    When an exception request for a particular finding or remediation task expires, the impacted finding or remediation task reverts to its **Open** state.


-   **[Approver roles required for Security Exposure Management Workspace](sem-approve-or-reject-request.md)**  
You can see the required roles for the approvers in the Security Exposure Management Workspace.
-   **[Questionnaire support in Exception Management via Smart Assessment](sem-smart-assessment-exp-management.md)**  
Configure advanced questionnaires as part of the exception management process using Smart Assessment. This enables Remediation Owners to provide more detailed context for Exception Requests and enables Approvers to configure conditional questions to gather information for informed decision making.
-   **[Defer a Remediation task](../task/sem-defer-rem-task.md)**  
If you identify a finding or remediation task for which a fix is not yet available and can be safely deferred without additional analysis, you can use the **Request Exception** feature.
-   **[Request an extension for a deferred remediation task](../task/sem-extend-defer-rem.md)**  
As a remediation owner, you’re no longer required to wait until the deferred due date to make this request. Request an extension for a deferred remediation task before it reaches its deferred until due date.
-   **[Request a false positive for a vulnerable item or remediate task](../task/sem-falsepst-reqst.md)**  
Indicate a false positive request for a finding or a remediation task in the Security Exposure Management Workspace. A false positive is a condition where a scanner incorrectly reports that a finding exists in the system due to situations such as an incorrect classification, improper logic, or an algorithm in the scanner.

**Parent Topic:**[Using Unified Security Exposure Management](../../security-exposure-management-workspace/concept/using-unified-security-exposure-management.md)

