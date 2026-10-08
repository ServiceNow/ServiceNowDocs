---
title: Skill inputs for risk skills
description: Table and field inputs for the risk signal and issues summarization, and draft risk closure notes, skills.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/acct-lifecycle-events/account-lifecycle-otto-skill-inputs-risk.html
release: brazil
topic_type: reference
last_updated: "2026-09-22"
reading_time_minutes: 1
keywords: [skill inputs, risk]
breadcrumb: [Skill inputs, Reference, Customer Success Management]
---

# Skill inputs for risk skills

Table and field inputs for the risk signal and issues summarization, and draft risk closure notes, skills.

## Risk signal and issues summarization skill

Includes the inputs that identify the table and fields used when a risk signal and issues summary is generated.

<table id="table_inputs_risk_signal_1"><thead><tr><th>

Input

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Input table

</td><td>

Risk signal and issues

</td></tr><tr><td>

Input fields

</td><td>

-   Account Name
-   Priority
-   Description
-   Short description
-   State
-   Source record
-   Category Name
-   Probability

</td></tr></tbody>
</table><table id="table_inputs_risk_signal_2"><thead><tr><th>

Input

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Input table

</td><td>

Risk solution

</td></tr><tr><td>

Input fields

</td><td>

-   Source record
-   Source table
-   impacted\_record
-   impacted\_table

</td></tr></tbody>
</table>## Draft risk closure notes summarization skill

Automatically generates closure notes and closes eligible risk signals at the end of each day based on the status of their associated risk solutions.

<table id="table_inputs_risk_closure"><thead><tr><th>

Input

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Input table

</td><td>

Risk signal and issues

</td></tr><tr><td>

Input fields

</td><td>

-   Account Name
-   Priority
-   Description
-   Short description
-   State
-   Source record
-   Category Name
-   Probability

</td></tr></tbody>
</table>**Parent Topic:**[Skill inputs for ServiceNow Otto for Customer Success Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/acct-lifecycle-events/account-lifecycle-otto-skill-inputs-reference.md)

