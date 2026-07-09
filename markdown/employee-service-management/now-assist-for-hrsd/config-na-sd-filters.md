---
title: Configure sensitivity detection
description: Configure sensitivity detection in the Now Assist for HR Service Delivery \(HRSD\) application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/employee-service-management/now-assist-for-hrsd/config-na-sd-filters.html
release: yokohama
product: Now Assist for HRSD
classification: now-assist-for-hrsd
topic_type: task
last_updated: "2025-09-17"
reading_time_minutes: 4
breadcrumb: [Configure, Now Assist for HR Service Delivery \(HRSD\), HR Service Delivery, Employee Service Management]
---

# Configure sensitivity detection

Configure sensitivity detection in the Now Assist for HR Service Delivery \(HRSD\) application.

## Before you begin

Role required:sn\_hr\_core.admin

## About this task

This capability helps you configure sensitivity detection and filters for the types of sensitive cases such as the harassment complaints, discrimination allegations, workplace violence, safety, employee behavior, and employee personal issues. You can also block Now LLM Service from engaging with these sensitive case types to allow agents to create cases for these sensitive case types.

**Note:**

Configurations are available on the Now Assist Admin Panel settings as part of Now Assist guardian. The **sn\_hr\_gen\_ai.admin** role can only **Edit**, **Activate** and **Deactivate** skills on **Guided** setup view only.

## Procedure

1.  Navigate to the **Now Assist Admin Panel** and select the **Settings** tab. \[Omitted image "sd-na-admin-panel-settings.png"\] Alt text: Access to Now Assist Admin Panel and Settings tab

2.  Select **Now Assist Guardian** and select **Filters**.\[Omitted image "sd-na-admin-panel-filters.png"\] Alt text: Filters tab view that lists the existing filters

    Filter configurations include the ability to **Edit** or **Deactivate** a filter. Only **sn\_hr\_gen\_ai.admin** can **Edit** or **Deactivate**.\[Omitted image "sd-na-admin-panel-editdeact.png"\] Alt text: Shows the ability to Edit or Deactivate a filter from the list

3.  Select **General Details** tab to configure the filter details.\[Omitted image "sd-na-admin-panel-generaldetails.png"\] Alt text: Shows the ability to add filter type and description details

4.  Select **Sample phrases** tab to add phrases that apply to filters.\[Omitted image "sd-na-admin-panel-newphrase.png"\] Alt text: Shows the ability to add new and edit existing sample phrases

    **Note:** The ability to edit and update existing filters is available. There is a maximum of 10 phrases that can be generated.

5.  Select **Applicability** to choose what filters apply to active virtual agents.\[Omitted image "sd-na-admin-panel-applicability.png"\] Alt text: Shows the ability to add virtual agents to sensitive phrases


## Result

When an employee enters one of the configured sensitive phrases, the virtual agent offers to either redirect the employee to a live agent, create a case, or if the virtual agent incorrectly identifies a sensitive topic, the employee can select to proceed with the interaction.

**Parent Topic:**[Configure Now Assist for HR Service Delivery \(HRSD\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/employee-service-management/now-assist-for-hrsd/configure-now-assist-hr.md)

**Related topics**  


[Skill inputs and triggers for Now Assist for HR Service Delivery \(HRSD\)]()

[RCA approvals for Now Assist for HR Service Delivery \(HRSD\)]()

[Restrict Now Assist capabilities for employee relations cases]()

[Customize the Now Assist for HRSD skills]()

[Configure attachment summary]()

[Configure resolution notes generation for Now Assist for HRSD]()

[Configure Gen AI Virtual Agent for HRSD]()

[Configure the Now Assist for HRSD Virtual Agent topics]()

[Configure HCM agents for HR Service Delivery AI Agent Collection]()

[Configure Now Assist AI Helper – Galileo Inside]()

[bundle-platai.add-semantic-filtering-for-sensitive-information]

[Detect sensitive topics by using sensitivity detection in Now Assist for HR Service Delivery \(HRSD\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/employee-service-management/now-assist-for-hrsd/now-assist-hrsd-sensitivity-detection.md)

[Sensitivity detection configuration tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/employee-service-management/now-assist-for-hrsd/reference-sd-config-tables.md)

[Sensitivity detection configuration table filters](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/employee-service-management/now-assist-for-hrsd/reference-sd-config-shipment-tables.md)

[Sensitivity detection filters mapping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/employee-service-management/now-assist-for-hrsd/reference-sd-info-values.md)

