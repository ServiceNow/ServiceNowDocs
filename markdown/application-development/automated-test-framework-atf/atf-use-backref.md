---
title: Automated Test Framework use case: reference a value from a previous step
description: This use case illustrates assigning a form field the value of an output variable from a previous step.
locale: en-US
release: australia
product: Automated Test Framework \(ATF\)
classification: automated-test-framework-atf
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Automated Test Framework use case examples, Automated Test Framework \(ATF\) reference, Automated Test Framework \(ATF\), Testing and debugging applications, Building applications]
---

# Automated Test Framework use case: reference a value from a previous step

This use case illustrates assigning a form field the value of an output variable from a previous step.

## Before you begin

Role required: atf\_test\_admin

## About this task

Automated Test Framework: In this example, the second step references an output value from the first step. Pass values from one step to another example.

![Pass values from one step to another example](../image/atf-use-backref-02.png)

## Procedure

1.  Insert a record into the incident table.

    This example inserts a record into the Incident table.

    ![Record insert](../image/atf-use-backref-01.png "Step 1 - Record Insert")

2.  Open the record just inserted by assigning to the **Record** field the output variable from Step 1.

    ![Open an existing record test step](../image/atf-use-backref-form.png "Step 2 - Specify the record")

3.  Validate that fields on the open record have the values you expect.

    ![Field values validation test step](../image/atf-use-backref-03.png "Step 3 - Field Values Validation")


**Parent Topic:**[Automated Test Framework use case examples](../concept/atf-use-cases.md)

**Related topics**  


[Pass values from one automated test step to another](atf-retrieve-value.md)

