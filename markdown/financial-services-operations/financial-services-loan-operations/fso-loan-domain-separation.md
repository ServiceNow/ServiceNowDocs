---
title: Domain separation and Financial Services Loan Operations
description: Domain separation is unsupported for the Financial Services Loan Operations application. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
release: yokohama
product: Financial Services Loan Operations
classification: financial-services-loan-operations
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Setting up Financial Services Loan Operations, Loan Operations, Using banking applications, Financial Services Operations \(FSO\)]
---

# Domain separation and Financial Services Loan Operations

Domain separation is unsupported for the Financial Services Loan Operations application. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

## Support level: Basic



-   Business logic: Ensure that data goes into the proper domain for the application’s service provider use cases.
-   The application supports domain separation at run time. The domain separation includes separation from the user interface, cache keys, reporting, rollups, and aggregations.
-   The owner of the instance must set up the application to function across multiple tenants.

Sample use case: When a service provider \(SP\) uses chat to respond to a tenant-customer’s message, the customer must be able to see the SP's response.

For more information on support levels, see [Application support for domain separation](https://www.servicenow.com/docs/access?context=domain-separated-apps&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US).

## How domain separation works in Financial Services Loan Operations

-   All Financial Service Loan Operations applications are built on top of Customer Service Management \(CSM\) and use many CSM tables. The key reference tables are the customer tables, such as Consumer, Account, and Contact. These tables are domain-separated.

**Parent Topic:**[Setting up Financial Services Loan Operations](setting-up-fso-loan-ops.md)

**Related topics**  


[Domain separation for service providers](https://www.servicenow.com/docs/access?context=domain-sep-landing-page&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US)

