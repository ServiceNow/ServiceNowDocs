---
title: Generate the Vendor Satisfaction Assessment in Vendor Management Workspace
description: Use Assessments and Surveys to assess how satisfied your stakeholders are with the vendors they collaborate with. Generate assessments using the Vendor Satisfaction Assessment metric type that comes with the Vendor Management Workspace application.
locale: en-US
release: zurich
product: Vendor Management Workspace
classification: vendor-management-workspace
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure, Vendor Management Workspace, IT Service Management]
---

# Generate the Vendor Satisfaction Assessment in Vendor Management Workspace

Use Assessments and Surveys to assess how satisfied your stakeholders are with the vendors they collaborate with. Generate assessments using the Vendor Satisfaction Assessment metric type that comes with the Vendor Management Workspace application.

## Before you begin

Role required: assessment\_admin or sn\_vlm.vendor\_manager

## About this task

The **Vendor Satisfaction Assessment** metric type is used to measure the satisfaction of stakeholders who collaborate with your vendors. This metric type uses the **Vendor Satisfaction** metric category to determine the vendor satisfaction score that displays in Vendor Management Workspace. Any new categories that are added to the metric type do not contribute towards the calculation of the vendor satisfaction score.

## Procedure

1.  Navigate to **All** &gt; **Vendor Management** &gt; **Assessment Administration** &gt; **Types**.

2.  Set the desired conditions for the Company \[core\_company\] table.

    1.  Select **Vendor Satisfaction Assessment**.

        For descriptions of the assessment metric type fields, refer to [Configure an assessment](https://www.servicenow.com/docs/access?context=configure-assessment&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).

    2.  Select the **Conditions** tab.

    3.  Add the desired filter conditions for the Company \[core\_company\] table.

    4.  Click **Update**.

3.  Associate users to the metric categories for the assessment.

    1.  In the **Metric Categories** tab, select **Vendor Satisfaction**.

    2.  In the **Users** tab, select **Edit**.

    3.  Add all users you want to associate with vendors to the Users List for Vendor Satisfaction.

    4.  Select **Save**.

4.  Associate users with vendors.

    1.  Navigate to **Vendor Management** &gt; **Assessment Administration** &gt; **Stakeholders**.

    2.  Select the Vendor Satisfaction Assessment metric type.

    3.  Select a user from **Category Users**.

    4.  Select the vendor you want to associate the user with from **Assessable Records**.

    5.  Select **Associate**.

    6.  Associate additional users to vendors.

5.  Verify the association of users to vendors.

    1.  Navigate to **All** &gt; **Assessments** &gt; **Advanced** &gt; **Assessment Stakeholder**.

    2.  Verify the association between the user and the vendor.

        **Note:** The **Category user** field lists all users and the **Assessable record** field display the associated vendors.

6.  Generate the assessment.

    1.  Navigate to **All** &gt; **Vendor Management** &gt; **Assessment Administration** &gt; **Types**.

    2.  In the **Assessment Metric Types** record, select **Vendor Satisfaction Assessment**.

    3.  Select **Generate Assessments**.


**Related topics**  


[Configure an assessment](https://www.servicenow.com/docs/access?context=configure-assessment&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US)

[Survey Management](https://www.servicenow.com/docs/access?context=r_SurveyManagementLandingPage&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US)

[Assessment metrics](https://www.servicenow.com/docs/access?context=c_AssessmentMetrics&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US)

