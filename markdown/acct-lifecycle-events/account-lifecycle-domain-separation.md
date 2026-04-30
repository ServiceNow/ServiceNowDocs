---
title: Domain separation and Customer Success Management
description: If any conkeyrefs are broken, re-add them from the doc/source/reuse/domain-separation/domain-separation-overview.dita file.In the short description, edit the first sentence to state whether domain separation is supported or not and add the application name. Keep the conkeyref at the end that describes domain separation.Domain separation is supported for Customer Success Management. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Customer Success Management reference, Customer Success Management]
---

# Domain separation and Customer Success Management

Domain separation is supported for Customer Success Management. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

## Support level: Basic



-   Business logic: Ensure that data goes into the proper domain for the application’s service provider use cases.
-   The application supports domain separation at run time. The domain separation includes separation from the user interface, cache keys, reporting, rollups, and aggregations.
-   The owner of the instance must set up the application to function across multiple tenants.

Sample use case: When a service provider \(SP\) uses chat to respond to a tenant-customer’s message, the customer must be able to see the SP's response.

For more information on support levels, see [Application support for domain separation](https://www.servicenow.com/docs/access?context=domain-separated-apps&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US).

## Customer Success Management domain separation overview

With the Customer Success Management application, you can create onboarding cases and related onboarding case tasks, track objectives, outcomes, and define documented plans to ensure success. The account onboarding case and related tasks support domain separation at the account level. Engagements, objectives, outcomes , initiatives, success cases, risk signals and internal plays are domain separated at the account level.

## How domain separation works in Customer Success Management

-   Account onboarding cases, account lifecycle tasks, and account lifecycle import case tasks are domain separated using the account domain.
-   All other staging tables used for the Data Import are not domain separated.
-   All customer success tables are domain separated.

## Setting up domain separation in Customer Success Management

Domain separation for Customer Success Management requires the domain separation plugin and enabling the csm\_auto\_account\_domain\_generation domain separation property. For more information on setting up domain separation, see [Domain separation and Customer Service Management](https://www.servicenow.com/docs/access?context=domain-separation-customer-service&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US).

## Domain separated tables

-   Account onboarding case \[sn\_acct\_lc\_onb\_case\]
-   Account lifecycle import task \[sn\_ti\_core\_imp\_task\]
-   Account lifecycle task \[sn\_ti\_core\_task\]
-   Engagement \[sn\_acct\_lc\_engagement\]
-   Success objective \[sn\_acct\_lc\_success\_objective\]
-   Success outcome \[sn\_acct\_lc\_success\_outcome\]
-   Success initiative \[sn\_acct\_lc\_success\_initiative\]
-   Success case \[sn\_acct\_lc\_success\_case\]
-   Success task \[sn\_acct\_lc\_success\_task\]
-   Touchpoint \[sn\_acct\_lc\_touchpoint\]
-   Internal play \[sn\_acct\_lc\_internal\_play\]
-   Internal play task \[sn\_acct\_lc\_internal\_play\_task\]

**Parent Topic:**[Customer Success Management reference](../reference/account-lifecycle-reference.md)

**Related topics**  


[Domain separation for service providers](https://www.servicenow.com/docs/access?context=domain-sep-landing-page&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US)

