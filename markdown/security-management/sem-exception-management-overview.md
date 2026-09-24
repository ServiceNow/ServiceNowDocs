---
title: Exception Management Overview
description: When your organization can't comply with a published finding or security policy, standard, or guideline, you can request an exception. Exception management entails requesting, reviewing, approving, or rejecting exceptions to a finding or remediation task \(RT\) that can’t be remediated.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/sem-exception-management-overview.html
release: brazil
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 4
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


## Exception Rules

Exception Rules allow administrators to define reusable rules that automatically apply exceptions to findings matching specific conditions. Instead of requesting exceptions on individual findings, an exception rule can defer all matching findings within a defined validity period.

An exception rule progresses through the following states:

-   **Draft**: The rule is being created and has not been submitted.
-   **In Review**: The rule has been submitted for approval and is awaiting action.
-   **Approved**: The rule has been approved and is actively applied to matching findings.
-   **Rejected**: The rule has been rejected by an approver.
-   **Expired**: The rule has passed its validity end date.
-   **Marked for deletion**: The rule is queued for removal.

Exception rules support multi-level approval workflows and can apply to multiple finding tables, including Vulnerable Items, Application Vulnerable Items, Container Image Vulnerable Items, and Compliance Results.

## Questionnaire Configuration

The **Questionnaire Configuration** \(sn\_sec\_exception\_questionnaire\_config\) table enables administrators to define conditional questionnaires for different approval rule types. You can associate distinct questionnaires with specific approval rules \(deferral requests, compensating control management, or false positive\) and define conditions to control which questionnaire appears based on the characteristics of the finding or remediation task.

## End-to-end exception flow

The exception lifecycle moves through three role-driven phases. Each phase has a specific actor, a specific input, and a specific output that becomes the next phase's input.

1.  **Request \(Remediation Owner\)** — the remediation owner opens a finding or remediation task in the Security Exposure Management Workspace and selects **Request Exception**, **Mark as False Positive**, **Unassign**, or **Request Extension**. The owner provides a reason, justification, and \(if configured for the matching approval rule\) completes a questionnaire. On submit, the request enters the **In Review** state and an approval record \(VCA\#\) is generated.
2.  **Review \(Approver\)** — the approver assigned by the matching approval rule receives an email notification and an entry in the Unified Approvals View. The approver opens the request, reviews the finding details, the questionnaire response, and the Now Assist recommendation \(if available\), then selects **Approve** or **Reject**. For multi-level approval rules, the request routes to the next configured level only after the current level approves.
3.  **Outcome \(System\)** — on full approval, the finding transitions to **Deferred** \(exception\), **Closed** with reason **False positive** \(false-positive request\), or to the reassigned group \(unassign\). On rejection or expiry, the finding reverts to its previous state. The requester receives an email notification with the outcome.

For questionnaire-driven requests, the request remains in **Draft** until the questionnaire is submitted. After approval or rejection, a resubmission may be allowed depending on the rule's resubmission-context setting.

