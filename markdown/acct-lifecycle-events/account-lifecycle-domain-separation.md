---
title: Domain separation and Customer Success Management
description: If any conkeyrefs are broken, re-add them from the doc/source/reuse/domain-separation/domain-separation-overview.dita file.In the short description, edit the first sentence to state whether domain separation is supported or not and add the application name. Keep the conkeyref at the end that describes domain separation.Domain separation is supported for Customer Success Management. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Reference, Customer Success Management]
---

# Domain separation and Customer Success Management

Domain separation is supported for Customer Success Management. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

## Support level: Basic



-   Business logic: Ensure that data goes into the proper domain for the application’s service provider use cases.
-   The application supports domain separation at run time. The domain separation includes separation from the user interface, cache keys, reporting, rollups, and aggregations.
-   The owner of the instance must set up the application to function across multiple tenants.

Sample use case: When a service provider \(SP\) uses chat to respond to a tenant-customer’s message, the customer must be able to see the SP's response.

For more information on support levels, see [Application support for domain separation](https://www.servicenow.com/docs/access?context=domain-separated-apps&version=australia&pubname=australia-platform-security&ft:locale=en-US).

## Overview of Customer Success Management

With the Customer Success Management application, you can create onboarding cases and related onboarding case tasks, track objectives, outcomes, and define documented plans to ensure success. The account onboarding case and related tasks support domain separation at the account level. Engagements, objectives, outcomes, initiatives, success cases, risk signals and internal plays are domain separated at the account level.

## How domain separation works in Customer Success Management

-   Account onboarding cases, onboarding tasks, and data import case tasks are domain separated using the account domain.
-   All other staging tables used for the Data Import are not domain separated.
-   All customer success tables are domain separated.

## Setting up domain separation in Customer Success Management

Domain separation for Customer Success Management requires the domain separation plugin and enabling the csm\_auto\_account\_domain\_generation domain separation property. For more information on setting up domain separation, see [Domain separation and Customer Service Management](https://www.servicenow.com/docs/access?context=domain-separation-customer-service&version=australia&pubname=australia-customer-service-management&ft:locale=en-US).

## Domain separated tables

-   Account onboarding case \[sn\_acct\_lc\_onb\_case\]
-   Data import task \[sn\_ti\_core\_imp\_task\]
-   Onboarding task \[sn\_ti\_core\_task\]
-   Engagement \[sn\_acct\_lc\_engagement\]
-   Success objective \[sn\_acct\_lc\_success\_objective\]
-   Success outcome \[sn\_acct\_lc\_success\_outcome\]
-   Success initiative \[sn\_acct\_lc\_success\_initiative\]
-   Customer play \[sn\_acct\_lc\_success\_case\]
-   Success task \[sn\_acct\_lc\_success\_task\]
-   Touchpoint \[sn\_acct\_lc\_touchpoint\]
-   Internal play \[sn\_acct\_lc\_internal\_play\]
-   Internal play task \[sn\_acct\_lc\_internal\_play\_task
-   Risk Signal and Issue \(sn\_acct\_lc\_risk\_signal\_issue\)
-   Implementation Record \(sn\_acct\_lc\_implementation\_record\)
-   Risk Solution \(sn\_acct\_lc\_risk\_signal\_solution\_relationship\)
-   Engagement Health Definition \(sn\_acct\_lc\_eng\_hlt\_def\)
-   Health Metric Configuration \(sn\_acct\_lc\_eng\_hlt\_mtr\_config\)
-   Engagement Risk Definition \(sn\_acct\_lc\_eng\_risk\_def\)
-   Risk Threshold Override \(sn\_acct\_lc\_risk\_threshold\_override\)
-   Risk Occurrence \(sn\_acct\_lc\_risk\_occurrence\)
-   Data Source \(sn\_data\_ctx\_engine\_src\)
-   Context Engine Mapper \(sn\_data\_ctx\_engine\_map\)
-   Context \(sn\_data\_ctx\_engine\_ctx\)
-   Context Engine Data \(sn\_data\_ctx\_engine\_data\)
-   Segment \(sn\_data\_ctx\_engine\_brkdwn\_seg\)
-   Segment Configuration \(sn\_data\_ctx\_engine\_seg\_conf\)
-   DCE Insight \(sn\_data\_ctx\_engine\_insight\)
-   DCE Insight Item \(sn\_data\_ctx\_engine\_insight\_item\)
-   DCE Visualization \(sn\_data\_ctx\_engine\_visualization\)
-   DCE Visualization M2M \(sn\_data\_ctx\_engine\_visualization\_m2m\)
-   Product Capability \(sn\_prod\_cap\_core\_prod\_cap\)
-   Product Capability Map \(sn\_prod\_cap\_core\_prod\_cap\_map\)
-   Capability Relationship Map \(sn\_prod\_cap\_core\_cap\_rel\_map\)
-   Product Usage \(sn\_prod\_cap\_core\_prod\_usage\)
-   Product Capability Usage \(sn\_prod\_cap\_core\_prod\_cap\_usage\)

**Parent Topic:**[Customer Success Management reference](../reference/account-lifecycle-reference.md)

**Related topics**  


[Domain separation for service providers](https://www.servicenow.com/docs/access?context=domain-sep-landing-page&version=australia&pubname=australia-platform-security&ft:locale=en-US)

