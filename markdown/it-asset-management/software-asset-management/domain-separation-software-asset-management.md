---
title: Domain separation and Software Asset Management
description: Domain separation is supported in Software Asset Management. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/software-asset-management/domain-separation-software-asset-management.html
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Software Asset Management references, Software Asset Management, IT Asset Management]
---

# Domain separation and Software Asset Management

Domain separation is supported in Software Asset Management. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

## Support level: Enhanced

-   Includes all aspects of **Basic** and **Standard** levels of support.
-   Data-driven process enables service provider customers to modify business logic that is based on defined use cases. These configurations are UI-based and fail-safe so that configurations by one customer cannot affect another.
-   Tenants of the instance must be able to configure minimum viable product \(MVP\) business logic and data parameters for themselves. This logic and parameters would be expected for the application's normal function.

Sample use case: Tenant-customers of a shared environment must be able to modify the impact, urgency, or priority matrix to set priority within their domain.

For more information on support levels, see [Application support for domain separation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/servicenow-ai-platform-security/domain-separated-apps.md).

## Domain separation support

Domain separation in Software Asset Management enables service providers to offer managed Software Asset Management services to their customers. It also enables large organizations to manage their subsidiaries as independent domains.

With multi-tenant support for Software Asset Management, you can manage the entire Software Asset Management lifecycle for your customers in a shared ServiceNow instance. This model provides complete data and process separation between tenants, along with tenant admin support.

## Service provider benefits

Multi-tenant support for Software Asset Management offers the following benefits to service providers:

-   Expand the service portfolio to include Software Asset Management.
-   Offer Software Asset Management as a service to your users that includes:
    -   Contract and entitlement management
    -   Discovery and normalization reporting
    -   Software reconciliation, optimization, and licensing expertise
    -   Audit response
    -   Software lifecycle and vulnerability reporting
    -   SaaS license management
    -   Engineering license management

## Customer benefits

Customers gain the following benefits when a service provider manages their assets on the shared ServiceNow instance:

-   Access to established Software Asset Management services and processes delivered by domain experts
-   No platform or process ownership required from the customer

## How domain separation works in Software Asset Management

In Software Asset Management, domain separation occurs in two stages: data separation and process separation. From the Paris release, both data and process are domain-separated.

Any user with sam\_integrator role has access to create and modify the SaaS integration profiles. Since users with this role can also access the Oauth application registry \(currently not domain-separated, so records across all domains are visible\), this sam\_integrator role should be assigned with caution. The user should be in the service provider organization and satisfy high permissions criteria.

To view logs for domain separation, create a system property named **asset.log\_level** and set its value to **debug**, **trace** or **info**. The level you set determines which logs appear when any scheduled job that extends the **AssetManagementBaseJob** scheduled job runs.

In a domain-separated instance, the content data service \(CDS\) should populate data in the instance with domain set as **global**.

**Note:**

Avoid customizing the base system domain configuration record. For more information, see [Recommended practice](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/servicenow-ai-platform-security/bp-domain-sep-recommended.md).

\[Omitted image "mmasset0021805-ham-sam-multitenant.svg"\] Alt text: Diagram showing how a service provider manages the IT Asset Management lifecycle for multiple tenant customers in a shared ServiceNow instance, with complete data and process separation between tenants

## Required plugins

-   Domain separation extension \(com.glide.domain.msp\_extensions.installer\)
-   Performance Analytics – Domain Support \(com.snc.pa.domain\_support\)
-   Software Asset Management Professional \(com.sn\_samp\_master\)

## Other supported plugins

-   Service Catalog – Domain Separation \(com.glideapp.servicecatalog.domain\_separation\)
-   Procurement \(com.snc.procurement\)
-   Cost Management \(com.snc.cost\_management\)
-   Contract Management \(com.snc.contract\_management\)

To learn more, see [Domain separation explained](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/servicenow-ai-platform-security/bp-what-is-domain-separation.md), [Contains queries and domain access](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/servicenow-ai-platform-security/bp-contains-domain-visibility.md), and [Importance of Default domain](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/servicenow-ai-platform-security/bp-default-domain.md).

-   **[Domain separation and lifecycle reports](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/software-asset-management/domain-sep-sam-lifecycle.md)**  
There are certain domain separation aspects to consider when running software lifecycle reports.

**Parent Topic:**[Software Asset Management references](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/software-asset-management/references.md)

**Related topics**  


[Domain separation for service providers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/servicenow-ai-platform-security/domain-sep-landing-page.md)

