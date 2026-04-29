---
title: AWS Domain Separation
description: Domain separation is supported for AWS Security Hub application. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2026-03-16"
reading_time_minutes: 1
breadcrumb: [Amazon Web Services \(AWS\) Security Hub integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# AWS Domain Separation

Domain separation is supported for AWS Security Hub application. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

## Support level: Basic



-   Business logic: Ensure that data goes into the proper domain for the application’s service provider use cases.
-   The application supports domain separation at run time. The domain separation includes separation from the user interface, cache keys, reporting, rollups, and aggregations.
-   The owner of the instance must set up the application to function across multiple tenants.

Sample use case: When a service provider \(SP\) uses chat to respond to a tenant-customer’s message, the customer must be able to see the SP's response.

For more information on support levels, see [Application support for domain separation](https://www.servicenow.com/docs/access?context=domain-separated-apps&version=australia&pubname=australia-platform-security&ft:locale=en-US).

## How domain separation works in AWS Security Hub

The AWS Security Hub integration with ServiceNow Security Incident Response \(SIR\) supports domain separation, enabling you to route AWS Security Hub findings into the appropriate domain-scoped security incidents.

-   -   Replicate the following scheduled jobs for every domain:
    -   AWS SecurityHub Process Raw Data
    -   AWS SecurityHub Profile Process
    -   AWS SecurityHub AdditionalOptions Sync
    -   AWS SecurityHub Bidirectional Attributes Sync
    -   AWS SecurityHub Fields Import Queue Process

## Use Case

The following example shows how to replicate the AWS Security Hub comments and Status update job and run the job as a system user.

![AWS Domain Separation](../image/aws-domain-sep.png)

