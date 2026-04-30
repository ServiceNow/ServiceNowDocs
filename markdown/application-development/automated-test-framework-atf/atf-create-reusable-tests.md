---
title: Create a reusable test
description: Create a reusable test to avoid redundancy, ensuring better test maintenance and reliable test execution across the instance.
locale: en-US
release: zurich
product: Automated Test Framework \(ATF\)
classification: automated-test-framework-atf
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Reusable tests, Test types and techniques, Automated Test Framework \(ATF\), Testing and debugging applications, Building applications]
---

# Create a reusable test

Create a reusable test to avoid redundancy, ensuring better test maintenance and reliable test execution across the instance.

## Before you begin

Role required: atf\_test\_admin or atf\_test\_designer

## Procedure

1.  Navigate to **All** &gt; **Automated Test Framework \(ATF\)** &gt; **Reusable Tests**.

    A list of reusable tests created on the instance shows up.

2.  Select **New** to create a new reusable test.

    ![Screenshots showing the reusable test form](../image/atf-reusable-test-form.png)

    The Reusable Test form shows up.

3.  On the form, fill in the fields.

    The read-only fields are filled up automatically.

<table id="table_d5m_h11_2dc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the reusable test.

</td></tr><tr><td>

Application

</td><td>

Read-only field with the scope of the test.

</td></tr><tr><td>

Active

</td><td>

Option to define the test as active or not.

</td></tr><tr><td>

Category

</td><td>

The test step category in which the test shows up. ![Screenshot showing the reusable test step category](../image/atf-reusable-test-step-category.png)

**Note:** If you leave this field empty, the test shows up under the Reusable Tests test category by default.

</td></tr><tr><td>

Description

</td><td>

Description of the reusable test.**Note:** The description of the reusable test is displayed in the step creator modal.

![Screenshot showing the reusable test description](../image/atf-reusable-test-description.png)

See [Reusable Tests category](../reference/test-steps-reusable-tests-category.md) for more information.

</td></tr></tbody>
</table>4.  Select **Save** to create the reusable test.

    The reusable test shows up.

    **Note:** Reusable tests can’t run independently. They can run only when it becomes a part of another test. They also can’t be added to a test suite independently. They must be invoked in another test within a test suite.


**Parent Topic:**[Reusable tests](../concept/atf-reuse-tests.md)

