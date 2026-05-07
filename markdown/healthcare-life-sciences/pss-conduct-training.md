---
title: Manage a training task in Workspace
description: Manage the training support for a Patient Support Services program with training tasks and checklists.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Manage enrollment requests, Patient Support Services, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Manage a training task in Workspace

Manage the training support for a Patient Support Services program with training tasks and checklists.

## Before you begin

**Important:**

Starting with the Yokohama release, Patient Support Services is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported.

For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support knowledge base.

You must have access to enrollment cases.

Role required: sn\_patientservice.nurse\_educator

## About this task

A training task is created based on the appointment booking workflow. For more information, see [Appointment booking workflow in Patient Support Services](../concept/pss-appt-booking-feature.md).

## Procedure

1.  Open your Workspace by navigating to **All** &gt; **Patient Support Services** &gt; **Workspace**.

2.  Go to **Lists** &gt; **Conduct training tasks** &gt; **My tasks**.

3.  Click a link to the task you want to update the status for.

    You can work on a training task when the state of the task is **Booked appointment**. In the Patient Support Services application, the training tasks are booked by patients.

4.  In the **State** field, update the status of your task.

    -   Select **Work in progress** when you are still conducting the task.
    -   Select **Completed** when the task is completed.
    -   Select **Canceled** when the task could not be completed.
5.  Save your changes.

    -   When the task is still in progress or canceled, click **Save** on the training page.
    -   When the task is completed, click **Complete** on the training page.

## Result

The status of the task is reflected on the Fulfill services task page of the Program services activity in the playbook. For more information, see [Working on an enrollment case in Workspace](../concept/pss-playbook.md).

