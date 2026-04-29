---
title: Default Model Risk Management email notifications
description: Default Model Risk Management notifications inform users about important events and status changes throughout the Model Risk Management workflow.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Reference, Model Risk Management, Governance, Risk, and Compliance]
---

# Default Model Risk Management email notifications

Default Model Risk Management notifications inform users about important events and status changes throughout the Model Risk Management workflow.

Default Model Risk Management notifications keep stakeholders informed about key events and status changes throughout the Model Risk Management life cycle. These notifications typically cover updates such as model creation, assignment changes, assessment or validation progress, approval requirements, and status transitions. They ensure that users receive consistent and reliable communication without requiring initial configuration.

## Default email notification configurations for Model Risk Management

Use the default notification configurations to notify users about specific activities in Model Risk Management. Notification configurations enable administrators to specify:

-   When to send the notification
-   Who receives the notification
-   What content is in the notification

To access these configurations, navigate to **All** &gt; **System Notification** &gt; **Email** &gt; **Notifications**.

|Notification configurations|Event|Recipients|
|---------------------------|-----|----------|
|Assessment task submitted|An assessment task is submitted for approval.|Approver|
|Validation task approval and completion|A validation task is approved and marked as Completed.|Assigned validator|
|Assessment task approval and completion|An assessment task is approved and marked as Completed.|Assessment assignee|
|Assessment task smart asmt cancelled|An assessment task is canceled.|Assessment assignee|
|Validation task assignment|A validation task is submitted and is ready for validation.|Assigned validator|
|Validation checklist reopened|A validation task is reopened.|Assigned validator|
|Assessment task reopened|An assessment task is reopened.|Assessment assignee|
|Assessment task assignment|An assessment task is assigned to an assessor for assessment.|Assessment assignee|
|Validation checklist cancelled|A validation task is canceled.|Assigned validator|
|Notify model owner for new model|A model is created.|Model owner|
|New model submission|A model is submitted for review.|Model Risk Governance team|

**Parent Topic:**[Model Risk Management reference](mrm-reference.md)

