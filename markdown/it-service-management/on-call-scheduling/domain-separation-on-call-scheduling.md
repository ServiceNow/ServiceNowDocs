---
title: Domain separation and On-Call Scheduling
description: Domain separation is supported in On-Call Scheduling. The On-Call Scheduling application helps you to ensure that dedicated support team members are available to resolve issues as they arise. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
release: zurich
product: On-Call Scheduling
classification: on-call-scheduling
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Reference, On-Call Scheduling, IT Service Management]
---

# Domain separation and On-Call Scheduling

Domain separation is supported in On-Call Scheduling. The On-Call Scheduling application helps you to ensure that dedicated support team members are available to resolve issues as they arise. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

## Support level: Standard

-   Includes all aspects of **Basic** level support.
-   Application properties are domain-aware as needed.
-   Business logic: The service provider \(SP\) creates or modifies processes per customer. The use cases reflect proper use of the application by multiple SP customers in a single instance.
-   The instance owner must configure the minimum viable product \(MVP\) business logic and data parameters per tenant as expected for the specific application.

Sample use case: An Admin must be able to make comments required when a record closes for one tenant, but not for another.

For more information on support levels, see [Application support for domain separation](https://www.servicenow.com/docs/access?context=domain-separated-apps&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

## On-Call Scheduling domain separation overview

-   On-Call Scheduling behaves the same with domain support as it does without domain support. Customers have the same ability to create and maintain on-call shifts.

-   A shift includes a selection of users from a group. It uses the base-system Advanced Schedules Support plugin to specify when the shift is active.


## How domain separation works in On-Call Scheduling

With domain separation enabled, a user with the rota\_admin role uses the Create New Schedule wizard to generate schedules in the group's domain. All generated related records for the new schedule are created with a matching domain.

This setup is enforced with a combination of the domain field and the **domain\_master** attribute. The attribute is used to derive the domain of the record from the master record. For the roster table, it derives the domain from the associated shift record.

## Domain-separated tables

-   Shift \[cmn\_rota\]
-   Rotation Escalation \[cmn\_rota\_escalation\]
-   Shift Escalation Set \[cmn\_rota\_escalation\_set\]
-   Shift Escalation Step Definition \[cmn\_rota\_esc\_step\_def\]
-   On-Call Group Preference \[on\_call\_group\_preference\]
-   On-Call Contact Source \[sys\_on\_call\_contact\_source\]
-   On-Call Group Template \[sys\_on\_call\_group\_template\]
-   On-Call Shift Template \[sys\_on\_call\_shift\_template\]
-   On-Call Template Contact Attempt \[on\_call\_template\_contact\_attempt\]
-   On-Call Template Contact Preference \[on\_call\_template\_contact\_preference\]
-   On-Call Template Escalation Policy \[on\_call\_template\_escalation\_policy\]
-   On-Call Template Escalation Step \[on\_call\_template\_escalation\_step\]
-   On-Call Escalation \[on\_call\_escalation\]
-   On-Call Escalation Level \[on\_call\_escalation\_level\]
-   On-Call Escalation Contact Attempt \[on\_call\_escalation\_con\_attempt\]
-   On-Call Escalation Notification \[on\_call\_escalation\_comm\]

## Tables that use the domain\_master attribute

-   Roster \[cmn\_rota\_roster\]: **domain\_master**=**rota**
-   Rota Member \[cmn\_rota\_member\]: **domain\_master**=**roster**
-   Roster Schedule Span \[roster\_schedule\_span\]: **domain\_master**=**schedule**
-   Shift Escalation Set \[cmn\_rota\_escalation\_set\]: **domain\_master**=**cmn\_rota**
-   Shift Escalation Step Definition \[cmn\_rota\_esc\_step\_def\]: **domain\_master**=**cmn\_rota\_escalation\_set**
-   On-Call Escalation Level \[on\_call\_escalation\_level\]: **domain\_master**=**escalation**
-   On-Call Escalation Contact Attempt \[on\_call\_escalation\_con\_attempt\]: **domain\_master**=**escalation\_level**
-   On-Call Escalation Notification \[on\_call\_escalation\_comm\]: **domain\_master**=**contact\_attempt**

To learn more, see [Domain support for schedules](https://www.servicenow.com/docs/access?context=domain-support-for-schedules&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)

## Use cases

For the following On-Call Scheduling features, domain separation ensures that end users \(whether they possess the itil or rota\_admin role\) are able to see only shifts accessible via their domain:

-   On-Call calendars
-   On-Call schedules
-   My Schedule reports
-   Schedule reports
-   Escalations

**Parent Topic:**[Reference for on-call scheduling](reference-for-on-call-scheduling.md)

**Related topics**  


[Domain separation for service providers](https://www.servicenow.com/docs/access?context=domain-sep-landing-page&version=zurich&pubname=zurich-platform-security&ft:locale=en-US)

