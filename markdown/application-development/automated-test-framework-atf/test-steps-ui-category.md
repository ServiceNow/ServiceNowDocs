---
title: UI category
description: Validate the functionality of the UI actions.Executes a client-side test script entirely in the browser without requiring server-side processing.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/automated-test-framework-atf/test-steps-ui-category.html
release: australia
product: Automated Test Framework \(ATF\)
classification: automated-test-framework-atf
topic_type: reference
last_updated: "2026-06-10"
reading_time_minutes: 1
breadcrumb: [Automated Test Framework \(ATF\) test step categories, Automated Test Framework \(ATF\), Testing and debugging applications, Building applications]
---

# UI category

Validate the functionality of the UI actions.

## Run UI Test Script

Executes a client-side test script entirely in the browser without requiring server-side processing.

<table id="table_od3_dgb_hzb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Execution order

</td><td>

Integer specifying the order in which the test executes this step.As you create steps, the system automatically assigns each step an incremental value. This value causes the test to execute steps in the order that you created them in. You can change this default order by editing the **Execution order** values.

</td></tr><tr><td>

Application

</td><td>

Application scope in which the system runs this step.

</td></tr><tr><td>

Active

</td><td>

Option to activate this test step for use.

</td></tr><tr><td>

Test

</td><td>

Name of the test that you're adding the step to.

</td></tr><tr><td>

Step config

</td><td>

Name of the step.

</td></tr><tr><td>

Notes

</td><td>

Notes about the test step.

</td></tr><tr><td>

Script

</td><td>

Script to be executed by the client test runner. The Run UI Test Script API is called in this test step.

</td></tr></tbody>
</table>