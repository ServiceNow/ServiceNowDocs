---
title: Extending the Retail base case
description: Extend the Retail Case \(sn\_retail\_case\) base case to create custom case types that take advantage of prebuilt roles, business rules, workflows, and the Retail data model rather than creating them manually.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/retail-industry/rahi-retail-extending-retail-base-case.html
release: australia
topic_type: concept
last_updated: "2026-06-28"
reading_time_minutes: 1
keywords: [extend retail case, custom case type, retail case extension]
breadcrumb: [Retail case types, Explore, Retail]
---

# Extending the Retail base case

Extend the Retail Case \(`sn_retail_case`\) base case to create custom case types that take advantage of prebuilt roles, business rules, workflows, and the Retail data model rather than creating them manually.

For general guidelines on implementing case types, see [Best Practices to Implement Case Types](https://mynow.servicenow.com/now/best-practices/assets/best-practices-to-implement-case-types).

All prebuilt Retail case types—except for Retail Customer Complaint, which extends the base CSM case \(`sn_customerservice_case`\)—extend from the Retail Case \(`sn_retail_case`\) base case, which in turn extends the CSM case. Use the Retail base case as the starting point when adding a case type.

## Criteria for creating a case type

Use the following questions to determine whether your organization needs a new case type or whether an existing service definition is sufficient. More "yes" answers indicate a stronger need for a new case type:

-   Is a service definition not enough to support the process due to field attribute or automation requirements? If an existing case type's attributes already fit, define the new work as a service definition rather than a new case type.
-   Is the process fundamentally different from every prebuilt and existing custom retail case type?
-   Are there different processes or integrations required based on work type, business unit, or the products and services being supported?
-   Does the new process have a different state model than your existing ones?
-   Are there meaningfully different attributes that need to be collected on the case during intake for this use case?
-   Are there meaningfully different attributes for agents to capture on the case as they fulfill for this process?
-   Does the fulfilling group interact with a different set of back-end systems to resolve the case?
-   Do access and visibility requirements differ? For example, do the records generated for this use case have distinct view restrictions?
-   Do fulfillers need a different workspace experience and guidance for this case type?
-   Are there future scalability needs, or change-management considerations where shared intake forms and workflows would increase complexity across teams?

**Related topics**  


[Service definitions in Retail](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/retail-industry/rahi-retail-service-definitions.md)

