---
title: Domain separation and ServiceNow Otto for Financial Services Operations \(FSO\)
description: If any conkeyrefs are broken, re-add them from the doc/source/reuse/domain-separation/domain-separation-overview.dita file.In the short description, edit the first sentence to state whether domain separation is supported or not and add the application name. Keep the conkeyref at the end that describes domain separation.Domain separation is supported for ServiceNow Otto for Financial Services Operations \(FSO\). Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/financial-services-operations/now-assist-for-financial-services-operations-fso/now-assist-for-financial-services-operations-domain-separation.html
release: zurich
product: Now Assist for Financial Services Operations \(FSO\)
classification: now-assist-for-financial-services-operations-fso
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
keywords: [generative AI for financial services operations domain separation, generative AI for FSO domain separation]
breadcrumb: [Reference, ServiceNow Otto for FSO, Financial Services Operations \(FSO\)]
---

# Domain separation and ServiceNow Otto for Financial Services Operations \(FSO\)

Domain separation is supported for ServiceNow Otto for Financial Services Operations \(FSO\). Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

## Support level: Basic



-   Business logic: Ensure that data goes into the proper domain for the application’s service provider use cases.
-   The application supports domain separation at run time. The domain separation includes separation from the user interface, cache keys, reporting, rollups, and aggregations.
-   The owner of the instance must set up the application to function across multiple tenants.

Sample use case: When a service provider \(SP\) uses chat to respond to a tenant-customer’s message, the customer must be able to see the SP's response.

For more information on support levels, see [Application support for domain separation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-security/domain-separated-apps.md).

## Domain separation overview

In ServiceNow Otto for FSO, generative AI capabilities are organized into skills. Each skill can be configured differently for each domain. By default, all skills exist in the global domain.

## How domain separation works in ServiceNow Otto for FSO

You must enable domain separation on your instance first before you can use it for ServiceNow Otto for Financial Services Operations \(FSO\) skills.

ServiceNow Otto for Financial Services Operations \(FSO\) works with domain separation. When you use ServiceNow Otto for Financial Services Operations \(FSO\) in a domain-separated environment, users are only able to access data within their domain. For example, when a user uses the summarization skill, ServiceNow Otto for Financial Services Operations \(FSO\) only uses material that exists within the user's domain when generating that summary. When a skill is domain-separated, only users who are in that domain can use the skill that you have configured for that scope.

If you're a service provider that hosts multiple clients in the same instance, you can set up domain separation to separate tenant data, processes, and administrative tasks. However, ServiceNow Otto for Financial Services Operations \(FSO\) consumption is tracked according to the instance without differentiating between tenants. You can track your ServiceNow Otto for Financial Services Operations \(FSO\) usage in the Subscription Management dashboard.

If you want a domain to have a different version of an existing skill, you can reconfigure and activate the skill or create a variant in the preferred domain. See [Domain separation in the AI Admin Hub console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/domain-separation-in-the-now-assist-admin-console.md).

## Use cases

You can configure the roles when you’re activating or editing a skill.

For example, you can grant certain roles access to the ServiceNow Otto panel in one domain, while another domain has no role restrictions.

**Parent Topic:**[ServiceNow Otto for Financial Services Operations \(FSO\) reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/financial-services-operations/now-assist-for-financial-services-operations-fso/now-assist-for-fso-reference.md)

**Related topics**  


[Domain separation for service providers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-security/domain-sep-landing-page.md)

