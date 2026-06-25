---
title: Employee Profile upgrade scenarios
description: After upgrading Employee Profile to version 11.0.3, the profile pages on all portals are updated based on the following scenarios.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/employee-experience-foundation/emp-profile-upgrade.html
release: australia
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configure Employee Profile for a portal, Employee profile, Setup task management, Configuring Employee Center, Employee Center, Unified Employee Experience, Employee Service Management]
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

**Note:** To disable the widget overview panel, you must create a profile portal configuration. For more information, see [Configure Employee Profile for a portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/employee-experience-foundation/create-portal-profile-config.md).

-   If an Employee Profile header configuration record doesn't exist, the [default record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/employee-experience-foundation/default-profile-header.md) is used.
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
-   If an Employee Profile header configuration record doesn’t exist, the [default record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/employee-experience-foundation/default-profile-header.md) is used.
-   If an Employee Profile header configuration record exists, it’s updated with the following fields and values:
    -   Action Groups: Filled from the widget instance options
    -   Background Image: Selected
    -   Edit Images: Selected
    -   Disable Links: Cleared

</td></tr></tbody>
</table>**Parent Topic:**[Employee Center reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/employee-experience-foundation/emp-center-reference.md)

**Related topics**  


[Activity Configuration form]()

[Activity Configuration Detail form]()

[Approvals experience reference]()

[Connected Content form]()

[Default Employee Profile Header Configuration record]()

[Employee Center widgets]()

[Employee Profile form]()

[Employee Profile Header Configuration form]()

[Employee Profile portal configuration form]()

[Enhanced Requests Experience forms]()

[External Link form]()

[Featured Content form]()

[Footer form]()

[Footer Menus form]()

[Guided Self-Service reference]()

[Menu Item form]()

[Overview section form]()

[Portal notification configuration form]()

[Portal notification content form]()

[Trigger conditions form]()

[Quick Link form]()

[Tab widget mapping form]()

[Taxonomy form]()

[Topic form]()

[User Criteria form]()

[User Criteria output]()

[Schedule appointment form]()

[Location Consent form]()

[Website configuration form]()

