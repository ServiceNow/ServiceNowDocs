---
title: Properties installed with Smart Assessment Engine
description: System properties that control the behavior of Smart Assessment Engine.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/smart-assessment-engine/properties-installed-in-smart-assessment-engine.html
release: brazil
product: Smart Assessment Engine
classification: smart-assessment-engine
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Components installed with Smart Assessment Engine, Reference, Smart Assessment Engine, Governance, Risk, and Compliance]
---

# Properties installed with Smart Assessment Engine

System properties that control the behavior of Smart Assessment Engine.

## Properties installed with Smart Assessment Core

<table id="table_properties_core_r2s"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

`sn_smart_asmt.activity_merge_window_in_seconds`

</td><td>

Defines the maximum time gap, in seconds, allowed between consecutive changes to the same field on a question by the same user. If a change occurs within this window of the last recorded activity, the existing entry in the question's change history is updated instead of a new one being created. For more information, see [Question change history](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/smart-assessment-engine/sae-question-change-history.md).-   Type: integer
-   Default value: 300
-   Read roles: Assessment actor \[sn\_smart\_asmt.actor\], Assessment reader \[sn\_smart\_asmt.assessment\_reader\], Assessment admin \[sn\_smart\_asmt.assessment\_admin\]
-   Write role: Assessment admin \[sn\_smart\_asmt.assessment\_admin\]

</td></tr></tbody>
</table>