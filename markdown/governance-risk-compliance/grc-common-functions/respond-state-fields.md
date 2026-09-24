---
title: Respond state fields
description: Fields used in the activities of the Respond state in an issue's lifecycle.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/grc-common-functions/respond-state-fields.html
release: brazil
product: GRC Common Functions
classification: grc-common-functions
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Complete a playbook activity, Common GRC features, Governance, Risk, and Compliance]
---

# Respond state fields

Fields used in the activities of the Respond state in an issue's lifecycle.

The fields available in the Respond state depend on the playbook associated with the issue's workflow. The following activities and fields are examples from the default issue workflow playbook.

## Issue treatment

Determine how the issue will be addressed and document the rationale for the selected approach.

|Field|Description|
|-----|-----------|
|**Response**|The treatment approach for the issue, such as remediation or risk acceptance.|
|**Explanation**|The reason the selected treatment approach is appropriate for the issue.|

## Remediation planning

Define the remediation approach, timeline, and recommended actions.

|Field|Description|
|-----|-----------|
|**Planned end date**|The planned completion date for remediation. This value is prefilled from the issue record.|
|**Action plan**|The steps that will be taken to remediate the issue.|
|**Recommendation**|The recommended corrective or preventive actions identified during testing, assessment, or review.|

## Remediation tasks

Break down the remediation plan into individual tasks that can be tracked and assigned.

The related list includes the following columns:

|Column|Description|
|------|-----------|
|**Name**|The remediation task name.|
|**Number**|The remediation task record number.|
|**State**|The remediation task state.|
|**Assigned to**|The user assigned to the remediation task.|

**Parent Topic:**[Complete a playbook activity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/grc-common-functions/complete-a-playbook-activity.md)

**Related topics**  


[New state fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/grc-common-functions/new-state-fields.md)

[Analyze state fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/grc-common-functions/analyze-state-fields.md)

[Review and close state fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/grc-common-functions/review-and-close-state-fields.md)

[Complete a playbook activity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/grc-common-functions/complete-a-playbook-activity.md)

