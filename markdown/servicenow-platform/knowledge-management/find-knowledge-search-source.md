---
title: View the source of a knowledge article search
description: Analyze knowledge searches by finding the source used for searching a knowledge article.
locale: en-US
release: zurich
product: Knowledge Management
classification: knowledge-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [View knowledge logs, Configuring Knowledge Management, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# View the source of a knowledge article search

Analyze knowledge searches by finding the source used for searching a knowledge article.

## Before you begin

Role required: knowledge\_admin, knowledge\_manager

## Procedure

1.  Navigate to **All** &gt; **Knowledge** &gt; **Administration** &gt; **Search Log**.

2.  View the following data for a search record in the corresponding column of the Search log.

<table id="table_ndv_vjj_jlb"><thead><tr><th>

Column

</th><th>

Search record data

</th></tr></thead><tbody><tr><td>

Source Doc

</td><td>

Source record in the source table.For example, Problem: *problem\_number*, Case: *case\_number*, Incident: *incident\_number*, Service Portal: *Customer Support*

</td></tr><tr><td>

Source Table

</td><td>

Label and name of the source table.For example, Knowledge \[kb\_knowledge\], Service Portal \[sp\_portal\], Case \[sn\_customerservice\_case\], Incident \[incident\], Problem \[problem\], KCS Article \[kb\_template\_kcs\_article\]

</td></tr><tr><td>

Source Type

</td><td>

Application where the knowledge article search was performed.The **Source Type** column is set to one of the following values:

 -   **Portal**: Service Portal application
-   **Classic**: ServiceNow AI Platform application
-   **Workspace**: Agent assist in Workspace
-   **Knowledge Classic**: Knowledge Management v3 or v2
-   **Other**: Unidentifiable source


</td></tr><tr><td>

Source URL

</td><td>

URL of the searched text query.

</td></tr></tbody>
</table>
**Parent Topic:**[View knowledge logs](view-knowledge-logs.md)

**Related topics**  


[View knowledge logs](view-knowledge-logs.md)

