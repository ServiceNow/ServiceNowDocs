---
title: Configure sensitivity detection for Now Assist for HRSD
description: Configure sensitivity detection in the Now Assist for HR Service Delivery \(HRSD\) application.
locale: en-US
release: zurich
product: Now Assist for HRSD
classification: now-assist-for-hrsd
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure, Now Assist for HR Service Delivery \(HRSD\), HR Service Delivery, Employee Service Management]
---

# Configure sensitivity detection for Now Assist for HRSD

Configure sensitivity detection in the Now Assist for HR Service Delivery \(HRSD\) application.

## Before you begin

Role required:sn\_hr\_core.admin

## About this task

This capability helps you configure sensitivity detection and filters for the types of sensitive cases such as the harassment complaints, discrimination allegations, workplace violence, safety, employee behavior, and employee personal issues. You can also block Now LLM Service from engaging with these sensitive case types to allow agents to create cases for these sensitive case types.

**Note:**

Configurations are available on the Now Assist Admin Panel settings as part of Now Assist guardian. The **sn\_hr\_gen\_ai.admin** role can only **Edit**, **Activate** and **Deactivate** skills on **Guided** setup view only.

## Procedure

1.  Navigate to the **Now Assist Admin Panel** and select the **Settings** tab. ![Access to Now Assist Admin Panel and Settings tab](../image/sd-na-admin-panel-settings.png)

2.  Select **Now Assist Guardian** and select **Filters**.![Filters tab view that lists the existing filters](../image/sd-na-admin-panel-filters.png)

    Filter configurations include the ability to **Edit** or **Deactivate** a filter. Only **sn\_hr\_gen\_ai.admin** can **Edit** or **Deactivate**.![Shows the ability to Edit or Deactivate a filter from the list](../image/sd-na-admin-panel-editdeact.png)

3.  Select **General Details** tab to configure the filter details.![Shows the ability to add filter type and description details](../image/sd-na-admin-panel-generaldetails.png)

4.  Select **Sample phrases** tab to add phrases that apply to filters.![Shows the ability to add new and edit existing sample phrases](../image/sd-na-admin-panel-newphrase.png)

    **Note:** The ability to edit and update existing filters is available. There is a maximum of 10 phrases that can be generated.

5.  Select **Applicability** to choose what filters apply to active virtual agents.![Shows the ability to add virtual agents to sensitive phrases](../image/sd-na-admin-panel-applicability.png)


## Result

When an employee enters one of the configured sensitive phrases, the virtual agent offers to either redirect the employee to a live agent, create a case, or if the virtual agent incorrectly identifies a sensitive topic, the employee can select to proceed with the interaction.

**Parent Topic:**[Configure Now Assist for HR Service Delivery \(HRSD\)](configure-now-assist-hr.md)

**Related topics**  


[Now Assist Guardian](https://www.servicenow.com/docs/access?context=now-assist-guardian&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)

[bundle-platai.add-semantic-filtering-for-sensitive-information]

[Sensitivity detection filters mapping](../reference/reference-sd-info-values.md)

