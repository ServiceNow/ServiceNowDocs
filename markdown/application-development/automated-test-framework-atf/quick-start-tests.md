---
title: Quick start tests
description: Copy and customize quick start tests provided by the ServiceNow AI Platform to validate that your instance works after you make any configuration changes. For example, if you apply an upgrade or develop an application.
locale: en-US
release: zurich
product: Automated Test Framework \(ATF\)
classification: automated-test-framework-atf
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Test types and techniques, Automated Test Framework \(ATF\), Testing and debugging applications, Building applications]
---

# Quick start tests

Copy and customize quick start tests provided by the ServiceNow AI Platform® to validate that your instance works after you make any configuration changes. For example, if you apply an upgrade or develop an application.

The tests can only produce a pass result when you run them with the default demo data that's provided with the application or feature plugin.

**Note:** If your QST fails, it can be that the test doesn’t match your instance customizations. Use the **Notes** field for each test step to update the test to pass with your data. If you have customized the business process associated with a test, revise the test to match your customizations.

To apply a quick start test to your instance-specific data, copy the quick start test and add your custom data.

**Note:** You can copy either an individual quick start test or the entire quick start tests suite.

See [Getting started with quick start tests](https://www.youtube.com/watch?v=wV0SjY5gq8M) for more information.

## Activation

Each application or feature has its own plugin activation requirements for enabling quick start tests. See [Available quick start tests by application or feature](../reference/available-quick-start-tests.md) for activation information.

## Managing copies

When you copy a test, Automated Test Framework populates the **Copied from** field with the name of the copied test. When an upgrade changes, a quick start test Automated Test Framework notifies test designers about the change in a notification on the test form. Test designers can revert the copied test to the upgraded version with the **Revert Copy to Base System** UI action.

**Tip:** If a QST is updated, the previously copied versions of the QST does not have the recent changes. Review the old copies using **Copies to Review** for all the tests that have an associated warning message.

-   **[Available quick start tests by application or feature](../reference/available-quick-start-tests.md)**  
Validate that your instance still works after you make any configuration change such as apply an upgrade or develop an application. Copy and customize the ServiceNow -provided quick start tests to pass when using your instance-specific data.

**Parent Topic:**[Automated Test Framework \(ATF\) test types and techniques](atf-test-type-testing.md)

**Related topics**  


[Reusable tests](atf-reuse-tests.md)

[Mutually exclusive tests](mutual-exclusion-rule.md)

[Parallel testing](parallel-testing.md)

[Accelerate ATF tests failure resolution](../task/atf-test-triage.md)

[Performance profiling](atf-perf-prof.md#)

