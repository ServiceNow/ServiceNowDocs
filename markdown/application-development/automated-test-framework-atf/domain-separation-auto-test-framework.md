---
title: Domain separation and Automated Test Framework
description: Domain separation is supported in the Automated Test Framework. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
release: yokohama
product: Automated Test Framework \(ATF\)
classification: automated-test-framework-atf
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Getting started with the Automated Test Framework, Exploring Automated Test Framework, Automated Test Framework \(ATF\), Testing and debugging applications, Building applications]
---

# Domain separation and Automated Test Framework

Domain separation is supported in the Automated Test Framework. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

## Support level: Standard\*

The support level is Standard but has some exceptions or special conditions.

-   Includes all aspects of **Basic** level support.
-   Business logic: The service provider \(SP\) creates or modifies processes per customer. The use cases reflect proper use of the application by multiple SP customers in a single instance.
-   The instance owner must be able to configure minimum viable product \(MVP\) business logic and data parameters. This configuration is done per tenant, as expected for the specific application.

Sample use case: An admin must be able to make comments required when a record closes for one tenant, but not for another.

For more information on support levels, see [Application support for domain separation](https://www.servicenow.com/docs/access?context=domain-separated-apps&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US).

## ATF use case

Automated test framework design and runtime access are solely for the owner of the instance to validate domain-specific processes. By designing tests for my customers we confirm results per tenant.

## Testing

When testing domain separation during ATF test steps, you must set the domain first. This should be part of the first impersonation step of each of the ATF test steps when they are dependent on a domain being set. To learn more about domain separation recommended practices, see [Domain separation recommended practices for service providers](https://www.servicenow.com/docs/access?context=bp-domain-sep-recommended&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US)

**Parent Topic:**[Getting started with the Automated Test Framework](atf-intro.md)

**Related topics**  


[Domain separation for service providers](https://www.servicenow.com/docs/access?context=domain-sep-landing-page&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US)

