---
title: Automated Test Framework use case: test a data policy
description: This use case illustrates testing a data policy with the Automated Test Framework.
locale: en-US
release: yokohama
product: Automated Test Framework \(ATF\)
classification: automated-test-framework-atf
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Automated Test Framework use case examples, Automated Test Framework \(ATF\) reference, Automated Test Framework \(ATF\), Testing and debugging applications, Building applications]
---

# Automated Test Framework use case: test a data policy

This use case illustrates testing a data policy with the Automated Test Framework.

## Before you begin

Role required: atf\_test\_admin

## About this task

This example tests the data policy that sets the field **Assignment Group** to **mandatory** if **impact** is **high**.

![Data Policy Rules form for the data policy record being tested.](../image/atf-use-data-policy-02.png "Automated Test Framework: Data policy being tested")

![Test steps for data policy example.](../image/atf-data-policy-01-steps.png "Automated Test Framework: Data policy example")

## Procedure

1.  Impersonate a user with the necessary permissions.

    In this example, the step impersonates an admin user.

    ![Impersonate test step for data policy example.](../image/atf-use-data-policy-03.png "Step 1 - Impersonate")

2.  Open a form for the table to which this data policy applies.

    This example opens a new incident form.

    ![Test Step form for the Open a New Form test step.](../image/atf-use-data-policy-04.png "Step 2 - Open a New Form")

3.  Check that the data policy has not yet been triggered.

    In this example, the step checks to confirm that **Assignment group** is not **mandatory**.

    ![Test Step form for the Field State Validation test step.](../image/atf-use-data-policy-05.png "Step 3 - Field State Validation")

4.  If applicable, set the conditions that trigger the data policy.

    This example sets **Impact** to **High**.

    ![Test Step form for the Set Field Values test step.](../image/atf-use-data-policy-06.png "Step 4 - Set Field Values")

5.  Validate that the data policy is enforced.

    In this example, the test confirms that the data policy set **Assignment group** to **High** after the previous step set **Impact** to **High**.

    ![Test Step form for Field State Validation.](../image/atf-use-data-policy-07.png "Step 5 - Field State Validation")


**Parent Topic:**[Automated Test Framework use case examples](../concept/atf-use-cases.md)

