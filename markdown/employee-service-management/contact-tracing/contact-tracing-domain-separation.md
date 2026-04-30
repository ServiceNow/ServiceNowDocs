---
title: Domain separation and Contact Tracing
description: Domain separation is supported for the ServiceNow Contact Tracing application. The application helps organizations reduce workplace transmission of infectious diseases, such as COVID-19, by identifying anyone on site who might have been in contact with an affected person.
locale: en-US
release: yokohama
product: Contact Tracing
classification: contact-tracing
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Setting up Contact Tracing, Contact Tracing, Safe Workplace, Health and Safety, Employee Service Management]
---

# Domain separation and Contact Tracing

Domain separation is supported for the ServiceNow® Contact Tracing application. The application helps organizations reduce workplace transmission of infectious diseases, such as COVID-19, by identifying anyone on site who might have been in contact with an affected person.

## Support level: Standard\*

The support level is Standard but has some exceptions or special conditions.

-   Includes all aspects of **Basic** level support.
-   Business logic: The service provider \(SP\) creates or modifies processes per customer. The use cases reflect proper use of the application by multiple SP customers in a single instance.
-   The instance owner must be able to configure minimum viable product \(MVP\) business logic and data parameters. This configuration is done per tenant, as expected for the specific application.

Sample use case: An admin must be able to make comments required when a record closes for one tenant, but not for another.

For more information on support levels, see [Application support for domain separation](https://www.servicenow.com/docs/access?context=domain-separated-apps&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US).

## Overview

Service providers need to be able to manage multiple customers in a single instance to deliver their services via Contact Tracing in the [Safe Workplace](../../human-resources/concept/safe-workplace.md) suite. Beginning with the Paris release, scheduled jobs introduced support for domain separation at the Standard level.

Admins must install the [Domain separation plugin](https://www.servicenow.com/docs/access?context=t_ActivateDomainSeparation&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US) before working with the Contact Tracing tables.

See [Domain separation and Safe Workplace suite](../../workplace-safety-mgmt/concept/domain-separation-safe-workplace.md) to learn how to set up Contact Tracing with domain separation.

**Parent Topic:**[Setting up Contact Tracing](set-up-contact-tracing.md)

**Related topics**  


[Domain separation for service providers](https://www.servicenow.com/docs/access?context=domain-sep-landing-page&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US)

