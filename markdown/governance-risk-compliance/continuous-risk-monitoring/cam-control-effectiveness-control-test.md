---
title: Determine control effectiveness of a control test
description: Apply the objective effectiveness of the assessment procedures and the operating effectiveness of the control test to determine the control effectiveness of the control test. An assessment procedure is applied to check the control test at a granular level.
locale: en-US
release: zurich
product: Continuous Risk Monitoring
classification: continuous-risk-monitoring
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Implement, Use, Continuous Authorization and Monitoring, Governance, Risk, and Compliance]
---

# Determine control effectiveness of a control test

Apply the objective effectiveness of the assessment procedures and the operating effectiveness of the control test to determine the control effectiveness of the control test. An assessment procedure is applied to check the control test at a granular level.

## Before you begin

Role required: sn\_irm\_cont\_auth.system\_owner, sn\_irm\_cont\_auth.info\_system\_sec\_officer, sn\_irm\_cont\_auth.authorization\_official, sn\_irm\_cont\_auth.info\_system\_sec\_manager, sn\_irm\_cont\_auth.admin

## Procedure

1.  Navigate to **All** &gt; **Continuous Authorization &amp; Monitoring** &gt; **All Engagements**.

2.  Select the engagement.

3.  Select the **Control tests** tab and select a control test link in the **Number** column.

4.  In the Control test form that opens, you can view the effectiveness of the control in the **Control effectiveness** field.

5.  Select the **Operational test** tab to view the operating effectiveness of the control test.

    **Note:** The **Examine**, **Interview**, and **Test** fields are pre-populated from the NIST control objectives, and aren’t editable at the control test level. If you must edit any of these descriptions, you can do so in the test plan form. See [Generate assessment procedure plans for a test plan](cam-assess-controls-assess-obj.md).

6.  Select the Assessment procedures related list to view the objective effectiveness of all the assessment procedures.

    The number of assessment procedures generated is exactly equal to the number of assessment procedure plans that were generated from the test plan.

    ![Control effectiveness of a control test taking the operating effectiveness, and the objective effectiveness of all assessment objectives into effect.](../image/cam-control-effectiveness.png "Control effectiveness of a control test")



    The values of the operating effectiveness of a control test are:

    -   None
    -   Ineffective
    -   Effective
    The values of the objective effectiveness of an assessment objective are:

    -   None: Indicates that the assessment procedure hasn’t been analyzed or assessed yet.
    -   Effective
    -   Ineffective
    -   Not Applicable: Indicates that the assessment procedure isn’t valid or not required for this control test check.
    The Control effectiveness of the control test is determined by:

    |Operating effectiveness|Objective effectiveness|Control effectiveness|
    |-----------------------|-----------------------|---------------------|
    |Effective/Ineffective/None|Any one is Ineffective|Ineffective|
    |Effective|Not applicable/None/Effective|Effective|
    |Ineffective|Not applicable/None/Effective/Ineffective|Ineffective|
    |Ineffective|Ineffective|Ineffective|
    |None/Effective|Effective|Effective|
    |None|One is Effective and another Ineffective|Ineffective|
    |None|One is None and another is Not applicable|None|

    As long as the control test is in the Open or Work in Progress state, it does not matter if the objective effectiveness of the Assessment procedures is None. However, you cannot move the control test to the Review state until you mark every assessment objective as either Effective, Ineffective, or Not Applicable. An error message pops up to indicate that you must check the assessment objective and move it out of the None state, so as to move the control test to the Review or Closed Complete state.

7.  Select the link in the Identifier column of the Assessment procedures related list to view the Assessment procedure form.

    All fields in the form are read only except the **Objective effectiveness** field, which you can edit if the control test is either in Open or Work in Progress state. The **Objective effectiveness** field is read only in the Review state, or in any closed states such as Closed Complete, Closed Incomplete, and Closed Skipped.

8.  If you update the objective effectiveness value of the assessment procedure, select **Update** to save your changes.


