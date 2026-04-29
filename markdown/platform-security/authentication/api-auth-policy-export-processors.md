---
title: Access policy for System or Export Processors
description: Ability for System or Export Processors to leverage processor access policy to secure all the export endpoints.
locale: en-US
release: australia
product: Authentication
classification: authentication
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [API access policy, Authentication, Access Management]
---

# Access policy for System or Export Processors

Ability for System or Export Processors to leverage processor access policy to secure all the export endpoints.

Ability to secure all the export endpoints and apply the inbound authentication profile and processor access policies at a global or instance level.

**Note:**

-   Non-public processors, including the export processors like CSV, PDF, etc are supported for access policies.
-   Script processors are also supported for access policies.

## Sample use cases

-   Admin can block the RSS processor if not intending to use it, by leveraging the API access policy.
-   Admin can create an authentication profile with basic authentication and associate an authentication policy that always evaluates to false.

    Example, Create IP criteria with a range from `0.0.0.0` to `255.255.255.255` \(add Ipv6 address space as well\) and then add policy condition with the false operator. By this way, policy conditions will always evaluate as false, and the API access policy will block the access irrespective of where the request is originating.

-   Allowing access to the processor only from a trusted network.

