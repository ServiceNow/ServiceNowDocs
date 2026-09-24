---
title: Domain Separation release notes
description: ServiceNow Domain Separation provides robust isolation and management of customer data across multi-tenant and multi-instance environments. Domain Separation includes controls such as data domain policies, cross-domain access restrictions, and domain-aware security attributes. These controls provide comprehensive data segregation and help ensure compliance and data privacy requirements are met in complex deployment scenarios. See the following sections for release notes by version.The Brazil Early Availability release adds conversational access analysis capabilities to Domain Separation, making it easier to understand and verify access permissions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/release-notes/domain-separation-rn-static.html
release: brazil
topic_type: topic
last_updated: "2026-09-10"
reading_time_minutes: 2
keywords: [Domain Separation, multi-tenant, data isolation, compliance, security, Domain Separation, Access Analysis Agent, access control, conversational]
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

## Accessibility and localization

-   **Accessibility information**
    -   All user interface elements in Domain Separation meet WCAG 2.1 Level AA standards for accessibility. The administration console and all configuration workflows are fully navigable by keyboard and compatible with screen readers including JAWS and NVDA.
    -   Screen reader support includes proper ARIA labels for all UI components including domain policy configuration, access control settings, and cross-domain restriction interfaces.
    -   Color contrast ratios meet WCAG AA standards across all features and workflows.
    -   For accessibility questions or to report accessibility issues, contact ServiceNow Support.
-   **Localization information**

    All user-facing strings in Domain Separation are localized for supported ServiceNow languages at general availability \(GA\). Supported languages include English, French, German, Spanish, Italian, Japanese, Portuguese, Chinese \(Simplified and Traditional\), and Korean. Language packs are installed automatically when the corresponding ServiceNow base system language plugin is active.


## Brazil Early Availability

The Brazil Early Availability release adds conversational access analysis capabilities to Domain Separation, making it easier to understand and verify access permissions.

### What's new

-   **Access Analysis Agent**

    Ask whether a user, group, or role can access a table, record, field, Script Include, UI page, AI agent, or agentic workflow using guided, conversational workflows in the Now Assist panel. The agent returns clear results—Passed, Blocked, or Undefined—without requiring manual Access Analyzer configuration. The agent can also read the current page context, identify matching entities when names are ambiguous, and save evaluation results for future reference.


### What's deprecated or removed

There are no deprecated or removed features in this release.

