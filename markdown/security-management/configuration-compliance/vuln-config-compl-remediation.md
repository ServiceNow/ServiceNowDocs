---
title: Configuration Compliance remediation
description: Configuration Compliance remediation is primarily a manual process augmented by scheduled jobs \(integrations\), remediation tasks, workflows, and change requests.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/configuration-compliance/vuln-config-compl-remediation.html
release: australia
product: Configuration Compliance
classification: configuration-compliance
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuration Compliance, Unified Security Exposure Management, Security Operations]
---

# Configuration Compliance remediation

Configuration Compliance remediation is primarily a manual process augmented by scheduled jobs \(integrations\), remediation tasks, workflows, and change requests.

**Note:** Starting with v14.9 of Configuration Compliance, the following terms have been renamed:

|Terminology prior to v14.9|Terminology v14.9 onwards|
|--------------------------|-------------------------|
|Test Result Group|Remediation Task|
|Group Rules|Remediation Task Rules|
|Policy|Test group|

\[Omitted image "cc-remediation-overview-image.png"\] Alt text: Remediation workflow overview

Separate third-party SCA plugins acquire and transform data in Configuration Compliance. Before you can use Configuration Compliance to remediate configuration items, you must install a third-party scanner integration and perform at least one network scan.

Use change requests to remediate individual test failures from remediation tasks.

The states of remediation tasks automatically transition as associated change requests move through their life cycles with [State synchronization between change requests and remediation tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/configuration-compliance/cc-cr-state-synch.md). Users with the itil role can create and manage change requests directly from remediation tasks.

**Related topics**  


[Manually create a Configuration Compliance remediation task](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/configuration-compliance/create-test-result-group-module.md)

[Manually create a Configuration Compliance remediation task from the Test Results list](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/configuration-compliance/create-test-result-group-list.md)

[Create a change request in Configuration Compliance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/configuration-compliance/cc-CR-v12-create.md)

[Associate a remediation task to an existing change request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/configuration-compliance/cc-CR-v12-assoc.md)

[Remove assignments from remediation tasks for you or your groups](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/configuration-compliance/cc-unassign-trg.md)

[Automatic closing of test results](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/configuration-compliance/cc-auto-close-common.md)

[Close a remediation task](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/configuration-compliance/close-test-result-group.md)

[Configure approval rules for Exception Management in Configuration Compliance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/configuration-compliance/cc-exception-mgt-approval-rules.md)

