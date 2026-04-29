---
title: Domain separation and the Walk-up Experience application
description: This is an overview of domain separation as it pertains to the Walk-up Experience application and how it relates to Service Portal pages, interaction queues, and configurations. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
release: australia
product: Walk-Up Experience
classification: walk-up-experience
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Walk-up Experience reference, Walk-up Experience, IT Service Management]
---

# Domain separation and the Walk-up Experience application

This is an overview of domain separation as it pertains to the Walk-up Experience application and how it relates to Service Portal pages, interaction queues, and configurations. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

## Support level: Basic



-   Business logic: Ensure that data goes into the proper domain for the application’s service provider use cases.
-   The application supports domain separation at run time. The domain separation includes separation from the user interface, cache keys, reporting, rollups, and aggregations.
-   The owner of the instance must set up the application to function across multiple tenants.

Sample use case: When a service provider \(SP\) uses chat to respond to a tenant-customer’s message, the customer must be able to see the SP's response.

For more information on support levels, see [Application support for domain separation](https://www.servicenow.com/docs/access?context=domain-separated-apps&version=australia&pubname=australia-platform-security&ft:locale=en-US).

## Walk-up Experience overview

Domain separation in the Walk-up Experience application is supported at the basic level. However, the application depends on the Service Portal, which is not supported for domain separation. Domain separation pertains to the Walk-up Experience application in the following ways:

-   Walk-up location queues support domain separation in order to define which end users can access each location queue.
-   The Interaction table supports standard domain separation for data security. Interaction tickets are opened for a specific domain.
-   Walk-up location queues and interactions support domain separation. Therefore, the agents also work within a domain-separated environment when addressing interaction tickets associated with a location queue.
-   Management and administration configurations reside in the walk-up location queue records. Therefore, those configurations are available to the respective domain managers and admins.
-   While the Service Portal pages are not domain separated, the Walk-up Experience application's portal pages retrieve data within the user’s specific domain. Therefore, those pages can be reused across different service portals designed and configured for separate domains. The admins must build each portal themselves.
-   The **Domain** field is available on the wu\_location\_queue table. Setting domain here ensures that the users only see queues that are a part of their domains during online check-in.
-   For Advanced Work Assignment routing to operate, each wu\_location\_queue must include a work item routing condition which explicitly adds a reference to the domain the queue is part of.

    **Note:** The appointment booking feature is not domain separated. Since Appointment \[itil\_appointment\] table data is not domain separated, list views could reveal data across domains.


## How domain separation works in the Walk-up Experience application

For this application to be most effective, walk-up administrators should configure walk-up locations accordingly. This is done by configuring the `wu_location_queue` record to meet the needs of requesters. Each domain configured to the location queue record has its own set of rules. The same applies to other tables within the Walk-up application as well.

**Note:** Elements of the Service Portal platform such as settings, portals and widgets cannot be domain separated. However, the data within the widgets displays based on how the domain is configured. The recommended approach is to set up separate portals for each MSP customer.

The elements of Service Portal that are used as part of the walk-up experience are as follows:

-   Portal \(Walk-up\)
-   Pages \(``walkup_online_checkin, walkup_queue_on_site, walkup_home, walkup_survey, walkup_check_in``\)
-   Theme \(Walk-up theme\)
-   Widgets \(Online check-in experience, walk-up queue on site, walk-up check-in, walk-up exit survey, walk-up home, walk-up schedule\)

To learn more, see [Domain separation and Service Portal](https://www.servicenow.com/docs/access?context=domain-separation-service-portal&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US).

For data separation, the Walk-up Experience application uses the domain of the walk-up requester to determine in which domain the requester data should be placed.

-   Requesters can check in only in locations for which they have visibility.
-   Requesters are able to select the reasons that belong only to their own domain.
-   Interaction records are created in the Requester’s domain.

The application uses the domain of the walk-up agent or admin to determine which records are visible to the agent.

-   By domain separation rules, Agents can work only on interactions that are visible to them.
-   The agents are able to configure only walk-up location records that belong to their domain, are in the global domain, or have the parent-child hierarchy.
-   The same visibility rules apply for the Many to Many `[wu_m2m_location_queue_reason]`table that controls the mapping between a location and the reason.
-   The walk-up contexts records also have domain separation support. Thereby ensuring that the agents are able to view detailed information of the Requester only for the records that are visible by domain separation rules.

## Domain-separated tables

As part of the Walk-up Experience, records in the following tables can be domain separated.

-   Walk-up location queues `[wu_location_queue]`
-   Walk-up reasons for visit `[wu_reason]`
-   Walk-up reasons `[wu_m2m_location_queue_reason]`
-   Walk-up contexts `[wu_context]`
-   Interactions `[interaction]`

**Parent Topic:**[Walk-up Experience reference](../reference/walk-up-experience-reference.md)

**Related topics**  


[Domain separation for service providers](https://www.servicenow.com/docs/access?context=domain-sep-landing-page&version=australia&pubname=australia-platform-security&ft:locale=en-US)

