---
title: Components installed with Digital Experience Score​
description: Several types of components are installed with activation of the Digital Experience Score​ app, including tables and user roles.
locale: en-US
release: australia
product: Digital Experience Score
classification: digital-experience-score
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Reference, Digital Experience Score, Digital End-User Experience, IT Service Management]
---

# Components installed with Digital Experience Score​

Several types of components are installed with activation of the Digital Experience Score​ app, including tables and user roles.

## Roles installed

<table id="table_ekr_sp5_lyb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Dashboard Application Pages User

 \[sn\_dex\_score.dashboard\_application\_pages\_user\]

</td><td>

Can access only the application pages on the Digital Experience Score​ dashboard.

</td><td>

None

</td></tr><tr><td>

Dashboard Device Pages User

 \[sn\_dex\_score.dashboard\_device\_pages\_user\]

</td><td>

Can access only the device pages on the Digital Experience Score​ dashboard.

</td><td>

None

</td></tr><tr><td>

Dashboard User

 \[sn\_dex\_score.dashboard\_user\]

</td><td>

Can access Digital Experience Score​ dashboard.

</td><td>

sn\_sow.sow\_user

</td></tr><tr><td>

Digital Workplace Leader

 \[sn\_dex\_score.digital\_workplace\_leader\]

</td><td>

Allows users to use the Digital Experience Score​ dashboard. Can configure the metric definition, DEX Score system properties, qualitative mapping for the metric scores, and survey configuration.

</td><td>

-   sn\_dex\_score.dashboard\_user
-   sn\_dex\_feedbck\_sur.dex\_feedback\_survey\_admin
-   sn\_dex.user

</td></tr></tbody>
</table>## Tables installed

<table id="table_ikr_sp5_lyb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

DEX Score Hierarchy Weights

 \[dex\_score\_hierarchy\_weights\]

</td><td>

Stores the weights for health metrics, user sentiment experience metrics, and service experience metrics defined at the application experience, device experience, and overall DEX experience scoring levels.

</td></tr><tr><td>

DEX Score Metric Definition

 \[dex\_score\_metric\_definition\]

</td><td>

Stores the metric definition with predefined values for the upper bound, lower bound, and other info.

</td></tr></tbody>
</table>**Parent Topic:**[Digital Experience Score​ reference](../concept/dexscr-dex-score-reference.md)

