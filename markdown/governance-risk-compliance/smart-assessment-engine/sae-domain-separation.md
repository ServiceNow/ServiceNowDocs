---
title: Domain separation and Smart Assessment Engine \(SAE\)
description: If any conkeyrefs are broken, re-add them from the doc/source/reuse/domain-separation/domain-separation-overview.dita file.Domain separation is supported for Smart Assessment Engine. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
release: zurich
product: Smart Assessment Engine
classification: smart-assessment-engine
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Exploring Smart Assessment Engine, Smart Assessment Engine, Governance, Risk, and Compliance]
---

# Domain separation and Smart Assessment Engine \(SAE\)

Domain separation is supported for Smart Assessment Engine. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

## Support level: Basic



-   Business logic: Ensure that data goes into the proper domain for the application’s service provider use cases.
-   The application supports domain separation at run time. The domain separation includes separation from the user interface, cache keys, reporting, rollups, and aggregations.
-   The owner of the instance must set up the application to function across multiple tenants.

Sample use case: When a service provider \(SP\) uses chat to respond to a tenant-customer’s message, the customer must be able to see the SP's response.

For more information on support levels, see [Application support for domain separation](https://www.servicenow.com/docs/access?context=domain-separated-apps&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

## Smart Assessment Overview

The ServiceNow® Smart Assessment Engine \(SAE\) application helps you to reduce the manual burden and costs of your assessment processes through automation.

You can use the Smart Assessment Engine application to create and distribute assessments to employees for evaluating various situations, aspects, or records.

## How domain separation works in Smart Assessment Engine

-   To use a domain-separated model, the platform version must be in at least the Xanadu release.
-   Templates in SAE are process-separated.
-   Assessments are data-separated.
-   All actors including the assessment group should belong to the same domain or global domain.
-   The assessment template should be accessible in the common domain where the assessment is created.
-   Domain overrides aren't supported.

**Note:** The Smart assessment connected plugin \[com.sn\_smart\_asmt\_connect\] must be installed for domain separation to be available.

The table displays different scenarios within the assessment domain, illustrating the relationship between the domain of the scope item and the domain of the assessment actors. Each row represents a different scenario, indicating whether the assessment actor has access the assessment template.

|Scope item|Assessment actor|Assessment|
|----------|----------------|----------|
|Domain A|Domain B|Not possible​|
|Domain A|Domain A|Domain A|
|Not applicable|Domain A|Domain A|
|Global​|Domain A|Domain A|
|Domain A|Global​|Domain A|

## Domain-separated tables

-   sn\_smart\_asmt\_template
-   sn\_smart\_asmt\_section
-   sn\_smart\_asmt\_question
-   sn\_smart\_asmt\_response\_option
-   sn\_smart\_asmt\_template\_category
-   sn\_smart\_asmt\_context\_item
-   sn\_smart\_asmt\_instance
-   sn\_smart\_asmt\_combined\_assessment
-   sn\_smart\_asmt\_m2m\_instance\_combined\_assessment
-   sn\_smart\_asmt\_section\_instance
-   sn\_smart\_asmt\_question\_instance
-   sn\_smart\_asmt\_response\_option\_instance
-   sn\_smart\_asmt\_m2m\_instance\_persona
-   sn\_smart\_asmt\_m2m\_instance\_scope\_item
-   sn\_smart\_asmt\_condition
-   sn\_smart\_asmt\_condition\_result
-   sn\_smart\_asmt\_condition\_result\_set
-   sn\_smart\_asmt\_m2m\_question\_condition
-   sn\_smart\_asmt\_duration
-   sn\_smart\_asmt\_assessment\_group

**Related topics**  


[Domain separation for service providers](https://www.servicenow.com/docs/access?context=domain-sep-landing-page&version=zurich&pubname=zurich-platform-security&ft:locale=en-US)

