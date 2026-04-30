---
title: Domain separation and EMR Help
description: In the short description, edit the first sentence to state whether domain separation is supported or not and add the application name. Keep the conkeyref at the end that describes domain separation.Domain separation is supported for EMR Help. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
release: yokohama
product: EMR Help
classification: emr-help
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [EMR Help reference, EMR Help, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Domain separation and EMR Help

Domain separation is supported for EMR Help. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

## Support level: Basic



-   Business logic: Ensure that data goes into the proper domain for the application’s service provider use cases.
-   The application supports domain separation at run time. The domain separation includes separation from the user interface, cache keys, reporting, rollups, and aggregations.
-   The owner of the instance must set up the application to function across multiple tenants.

Sample use case: When a service provider \(SP\) uses chat to respond to a tenant-customer’s message, the customer must be able to see the SP's response.

For more information on support levels, see [Application support for domain separation](https://www.servicenow.com/docs/access?context=domain-separated-apps&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US).

## EMR Help domain seperation overview

The EMR Help application includes domain separation for configuration tables \(request definition, request parameters, and definition to parameter mapping\) as well as domain separation for transactional data like tasks and associated request data coming in from the EMR system.

Domain separation is enabled in the following aspects of the EMR Help application:

-   Data stored in the Remote Request Data \[sn\_ind\_rmt\_help\_request\_data\] table is domain separated.
-   Tasks created when raised either from a record producer or using a REST API are domain separated.
-   Request parameters can be created for use in different domains.
-   Request definitions can be created for use in different domains.
-   Request definition mappings can be created for use in different domains.

## How domain separation works in EMR Help

For customers using an EMR Help service portal within their EMR systems to raise ServiceNow IT service requests, the domain is set from the logged-in user’s session, in the task created, and the associated request data.

For customers using the Remote help request API, an administrator can domain separate a task and the associated remote request data by sending any of the following parameters in the **task\_parameters** object while creating the request.

-   Task for user \(task\_for\)

    **Note:** Valid for all task types.

-   Caller \(caller\_id\)

    **Note:** Valid only for the Incident \[incident\] table.


For incident, the task’s domain is set from the `caller_id` parameter if specified in the request body. When the `caller_id` parameter isn't specified, the task’s domain is set as the domain of the user specified in the `task_for` parameter. If neither of these parameters are specified in the request body, the task's domain is set from the domain of the authenticated user invoking the Remote help request API.

## Domain separated tables

-   Remote Request Definition \(sn\_ind\_rmt\_help\_request\_defn\)
-   Remote Request Parameter \(sn\_ind\_rmt\_help\_request\_param\)
-   Request configuration mapping \(sn\_ind\_rmt\_help\_defn\_param\_data\_map\)
-   Remote Request Data \(sn\_ind\_rmt\_help\_request\_data\) and its extended child data tables
-   Task \[task\]

**Parent Topic:**[EMR Help reference](../reference/emr-reference.md)

**Related topics**  


[Domain separation for service providers](https://www.servicenow.com/docs/access?context=domain-sep-landing-page&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US)

