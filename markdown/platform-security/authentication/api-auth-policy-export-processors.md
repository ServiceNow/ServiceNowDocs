---
title: Access policy for System or Export Processors
description: System or Export Processors can use processor access policy to secure all the export endpoints.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/platform-security/authentication/api-auth-policy-export-processors.html
release: australia
product: Authentication
classification: authentication
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [API access policy, Authentication, Access Management]
---

# Access policy for System or Export Processors

System or Export Processors can use processor access policy to secure all the export endpoints.

Ability to secure all the export endpoints and apply the inbound authentication profile and processor access policies at a global or instance level.

**Note:**

-   Non-public processors, including the export processors like CSV, PDF, and so on are supported for access policies.
-   Script processors are also supported for access policies.

## Sample use cases

-   Admin can block the RSS processor if not intending to use it, by using the API access policy.
-   Admin can create an authentication profile with basic authentication and associate an authentication policy that evaluates to false.

    Example, Create IP criteria with a range from `0.0.0.0` to `255.255.255.255` \(add IPv6 address space as well\) and then add policy condition with the false operator. In this way, policy conditions will evaluate as false, and the API access policy will block the access irrespective of where the request is originating.

-   Allowing access to the processor only from a trusted network.

