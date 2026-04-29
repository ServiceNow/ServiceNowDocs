---
title: Generate assessment procedure plans for a test plan
description: Use the test plan that is automatically generated for a control, which is in an assess state, to view and determine if the control is assessed in accordance with the assessment procedure plan.
locale: en-US
release: australia
product: Continuous Risk Monitoring
classification: continuous-risk-monitoring
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Implementing controls and assessment objectives in CAM, Using CAM, Continuous Authorization and Monitoring, Governance, Risk, and Compliance]
---

# Generate assessment procedure plans for a test plan

Use the test plan that is automatically generated for a control, which is in an assess state, to view and determine if the control is assessed in accordance with the assessment procedure plan.

## Before you begin

Role required: sn\_irm\_cont\_auth.system\_owner, sn\_irm\_cont\_auth.info\_system\_sec\_officer, sn\_irm\_cont\_auth.authorization\_official, sn\_irm\_cont\_auth.info\_system\_sec\_manager, sn\_irm\_cont\_auth.admin

## About this task

Assessment procedure plans are generated for the test plan of a control based on the control objective. Each control objective has a particular test template, and assessment procedure templates are created for this test template. Test plans are generated from the test template of a control objective. Assessment procedure plans are generated from the assessment procedure template.

## Procedure

1.  Navigate to **All** &gt; **Continuous Authorization &amp; Monitoring** &gt; **All Controls**.

2.  Select the control that has been assessed for which the test plans are created.

3.  Select the Test plans related list and select the test plan link in the **Number** column.

    In the Test plan form that opens, you can view the test plan details such as the name of the test template from which this test plan is generated and the name of the control that is to be assessed based on this test plan.

    The base system includes test templates for NIST 800-53 revision 5 controls. Test plans are automatically created from these test templates. Whenever the authorization package moves from the Implement state to the Assess state, the control tests are created from the test plans that are generated from the test templates.

    The Control test section includes **Operational assessment procedures**, **Examine**, **Interview**, and **Test** field descriptions. The Examine, Interview, and Test descriptions are drawn from the NIST guideline and are added to the Test template form. You can update the field descriptions in the Test plan form.

    ![Control test tab of test plan showing the NIST guideline descriptions.](../image/cam-test-plans-control-test-tab.png "Control test tab of test plan")

4.  To update the descriptions, select the field, update the text, and then select **Update**.

5.  To revert to the original control test descriptions in the associated test template, select **Revert to Template**.

6.  Select **OK** in the Confirmation popup to confirm your decision.

7.  To open the Assessment procedure plan and view the assessment objective, select the link in the **Identifier** column of the Assessment procedure plans section.

    In the Assessment procedure plan form, you can view the identifier of the assessment procedure plan, the name of the test plan, and the assessment objective. An assessment objective is the guideline as to how to assess the control. If necessary, update the objective.

    ![Assessment procedure plans to test a control.](../image/cam-test-plans.png "Assessment procedure plans")

8.  To view the control tests that are generated to assess the control, navigate to the Controls tests related list of the Engagement form.

    See [RMF steps 4, 5, and 6 - Assess, authorize, and monitor](assess-control-effectiveness.md).


