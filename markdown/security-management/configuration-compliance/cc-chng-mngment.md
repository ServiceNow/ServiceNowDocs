---
title: Configuration Compliance change management
description: As an IT remediation owner, you can create and manage change requests \(CHG\) directly from remediation tasks \(RTs\) in the Configuration Compliance application.
locale: en-US
release: yokohama
product: Configuration Compliance
classification: configuration-compliance
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Explore, Configuration Compliance, Unified Security Exposure Management, Security Operations]
---

# Configuration Compliance change management

As an IT remediation owner, you can create and manage change requests \(CHG\) directly from remediation tasks \(RTs\) in the Configuration Compliance application.

**Note:** Starting with v14.9 of Configuration Compliance, the following terms have been renamed:

|Terminology prior to v14.9|Terminology v14.9 onwards|
|--------------------------|-------------------------|
|Test Result Group|Remediation Task|
|Group Rules|Remediation Task Rules|
|Policy|Test group|

## Change requests and the Configuration Compliance workflow

Change requests and change management are part of the remediation process of the Configuration Compliance workflow. During this remediation phase, you might use change requests to help you prioritize, track, and remediate test results.

The Configuration Compliance application works with the ServiceNow AI Platform® IT change management process to help you remediate non-compliant software and technologies in your environment.

With change management in the Configuration Compliance application, you can associate test results to existing change requests, or split a remediation task and create a new remediation task only for selected test results.

For more information, see [Create a change request in Configuration Compliance](../task/cc-CR-v12-create.md).

## Key terms

-   **Tests**

    Tests are libraries of data records that organize scans of computing assets. Configuration tests define how a class of technology assets should be governed. A test is anything that can be used to identify a class of software or a hardware asset that is out of compliance.

-   **Test results**

    Test results are imported by third-party integrations. Once they are viewable in Configuration Compliance, they are remediated using **Remediation Tasks**. Groups are assigned for remediation according to assignment rules.

    **Note:** Starting with version 14.9 of Configuration Compliance, test result is labelled, Finding.

-   **Remediation task**

    Test results are grouped into remediation tasks according to assignment rules and automatically assigned to remediation owners for remediation.

    **Note:** Starting with version 14.9 of Configuration Compliance, test result is labeled Remediation Task.

-   **Test groups**

    Test groups are related to authoritative documents and test records. A group of configuration tests define Test groups.

-   **Change requests**

    Change requests help you implement controlled processes for remediation. You might use change requests with remediation tasks in Configuration Compliance to help you identify, track, and resolve non-compliant assets \(configuration items\) that require additional resources, or that you might target for deferral.


For more information about test results and remediation tasks, see [Configuration Compliance remediation tasks and remediation task rules overview](cc-groups.md).

## When to use change requests in Configuration Compliance

Change requests help you initiate and track remediation activities on your test results. When remediation owners have large numbers of unremediated test results or configuration items, they might use change requests to identify test results for deferral. Alternatively, they might identify and regroup test results and configuration items that require more resources than initially identified in the original remediation task.

-   **Create change requests from a remediation task**

    Create a change request directly from a remediation task for all the test results in the remediation task, or use filtering to identify only test results that match specific criteria. Create a change request with pre-populated information to expedite your investigation for test results that require manual intervention.

-   **Split a remediation task**

    From an existing remediation task, identify a subset of test results that you want to move to a new remediation task. By creating a new TRG, you can work with a specific group of test results without impacting the original remediation task.

-   **Associate test results to an existing change request**

    Associate test results to existing tasks to avoid creating duplicate change requests as you work to resolve your remediation tasks. By associating a remediation task to a change request that is already available in your instance, you can use an existing lists of tasks.


## Types of change requests for a remediation task

You can create, approve, implement, review, and close change requests directly from remediation tasks that are assigned to you. You can create three types of change requests with pre-populated information from a remediation task:

-   Standard. A pre-authorized change that is low risk, relatively common and follows a specified procedure or work instruction.
-   Normal. Normal change requests follow a prescriptive process which requires two levels of approval before being implemented, reviewed, and closed.
-   Emergency. A change to resolve a major incident.

