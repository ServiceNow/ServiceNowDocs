---
title: Choose input data form
description: The Choose input data form for the Regulatory alert summarization skill defines how data is structured and transmitted to the LLM, helping ensure integrity and relevance. It uses rule-based input templates and related tables to provide contextual information about alerts.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/regulatory-change-management-service-portal/input-data-rcm-skill.html
release: brazil
product: Regulatory Change Management Service Portal
classification: regulatory-change-management-service-portal
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Activate regulatory alert summarization skill, Regulatory alert summarization skill, AI in Regulatory Change Management, Regulatory Change Management, Governance, Risk, and Compliance]
---

# Choose input data form

The Choose input data form for the Regulatory alert summarization skill defines how data is structured and transmitted to the LLM, helping ensure integrity and relevance. It uses rule-based input templates and related tables to provide contextual information about alerts.

|Field|Description|
|-----|-----------|
|Input table|Table used to determine where to pull the data from. This will be applicable to all the templates.|

<table id="table_us2_nmr_xgc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

New stateBase input table fields: each skill relies on a base input table and input fields with descriptions to provide context for the LLM to generate a response.

</td></tr><tr><td>

Default input field

</td><td>

Title

</td></tr><tr><td>

Field description

</td><td>

Alert Title

</td></tr><tr><td>

Default input field

</td><td>

Description

</td></tr><tr><td>

Field description

</td><td>

Alert Description

</td></tr><tr><td>

Default input field

</td><td>

Summary

</td></tr><tr><td>

Field description

</td><td>

Alert Summary

</td></tr><tr><td>

Default input field

</td><td>

Source publication date

</td></tr><tr><td>

Field description

</td><td>

Source publication date

</td></tr><tr><td>

Default input field

</td><td>

Effective date

</td></tr><tr><td>

Field description

</td><td>

Effective date

</td></tr><tr><td>

Default input field

</td><td>

Compliance date

</td></tr><tr><td>

Field description

</td><td>

Compliance date

</td></tr><tr><td>

Default input field

</td><td>

Enriched insights

</td></tr><tr><td>

Field description

</td><td>

Enriched insights

</td></tr><tr><td>

Default input field

</td><td>

Provider

</td></tr><tr><td>

Field description

</td><td>

Provider

</td></tr><tr><td>

Default input field

</td><td>

Expiration date

</td></tr><tr><td>

Field description

</td><td>

Date of expiration

</td></tr><tr><td>

Default input field

</td><td>

Type

</td></tr><tr><td>

Field description

</td><td>

Alert type

</td></tr><tr><td>

Default input field

</td><td>

Citation

</td></tr><tr><td>

Field description

</td><td>

Citation

</td></tr><tr><td>

Default input field

</td><td>

State

</td></tr><tr><td>

Field description

</td><td>

State

</td></tr><tr><td>

Default input field

</td><td>

Stage

</td></tr><tr><td>

Field description

</td><td>

Stage

</td></tr><tr><td>

Default input field

</td><td>

Overall impact

</td></tr><tr><td>

Field description

</td><td>

Overall impact

</td></tr><tr><td>

Default input field

</td><td>

Source

</td></tr><tr><td>

Field description

</td><td>

Source

</td></tr><tr><td>

Default input field

</td><td>

Functional domain

</td></tr><tr><td>

Field description

</td><td>

Functional domain

</td></tr><tr><td>

Default input field

</td><td>

Created

</td></tr><tr><td>

Field description

</td><td>

Date of alert creation

</td></tr><tr><td>

Default input field

</td><td>

Moved to impact assessment

</td></tr><tr><td>

Field description

</td><td>

Date the alert state changed to Impact assessment

</td></tr><tr><td>

Default input field

</td><td>

Moved to progress

</td></tr><tr><td>

Field description

</td><td>

Date the alert state changed to In progress.

</td></tr><tr><td>

Default input field

</td><td>

Closed on

</td></tr><tr><td>

Field description

</td><td>

Date the alert was closed

</td></tr><tr><td class="sub-head" colspan="2">

Add rule conditions to the input template

</td></tr><tr><td>

Rule condition

</td><td>

Rule conditions determine when the input template is used. By default, the record state determines which input template the LLM uses.

</td></tr><tr><td class="sub-head" colspan="2">

Add additional input data sourcesYou can add input data sources like related tables, activity streams, and relationships to provide more context to the LLM. You can also add rule conditions to these additional data sources.

</td></tr><tr><td colspan="2">

Taxonomy

</td></tr><tr><td>

Related table

</td><td>

Regulatory alert to taxonomy-&gt;Regulatory alert

</td></tr><tr><td>

Related Table Field

</td><td>

Taxonomy

</td></tr><tr><td>

Field description

</td><td>

Taxonomy name

</td></tr><tr><td>

Related Table Field

</td><td>

Class

</td></tr><tr><td>

Field description

</td><td>

Taxonomy category

</td></tr><tr><td colspan="2">

Impacted area

</td></tr><tr><td>

Related table

</td><td>

Impacted area-&gt;Regulatory alert

</td></tr><tr><td>

Related Table Field

</td><td>

Impacted area table

</td></tr><tr><td>

Field description

</td><td>

Impacted area type

</td></tr><tr><td>

Related Table Field

</td><td>

Impacted area

</td></tr><tr><td>

Field description

</td><td>

Impacted area table

</td></tr><tr><td>

Related Table Field

</td><td>

AI-assisted

</td></tr><tr><td>

Field description

</td><td>

AI-assisted

</td></tr><tr><td colspan="2">

Regulatory change task

</td></tr><tr><td>

Related table

</td><td>

Regulatory Change Task-&gt;Regulatory alert

</td></tr><tr><td>

Related Table Field

</td><td>

Number

</td></tr><tr><td>

Field description

</td><td>

Task number

</td></tr><tr><td>

Related Table Field

</td><td>

Short description

</td></tr><tr><td>

Field description

</td><td>

Task description

</td></tr><tr><td>

Related Table Field

</td><td>

State

</td></tr><tr><td>

Field description

</td><td>

Task state

</td></tr><tr><td>

Related Table Field

</td><td>

Assigned to

</td></tr><tr><td>

Field description

</td><td>

Assignee

</td></tr><tr><td>

Related Table Field

</td><td>

Due date

</td></tr><tr><td>

Field description

</td><td>

Due date

</td></tr></tbody>
</table>