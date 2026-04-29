---
title: Domain Separation and Appointment Booking
description: Domain separation is supported for Appointment Booking. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
release: australia
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure Appointment Booking, Configuring Appointment Booking, Additional scheduling configuration options, Setting up a Field Service scheduling method, Configure, Field Service Management]
---

# Domain Separation and Appointment Booking

Domain separation is supported for Appointment Booking. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

## Support level: Basic



-   Business logic: Ensure that data goes into the proper domain for the application’s service provider use cases.
-   The application supports domain separation at run time. The domain separation includes separation from the user interface, cache keys, reporting, rollups, and aggregations.
-   The owner of the instance must set up the application to function across multiple tenants.

Sample use case: When a service provider \(SP\) uses chat to respond to a tenant-customer’s message, the customer must be able to see the SP's response.

For more information on support levels, see [Application support for domain separation](https://www.servicenow.com/docs/access?context=domain-separated-apps&version=australia&pubname=australia-platform-security&ft:locale=en-US).

## Domain separation and Appointment Booking overview

Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

## How domain separation works in Appointment Booking

Domain separation adds the following fields and attributes to Appointment Configuration tables:

<table id="tableID-appointment_configuration_tables_with_domain_separation"><thead><tr><th>

Table

</th><th>

Fields and Attributes

</th></tr></thead><tbody><tr><td>

Appointment Booking Configuration\[sn\_apptmnt\_booking\_config\]

</td><td>

Fields-   Domain ID
-   Domain Path

</td></tr><tr><td>

Appointment Booking Service Configuration\[sn\_apptmnt\_booking\_service\_config\]

</td><td>

Fields-   Domain ID
-   Domain Path

</td></tr><tr><td>

Service Configuration Rule\[sn\_appmnt\_booking\_config\_rule\]

</td><td>

Attributes:

 domain\_master=sn\_apptmnt\_bookig\_service\_config

</td></tr><tr><td>

Advanced Configurations\[sn\_appmnt\_booking\_day\_configuration\]

</td><td>

Attributes

 domain\_master=sn\_apptmnt\_bookig\_service\_config

</td></tr><tr><td>

Appointment Booking Lock\[sn\_appmnt\_booking\_lock\]

</td><td>

Fields-   Domain ID
-   Domain Path

</td></tr><tr><td>

Appointment Recommendation\[sn\_apptmnt\_recommendation\]

</td><td>

Fields-   Domain ID
-   Domain Path

</td></tr></tbody>
</table>**Related topics**  


[Domain separation for service providers](https://www.servicenow.com/docs/access?context=domain-sep-landing-page&version=australia&pubname=australia-platform-security&ft:locale=en-US)

