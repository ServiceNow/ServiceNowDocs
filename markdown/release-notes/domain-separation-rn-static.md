---
title: Domain Separation release notes
description: ServiceNow Domain Separation provides robust isolation and management of customer data across multi-tenant and multi-instance environments. Domain Separation includes controls such as data domain policies, cross-domain access restrictions, and domain-aware security attributes. These controls provide comprehensive data segregation and help ensure compliance and data privacy requirements are met in complex deployment scenarios. See the following sections for release notes by version.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/release-notes/domain-separation-rn-static.html
release: australia
topic_type: topic
last_updated: "2026-09-10"
reading_time_minutes: 1
keywords: [Domain Separation, multi-tenant, data isolation, compliance, security]
breadcrumb: [ServiceNow AI Platform security release notes, Features and changes by product, Release notes for upgrading from Australia, Learn about the Brazil release, Brazil release notes]
---

# Domain Separation release notes

ServiceNow Domain Separation provides robust isolation and management of customer data across multi-tenant and multi-instance environments. Domain Separation includes controls such as data domain policies, cross-domain access restrictions, and domain-aware security attributes. These controls provide comprehensive data segregation and help ensure compliance and data privacy requirements are met in complex deployment scenarios. See the following sections for release notes by version.

## About Domain Separation

-   Isolate customer data across multiple domains or tenants to ensure that data accessed by one customer is not visible to another customer, meeting strict data privacy and compliance requirements.
-   Define domain-aware access control policies that restrict cross-domain visibility and access at the record and field level using security attributes and domain-specific rules.
-   Monitor and enforce domain boundaries across applications and workflows to prevent accidental or unauthorized cross-domain data access.
-   Configure domain separation policies centrally and apply them consistently across your platform for predictable and auditable data isolation.
-   Support complex deployment scenarios including managed service provider \(MSP\) environments, reseller platforms, and hybrid multi-tenant architectures.

See Domain Separation documentation for more information.

## Activation and other requirements

-   **Activation information**

    Domain Separation is a ServiceNow AI Platform feature available with activation of the com.glide.domain.activation\_utility plugin. Upon activation, navigate to the Domain Separation administration console to configure domains, policies, and cross-domain access restrictions for your environment.

-   **Upgrade information**

    Before upgrading to this release, review the product documentation for any breaking changes or upgrade considerations specific to your current version. Test upgrades in a non-production instance first to ensure compatibility with your domain policies and customizations. Domain separation policies may require validation or adjustment after upgrade to ensure continued enforcement.

-   **Browser requirements**

    For optimal performance with Domain Separation features, use the latest release of Chrome, Firefox, or Safari. Internet Explorer is not supported. Modern browsers with JavaScript enabled are required for all administrative and policy configuration interfaces.

-   **Additional requirements**
    -   Appropriate user roles assigned: Domain Separation Admin, Domain Policy Admin, and other role-based permissions for domain management and configuration.

