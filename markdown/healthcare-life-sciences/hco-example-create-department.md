---
title: Example - Create a department
description: Explore how a department is created under an existing hospital for Healthcare Operations, under which department organization teams can then be created.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/healthcare-life-sciences/hco-example-create-department.html
release: zurich
topic_type: task
last_updated: "2025-11-05"
reading_time_minutes: 1
breadcrumb: [Organizing your healthcare organizations, Setting up healthcare locations and healthcare organizations, Configure, Care Team Work Management, Healthcare Operations, Healthcare and Life Sciences]
---

# Example - Create a department

Explore how a department is created under an existing hospital for Healthcare Operations, under which department organization teams can then be created.

## Before you begin

Role required: admin

## About this task

Scenario: Armand, a ServiceNow administrator for a hospital, needs to set up a pediatrics department at Alectri Santa Clara hospital. Armand creates the department within the hospital in ServiceNow so it is ensured that all related entities inherit the correct organizational structure and permissions.

## Procedure

1.  Navigate to **All** &gt; **Healthcare Operations** &gt; **Healthcare organizations** &gt; **All**.

2.  Select **New**.

3.  Fill in the following fields.

    -   Name - Enter **Pediatrics Alectri Santa Clara**.
    -   Organization type - Select **Healthcare Department**.
    -   Parent organization - Select the parent hospital created in [Example - Create a hospital](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/healthcare-life-sciences/hco-example-create-hospital.md), **Alectri Santa Clara**.
4.  Select **Submit**.


## Result

The **Pediatrics Alectri Santa Clara Department** has been created under the parent hospital **Alectri Santa Clara**. Armand can then repeat this process for all other departments within this hospital as needed.

