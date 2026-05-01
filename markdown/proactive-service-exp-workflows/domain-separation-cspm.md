---
title: Domain Separation and Customer Service Problem Management
description: Domain separation provides a structured and efficient way to manage complex, multi-tiered organizational environments. It enables tailored access and control, ensuring that users see only the data relevant to their domain, enhancing security and efficiency.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Reference, Customer Service Problem Management]
---

# Domain Separation and Customer Service Problem Management

Domain separation provides a structured and efficient way to manage complex, multi-tiered organizational environments. It enables tailored access and control, ensuring that users see only the data relevant to their domain, enhancing security and efficiency.

## Support level: Basic



-   Business logic: Ensure that data goes into the proper domain for the application’s service provider use cases.
-   The application supports domain separation at run time. The domain separation includes separation from the user interface, cache keys, reporting, rollups, and aggregations.
-   The owner of the instance must set up the application to function across multiple tenants.

Sample use case: When a service provider \(SP\) uses chat to respond to a tenant-customer’s message, the customer must be able to see the SP's response.

For more information on support levels, see [Application support for domain separation](https://www.servicenow.com/docs/access?context=domain-separated-apps&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

## Introduction to Customer Service Problem Management

Customer Service Problem Management \(CSPM\) supports domain separation at an account level. All customer data and service problem cases have account \(customer\) level separation.

## How domain separation works in Customer Service Problem Management

-   Ensure that the account is domain separated according to the domain separation guidelines in Customer Service Management. For more information, see [Domain separation and Customer Service Management](https://www.servicenow.com/docs/access?context=domain-separation-customer-service&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US).
-   Customer details and service problem cases are domain separated using the account name.
-   If an administrator assigns fulfillment agents and managers to work on the service problem cases for a specific domain, these agents and managers can work on these types of transactions across accounts.

## Domain separated tables

-   Service Problem Case
-   Service Diagnostic Task
-   Service Resolution Task
-   Service Test Group
-   Service Test Definition
-   Test Measure Definition
-   Test Definition Characteristic
-   Test Definition Relationship
-   Specification to Test Definition Relationship
-   Threshold Rule
-   Measure Consequence
-   Test Run
-   Test Characteristic
-   Test Measure
-   Threshold Rule Violation
-   Applied Consequence

## Use cases

If customer or service problem cases have an account name, an administrator can identify and separate the customer or service problem cases for different domains.

If fulfillment agents or managers are assigned to a domain, an administrator can assign them to work on the service problem cases for a specific domain \(account\).

## How domain values are allocated to CSPM objects

|CSPM objects|Domain source|
|------------|-------------|
|Service Problem Case|Gets domain value from Account.|
|Service Diagnostic Task|Setting domain from Company.|
|Service Resolution Task|Setting domain from Company / task\_for / task\_for.company / default.|
|Service Test Definition|Setting domain of current user.|
|Test Measure Definition|Setting domain from Test Definition.|
|Test Definition Characteristic|Test Definition Characteristic|
|Test Definition Relationship|Setting domain from Test Definition.|
|Specification to Test Definition Relationship|Setting domain from test definition.|
|Threshold Rule|Setting domain from Test measure.|
|Measure Consequence|Setting domain from threshold rule.|
|Test Run|Setting domain from Service Diagnostic task.|
|Test Characteristic|Setting domain from Test Run.|
|Test Measure|Setting domain from Test Run.|
|Threshold Rule Violation|Setting domain from Test Measure.|
|Applied Consequence|Setting domain from Threshold Rule Violation has context menu.|

