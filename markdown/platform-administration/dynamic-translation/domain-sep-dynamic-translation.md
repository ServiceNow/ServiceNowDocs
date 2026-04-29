---
title: Domain separation and Dynamic Translation
description: Domain separation is supported in Dynamic Translation and is configured to apply to translator configurations and Exclusion Framework. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
release: australia
product: Dynamic Translation
classification: dynamic-translation
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Reference for Dynamic Translation, Dynamic Translation, Translation and localization, Configure core features, Administer the ServiceNow AI Platform]
---

# Domain separation and Dynamic Translation

Domain separation is supported in Dynamic Translation and is configured to apply to translator configurations and Exclusion Framework. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

## Support level: Basic



-   Business logic: Ensure that data goes into the proper domain for the application’s service provider use cases.
-   The application supports domain separation at run time. The domain separation includes separation from the user interface, cache keys, reporting, rollups, and aggregations.
-   The owner of the instance must set up the application to function across multiple tenants.

Sample use case: When a service provider \(SP\) uses chat to respond to a tenant-customer’s message, the customer must be able to see the SP's response.

For more information on support levels, see [Application support for domain separation](https://www.servicenow.com/docs/access?context=domain-separated-apps&version=australia&pubname=australia-platform-security&ft:locale=en-US).

## Activation information

You should activate the Domain Support - Domain Extensions Installer plugin \(com.glide.domain.msp\_extensions.installer\). For information on how you can request for the plugin activation, see [Request for domain separation in Dynamic Translation](../task/activate-domainsep-dyn-transl.md).

## How domain separation works in Dynamic Translation

A service provider with domain separated instances can implement the Dynamic Translation framework so that users can use the translation service providers configured in the translator configurations specific to their domain.​ Translator configurations are process-separated in Dynamic Translation. All translation service providers configured in the translator configurations of the parent domain are available in child domains.

A translator configuration in the global domain is visible in all other domains. In any domain, a user can only view the translator configurations configured in the following domains:

-   Current domain
-   Parent domains
-   Global domain

**Note:** If there are multiple translator configurations in a domain for the same translation service provider, the translator configuration of the current domain or the closest parent domain is considered for dynamic translation.

Also, different connections can be configured for the same connection and credential alias of a translation service provider in multiple domains. However, Credentials and Connections are data-separated. So, a connection configured in a child domain is visible in parent domains. For information on domain separation for Connections and Credentials, see [Domain separation for Credentials and Connections](https://www.servicenow.com/docs/access?context=domain-separation-credentials_conn&version=australia&pubname=australia-platform-security&ft:locale=en-US).

For example, consider the following scenario:

![Translation service provider in multiple domains](../image/domain-sep-conn.png "Connections for a translation service provider in multiple domains")

Different connections are configured for the same connection and credential alias of Google in multiple domains. When in Domain A, all the following connections are visible:

-   Connection1
-   Connection2
-   Connection3

**Note:** When multiple active connections are visible for the same connection and credential alias in a domain, the connection with the highest order is given priority when the **Support Multiple Active Connections** check box is selected.

## Domain-separated table

Translator Configuration \[sn\_dt\_translator\_configuration\].

## Default translator configuration for a domain

The default translator configuration of the current domain is always considered for dynamic translation. If the current domain does not have any default translator configuration, then the available default translator configuration of the nearest parent is considered.

A domain can have multiple default translator configurations. In this case also, the default translator configuration of the current domain is considered for dynamic translation. For example, let us consider the following scenario:

![Domain separation in Dynamic Translation](../image/domain-sep-tc.png "Domain separation in Dynamic Translation")

In Domain B, both TC1 and TC2 are visible. From Domain B, TC2 is first set as the default translator configuration. From Domain A, TC1 is then overridden and set as the default translator configuration. This results in multiple default translator configurations in Domain B. In this case, when in Domain B, TC2 is used as the default translator configuration for dynamic translation.

## Overriding a translator configuration

In any domain, you can override the translator configuration of that domain or the parent domain. The overridden translator configuration of a parent domain is also visible in child domains. However, the overridden translator configuration of a child domain is not visible in the parent domain.

After you override a translator configuration of the same domain, only the overridden translator configuration is visible in that domain.

After you override a translator configuration of a parent domain, the following scenarios happen:

-   Only the overridden translator configuration is visible in the child domain.
-   The **Overrides** field of overridden translator configuration refers to the original translator configuration of the parent domain.

For example, consider the following scenario:

![Screenshot for Domain separation in Dynamic Translation](../image/domain-sep-tc.png "Domain separation in Dynamic Translation")

You can override a translator configuration TC1 from Domain B. After overriding, only the overridden configuration TC1 is available in Domain B and the **Overrides** field of TC1 refers to **TC1** of the parent domain.

## Domain separation in Exclusion Framework

The Exclusion Framework module in Dynamic Translation supports domain separation. Each domain on an instance can have its own set of Exclusion Framework rules, so the rules are specific to one domain. Activation of Exclusion Framework on an instance applies to all domains on the instance. For more information see [Exclusion Framework in Dynamic Translation](dyn-translation-exclusion-framework.md).

**Related topics**  


[Domain separation for service providers](https://www.servicenow.com/docs/access?context=domain-sep-landing-page&version=australia&pubname=australia-platform-security&ft:locale=en-US)

