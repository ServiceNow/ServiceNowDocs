---
title: ServiceNow AI Lens form auto-filler
description: The ServiceNow AI Lens form auto-filler uses AI image recognition to populate form fields from photos that field service technicians capture in the ServiceNow Agent mobile application. Technicians can auto-fill Input Forms and Scripted Input Forms, such as Smart Assessment questionnaires.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/field-service-management/work-order-management/c\_form-auto-filler-fsm.html
release: australia
product: Work Order Management
classification: work-order-management
topic_type: concept
last_updated: "2026-07-10"
reading_time_minutes: 1
breadcrumb: [Prioritizing on ServiceNow Agent, ServiceNow Agent mobile app, Completing work on mobile, Use, Field Service Management]
---

# ServiceNow AI Lens form auto-filler

The ServiceNow AI Lens form auto-filler uses AI image recognition to populate form fields from photos that field service technicians capture in the ServiceNow Agent mobile application. Technicians can auto-fill Input Forms and Scripted Input Forms, such as Smart Assessment questionnaires.

**Note:**

Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents. For more information, see.

## ServiceNow AI Lens form auto-filler

The ServiceNow AI Lens form auto-filler reduces the effort of manually entering data by using AI image recognition to extract information from photos and populate form fields automatically.

The feature is a direct implementation of the platform-level ServiceNow AI Lens capability for Field Service Management. Technicians access it from the **Lens Launcher** button on supported forms, or from the ServiceNow AI Lens topic in ServiceNow Otto Virtual Agent.

## Supported form types

The ServiceNow AI Lens form auto-filler is available on the following form types in the ServiceNow Agent mobile application:

-   **Input Forms**

    Technicians can launch ServiceNow AI Lens from a record-based Input Form to auto-populate fields with extracted image data.

-   **Scripted Input Forms**

    Technicians can launch ServiceNow AI Lens from a Scripted Input Form, such as Smart Assessment questionnaires to auto-populate fields based on the form's underlying script.


## ServiceNow AI Lens in ServiceNow Otto Virtual Agent

Technicians can use in-form auto-fill or access ServiceNow AI Lens through ServiceNow Otto Virtual Agent in the ServiceNow Agent mobile application. In this process, the technician selects ServiceNow AI Lens from the Virtual Agent topic picker, uploads or captures an image, and receives a text summary response. This flow does not auto-fill form fields. For more information, see [Use ServiceNow AI Lens in ServiceNow Otto Virtual Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/work-order-management/t_use-lens-nava-fsm.md).

## Plugins

The ServiceNow AI Lens form auto-filler requires the following plugins:

-   `com.sn_ai_lens`- Platform ServiceNow AI Lens plugin.
-   `com.sn.fsm.gen.ai`- ServiceNow Otto for the FSM plugin. Controls access to the Lens Launcher icon on the FSM forms.
-   `com.snc.fsm_smart_asmt_questionnaire`- Smart Assessment questionnaire plugin. Required for Lens Launcher on Smart Assessment questionnaires.
-   `com.snc.app_lens_until_pack`- Defines who can use the feature, how data is processed, and the fields that ServiceNow AI Lens can populate.

