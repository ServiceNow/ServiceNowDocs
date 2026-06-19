---
title: LEAP Installer fields
description: Field values that you configure when installing LEAP using the LEAP Installer.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/aiops-leap-learning-enhanced-automation-playbooks/aiops-leap-installation-fields.html
release: australia
product: AIOps LEAP \(Learning-Enhanced Automation Playbooks\)
classification: aiops-leap-learning-enhanced-automation-playbooks
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [LEAP reference, Learning Enhanced Automation Platform \(LEAP\), Now Assist for ITOM, IT Operations Management]
---

# LEAP Installer fields

Field values that you configure when installing LEAP using the LEAP Installer.

<table id="table_egn_x3m_s2c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Run frequency

</td><td>

Frequency at which LEAP runs on the configured table. This field is automatically set to Run every month.

</td></tr><tr><td>

Group records from this table

</td><td>

Table from which LEAP queries and filters records for grouping. This field is automatically set to Incident.

</td></tr><tr><td>

Use this column for grouping

</td><td>

Column from the selected table used to read records for grouping. This field is automatically set to Short description.

</td></tr><tr><td>

Use this filter

</td><td>

Condition filter used to select records for grouping. The default filter is `active=false^ORactive=true`. Modify this filter to change the scope of records that LEAP processes.**Note:** By default, incidents are grouped and filtered for the last 6 months.

</td></tr><tr><td>

Use this column for topic generation

</td><td>

Column from the selected table used to generate titles for the created groups. This field is automatically set to Short description.

</td></tr></tbody>
</table>|Field|Description|
|-----|-----------|
|Roles|Roles assigned to the ACL entry that determine who can access the skill. This field is automatically set to `sn_itom_leap.leap_genai_worker`. Roles selected here are available in the Select display step.|
| |

