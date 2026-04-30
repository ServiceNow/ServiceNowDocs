---
title: Requesting and approving an exception for a remediation task
description: You can request to defer the remediation of a remediation task for a specified period. Users who are a part of the approver group can approve exception requests.
locale: en-US
release: xanadu
product: Configuration Compliance
classification: configuration-compliance
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Configuration Compliance remediation, Configuration Compliance, Unified Security Exposure Management, Security Operations]
---

# Requesting and approving an exception for a remediation task

You can request to defer the remediation of a remediation task for a specified period. Users who are a part of the approver group can approve exception requests.

**Note:** Starting with v14.9 of Configuration Compliance, the following terms have been renamed:

|Terminology prior to v14.9|Terminology v14.9 onwards|
|--------------------------|-------------------------|
|Test Result Group|Remediation Task|
|Group Rules|Remediation Task Rules|
|Policy|Test group|

To request or approve exception requests, see:

-   [Request an exception for a remediation task in Configuration Compliance](../task/cc-ex-request-test-result-group.md)
-   [Approve an exception request in Configuration Compliance](../task/cc-ex-request-approve.md)

**Note:**

Email notifications are sent at every stage of exception management, providing the status and other details of a request. For example, when an exception is requested, the requester receives an email confirming that the request is raised. The approver also receives an email stating that an exception has been requested.

Starting from v14.11 of Configuration Compliance, you can configure the time frames for approving exceptions, along with email notifications for both the approver and requester after a set number of days. When a request is raised, the test result changes to In-Review status and a state change record is created. If the approver doesn't respond within the configured time frame, the test result reverts to Open status. The previous state is stored in the **backup\_state** field. For more information, see [Configure approval rules for Exception Management](../../vulnerability-response/task/exception-mgt-approval-rules.md).

-   **[Request an exception for a remediation task in Configuration Compliance](../task/cc-ex-request-test-result-group.md)**  
Request an exception to defer the remediation of a remediation task for a specified period if it can’t be remediated immediately.
-   **[Request an extension for an exception rule in Configuration Compliance](../task/extend-cc-ex-rule-request.md)**  
Request an extension for a deferred exception rule before it reaches its deferred until due date. As a remediation owner, you’re no longer required to wait until the deferred due date to make this request.
-   **[Request an exception for remediation tasks using GRC: Policy and Compliance Management](../task/integrate-with-grc-cc.md)**  
Request policy exceptions using the GRC policy exception management capability in the Policy and Compliance Management application from within Configuration Compliance.
-   **[Approve an exception request in Configuration Compliance](../task/cc-ex-request-approve.md)**  
Approve exception requests for remediation tasks that can't be remediated immediately. You must assess these requests for risk and then approve them for deferral until they can be remediated.
-   **[Define policy reason mappings](../task/define-policy-reason-mappings.md)**  
You can define the reason choices to be available to any user who requests an exception.

**Parent Topic:**[Configuration Compliance remediation](vuln-config-compl-remediation.md)

