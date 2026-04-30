---
title: Set up a safety audit schedule
description: Create an audit schedule and define the top-level audit details and the recurrence, for example, monthly or bi-monthly.
locale: en-US
release: xanadu
product: Health and Safety Risk Management
classification: health-and-safety-risk-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Safety inspections and audits, Use, Health and Safety Risk Management, Health and Safety, Employee Service Management]
---

# Set up a safety audit schedule

Create an audit schedule and define the top-level audit details and the recurrence, for example, monthly or bi-monthly.

## Before you begin

Role required: sn\_hs\_rm.safety\_audit\_manager or sn\_hs\_rm.audit\_schedule\_writer

## Procedure

1.  Navigate to **All** &gt; **Health and Safety** &gt; **Health and Safety Workspace**.

2.  Select the risk management icon \(![Risk assessment icon](../image/icon-risk-assessment.png)\).

3.  Select **Audit schedules** list and then **All**.

4.  Select **New** to create an audit schedule.

5.  On the form, fill in the fields.

    Define the audit scope, finalize the goals, and choose regulations for the audit so that the audit process is well structured and organized. For more information on audit field descriptions, see [Audit schedule form](../reference/hs-audit-schedule-form.md).

6.  Select **Save**.

    -   The **Audit surveys** and **Scheduled audits** tabs appear for this audit.
    -   An information message that prompts to create an audit survey appears.
7.  In the **Audit surveys** tab, select **New** to add surveys to be added to each scheduled audit.

    Surveys can also be added to each scheduled audit individually after they’re scheduled.

8.  In the **Scheduled audits** tab, add the following details to each scheduled audit record.

    -   People involved and their responsibilities
    -   Standards and documents used to benchmark findings
    -   Audit actions
    -   Risk assessments
    For more information on completing an audit record, see, [Create and manage a safety audit](hs-create-manage-safety-audit-workspace.md).

9.  Alternatively, select **Create Audits** in the audit schedule record to create an audit record.

    If an audit survey has not been created, an informational message is displayed on the modal, with a prompt to create one before proceeding with scheduling audits. This message is not shown if an audit survey already exists for the audit schedule record. In the modal,

    -   Select **Create next scheduled audit** to create the first upcoming audit.
    -   Select **Create all scheduled audits at once** to create all scheduled audits immediately.

## Result

-   Based on the duration and the selected frequency of the audit schedule, audit records are created one by one on the start date.

    **Note:**

    Audit records are created using the **Automate audit schedule** flow available with the application. To generate the audits instantly rather than on scheduled days, your administrator can adjust the job in this flow.

    The flows are built using ServiceNow Workflow Studio, so make sure you’re familiar with the [Flow Designer](https://www.servicenow.com/docs/access?context=flow-designer-home-landing-page&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US) basics.

-   All audit records for an audit schedule are generated in its **Scheduled audits** tab. These audit records are also available under **Audits** &gt; **All**.
-   All required fields are copied from the audit schedule to its audit records.
-   The assigned user receives a notification about the audit survey. They can complete the audit in the Employee Center or on Now Mobile app.
-   The safety agent can also create actions for the survey responses. For more information, see [Add an action from survey response in safety inspection through Employee center](add-action-from-survey-response-in-safety-inspection.md)

**Parent Topic:**[Safety inspections and audits](../concept/hs-safety-inspections.md)

