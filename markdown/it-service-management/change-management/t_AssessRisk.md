---
title: Perform risk assessment
description: You can perform risk assessment of existing change requests after the risk assessment criteria are defined. After assessing the risk, you can view the risk assessment responses in the change request.
locale: en-US
release: xanadu
product: Change Management
classification: change-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Risk assessment, Analyze change request risk and impact rating, Reference section for Change Management, Change Management, IT Service Management]
---

# Perform risk assessment

You can perform risk assessment of existing change requests after the risk assessment criteria are defined. After assessing the risk, you can view the risk assessment responses in the change request.

## Before you begin

Role required: itil, sn\_change\_write, or admin

## About this task

Verify that the **Risk Assessment** related list is configured on the Change Request form. If it is not configured, an administrator can add the **Task Assessment** &gt; **Task** related list.

The **Risk Assessment** related link is available only when the change request meets the risk assessment condition and risk assessment category condition, the change request type is **Normal** or **Emergency**, and the **State** is **New**, **Assess**, or **Authorized**. On clicking the **Risk Assessment** related link, the Change Risk Assessment form appears if you have not assessed the risk for this change request before. When you submit the form, these three things appear at the top of the change request form:

-   **Risk assessment evaluated**: The estimation of risk after it is assessed against the Change Risk Assessment form and the criteria set for assessment for the change request.
-   **Risk Condition applied**: The result of the risk calculated against pre-defined risk conditions.
-   **Risk set to**: The final weight of risk based on risk assessment and risk calculation.

    **Note:** If you have filled the Change Risk Assessment form earlier but clicked **Risk Assessment** related list again, a pop-up window appears informing that you have already completed the risk assessment for the change request and confirms whether you want to edit the existing risk assessment. Click **Yes** to fill the Change Risk Assessment form again. Click **No** to use the existing risk assessment to calculate risk.


## Procedure

1.  Open a change request.

2.  Click the **Risk Assessment** related link.

3.  Answer the questions and click **Submit**.

    After submitting the risk assessment, click the **Risk Calculation** related link to calculate the risk. The result of risk assessment, risk calculation, and the value that appears in the **Risk** field of the change request form appears.

    ![risk calculation results](../image/RSKASS4.png "Risk calculation results")

    Users with survey\_admin or survey\_reader role can navigate to **Legacy Surveys** &gt; **Survey Responses** and filter by **Instance**. Survey instances are individual assessments distinguished by the date and time when they are taken.


**Parent Topic:**[Risk assessment](../concept/c_RskAsmtCalc.md)

**Related topics**  


[Define risk assessments](t_DefineARiskAssessment.md)

[Risk assessment](../concept/c_RskAsmtCalc.md)

