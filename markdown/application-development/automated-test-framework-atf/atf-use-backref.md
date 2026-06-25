---
title: Automated Test Framework use case: reference a value from a previous step
description: This use case illustrates assigning a form field the value of an output variable from a previous step.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/automated-test-framework-atf/atf-use-backref.html
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

\[Omitted image "atf-use-backref-02.png"\] Alt text: Pass values from one step to another example

## Procedure

1.  Insert a record into the incident table.

    This example inserts a record into the Incident table.

    \[Omitted image "atf-use-backref-01.png"\] Alt text: Record insert

2.  Open the record just inserted by assigning to the **Record** field the output variable from Step 1.

    \[Omitted image "atf-use-backref-form.png"\] Alt text: Open an existing record test step

3.  Validate that fields on the open record have the values you expect.

    \[Omitted image "atf-use-backref-03.png"\] Alt text: Field values validation test step


**Parent Topic:**[Automated Test Framework use case examples](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/automated-test-framework-atf/atf-use-cases.md)

**Related topics**  


[Pass values from one automated test step to another](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/automated-test-framework-atf/atf-retrieve-value.md)

