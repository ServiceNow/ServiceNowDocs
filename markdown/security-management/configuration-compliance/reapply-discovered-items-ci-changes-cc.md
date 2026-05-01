---
title: CI changes for discovered items for Configuration Compliance
description: The default value of the property sn\_sec\_cmn.update\_on\_ci\_change is true. So, when the configuration item \(CI\) for a discovered item is updated, the test results are updated as well.
locale: en-US
release: zurich
product: Configuration Compliance
classification: configuration-compliance
topic_type: concept
last_updated: "2026-05-01"
reading_time_minutes: 1
breadcrumb: [Discovery Items, Data Import, Explore, Configuration Compliance, Unified Security Exposure Management, Security Operations]
---

# CI changes for discovered items for Configuration Compliance

The default value of the property `sn_sec_cmn.update_on_ci_change` is `true`. So, when the configuration item \(CI\) for a discovered item is updated, the test results are updated as well.

**Note:** Starting with v14.9 of Configuration Compliance, the following terms have been renamed:

|Terminology prior to v14.9|Terminology v14.9 onwards|
|--------------------------|-------------------------|
|Test Result Group|Remediation Task|
|Group Rules|Remediation Task Rules|
|Policy|Test group|

The external ID for the test result is updated and the risk score, assignment rules, remediation task rules, remediation target rule are reevaluated. If a test result exists with the same test and CI, the test results are updated with the existing test result and the current test result is closed with the substate `invalidCI`. Work notes are added accordingly.

If you do not want to update the CI for the existing test result, set the property to false. In this case, if a CI changes, a new test result is created and the existing one is closed as an `invalidCI`.

