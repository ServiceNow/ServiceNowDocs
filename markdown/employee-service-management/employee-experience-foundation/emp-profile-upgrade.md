---
title: Employee Profile upgrade scenarios
description: After upgrading Employee Profile to version 11.0.3, the profile pages on all portals are updated based on the following scenarios.
locale: en-US
release: zurich
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure Employee Profile for a portal, Employee profile, Setup task management, Configure, Employee Center, Unified Employee Experience, Employee Service Management]
---

# Employee Profile upgrade scenarios

After upgrading Employee Profile to version 11.0.3, the profile pages on all portals are updated based on the following scenarios.

<table id="table_fqs_w3d_q1c"><thead><tr><th>

Portal

</th><th>

Upgrade Scenario

</th></tr></thead><tbody><tr><td>

Employee Center

</td><td>

-   All active tabs are associated with the profile page.
-   The widget overview panel is visible.

**Note:** To disable the widget overview panel, you must create a profile portal configuration. For more information, see [Configure Employee Profile for a portal](../task/create-portal-profile-config.md).

-   If an Employee Profile header configuration record doesn't exist, the [default record](default-profile-header.md) is used.
-   If an Employee Profile header configuration record exists, it’s updated with the following fields and values:
    -   Action Groups: Filled from the widget instance options
    -   Background Image: Selected
    -   Edit Images: Selected
    -   Disable Links: Cleared

</td></tr><tr><td>

Custom portal

</td><td>

-   All tabs are associated and visible on the profile page.
-   The widget overview panel is visible.
-   If an Employee Profile header configuration record doesn’t exist, the [default record](default-profile-header.md) is used.
-   If an Employee Profile header configuration record exists, it’s updated with the following fields and values:
    -   Action Groups: Filled from the widget instance options
    -   Background Image: Selected
    -   Edit Images: Selected
    -   Disable Links: Cleared

</td></tr></tbody>
</table>