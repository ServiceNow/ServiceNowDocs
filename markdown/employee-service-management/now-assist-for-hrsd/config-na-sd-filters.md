---
title: Configure sensitivity detection
description: Configure sensitivity detection in the ServiceNow Otto for HR Service Delivery \(HRSD\) application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/employee-service-management/now-assist-for-hrsd/config-na-sd-filters.html
release: zurich
product: Now Assist for HRSD
classification: now-assist-for-hrsd
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, ServiceNow Otto for HR Service Delivery \(HRSD\), HR Service Delivery, Employee Service Management]
---

# Configure sensitivity detection

Configure sensitivity detection in the ServiceNow Otto for HR Service Delivery \(HRSD\) application.

## Before you begin

Role required:sn\_hr\_core.admin

## About this task

This capability helps you configure sensitivity detection for harassment complaints, discrimination allegations, workplace violence, safety, employee behavior, and employee personal issues. You can also block Now LLM Service from engaging with these sensitive cases and redirect employees to work with live agents.

**Note:**

Configurations are available on the ServiceNow Otto Admin Panel settings as part of AI Guardian. The **sn\_hr\_gen\_ai.admin** role can only **Edit**, **Activate** and **Deactivate** skills on **Guided** setup view only.

## Procedure

1.  Navigate to the **ServiceNow Otto Panel** and select the **Settings** tab. \[Omitted image "sd-na-admin-panel-settings.png"\] Alt text: Access to ServiceNow Otto Admin Panel and Settings tab

2.  Select **ServiceNow Otto Guardian** and select **Filters**.\[Omitted image "sd-na-admin-panel-filters.png"\] Alt text: Filters tab view that lists the existing filters

    Filter configurations include the ability to **Edit** or **Deactivate** a filter. Only **sn\_hr\_gen\_ai.admin** can **Edit** or **Deactivate**.\[Omitted image "sd-na-admin-panel-editdeact.png"\] Alt text: Shows the ability to Edit or Deactivate a filter from the list

3.  Select **General Details** tab to configure the filter details.\[Omitted image "sd-na-admin-panel-generaldetails.png"\] Alt text: Shows the ability to add filter type and description details

4.  Select **Sample phrases** tab to add phrases that apply to filters.\[Omitted image "sd-na-admin-panel-newphrase.png"\] Alt text: Shows the ability to add new and edit existing sample phrases

    **Note:** The ability to edit and update existing filters is available. There is a maximum of 10 phrases that can be generated.

5.  Select **Applicability** to choose what filters apply to active virtual agents.\[Omitted image "sd-na-admin-panel-applicability.png"\] Alt text: Shows the ability to add virtual agents to sensitive phrases


**Parent Topic:**[Configure ServiceNow Otto for HR Service Delivery \(HRSD\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/now-assist-for-hrsd/configure-now-assist-hr.md)

**Related topics**  


[bundle-platai.add-semantic-filtering-for-sensitive-information]

[Sensitivity detection filters mapping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/now-assist-for-hrsd/reference-sd-info-values.md)

