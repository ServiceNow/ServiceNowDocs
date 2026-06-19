---
title: Create new highlighted values for Prioritization columns in Portfolio Planning
description: Customize the fields to be highlighted on the Prioritization page of a portfolio plan according to your planning manager's needs.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-business-management/portfolio-planning/create-highlighted-values-prioritization-portfolio-planning.html
release: zurich
product: Portfolio Planning
classification: portfolio-planning
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
keywords: [alignment planner workspace, portfolio planning workspace, portfolio planner, strategic planner, strategic planning workspace]
breadcrumb: [Customizing highlighted fields, Configuring Prioritization and Roadmap settings in Portfolio Planning, Configure, Portfolio Planning, Strategic Portfolio Management]
---

# Create new highlighted values for Prioritization columns in Portfolio Planning

Customize the fields to be highlighted on the Prioritization page of a portfolio plan according to your planning manager's needs.

## Before you begin

[Modify Script Includes for Prioritization page in Portfolio Planning](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/portfolio-planning/modify-script-includes-prioritization-page-portfolio-planning.md).

Role required: admin

## Procedure

1.  Navigate to **Workspace Experience** &gt; **Administration** &gt; **Highlighted Values**.

2.  Select **New**.

3.  On the form, fill in the fields.

    For field information, see [Highlighted Value form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/portfolio-planning/highlighted-value-form-portfolio-planning.md).

4.  Save the form.

5.  In the Highlighted Value Conditions related list, create records to configure the color, order, and icon for each of the field values that you want to be highlighted in the workspace.

    1.  Select **New**

    2.  On the form, fill in the fields.

        For field, information, see [Highlighted Value Condition form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/portfolio-planning/highlighted-value-condition-form-portfolio-planning.md).

    3.  Select **Submit**.

6.  Repeat step 5 to complete this configuration for all the field values.

    For example, if you are configuring for status column, you must create three records in the Highlighted Value Conditions related list for each of the choices Red, Green, and Yellow.

7.  Select **Update**.


**Parent Topic:**[Customizing highlighted fields on prioritization tab of Portfolio Planning workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/portfolio-planning/customizing-highlighted-fields-prioritization-page-portfolio-planning-workspace.md)

