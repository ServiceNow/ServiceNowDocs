---
title: Components installed with Now Assist for HR - Galileo Inside
description: Information about the roles and scheduled jobs that are installed.
locale: en-US
release: zurich
product: Now Assist for HRSD
classification: now-assist-for-hrsd
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Reference, Now Assist for HR Service Delivery \(HRSD\), HR Service Delivery, Employee Service Management]
---

# Components installed with Now Assist for HR - Galileo Inside

Information about the roles and scheduled jobs that are installed.

<table id="id_d2n_jcw_nbc"><thead><tr><th>

Role

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_hr\_na\_galileo.admin

</td><td>

Is auto-assigned to the sn\_hr\_gen\_ai\_helper.admin role.

 Grants administrative access to the Galileo data store.

</td></tr><tr><td>

sn\_hr\_na\_galileo.read

</td><td>

Enables users to receive Now Assist responses containing Galileo data

</td></tr></tbody>
</table><table id="table_l5y_yht_dfc"><thead><tr><th>

Scheduled job name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Fetch and Index Galileo data

</td><td>

Retrieves data from the Josh Bersin company. The admin first manually executes the scheduled job to begin the initial indexing.

 Subsequently, the system runs the scheduled job monthly to retrieve new data.

</td></tr></tbody>
</table>**Parent Topic:**[Reference for Now Assist for HR Service Delivery \(HRSD\)](reference-now-assist-hrsd.md)

