---
title: Create feedback template using survey designer
description: As an admin, you can create feedback templates using survey designer that managers can use to collect specific feedback.
locale: en-US
release: australia
product: Talent Feedback
classification: talent-feedback
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Using Employee feedback collection AI agent, Using Talent Feedback, Talent Feedback, Growth Experiences, HR Service Delivery, Employee Service Management]
---

# Create feedback template using survey designer

As an admin, you can create feedback templates using survey designer that managers can use to collect specific feedback.

## Before you begin

Role required: admin

-   Ensure Scope/Application of the Survey Template is **Talent feedback \(sn\_tf\)**
-   Ensure the Active field on the Survey Template \(**asmt\_metric\_type\) is true**
-   Ensure Publish State on the Survey Template is **Published**
-   Ensure ALL metrics \(questions in the survey\) have datatype: **scale, numericscale, or string ONLY**

## Procedure

1.  Navigate to **All** &gt; **Survey** &gt; **View Surveys**.

2.  Open a survey definition in Survey Designer.

3.  Select the **Configuration** tab.

4.  On the Survey Designer Configuration form, fill in the fields.

    For a description of the field values, see [Survey Designer Configuration form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/survey-design-config-form.md).

    **Note:**

    -   The default value of a survey's duration field is 14 days. For a feedback template, it should be modified to 0 days.
    -   A survey instance is created for every feedback request sent using a feedback template, and every instance has a Due Date field. This due date field is overwritten by the due date given by the manager in the agent flow during feedback request creation.
    -   The description of the survey is shown to the managers in the agent flow during the template selection step.
5.  Select the **Availability** tab and complete the form.


