---
title: Configuration Compliance Exception Management overview
description: When your organization can't comply with a published vulnerability management or security policy, standard, or guideline, you can request an exception. Exception management entails requesting, reviewing, approving, or rejecting exceptions for a remediation task that cannot be remediated according to the policy.
locale: en-US
release: australia
product: Configuration Compliance
classification: configuration-compliance
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Explore, Configuration Compliance, Unified Security Exposure Management, Security Operations]
---

# Configuration Compliance Exception Management overview

When your organization can't comply with a published vulnerability management or security policy, standard, or guideline, you can request an exception. Exception management entails requesting, reviewing, approving, or rejecting exceptions for a remediation task that cannot be remediated according to the policy.

**Important:** Exception management is supported in the [Vulnerability Manager Workspace](../../vulnerability-response/concept/vr-ws-exceptions-split-VMGR-ws.md) and [IT Remediation Workspace](../../vulnerability-response/task/vr-ws-request-exception.md).

**Note:** Starting with v14.9 of Configuration Compliance, the following terms have been renamed:

|Terminology prior to v14.9|Terminology v14.9 onwards|
|--------------------------|-------------------------|
|Test Result Group|Remediation Task|
|Group Rules|Remediation Task Rules|
|Policy|Test group|

Some vulnerabilities might not have an existing patch, fix, or solution. When an exception is approved, it also means that you're accepting a risk because you're acknowledging and agreeing to the consequences of not remediating the configuration-related vulnerability.

## Life cycle of an exception

An exception is a request to defer the remediation of a remediation task for a specified period.

The life cycle of an exception is as follows:

-   Requesting an exception
-   Approving an exception request
-   Tracking an exception request
-   Expiry of an exception request

**Requesting an exception**

As the remediation owner, you can ask for an exemption for a remediation task using the exception management process. During the approval process, the remediation task remains in **In review** state. After the exception approver approves this request, the remediation task moves to a **Deferred** state.

**Important:** You can request an exception from the IT Remediation Workspace. For more information, see [Request an exception in the IT Remediation Workspace](../../vulnerability-response/task/vr-ws-request-exception.md).

**Approving an exception request**

Remediation tasks that can't be remediated immediately are reviewed, assessed for risk, and approved for deferral until they can be remediated. Approving an exception request can be a two-level workflow. If only the first-level approver is present, the exception can be requested and approved. However, if there's no first-level approver, an exception can't be requested. See [Add an exception approver for Configuration Compliance](../task/cc-ex-request-add-approver.md) for more information.

**Important:** You can approve or reject an exception request from the Vulnerability Manager Workspace. For more information, see [Request exceptions for remediation tasks and records in the Vulnerability Manager Workspace](../../vulnerability-response/concept/vr-ws-exceptions-split-VMGR-ws.md).

**Note:**

Starting from Configuration Compliance v13.0, if you are deploying the CC application for the first time, the flow designer for exception management is enabled by default. If you are already using the workflow, you can update to the flow designer. In both cases, you cannot change it back to workflow.

Once an exception request for a remediation task is approved, you can perform the following actions:

-   Reopen
-   Delete

**Note:** Rejection comments are shown in the Work notes for a remediation task. If an exception request is rejected, this remediation task reverts to its previous state.

**Tracking an exception request**

After raising the exception, you can track its status by using the **State Change Approvals** tab of the remediation task. If an action is taken on a remediation task, you can't track the status of the individual test results in that remediation task.

**Expiry of an exception request**

When an exception request for a remediation task expires, the remediation task reverts to its **Open** state.

![Exception management life cycle for CC](../image/cc-exception-management-lifecycle.png "Exception management approval process prior to CC v13.0")

**Related topics**  


[Configure Exception Management for Security Exposure Management](../../security-exposure-management-administration/task/sem-configure-exp-mngmt-vr.md)

[Specify the duration of an exception requested for a remediation task](../../security-exposure-management-administration/task/sem-ex-req-sysprop.md)

