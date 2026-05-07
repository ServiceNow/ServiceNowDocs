---
title: Personas for consumers
description: Learn about the different personas in the Service Exchange application.
locale: en-US
release: australia
product: Service Exchange
classification: service-exchange
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure for consumers, Service Exchange for Consumers, Service Exchange]
---

# Personas for consumers

Learn about the different personas in the Service Exchange application.

Remote record producers can be associated with personas. If a remote record producer does not have a persona, any user with the Service Exchange Requestor role can place an order for the item. However, if one or more personas are assigned to a remote record producer, the user must have the Requestor role and at least one of the listed personas. Personas are assigned to users through the Authorized Users table. To access items protected by personas, the user's Authorized User record must be approved by the provider, activated in the consumer instance, and have the appropriate persona\(s\).

<table id="table_h2n_nkm_cmb"><thead><tr><th>

Persona

</th><th>

Skills

</th><th>

Tasks

</th><th>

Roles

</th></tr></thead><tbody><tr><td>

System administrator

</td><td>

Is a certified ServiceNow system administrator

</td><td>

-   Creates provider and connection records.
-   Installs the Service Exchange applications.
-   Creates and maintains transforms.
-   Activates published remote task definitions and remote record producers.
-   Troubleshoots Service Exchange transport payloads.

</td><td>

-   admin
-   sn\_sb.admin
-   sn\_transport.admin

</td></tr><tr><td>

Service Exchange Requester

</td><td>

Is an IT administrator

</td><td>

-   Responsible for some form of IT service that is either completely or in part supported by one or more external vendors.
-   Requests and monitors the service requests that are placed with the external provider from their own instance.

</td><td>

-   itil
-   sn\_sb.requestor

</td></tr><tr><td>

Consumer Requestor

</td><td>

End user

</td><td>

Makes requests from the Remote Catalog.

</td><td>

sn\_sb.requestor

</td></tr></tbody>
</table>