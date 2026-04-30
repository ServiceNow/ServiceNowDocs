---
title: Reusable Tests category
description: Create reusable test components that can be incorporated into various other tests \(regular or reusable test\), minimizing redundant test code and enhancing test maintainability.
locale: en-US
release: zurich
product: Automated Test Framework \(ATF\)
classification: automated-test-framework-atf
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Test step categories, Automated Test Framework \(ATF\), Testing and debugging applications, Building applications]
---

# Reusable Tests category

Create reusable test components that can be incorporated into various other tests \(regular or reusable test\), minimizing redundant test code and enhancing test maintainability.

The Reusable Tests test step category contains all the reusable tests created on the instance by default. When you add a test step, select **Add Test Step**. You can now invoke the reusable tests you have created through the Reusable Tests test step category.

**Note:** By default, the reusable tests show up in this category. If you have customized a reusable test for another category, it shows up under the selected test step category.

<table id="table_od3_dgb_hzb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Execution order

</td><td>

Integer specifying the order in which the test executes this step.As you create steps, the system automatically assigns each step an incremental value. This value causes the test to execute steps in the order that you created them in. You can change this default order by editing the **Execution order** values.

</td></tr><tr><td>

Active

</td><td>

Option to activate this test step for use.

</td></tr><tr><td>

Application

</td><td>

Read-only application scope in which the system runs this step.

</td></tr><tr><td>

Test

</td><td>

Read-only name of the test that you're adding the step to. The test can be a regular or reusable test.

</td></tr><tr><td>

Timeout

</td><td>

Amount of time to wait for the step to pass.

</td></tr><tr><td>

Reusable Test

</td><td>

Read-only name of the reusable test that you're adding.

</td></tr><tr><td>

Notes

</td><td>

Description of the test step.

</td></tr></tbody>
</table>See [Reusable tests](../concept/atf-reuse-tests.md) for more details.

