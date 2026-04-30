---
title: Pass values from one automated test step to another
description: Assign a form field the value of an output variable returned from a previous step.
locale: en-US
release: zurich
product: Automated Test Framework \(ATF\)
classification: automated-test-framework-atf
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Passing data from one automated test step to another, Building and running automated tests with the Automated Test Framework, Test building and execution, Automated Test Framework \(ATF\), Testing and debugging applications, Building applications]
---

# Pass values from one automated test step to another

Assign a form field the value of an output variable returned from a previous step.

## Before you begin

You must have a previous test step that returns an appropriate output variable.

Role required: admin, atf\_test\_admin and atf\_test\_designer

## Procedure

1.  To the right of the field whose value you want to assign, click the input value icon \( ![Input value icon](../image/rem-value-icon.png)\)

    The input value mapping control lists previous steps that create an output variable. If no previous steps create an output variable, the control displays the message: There are no elements to show.

2.  Click the row for the step that contains the output variable you want to use as an input.

3.  Click the output variable you want to use.

    If the output variable is an id for a glide record, the control displays a tree picker providing access to fields for this record.

4.  Navigate through the tree picker hierarchy until you find and select the value you want.


**Parent Topic:**[Passing data from one automated test step to another](../concept/atf-passing-data.md)

**Related topics**  


[Automated Test Framework use case: reference a value from a previous step](atf-use-backref.md)

