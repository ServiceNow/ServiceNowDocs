---
title: Container Vulnerability Response release notes
description: The ServiceNow Container Vulnerability Response application brings security and IT together to enable you to remediate your most critical vulnerabilities more quickly and efficiently. Container Vulnerability Response was enhanced and updated in the Brazil release.This release features new integrations for the Vulnerability Response Integration with Wiz and enhancements to Container Vulnerability Response application that provide you with information about your runtime visibility and container vulnerabilities.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/release-notes/secops-cvr-rn.html
release: brazil
topic_type: topic
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [Security Operations release notes, Features and changes by product, Release notes for upgrading from Australia, Learn about the Brazil release, Brazil release notes]
---

# Container Vulnerability Response release notes

The ServiceNow® Container Vulnerability Response application brings security and IT together to enable you to remediate your most critical vulnerabilities more quickly and efficiently. Container Vulnerability Response was enhanced and updated in the Brazil release.

## About Container Vulnerability Response

-   If you're currently using Container Vulnerability Response and you want to upgrade to Unified Security Exposure Management \(USEM\), see [Unified Security Exposure Management \(USEM\) release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/release-notes/secops-sem-rn.md) for more information about USEM and the Unified Security Exposure Management migration.
-   Import container image vulnerability data from the Wiz scanners into container vulnerable items \(CVITs\) with the Vulnerability Response Integration with Wiz.
-   With the sn\_vul\_container.vulnerability\_analyst or sn\_vul\_container.vulnerability\_admin role, create container remediation tasks manually in the Vulnerability Manager Workspace.
-   With the role sn\_vul\_container.remediation\_owner, create container remediation tasks manually in the IT Remediation Workspace.

See [Container Vulnerability Response](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/security-management/cvr-landing.md) for more information.

## Activation and other requirements

**Important:** Container Vulnerability Response is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

-   **Activation information**

    Install Container Vulnerability Response and third-party integrations by requesting them from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).

-   **Upgrade information**

    ServiceNow Otto® is the new AI experience brand. This change is reflected in the name of ServiceNow products, including the Now Assist for Vulnerability Response product name, which will be replaced with ServiceNow Otto for Unified Security Exposure Management. Your product entitlements remain unchanged. Check your entitlements to determine your access to specific features.

    Enhancements to Container Vulnerability Response permit you to see enriched container vulnerability data on data imports from your third-party scanners. After you upgrade, perform a full import to view the features on discovered container image, container image finding, and container vulnerable item records that are described in the following New in the Brazil release section.

    If you're currently using Container Vulnerability Response, and you don't intend to upgrade to Unified Security Exposure Management \(USEM\), install a version below v30.x of Container Vulnerability Response and for upgrades to supported third-party integration applications.

    For more information about the released versions of the Container Vulnerability Response application as well as the third-party and ServiceNow applications that are compatible with the Brazil release, see the [Vulnerability Response Compatibility Matrix and Release Schema Changes \[KB0856498\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0856498) article in the Now Support Knowledge Base.


**Parent Topic:**[Security Operations release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/release-notes/security-operations-rn-landing.md)

## Brazil Early Availability

This release features new integrations for the Vulnerability Response Integration with Wiz and enhancements to Container Vulnerability Response application that provide you with information about your runtime visibility and container vulnerabilities.

### What's new

-   **[Enhancements to the Wiz Vulnerability Response Integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/security-management/wiz-container-runtime-exposure-cvr.md)**

    Two new chained integrations for the Wiz container vulnerability pipeline:

    -   The Wiz Container Grouped Vulnerability Integration that retrieves vulnerability findings from Wiz that are grouped by image.
    -   The Wiz Container Deployment Context Integration that retrieves the complete deployment/execution context that includes clusters, namespaces, services for each image.
    -   View both integrations in your Vulnerability Integrations list alongside the existing Wiz Container Vulnerability Integration. The integrations are installed automatically and are activated by default.

        **Note:** To disable this integration chain, set the sn\_vul\_wiz.deployment\_context\_gate\_writes system property to 'false'. This deactivates the Wiz Container Grouped Vulnerability and Wiz Container Deployment Context integrations so that container vulnerable item creation remains based on your existing settings with the Wiz Container Vulnerability Integration integration.


### What's changed

-   **Container Vulnerability Response**
    -   Enhancements to improve handling of Wiz API error codes that include clearer notifications directing users to contact the Wiz support team when a vendor-side error occurs.
    -   Enhancements to improve the reliability of the data migration for Wiz Container Vulnerability Response.

### What's deprecated or removed

-   **Now LLM Service**

    Starting with the September 2026 release, Gemma 4 joins our growing portfolio of open-weight models available through Now LLM Service. The latest industry advancements are available alongside sovereignty-focused options. All models are hosted and governed by ServiceNow with the same infrastructure and data protections. Older models will remain available for existing published AI skills, agents, and agentic workflows, but will no longer be available for new development or configuration. For details, see the [KB3066214: ServiceNow Otto Model Upgrades](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3066214) article in the Now Support Knowledge Base.


