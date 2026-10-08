---
title: Create a demand experience
description: Create a demand experience to control the form view, demand modules, and dynamic attributes that appear on demands to support configuration independence across different types of demands.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-business-management/strategic-planning/create-a-demand-experience-dw.html
release: brazil
product: Strategic Planning
classification: strategic-planning
topic_type: task
last_updated: "2026-09-25"
reading_time_minutes: 1
breadcrumb: [Configuring demand experiences, Configure, Next Experience for Demand Management in Strategic Planning, Strategic Planning, Strategic Portfolio Management]
---

# Create a demand experience

Create a demand experience to control the form view, demand modules, and dynamic attributes that appear on demands to support configuration independence across different types of demands.

## Before you begin

If the demand experience uses a dynamic category, the dynamic category that defines its custom fields must already exist.

Role required: pps\_admin

## About this task

A demand experience consists of a custom form view, demand modules, and, optionally, a dynamic category that defines custom fields for that experience. For example, you can create experiences for Marketing or IT governance processes. For more information, see [Demand experiences](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/strategic-planning/demand-experiences-dw.md).

## Procedure

1.  Navigate to **All** &gt; **Demand Experiences**.

    \[Omitted image "demand-experiences-navigation.png"\] Alt text: Navigation for Demand Experiences.

2.  Select **New**.

3.  Fill in the fields on the form.

    For a description of the field values, see [Demand experience form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/portfolio-planning/demand-experience-form-ppw.md).

    \[Omitted image "demand-experiences-form.png"\] Alt text: Demand experience form.

4.  Under **Show modules**, clear the check box for any module that you don't want to show for demands that use this experience.

    Every module is selected by default.

5.  Select **Submit**.


## Result

The demand experience is available to select when a demand is created. Only the modules that you left selected are shown for demands that use this experience, and a view rule and workspace view rule are created automatically. If you selected a dynamic category with dynamic attributes, an **Additional Information** tab appears in the Details module, showing those attributes.

**Related topics**  


[Create a demand](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/strategic-planning/create-demand-from-dw.md)

[Add dynamic attributes to a demand](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/strategic-planning/add-dynamic-attributes-to-a-demand-dw.md)

