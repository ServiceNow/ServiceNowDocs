---
title: Define AI prompt configurations
description: Define prompt configurations to control how data from each source is queried and presented to the large language model \(LLM\)
locale: en-US
release: zurich
product: Now Assist for WSD
classification: now-assist-for-wsd
topic_type: task
last_updated: "2025-10-27"
reading_time_minutes: 1
breadcrumb: [Insight cards on the Workplace Central dashboard, Workplace Advisor Overview, Using AI agent workflows in Now Assist for WSD, Now Assist for Workplace Service Delivery \(WSD\), Workplace Service Delivery, Employee Service Management]
---

# Define AI prompt configurations

Define prompt configurations to control how data from each source is queried and presented to the large language model \(LLM\)

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Workplace Insights** &gt; **Configuration**.

2.  On the AI Prompt Configurations page, select **New**.

3.  On the form, fill in the fields.

<table id="table_ex4_5dr_bhc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Data source

</td><td>

The Workplace Data Source that is used to generate insights.

</td></tr><tr><td>

Skill

</td><td>

The Now Assist skill that generates AI‑assisted output from ServiceNow data using a large language model \(LLM\).

</td></tr><tr><td>

Category

</td><td>

The classification or grouping of the AI prompt configuration. Select the required category from the following options:-   Reservation
-   Space Management
-   Workplace Connectors
For example, when you select **Reservation** and specify the instructions to the AI system, the system displays reservation insights on the **Reservation Management** tab on the Workplace Central dashboard.

</td></tr><tr><td>

Active

</td><td>

The option to enable the prompt configuration. By default, the field is set to **Active**.

</td></tr><tr><td>

Order

</td><td>

The order that this prompt configuration is displayed before the input.

</td></tr><tr><td>

AI instructions

</td><td>

Description of the specific tasks or analysis that the AI system is configured to perform. Include instructions and actions like data analysis, pattern detection, or predictive modeling. Provide clear and direct instructions for the AI system to follow when generating outputs. For example, Systematically analyze 2-week occupancy data to identify capacity utilization patterns, space optimization opportunities, and operational anomalies.

</td></tr><tr><td>

Threshold

</td><td>

Definition of the numerical or categorical limits or values that trigger specific analysis or flags within the AI system. For example, -   High Occupancy Detection: 90% capacity threshold
-   Low Utilization Analysis: below 40% capacity threshold
These thresholds help the AI system determine when to flag certain conditions or anomalies.

</td></tr><tr><td>

Example

</td><td>

Illustrative cases or scenarios that demonstrate how AI system instructions and thresholds are applied. This field helps users understand the expected inputs and outputs of the AI configuration. For example:

-   Campus attendance dropped 22% week-over-week \(WoW\)
-   Friday is consistently the lowest attendance day \(-30% compared to Wednesday\)


</td></tr></tbody>
</table>4.  In the User Criteria section, select the user criteria record to decide which users, roles, and groups can see the respective insights.

    For example, Users with Reservation Manager role can view insights related to Reservation Management on the Workplace Central dashboard.

5.  Select **Submit**.


