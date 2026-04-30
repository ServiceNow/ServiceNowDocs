---
title: Security incidents created from events and alerts
description: As events are imported from alert monitoring tools, they are first processed by Event Management and grouped into alerts. These alerts can be used to create security incidents based on customizable alert rules, or manually reviewed to select those alerts to be investigated as a security incident.
locale: en-US
release: zurich
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Security incident automatic creation, Security incident creation, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Security incidents created from events and alerts

As events are imported from alert monitoring tools, they are first processed by Event Management and grouped into alerts. These alerts can be used to create security incidents based on customizable alert rules, or manually reviewed to select those alerts to be investigated as a security incident.

You can find a sample alert rule called **Create security incidents from critical alerts** in the Alert Rules module of the Event Management application. This alert rule automatically creates security incidents when critical security-related events are received from within ServiceNow or from third-party monitoring applications. After the security incident has been created, it will be updated as new events are received. You can modify the task template in the alert rule to change the initial values for the security incident created by this alert rule. To handle each distinct variety of security incident that you would like to create, you can define other alert rules with different conditions.

Alternatively, if you are a user with the Security Admin role, you can manually create a security incident by clicking the **Create Security Incident** button from any suspicious alert.

It is important that the events received from external tools include the following information:

-   The node set to the name, IP address, or sys\_id of the CI that becomes the affected resource.
-   The event classification is set to Security to distinguish them from other IT events.
-   The event description, which populates the description of the security incident.
-   The additional information can include any extra information that does not fit into the previously listed fields or other event fields, such as the category, attack vectors, return URL, or correlation ID. The format is a string that lists field names along with their values, using the following JSON format:

    ```
    { "fieldName" : "fieldValue", "fieldName" : "fieldValue" }
    ```


**Note:** For each field and value pair, if the field in the security incident where the column name matches the fieldName is empty, it is set to the fieldValue. If the field in the security incident is not empty, it is not changed. In either case, the event and all the fields and values encoded in the additional information are recorded in a work notes entry describing the event. If nothing changes in the security incident, a work note entry is not created. Any fields in a security incident, including custom fields you add to the table, can be set.

