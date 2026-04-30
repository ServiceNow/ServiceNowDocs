---
title: Set up the feedback definition
description: Configure the feedback definition to curate the finer details of each feedback type.
locale: en-US
release: xanadu
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Integrated experience and service feedback, Setup continuous improvement features, Configure, Employee Center, Employee Service Management]
---

# Set up the feedback definition

Configure the feedback definition to curate the finer details of each feedback type.

## Before you begin

Role required: sn\_hr\_sp.esc\_admin

## About this task

Feedback definition provides you with the liberty to select how and at what point and mode do you want to gather your feedback data from your users. You can:

-   Select the questions to ask.
-   Select the kind of question, whether static or survey.
-   Select the mode of the feedback request, whether it's a drawer widget or In page, and so on.

## Procedure

1.  Navigate to **All** &gt; **Employee Center** &gt; **Experience and Service Feedback** &gt; **Feedback Definitions**.

2.  Select **New** to create a feedback definition for a portal page.

3.  On the feedback definition form, fill in the fields.

    For a description of the field values, see [Feedback definition form](../reference/fdbck-dfnition-record.md).

4.  Save your modifications.

    -   To save your changes and stay on the form, select **Save**.
    -   To save your changes and return to the Feedback Definitions \[sn\_ex\_sp\_pro\_feedback\_definition\] table, select **Submit**.
    -   **Note:** The following feedback definitions are active on installation of Employee Center Pro version 32.0.

        -   **Experience feedback**
        -   **Experience feedback for Kiosk**
        -   **Experience feedback for Virtual Agent**
        -   **Experience feedback for mobile**
    -   You only see **Experience feedback for Kiosk** when you have the Employee Center Pro Kiosk plugin \(sn\_ex\_sp\_pro\_kiosk\) installed.
    -   The following feedback definitions are active on installation of Employee Center Pro plugin \(sn\_ex\_sp\_pro\) version 35.0.
        -   **Star rating for experience**
        -   **Experience feedback for Kiosk**
        -   **Experience feedback for Virtual Agent**
        -   **Experience feedback for mobile**
    -   If you're originally deploying the experience feedback functionality or the Employee Center Pro plugin \(sn\_ex\_sp\_pro\) itself with version 35.0, the **Star rating for experience** definition is active by default. The **Experience feedback** definition is inactive.
    -   If you're an existing user of the **Experience feedback** definition, the **Star rating for experience** definition is inactive by default. You can enable the former in Employee Center Pro plugin \(sn\_ex\_sp\_pro\) version 35.0.
    -   If you have the Browser Extension for Employee Center plugin \(sn\_ex\_brw\_ext\) version 1.0 along with the Employee Center Pro plugin \(sn\_ex\_sp\_pro\) version 36.0, you have **Experience Feedback for Browser Extension** definition by default. The following are some key differentiators from the generic experience feedback definitions.
        -   The **Star - 5 point scale** is active with the feedback definition by default. You can change it to any other form of experience feedback according to your organizational requirement.
        -   The **Page selection** only has **ecbe\_pro\_home** option for the **Included pages** field.
        -   The **Widget mode** field has **Inline** option for the experience feedback for the browser extension. For more information on the field values, see [Feedback definition form](../reference/fdbck-dfnition-record.md).
5.  Trigger Conditions \[asmt\_condition\] table is visible only for the feedback type Service - workflow once the definition is saved.

6.  Select **New**.

7.  On the trigger condition form, fill in the fields.

    For the description of the field values, see [Trigger Condition form for surveys](https://www.servicenow.com/docs/access?context=trigger-condition-form&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).

    **Note:**

    -   Access the experience feedback widget in the topic pages, the Service Catalog items, and in the My Requests page available by default.
    -   Add the widget manually in any other page.
    -   Create only one feedback definition for a portal at a time.
    -   Create unique survey feedback for each feedback definition.
    -   Change the default reset timer of the feedback definition trigger condition from 30 days to your required period.

## What to do next

-   Use the feedback widgets across the Employee Center portal. For more information, see [Use the integrated service and experience feedback](../concept/using-ex-fdback.md).
-   Check the responses received on the experience feedback dashboard. For more information, see [Feedback Analytics dashboard](../concept/ex-fdback-board.md).
-   Customize the appearances of the experience flow and the workflow feedback widgets. For more information, see [Integrated service and experience feedback management](../concept/ex-fdbck-manage.md).

