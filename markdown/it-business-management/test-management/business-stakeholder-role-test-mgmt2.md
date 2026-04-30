---
title: Business stakeholder role for Test Management 2.0
description: Use the business stakeholder role to read and retrieve data from any table of the Test Management 2.0 applications to generate reports.
locale: en-US
release: yokohama
product: Test Management
classification: test-management
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Test Management 2.0, Test Management applications, Strategic Portfolio Management]
---

# Business stakeholder role for Test Management 2.0

Use the business stakeholder role to read and retrieve data from any table of the Test Management 2.0 applications to generate reports.

When you activate the Business Stakeholder plugin \(com.snc.business\_stakeholder\) in your ServiceNow instance, the Read only roles for Test Management 2.0 plugin \(com.snc.tm2\_read\_roles\) is also activated. This plugin provides a business stakeholder role \(sn\_tm2\_read\) with which you can access all the tables of Test Management 2.0 application. This role also allows read-only access to the Test Management dashboard. You can assign this role to any user in your organization who is a business stakeholder.

## Plugin availability

If you are a new customer, the Read only roles for Test Management 2.0 plugin \(com.snc.tm2\_read\_roles\) is activated on zBoot. However, the business stakeholder role \(sn\_tm2\_read\) is available only when you activate the Test Management 2.0 plugin \(com.snc.test\_management.2.0\).

If you are an upgrade customer, you must manually activate the Read only roles for Test Management 2.0 plugin \(com.snc.tm2\_read\_roles\).

## Test Management 2.0 tables accessible by users with the business stakeholder role

When the read-only roles for Test Management 2.0 plugin \(com.snc.tm2\_read\_roles\) and Test Management 2.0 plugin \(com.snc.test\_management.2.0\) are active in your ServiceNow instance, the user with the business stakeholder role \(sn\_tm2\_read\) has read access to the following tables.

<table id="table_dqt_pnp_kc00"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Task Test\[sn\_test\_management\_m2m\_task\_test\]

</td><td>

Associates tests to multiple scrum tasks.

</td></tr><tr><td>

Test Set Test\[sn\_test\_management\_m2m\_test\_set\_test\]

</td><td>

Associates tests to multiple test sets.

</td></tr><tr><td>

Planned Test Task\[sn\_test\_management\_planned\_task\]

</td><td>

Extends the Planned Task table.

</td></tr><tr><td>

Steps\[sn\_test\_management\_step\]

</td><td>

Stores details of test steps.

</td></tr><tr><td>

Step Result\[sn\_test\_management\_step\_result\]

</td><td>

Stores details of step results.

</td></tr><tr><td>

Test\[sn\_test\_management\_test\]

</td><td>

Stores details of tests.

</td></tr><tr><td>

Test Execution Assignment\[sn\_test\_management\_test\_assignment\]

</td><td>

Stores the linking of tests to testers.

</td></tr><tr><td>

Test Cycle\[sn\_test\_management\_test\_cycle\]

</td><td>

Stores details of test cycles.

</td></tr><tr><td>

Test Environment\[sn\_test\_management\_test\_environment\]

</td><td>

Stores details of test environments.

</td></tr><tr><td>

Test Execution Suite\[sn\_test\_management\_test\_execution\_suite\]

</td><td>

Stores details of test execution suites.

</td></tr><tr><td>

Test Plan\[sn\_test\_management\_test\_plan\]

</td><td>

Stores details of test plans.

</td></tr><tr><td>

Test Result\[sn\_test\_management\_test\_result\]

</td><td>

Stores details of test results.

</td></tr><tr><td>

Test Run\[sn\_test\_management\_test\_run\]

</td><td>

Stores details of test runs.

</td></tr><tr><td>

Test Set\[sn\_test\_management\_test\_set\]

</td><td>

Stores details of test sets.

</td></tr><tr><td>

Test Version\[sn\_test\_management\_test\_version\]

</td><td>

Stores details of test versions.

</td></tr></tbody>
</table>