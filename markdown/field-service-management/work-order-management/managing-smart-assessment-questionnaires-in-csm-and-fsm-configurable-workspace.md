---
title: Managing Smart Assessment questionnaires in CSM/FSM Configurable Workspace
description: CSM/FSM Configurable Workspace enables Field Service technicians to view, track, and complete work order tasks and the associated Smart Assessment questionnaires.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/field-service-management/work-order-management/managing-smart-assessment-questionnaires-in-csm-and-fsm-configurable-workspace.html
release: yokohama
product: Work Order Management
classification: work-order-management
topic_type: concept
last_updated: "2026-06-09"
reading_time_minutes: 2
breadcrumb: [Complete work orders on the web interface, Using Field Service Management, Field Service Management]
---

# Managing Smart Assessment questionnaires in CSM/FSM Configurable Workspace

CSM/FSM Configurable Workspace enables Field Service technicians to view, track, and complete work order tasks and the associated Smart Assessment questionnaires.

In CSM/FSM Configurable Workspace, Smart Assessment appears directly on work order task records when the configured trigger conditions are met. Accessing questionnaires on the task enables technicians to complete assessments without navigating away from the task.

Smart Assessment supports:

-   Conditional questions based on previous answers: For example, in a work order task related to HVAC inspection, the Smart Assessment questionnaire is conditional. One of the questions is about the refrigerator's cooling temperature, and the technician provides a value that is more than four degrees Celsius. A follow-up question is displayed, prompting the technician to provide the suspected reason for the refrigerator's malfunction. Similarly, if the technician provides any value below four degrees Celsius as the cooling temperature, no follow-up question is displayed.
-   Attachments and comments: Some fields in the questionnaire prompt the technician to attach an image or other file as proof of work. For example, one of the fields in the questionnaire can be: Clean the air filters and attach an image after cleaning.
-   Required responses before closing tasks, if configured: The questionnaire can be configured so that some questions are required. Mandatory questions require a response before the technician can proceed with the questionnaire and the task remains in the **Incomplete** state.

The questionnaire responses are stored with the task for reference, reporting, and audit purposes after submission.

Additionally, with Smart Assessment questionnaires, technicians can:

-   Reduce manual effort during job execution by filling in responses that are only relevant to their tasks.
-   Capture accurate data through a guided process that includes numeric validation, predefined ranges, and conditional enforcement.
-   Use barcode scanning directly inside the questionnaire for efficient asset identification.
-   Reduce follow-ups from dispatchers or back-office staff because planners and reviewers can see assessment results in real time.
-   Rely on automatic follow-up actions based on questionnaire responses.

-   **[View and complete Smart Assessments in CSM/FSM Configurable Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/field-service-management/work-order-management/view-and-complete-smart-assessments-in-workspace.md)**  
Technicians can use CSM/FSM Configurable Workspace to view, complete, and submit the Smart Assessment questionnaires that were partially completed in the mobile application.

**Parent Topic:**[Complete work orders on the web interface](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/field-service-management/work-order-management/completing-work-orders-on-the-web-interface.md)

