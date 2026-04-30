---
title: Retail KPI JSON parameters
description: JSON parameters define aspects of the Retail KPI list widget on the portal page.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Add and configure the Retail KPI widget, Set up Retail Portal, Configure, Retail]
---

# Retail KPI JSON parameters

JSON parameters define aspects of the Retail KPI list widget on the portal page.

**Note:**  This information assumes that you’re familiar with the JSON code format.

<table id="table_h41_nyj_c2c"><tbody><tr><td>

**Field**

</td><td>

**Description**

</td></tr><tr><td>

title

</td><td>

Placeholder title to understand configuration done for related party types and their reports or KPIs.

</td></tr><tr><td>

relatedPartyTypes

</td><td>

Array of related party type sys\_ids \(Table: \[sn\_customerservice\_related\_party\_configuration\]\) to whom the mentioned reports should be shown.

</td></tr><tr><td>

reports

</td><td>

Array of reports where each report has information about the report\_id and link to navigate to.

</td></tr><tr><td>

report\_id

</td><td>

sys\_id of the report that is to be shown \(Table: \[sys\_report\]\).

</td></tr><tr><td>

link

</td><td>

Web page that is accessed when the KPI is selected.

</td></tr><tr><td>

order

</td><td>

Number field that defines the order of execution. The lower value is evaluated first.

</td></tr></tbody>
</table>