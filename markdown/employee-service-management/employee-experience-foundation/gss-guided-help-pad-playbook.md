---
title: Build a visual flow for Guided Self-Service
description: Create a visual playbook flow of activities so that employees can find information in a more intuitive and visual way.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/employee-experience-foundation/gss-guided-help-pad-playbook.html
release: australia
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Guided Self-Service in Employee Center, Setup Employee Center browse experience features, Configuring Employee Center, Employee Center, Unified Employee Experience, Employee Service Management]
---

# Build a visual flow for Guided Self-Service

Create a visual playbook flow of activities so that employees can find information in a more intuitive and visual way.

## Before you begin

Understand the basics of playbooks and workflow studio .

Review the information from [Guided Self-Service reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/employee-experience-foundation/gss-guided-self-service-reference-info.md).

Role required: sn\_hr\_sp.esc\_admin, playbook.write

## Procedure

1.  Follow the instructions available in .

2.  On the Workflow Studio, use the existing questionnaire activity available from **Add activity** &gt; **Common Activities** &gt; **Questionnaire** for authoring question and answer flow.

    Here is a sample illustration of the entire flow.

    \[Omitted image "gss-playbook-design-flow.png"\] Alt text: process design flow

    Each activity definition contains some basic configuration details, as well as an automation plan and activity experience. Table is Guided Self-Service \(GSS\) Process Execution.

3.  On the Workflow Studio, use the new GSS-specific activities.

    -   **Add activity** &gt; **Guided Self-Service in Employee Center** &gt; **Catalog Item Guidance**.
    -   **Add activity** &gt; **Guided Self-Service in Employee Center** &gt; **Show Knowledge Article Guidance**.
    -   **Add activity** &gt; **Common Activities** &gt; **Instruction Activity**.
    \[Omitted image "gss-add-activity-ec-interactive.png"\] Alt text: Add activity for GSS

    For more information, see the activity information such as Input, Output, and Advanced Properties on the UI.

4.  On the Workflow Studio, customize triggers, flows, decisions, and so on.

    Here is a sample illustration for time off flow.

    \[Omitted image "gss-pad-trigger-flow-confi.png"\] Alt text: Workflow Studio PAD design

    **Note:** Ensure you configure the Restart operation for every activity in the flow. When only one activity has the restart operation, it won't work.

    Based on the security access and user permissions, the catalog items and KBs appear. For more information, see .

    **Note:** The Activity Definition \[sys\_pd\_activity\_definition\] table lists the definitions for the activities that you can add to a playbook in **Workflow Studio**.

5.  Click **Activate**.

    **Note:** Only when you activate the GSS process, the **Add** button is displayed on the **Assigned Topics**.


## Result

GSS is configured to guide employees. For more information, see [Use Guided Self-Service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/employee-experience-foundation/gss-guided-self-service-homepage.md).

