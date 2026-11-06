---
title: Perform risk assessment
description: Perform a risk assessment on an existing change request after the risk assessment criteria are defined, and view the responses on the change request.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-service-management/change-management/t\_AssessRisk.html
release: australia
product: Change Management
classification: change-management
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Risk assessment, Analyze change request risk and impact, Reference, Change Management, IT Service Management]
---

# Perform risk assessment

Perform a risk assessment on an existing change request after the risk assessment criteria are defined, and view the responses on the change request.

## Before you begin

Role required: itil, sn\_change\_write, or admin

## About this task

Verify that the **Risk Assessment** related list is configured on the Change Request form. If it is not configured, an administrator can add the **Task Assessment** &gt; **Task** related list.

The **Risk Assessment** related link is available only when the change request meets the risk assessment condition and risk assessment category condition, the change request type is **Normal** or **Emergency**, and the **State** is **New**, **Assess**, or **Authorized**. When you select the **Risk Assessment** related link, the Change Risk Assessment form appears if you have not assessed the risk for this change request before. When you submit the form, the following fields appear at the top of the change request form:

-   **Risk assessment evaluated**: The estimation of risk after it is assessed against the Change Risk Assessment form and the criteria set for assessment for the change request.
-   **Risk Condition applied**: The result of the risk calculated against predefined risk conditions.
-   **Risk set to**: The final weight of risk based on risk assessment and risk calculation.

    **Note:** If you already completed the Change Risk Assessment form and select the **Risk Assessment** related link again, a dialog box asks whether you want to edit the existing risk assessment. Select **Yes** to complete the form again, or select **No** to use the existing risk assessment to calculate risk.


## Procedure

1.  Open a change request.

2.  Select the **Risk Assessment** related link.

3.  Answer the questions and select **Submit**.

    After you submit the risk assessment, select the **Risk Calculation** related link to calculate the risk. The results of the risk assessment and risk calculation are displayed, along with the value that appears in the **Risk** field of the change request form.

    \[Omitted image "RSKASS4.png"\] Alt text: risk calculation results

    Users with the survey\_admin or survey\_reader role can navigate to **Legacy Surveys** &gt; **Survey Responses** and filter by **Instance**. Survey instances are individual assessments distinguished by the date and time when they are taken.


**Parent Topic:**[Risk assessment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/change-management/c_RskAsmtCalc.md)

**Related topics**  


[Define risk assessments]()

[Risk assessment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/change-management/c_RskAsmtCalc.md)

