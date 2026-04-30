---
title: Automate reviews of vaccine responses
description: Configure Vaccination Status to automatically approve reviews using the results of vaccine validations.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Automating vaccine response reviews, Vaccination Status, Safe Workplace, Health and Safety, Employee Service Management]
---

# Automate reviews of vaccine responses

Configure Vaccination Status to automatically approve reviews using the results of vaccine validations.

## Before you begin

You must integrate with a third-party validator service and enable Vaccination Status to be able to automatically validate vaccine responses.

For more information, see [Validate vaccine responses automatically](validate-vaccine-responses-automatically.md).

Role required: admin

## About this task

This process automates the entire review process so that validator engine can set a vaccine response to **Approved** or **Not yet reviewed** \(needs a manual review\). These results are based on the validation of vaccine responses. If you want only to validate vaccine responses and their attachments, you can choose to continue doing manual reviews in the approval portal. For more information, see [Validate vaccine responses automatically](validate-vaccine-responses-automatically.md).

## Procedure

1.  Navigate to **All** &gt; **Vaccination Status** &gt; **Properties**.

2.  Locate the **Allow validation engine approvals to update Vaccine Review Outcome records** property and select **Yes**.

3.  Click **Save**.


## Result

Automated vaccine response reviews are enabled for your organization. The validator engine will automatically determine whether a vaccine response is approved or needs a manual review based on information from the attachment type.

**Parent Topic:**[Automating vaccine response reviews](../concept/vaccination-status-vaccine-validation.md)

