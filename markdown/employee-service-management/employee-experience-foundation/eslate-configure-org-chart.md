---
title: Configure the organization chart for Employee Slate
description: Configure the organization chart in Employee Slate. Set the eligible users and the fields that appear on each card.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/employee-experience-foundation/eslate-configure-org-chart.html
release: australia
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2026-05-27"
reading_time_minutes: 1
keywords: [organization chart, org chart configuration, eligible users, employee card fields, Employee Slate]
breadcrumb: [Employee org chart, Working with Employee Slate capabilities, Employee Slate, Unified Employee Experience, Employee Service Management]
---

# Configure the organization chart for Employee Slate

Configure the organization chart in Employee Slate. Set the eligible users and the fields that appear on each card.

## Before you begin

Activate Employee Slate for Now Assist in the instance.

Role required: admin or Employee Slate administrator.

## About this task

The organization chart appears in the left navigation of the Employee Slate portal. Employees view a level above, a level below, and additional levels on demand.

The eligible user setting controls who appears in the chart. The card field setting controls what information appears for each employee.

## Procedure

1.  Go to **All** &gt; **Employee Center** &gt; **Organization chart**.

    The configuration page shows two settings: **Eligible users** and **User display**.

2.  Select **Eligible user** and declare the users who appear in the chart.

    Scope the chart by department, location, or any valid user attribute.

3.  Go to **Org chart configuration** and select the fields to display on each card.

    Common fields include **Name**, **Title**, **Manager email**, and **Team**. Each selected field appears in the order shown.

4.  In **Org chart configuration**, set the report count display to **Direct** or **Total**.

    **Direct** shows only the direct reports for each employee. **Total** shows the cumulative count of reports at each level below that employee.

5.  Preview the chart from an employee account.

    Open the Employee Slate portal and select **Org chart** in the left navigation. Confirm that the eligible users and the card fields match the configuration.

6.  Verify the AI conversational use cases.

    Ask the assistant `Who is Beth Anglin?` or `Show the org of Adela Cervantes.` The assistant returns the user profile or loads the requested org chart view.

7.  Save the configuration.

    The save commits the eligible user list and the card field selections. Refresh the chart to confirm the change.


## Result

Employees view the configured organization hierarchy and card fields when they open the org chart. The AI assistant honors the eligible user list when it responds to people-related queries.

**Important:** AI-generated responses may be inaccurate. Review the results before acting on them.

## What to do next

Employees can edit and upload profile images directly on the profile page.

**Related topics**  


[Organization chart in Employee Center Pro](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/employee-experience-foundation/employee-profile-org-chart.md)

