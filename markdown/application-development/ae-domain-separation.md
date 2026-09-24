---
title: Domain separation support in Autonomous Engineer
description: Autonomous Engineer supports domain separation, allowing you to set the domain \(sys\_domain\) and use sys\_override on APIs and records that support it.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ae-domain-separation.html
release: brazil
topic_type: reference
last_updated: "2026-09-08"
reading_time_minutes: 1
keywords: [domain separation, sys\_domain, sys\_override, Autonomous Engineer, Fluent]
audience: programmer
breadcrumb: [Reference, Autonomous Engineer, Agentic development on the ServiceNow AI Platform, Building applications]
---

# Domain separation support in Autonomous Engineer

Autonomous Engineer supports domain separation, allowing you to set the domain \(`sys_domain`\) and use `sys_override` on APIs and records that support it.

## Overview of domain separation

Autonomous Engineer supports domain separation on APIs and records that support it on the ServiceNow AI Platform. You can set the domain \(`sys_domain`\) on those APIs and records, and use `sys_override` where applicable.

Domain separation support is available through the ServiceNow Fluent SDK. When you author application code using ServiceNow Fluent and deploy it to an instance that uses domain separation, the generated artifacts respect the domain configuration of the target instance.

## Considerations for domain support

Review the following when developing applications for instances that use domain separation:

-   Domain separation applies to APIs and record types that support it. Not all APIs or records support domain assignment.
-   When you set a domain on a record, it applies to that record within the defined domain scope. Records set to the Global domain are accessible across all domains.
-   Use `sys_override` to override domain-controlled values on records where overrides are permitted.

For more general information about domain separation, see [Exploring domain separation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/c_DomainSeparation.md).

**Parent Topic:**[Autonomous Engineer reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/autonomous-engineer-reference-landing.md)

