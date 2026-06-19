---
title: Inputs and triggers for Now Assist for Threat Intelligence Security Center
description: You can configure some of the inputs or triggers for a generative AI skill. Inputs or triggers permit you to determine how and when a skill is used.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/security-operations/input-triggers-now-assist-tisc.html
release: australia
product: Security Operations
classification: security-operations
topic_type: reference
last_updated: "2026-05-18"
reading_time_minutes: 1
keywords: [Now Assist TISC, Threat Intelligence Security Center]
breadcrumb: [Configure, Now Assist for Threat Intelligence Security Center, Security Operations]
---

# Inputs and triggers for Now Assist for Threat Intelligence Security Center

You can configure some of the inputs or triggers for a generative AI skill. Inputs or triggers permit you to determine how and when a skill is used.

## Inputs and triggers

Inputs identify the data used for a skill. Inputs include the table and fields used to generate a threat case summary. A trigger initiates an action. For example, triggers determine when the system generates a summary.

You can modify inputs and triggers, but you can't modify a skill's data source. The data source contains the tables and fields that the skill relies on.

## Case Summarization skill

Inputs for the Case Summarization skill identify the table and fields used when a threat case summary is generated. The following table lists the inputs for the Case Summarization skill from the Choose Input page in the Now Assist Admin console.

<table id="table_tisc_case_summ_inputs"><thead><tr><th>

Input

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Data source

</td><td>

Case \[sn\_sec\_tisc\_case\] table.

</td></tr><tr><td>

Input fields

</td><td>

-   Short description
-   Description
-   State
-   Priority
-   Work notes
-   Automation Activity
-   Case Type
-   Notes
-   Analysis and Findings
-   Contributors
-   TLP
-   Recommendations or Actions
-   Due date
-   Updated
-   Closure Summary \(available when the case is in a closed state\)

</td></tr><tr><td>

Related Input tables

</td><td>

-   MITRE Techniques
-   Related Observables
-   Related Indicators
-   Related Objects
-   Affected Assets
-   Affected Services
-   Case Task

</td></tr></tbody>
</table>