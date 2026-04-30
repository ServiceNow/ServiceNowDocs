---
title: Create or edit an indicator to assess an application - Legacy
description: Application indicators are business metrics that assess the applications across dimensions such as cost, quality, technical risk, investments, user satisfaction, and business value.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Use - Legacy, Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Create or edit an indicator to assess an application - Legacy

Application indicators are business metrics that assess the applications across dimensions such as cost, quality, technical risk, investments, user satisfaction, and business value.

## Before you begin

**Important:**

Starting with the Xanadu release, the application indicators module is moved to the Enterprise Architecture Workspace. To learn more, see [Manage indicators](../concept/eaw-concept/eaw-configure-indicators.md).

Role required: sn\_apm.apm\_admin

## About this task

Each indicator periodically captures related application data which is used to calculate the application score. The assessment of applications is done on an extensible framework, which is based on the various configured indicators. If you require indicators other than the preconfigured ones to calculate the application score, then you can create an indicator based on your business requirements.

## Procedure

1.  Navigate to **All** &gt; **Enterprise Architecture** &gt; **Administration** &gt; **Application Indicators**.

2.  Click **New** or click an existing application indicator to edit.

3.  On the form, fill in the fields.

    For field information, see [Indicator form](../reference/indicator-form.md).

4.  Click **Submit**.

5.  To regenerate the indicator score of an application, click open an indicator.

    1.  Click the **Regenerate indicator score** option in the context menu.

        The action deletes the existing scores and generates new scores instead of just updating the existing scores for that indicator. This indicator may be attached to one or more scoring profiles, and therefore recalculates the scores of all business applications that are associated to this scoring profile.

    2.  Select the Fiscal Period in the Regenerate application indicator scores dialog box.

    3.  Click **OK**.

    4.  Click **Update**.

6.  To create a dependent indicator, click open the indicator.

    If you had selected Indicators in the **Data source** field, then when you open that indicator record, the Indicator Dependencies related list is displayed.

    **Note:** An indicator which has its data source as indicator cannot be added as a dependent child indicator.

    1.  Click **New** in the Indicator Dependencies related list.

        The parent indicator auto-populates in the Parent Indicator field.

    2.  Select a dependent indicator in the **Child Indicator** field.

    3.  Click **Submit**.

7.  To assess the business application, click **Generate Assessments**.


## What to do next

Use the [preconfigured indicators](../reference/preconfigured-indicators-and-sources.md) to assess the applications based on cost, quality, and risk.

-   **[Generate survey assessments and view the results within Enterprise Architecture - Legacy](generate-survey-assessments-results-apm.md)**  
Within Enterprise Architecture you can assign an assessment questionnaire to a user who uses a business application and get the feedback about the application.

**Parent Topic:**[Using Enterprise Architecture \(formerly Application Portfolio Management\) - Legacy](../concept/using-apm.md)

