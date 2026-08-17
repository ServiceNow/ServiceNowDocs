---
title: AI Control Tower Value reference
description: Find more information about the roles, tables, and the different system properties that are used in Value insights.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/measure-ai-value-reference.html
release: australia
topic_type: concept
last_updated: "2026-05-27"
reading_time_minutes: 1
breadcrumb: [Measure AI impact and value, Measure AI impact, AI Control Tower, Enable AI experiences]
---

# AI Control Tower Value reference

Find more information about the roles, tables, and the different system properties that are used in Value insights.

## Value roles

use the following roles to create and map the value templates.

|Roles|Description|
|-----|-----------|
|AI steward \[sn\_ai\_g overnance\_ai\_steward\]|AI Stewards control which assets get value measurement enabled \(by managing Managed vs. Unmanaged state\), and they view and interpret the Value dashboard.|
|AI asset owner \[sn\_ai\_asset\_mgmt.ai\_asset\_owner\]|The AI Asset Owner is accountable for the accuracy, lifecycle progression, and value realization of assigned AI assets.|

## System properties

The following systems properties are used in value templates.

<table id="table_v1v_12d_dkc"><thead><tr><th>

System property

</th><th>

Definition

</th></tr></thead><tbody><tr><td>

look\_back\_data\_value\_calc

</td><td>

Specifies the number of days of historical data to display for AI systems newly marked as Managed.**Note:** Existing Managed AI systems are unaffected and the older data is excluded.

Default value is **60**.

</td></tr><tr><td>

value.job.user

</td><td>

Verifies if the user is assigned for value calculation jobs when the Sys\_admin user assigned is not active.**Note:** This user does not require any additional privileges.

Default value role is **admin**.

</td></tr></tbody>
</table>