---
title: Automated Test Framework use case: test a business rule
description: This use case illustrates testing a business rule with the Automated Test Framework.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/automated-test-framework-atf/atf-biz-rule-use.html
release: australia
product: Automated Test Framework \(ATF\)
classification: automated-test-framework-atf
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Automated Test Framework use case examples, Automated Test Framework \(ATF\) reference, Automated Test Framework \(ATF\), Testing and debugging applications, Building applications]
---

# Automated Test Framework use case: test a business rule

This use case illustrates testing a business rule with the Automated Test Framework.

## Before you begin

Role required: atf\_test\_admin

## About this task

This example tests a business rule that sets the value of **Locked out** to **true** when **active** is set to **false**.

\[Omitted image "atf-biz-rule-use-small.png"\] Alt text: Test steps

## Procedure

1.  Impersonate a user with the necessary permissions.

    In this example, the step impersonates the admin user.

    \[Omitted image "atf-use-biz-rule-01.png"\] Alt text: Form for Impersonate

2.  Open a form for the table to which this business rule applies.

    This example opens a new User form.

    \[Omitted image "atf-use-biz-rule-02.png"\] Alt text: Form for Open a New Form

3.  Set values on the form that meet the requirements for submitting the form and for triggering the business rule.

    This example sets values for the **Active**, **Last name**, and **First name** fields.

    \[Omitted image "atf-use-biz-rule-03.png"\] Alt text: Form for Set Field Values

4.  Submit the form.

    \[Omitted image "atf-use-biz-rule-04.png"\] Alt text: Form for Submit Form

5.  Validate that the business rule ran.

    In this example the business rule tested sets **Locked out** to **true** if **Active** is set to **false**.

    \[Omitted image "atf-use-biz-rule-05.png"\] Alt text: Form for Field Values Validation


**Parent Topic:**[Automated Test Framework use case examples](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/automated-test-framework-atf/atf-use-cases.md)

