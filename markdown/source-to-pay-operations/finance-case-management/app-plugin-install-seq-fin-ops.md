---
title: Application plugin installation sequence in Finance Case Management
description: View the consolidated list of plugins, high-level description of each plugin, and the dependencies that are required before installing each plugin in Finance Case Management.
locale: en-US
release: zurich
product: Finance Case Management
classification: finance-case-management
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Components installed with Finance Case Management, Install Finance Case Management, Configure, Finance Case Management, Finance and Supply Chain applications, Finance and Supply Chain]
---

# Application plugin installation sequence in Finance Case Management

View the consolidated list of plugins, high-level description of each plugin, and the dependencies that are required before installing each plugin in Finance Case Management.

## Application plugin list

<table id="table_ep1_c32_q2c"><thead><tr><th>

Plugin name

</th><th>

Description

</th><th>

Dependencies

</th></tr></thead><tbody><tr><td>

Finance Common Architecture \(sn\_fin\)

</td><td>

Maintains primary data such as Enterprise Resource Planning \(ERP\) sources, legal entities, accounting periods, and so on.

</td><td>

-

</td></tr><tr><td>

Common Service Delivery \(sn\_spend\_sdc\)

</td><td>

Contains Finance Case, Finance Case Line, and Finance Task.

</td><td>

Finance Common Architecture \(sn\_fin\)

</td></tr><tr><td>

Finance Operations Workspace \(sn\_fin\_ops\_ws\)

</td><td>

Provides a single environment for finance specialists to work on finance cases, finance tasks, and more.

</td><td>

-

</td></tr><tr><td>

Finance Case Management

 \(sn\_fin\_ops\)

</td><td>

Maintains primary data to raise, track, and resolve finance-related requests.

</td><td>

-   Finance Common Architecture \(sn\_fin\)
-   Common Service Delivery \(sn\_spend\_sdc\)
-   Finance Operations Workspace \(sn\_fin\_ops\_ws\)

</td></tr><tr><td>

Source-to-Pay Common Architecture \(snc.sn\_shop\)

</td><td>

Maintains primary data such as Enterprise Resource Planning \(ERP\) sources, legal entities, accounting periods, and so on.

</td><td>

-   Finance Common Architecture \(sn\_fin\)
-   Common Service Delivery \(sn\_spend\_sdc\)

</td></tr><tr><td>

Advanced Work Assignment for Source-to-Pay Operations \(snc.sn\_spend\_awa\)

</td><td>

Provides configurations to support automatic routing, queuing, and assignment of finance cases and emails.

</td><td>

Advanced Work Assignment \(glide.awa\)

</td></tr></tbody>
</table>**Parent Topic:**[Components installed with Finance Case Management](installed-with-fin-ops.md)

