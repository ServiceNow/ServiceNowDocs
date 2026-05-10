---
title: Components installed with Workplace Visitor Management
description: Several types of components are installed with the Workplace Visitor Management application, including tables, user roles, and business rules.
locale: en-US
release: australia
product: Workplace Visitor Management
classification: workplace-visitor-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Reference, Workplace Visitor Management, Workplace Service Delivery, Employee Service Management]
---

# Components installed with Workplace Visitor Management

Several types of components are installed with the Workplace Visitor Management application, including tables, user roles, and business rules.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see [Find components installed with an application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/find-components.md).

Demo data is available for this feature.

## Roles installed with Workplace Visitor Management

<table id="table_wfr_4yr_cnb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Workplace visitors admin\[sn\_wsd\_visitor.admin\]

</td><td>

As an admin, you can:-   Has complete access to the application.
-   Perform all actions of a Visitor manager.
-   Access visitor logs.
-   Configure application settings.
-   View and manage the related record producers.

</td><td>

-   sn\_wsd\_visitor.manager
-   catalog\_editor
-   catalog\_admin

</td></tr><tr><td>

Workplace visitors manager\[sn\_wsd\_visitor.manager\]

</td><td>

As a manager, you can:-   Perform all actions of a Visitor staff.
-   Create, review and assign visitor policies that a visitor must accept before visiting the location.
-   View, manage, and update visitor registrations.
-   View the Visitor Reception Dashboard.
-   Register visitors.

</td><td>

sn\_wsd\_visitor.staff

</td></tr><tr><td>

Workplace reception staff\[sn\_wsd\_visitor.staff\]

</td><td>

As a reception staff, you can:-   View, manage, and update visitor registrations.
-   View and update visitor records.
-   Register visitors
-   View the Visitor Reception Dashboard.
-   Print badges for visitors.

</td><td>

sn\_wsd\_core.workplace\_user

</td></tr></tbody>
</table>## Tables installed with Workplace Visitor Management

<table id="table_fbz_45z_vdb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

User Visitor\[sn\_wsd\_visitor\_m2m\_user\_visitor\]

</td><td>

Stores information about the link between a visitor and an employee. The employee must have specified this information while registering the visitor.

</td></tr><tr><td>

Organization\[sn\_wsd\_visitor\_organization\]

</td><td>

Stores information about the visitor's organization, such as the organization's name and description.

</td></tr><tr><td>

Visit\[sn\_wsd\_visitor\_visit\]

</td><td>

Stores information about the visit. Each visitor is linked to a visit. A visit can hold multiple visitors.

</td></tr><tr><td>

Visitor\[sn\_wsd\_visitor\_visitor\]

</td><td>

Stores information about all the visitors who have visited. An employee can reuse the visitor details for future registrations.

</td></tr><tr><td>

Visitor Registration\[sn\_wsd\_visitor\_visitor\_registration\]

</td><td>

Stores information about all the visitor registrations created in the application.

</td></tr><tr><td>

Visit Log\[sn\_wsd\_visitor\_visit\_log\]

</td><td>

Stores information about the state changes that were logged during a visit.

</td></tr><tr><td>

Policy\[sn\_wsd\_visitor\_policy\]

</td><td>

Stores information about all the visitor policies created in the application.

</td></tr><tr><td>

Location Policy\[sn\_wsd\_visitor\_m2m\_location\_policy\]

</td><td>

Stores information about the visitor policies added to workplace locations.

</td></tr><tr><td>

Visitor Policy Confirmation\[sn\_wsd\_visitor\_visitor\_policy\_confirmation\]

</td><td>

Stores information about all the confirmations received for a visitor policy.

</td></tr><tr><td>

Invitations\[sn\_wsd\_visitor\_invitation\]

</td><td>

Stores information about all the invitations and the linked visit records.

</td></tr><tr><td>

Kiosk Page Configurations\[sn\_wsd\_visitor\_page\_configuration\]

</td><td>

Stores information about the pages created for Workplace Services Kiosk.

</td></tr><tr><td>

Kiosk Checkin Flow Configurations\[sn\_wsd\_visitor\_checkin\_flow\_configuration\]

</td><td>

Stores information about the check-in flows created for Workplace Services Kiosk.

</td></tr><tr><td>

Kiosk Checkout Flow Configurations\[sn\_wsd\_visitor\_checkout\_flow\_configuration\]

</td><td>

Stores information about the check-out flows created for Workplace Services Kiosk.

</td></tr><tr><td>

Kiosk Authentication Option\[sn\_wsd\_visitor\_authentication\_option\]

</td><td>

Stores information about the authentication options created for the Workplace Services Kiosk.

</td></tr><tr><td>

Visitor Authentication Option\[sn\_wsd\_visitor\_page\_m2m\_authentication\_option\]

</td><td>

Stores information about authentication options added to an authentication page configuration.

</td></tr><tr><td>

Kiosk Next Step\[sn\_wsd\_visitor\_next\_step\]

</td><td>

Store information about the next steps added to an end page configuration.

</td></tr></tbody>
</table>**Parent Topic:**[Workplace Visitor Management references](../concept/workplace-visitor-mgmt-references.md)

**Related topics**  


[Properties installed with Workplace Visitor Management](properties-installed-with-workplace-visitor-mgmt.md)

[Kiosk Check-in Flow Configuration form](kiosk-check-in-config-form.md)

[Kiosk Check-out Flow Configuration form](kiosk-check-out-config-form.md)

[Kiosk Page Configuration form](kiosk-page-config-form.md)

[Kiosk Page Customizations](kiosk-page-customizations.md)

[Location Policy form](location-policy-form.md)

[New visit form](new-visit-form.md)

[Additional requirement form](additional-req-form.md)

