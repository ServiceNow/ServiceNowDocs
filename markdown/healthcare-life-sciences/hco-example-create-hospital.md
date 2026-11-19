---
title: Example - Create a hospital
description: Explore how a hospital is created under an existing parent organization for Healthcare Operations, under which departments or similar sub-organizations can then be created and organized under.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/healthcare-life-sciences/hco-example-create-hospital.html
release: zurich
topic_type: task
last_updated: "2025-11-05"
reading_time_minutes: 1
breadcrumb: [Organizing your healthcare organizations, Setting up healthcare locations and healthcare organizations, Configure, Care Team Work Management, Healthcare Operations, Healthcare and Life Sciences]
---

# Example - Create a hospital

Explore how a hospital is created under an existing parent organization for Healthcare Operations, under which departments or similar sub-organizations can then be created and organized under.

## Before you begin

Role required: admin

## About this task

Scenario: Armand, a ServiceNow administrator for a hospital, needs to set up a pediatrics department at Alectri Santa Clara hospital. Armand creates the department within the hospital in ServiceNow so he can ensure that all related entities inherit the correct organizational structure and permissions.

## Procedure

1.  Navigate to **All** &gt; **Healthcare Operations** &gt; **Healthcare organizations** &gt; **All**.

2.  Select **New**.

3.  Fill in the following fields.

    -   Name - Enter **Alectri Santa Clara**.
    -   Organization type - Enter **Healthcare Provider**.
    -   Parent organization - Enter the parent organization created in [Example - Create a parent organization \(HQ\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/healthcare-life-sciences/hco-example-create-parent-organization.md). **Alectri Health**.
4.  Select **Submit**.


## Result

A hospital, **Alectri Santa Clara**, is created under the parent organization **Alectri Health**. Armand can now repeat this process for all other hospitals that fall under that parent organization.

