---
title: Smart Assessment questionnaires
description: Smart Assessment questionnaires enable Field Service Management technicians to capture accurate and task-critical information in a structured way during work execution. As part of completing work order tasks, Field Service technicians can be mandated to fill up questionnaires that record important details of the task.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/field-service-management/smart-assessment-questionnaire.html
release: brazil
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [Questionnaires in Field Service Management, Explore, Field Service Management]
---

# Smart Assessment questionnaires

Smart Assessment questionnaires enable Field Service Management technicians to capture accurate and task-critical information in a structured way during work execution. As part of completing work order tasks, Field Service technicians can be mandated to fill up questionnaires that record important details of the task.

Smart Assessment is built on Smart Assessment Engine- a platform-level capability available for Field Service Management through dedicated plugins and store applications. For more information on activating it, see [Activate Smart Assessment for Field Service questionnaire](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/field-service-management/mobile-experience-for-field-service-management-glide-family/activate-smart-assessment.md).

-   Smart Assessment questionnaires are used to collect task-specific information such as safety checks, inspection details, compliance confirmations, and work completion checklists from technicians. These questionnaires can be configured as mandatory. This ensures a work order or work order task is not closed until all relevant details are captured by the agent.
-   The questionnaires help in verifying if the field service agent has completed all the required steps and complied with organizational, safety, and regulatory requirements of the work order.
-   Technicians can complete assessments online or offline while executing tasks in fields, ensuring data is captured at the point of work.
-   Smart Assessment questionnaires use reusable templates that standardize the process of collecting information across different work order tasks, task types, and operational domains.

## Smart Assessment questionnaire use case

Priya is a field service technician who performs routine HVAC inspections across multiple retail locations for a facilities management company. Each inspection covers the same core checks, but some units require additional follow-up depending on what Priya finds on-site.

When Priya begins an inspection, a questionnaire becomes available for the task. While working through it, the questions adapt to the responses — if a partially blocked filter is flagged, additional questions appear prompting Priya to document the condition further. Questions that don't apply to the unit don't appear on the questionnaire. Even with a connection issue mid-inspection, Priya continues working and the responses sync automatically once the device is back online.

The same template drives every store visit, to ensure that the process stays consistent without administrators having to set up a new questionnaire each time. And if a response needs to be corrected after submission, Priya can revisit and update it without starting over.

## Example: Equipment Safety Inspection

A service technician needs to capture inspection and compliance data in a structured way during work execution. Smart Assessment questionnaires guide technicians through standardized checklists that adapt based on responses, preventing closure until all required information is recorded.

|Step|Actor|Action|
|----|-----|------|
|1|System|Generates work order from maintenance plan|
|2|Technician|Opens work order task in mobile app|
|3|Technician|Launches Smart Assessment questionnaire|
|4|Technician|Submits inspection results|
|5|System|Triggers follow-up tasks based on responses|
|6|System|Closes work order task|

**Related topics**  


[Survey-based questionnaires](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/field-service-management/survey-based-questionnaires.md)

[Questionnaires in Field Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/field-service-management/questionnaires-in-field-service-management.md)

