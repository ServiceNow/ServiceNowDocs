---
title: Field Service Management questionnaires
description: Both survey-based and Smart Assessment questionnaires are available in the ServiceNow Agent mobile application. If a questionnaire is configured as mandatory for a work order task, the task can't be closed until the questionnaire is completed.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/field-service-management/field-service-management-questionnaires.html
release: australia
topic_type: reference
last_updated: "2026-06-23"
reading_time_minutes: 2
breadcrumb: [Reference, Field Service Management]
---

# Field Service Management questionnaires

Both survey-based and Smart Assessment questionnaires are available in the ServiceNow Agent mobile application. If a questionnaire is configured as mandatory for a work order task, the task can't be closed until the questionnaire is completed.

## Work order task questionnaire workflow

An admin authors the questionnaire, then configures the trigger and mandatory rule that control when it appears and whether a response is required. The admin activates and deploys the questionnaire for the work order task, making it available to technicians. When a technician opens the work order task, they start filling the questionnaire. Depending on the initial configuration, the questionnaire is one of two types:

-   Survey-based questionnaire: presents a fixed list of questions, can be filled only while the technician is online, captures no per-response evidence, and is specific to the task.
-   Smart Assessment questionnaire: presents adaptive questions, works offline, and captures comments, files, and justifications. Responses stay editable after submission.

After completing the questionnaire, the technician validates and submits the responses, then closes the work order task.

|Purpose|Smart Assessment questionnaire|Survey-based questionnaire|
|-------|------------------------------|--------------------------|
|Primary purpose|Automating, standardizing, and enforcing structured data collection and validation during work execution — safety checks, compliance confirmations, inspection details, and work completion checklists|General questionnaire use cases tied to work order tasks — collecting task information before, during, or after work|
|Best suited for|Organizations with compliance, safety, or regulatory requirements where data must be captured consistently across many task types and operational domains|Organizations that need a straightforward questionnaire attached to specific work order tasks without cross-task standardization needs|
|Offline field work|Well suited — technicians can complete assessments online or offline; data syncs when connectivity is restored|No offline support|
|Reuse across task types|Use when the same data collection process needs to apply across different work order tasks, task types, or operational domains — reusable templates enable this|Use when questionnaires are task-specific and reuse across task types is not a requirement|
|Complex conditional logic|Supports conditional questions based on responses across all question types and across sections — use when question branching is needed|Supports conditional dependencies but they are not migrated if you later move to Smart Assessment; less flexible for cross-section logic|
|Additional context on responses|Allows agents to add comments or attach files to individual question responses — use when richer evidence capture is needed|No equivalent per-response attachment or comment capability mentioned|
|Template authoring|Templates are authored and published through Assessment Workspace using the Smart Assessment Engine Template Designer; templates must be published before a questionnaire can be created from them|Questionnaires are created directly using the Survey Designer tool- no publish step required|
|Retaking a questionnaire|Can be edited even after submission based on certain conditions|Not supported|
|Reversibility|Cannot be disabled once enabled at the instance level|Can exist until Smart Assessment is enabled|
|Recommended when|Your team works in the field with or without connectivity, compliance and standardization across tasks matter, and you need richer response capture \(comments, attachments, justifications\)|Your use case is simpler, your questionnaire uses data types Smart Assessment doesn't support|

**Parent Topic:**[Field Service Management reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/fsm-reference.md)

