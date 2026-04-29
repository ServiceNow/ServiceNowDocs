---
title: Test result and remediation task state transitions in the Security Posture Control application
description: The states on findings \(configuration test records\) and their associated remediation tasks are impacted if you modify your policies in the Security Posture Control application.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configuring and viewing findings, Use the workspace, Security Posture Control, Security Operations]
---

# Test result and remediation task state transitions in the Security Posture Control application

The states on findings \(configuration test records\) and their associated remediation tasks are impacted if you modify your policies in the Security Posture Control application.

## State transition scenarios between test results and remediation tasks

With some exceptions, states generally transition between your findings \(test results\) and their associated remediation tasks in Security Posture Control the same way they transition between test results and remediation tasks in the Configuration Compliance application. However, if you modify your policies in Security Posture Control, your changes impact how states transition on your findings and their associated remediation tasks.

The following tables illustrate how states transition on your findings if you edit and publish a new version \(edit\), deactivate, or delete your policies.

For more information about state changes in Configuration Compliance, see [Test result and remediation task state transitions in the Configuration Compliance application](../../vulnerability-config-compliance/concept/cc-state-transition.md).

**Note:** Starting with v14.9 of Configuration Compliance, the following terms have been renamed:

|Terminology prior to v14.9|Terminology v14.9 onwards|
|--------------------------|-------------------------|
|Test Result Group|Remediation Task|
|Group Rules|Remediation Task Rules|
|Policy|Test group|

Enhancements to policy audits ensure that retired assets are not evaluated by activated policies. If the state of an asset transitions from **Retired** back to **Active**, it is included in the next policy evaluation.

|If a policy is...|Field values on existing finding records for...|Transition to...|
|-----------------|-----------------------------------------------|----------------|
|Deactivated|Result|Retain original values|
| |State|Closed|
| |Resolution|Stale|
| | | |
| | | |

|If a policy is...|Field values on existing finding records for...|Transition to...|
|-----------------|-----------------------------------------------|----------------|
|Edited with the option to close any existing findings selected|Result|Retain original values|
| |State|Closed|
| |Resolution|Result Invalid|

|If a policy is...|Field values on existing finding records for...|Transition to...|
|-----------------|-----------------------------------------------|----------------|
|Edited with the option to retain any existing findings selected|Result|Valid \(Passed\) test cases retain original values and invalid test cases \(Failed\) are closed.|
| |State|Closed|
| |Resolution|Result Invalid|

|If a policy is...|Field values on existing finding records for...|Transition to...|
|-----------------|-----------------------------------------------|----------------|
|Deleted|Results|Retain original values|
| |State|Closed|
| |Resolution|Result Invalid|

