---
title: Configure Integration Provider Mapping \(Decision table\)
description: Add input choices and define conditions and results in a decision table for the Integration Gateway subflow to review and generate output results.
locale: en-US
release: australia
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure ESM framework, Enterprise Service Management Integrations Framework, Integration of HR Service Delivery with third-party systems, HR Service Delivery, Employee Service Management]
---

# Configure Integration Provider Mapping \(Decision table\)

Add input choices and define conditions and results in a decision table for the Integration Gateway subflow to review and generate output results.

## Before you begin

View [Now Assist for HR Service Delivery \(HRSD\) Virtual Agent topic mapping for Enterprise Service Management Integrations Framework](../reference/esm-framework-mapping.md).

Role required: decision\_table\_admin, sn\_hr\_integr\_fw.admin

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  Navigate to Decision Tables.

3.  Select **Integration Provider Mapping**.

4.  In Inputs, provide the required values:

    |Label|Description|
    |-----|-----------|
    |Feature name|In Type, create a list of choice options for a feature name. For example, options within Feature name can be Leave Management, or Expense Management.|
    |Service name|Create a list of choice options for a service name. For example, options within Service name can be Time Off Balance, or Get Holiday Calendar.|
    |User|Provide reference to a user from the User \[sys\_user\] table.|

5.  To add a decision row, select **add new decision row** and provide conditions on input choices, and define the results:

<table><thead><tr><th>

Conditions and Results

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Feature name

</td><td>

Option you select from the Feature name list. For example, Leave Management.

</td></tr><tr><td>

Service name

</td><td>

Option you select from the Service name list. For example, Time Off Balance.

</td></tr><tr><td>

User country

</td><td>

Option you select for user's country list. You can also add additional conditions on **User country** by adding a condition column. For example, you can also add a check based on user department.

</td></tr><tr><td>

Subflow

</td><td>

Subflow you select to generate results. For example, Get time off balance subflow.The Get Time off Balance topic in Employee Center Center retrieves holiday calendar of user from Oracle HCM system by running the Get time off balance subflow.

</td></tr><tr><td>

Needs Manager Role

</td><td>

When set to true, the user must be a manager to run the subflow.

</td></tr><tr><td>

User Authentication

</td><td>

When set to true, the OAuth entity value is considered to validate the user for running the subflow.

</td></tr><tr><td>

OAuth Entity

</td><td>

OAuth Entity details. For Oauth Entity, the profiles with grant type as authorization code are supported.

</td></tr></tbody>
</table>6.  To validate the conditions specified on inputs choices, click **Test**.

    1.  In the Test Decision table, select Feature Name, Service Name, and User.
    2.  Select **Test**. For example, the results display the Get time off balance subflow to fetch the time off balance of a user.
7.  Select **Publish**.


