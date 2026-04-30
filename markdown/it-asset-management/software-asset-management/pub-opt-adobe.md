---
title: Publisher optimizations for Adobe
description: View licensing optimizations for Adobe by selecting Adobe from the Publisher drop-down list.
locale: en-US
release: yokohama
product: Software Asset Management
classification: software-asset-management
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Software Asset Management references, Software Asset Management, IT Asset Management]
---

# Publisher optimizations for Adobe

View licensing optimizations for Adobe by selecting **Adobe** from the **Publisher** drop-down list.

<table id="table_lq5_ppf_fxb"><thead><tr><th>

Report

</th><th>

Source

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Creative Cloud user activity as per subscription

</td><td>

Software Subscriptions\[samp\_sw\_subscription\]

</td><td>

Number of user subscriptions per month with meaningful activity. This report displays data for all of your Adobe Creative Cloud All Apps subscriptions for the last 12 months.Select any data point to view the last activity date of user subscriptions with meaningful activity for a given subscription type.

</td></tr><tr><td>

Creative Cloud potential savings by type

</td><td>

Removal Candidate\[samp\_sw\_reclamation\_candidate\]

</td><td>

Potential monthly savings for your Adobe Creative Cloud All Apps licenses that are based on low usage, double licensed users, and consolidated subscriptions. This report displays potential savings for the last 12 months.-   **Low usage**: The Adobe Creative Cloud applications not being used for more than 60 days.
-   **Dual licensed users**: A user having subscription through both Adobe Creative Cloud All Apps and individual Adobe Creative Cloud applications.
-   **Consolidated subscriptions**: A user having multiple individual Adobe applications \(greater than 3 by default\) and all these subscriptions are consolidated to one Adobe Creative Cloud All Apps subscription.

</td></tr><tr><td>

Inactive user subscriptions

</td><td>

Software Subscriptions\[samp\_sw\_subscription\]

</td><td>

Number of inactive user subscriptions in the User \[sys\_user\] table of your ServiceNow instance based on the user status.

</td></tr><tr><td>

Unresolved user subscriptions

</td><td>

Software Subscriptions\[samp\_sw\_subscription\]

</td><td>

Number of users not having a record in the User \[sys\_user\] table of your ServiceNow instance.

</td></tr></tbody>
</table>**Parent Topic:**[Software Asset Management references](references.md)

**Related topics**  


[Integrating with Adobe Cloud](../concept/adobe-cloud-integration.md)

