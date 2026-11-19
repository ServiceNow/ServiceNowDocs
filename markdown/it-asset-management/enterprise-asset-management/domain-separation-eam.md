---
title: Domain separation and Enterprise Asset Management
description: Domain separation is supported in Enterprise Asset Management. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/it-asset-management/enterprise-asset-management/domain-separation-eam.html
release: yokohama
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Enterprise Asset Management reference, Enterprise Asset Management, IT Asset Management]
---

# Domain separation and Enterprise Asset Management

Domain separation is supported in Enterprise Asset Management. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

## Support level: Standard

-   Includes all aspects of **Basic** level support.
-   Application properties are domain-aware as needed.
-   Business logic: The service provider \(SP\) creates or modifies processes per customer. The use cases reflect proper use of the application by multiple SP customers in a single instance.
-   The instance owner must configure the minimum viable product \(MVP\) business logic and data parameters per tenant as expected for the specific application.

Sample use case: An admin must be able to make comments required when a record closes for one tenant, but not for another.

For more information on support levels, see [Application support for domain separation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-security/domain-separated-apps.md).

## Overview

Domain separation support in the product enables service providers to offer managed services for enterprise asset management to their customers. This feature also caters to large organizations who manage their subsidiaries as independent domains.

## How domain separation works in Enterprise Asset Management

In Enterprise Asset Management, domain separation occurs in two stages: data separation and process separation. There are two system properties that are used to enable or disable the separation. In the Tokyo release, both data and process are domain-separated.

**Note:**

The [Recommended practice](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-security/bp-domain-sep-recommended.md) is to avoid customizing the base system domain configuration record.

## Required plugins

-   Domain separation extension \(com.glide.domain.msp\_extensions.installer\)
-   Performance Analytics – Domain Support \(com.snc.pa.domain\_support\)
-   Work management \(com.snc.work\_management\)

## Other supported plugins

-   Service Catalog – Domain Separation \(com.glideapp.servicecatalog.domain\_separation\)
-   Procurement \(com.snc.procurement\)

To learn more, see [Domain separation explained](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-security/bp-what-is-domain-separation.md), [Contains queries and domain access](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-security/bp-contains-domain-visibility.md), and [Importance of Default domain](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-security/bp-default-domain.md).

**Parent Topic:**[Enterprise Asset Management reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-asset-management/enterprise-asset-management/reference-enterprise-asset-management.md)

**Related topics**  


[Enterprise Asset Management roles]()

[OT Asset Workspace roles]()

[Asset fields for enterprise assets]()

[Asset audit fields for enterprise assets]()

[Audit results]()

[Enterprise model categories and corresponding classes]()

[Mandatory fields in the bulk import spreadsheets]()

[Normalization status for enterprise models]()

[Model fields for Enterprise Asset Management]()

[Contract fields for Enterprise Asset Management]()

[Maintenance plan fields for Enterprise Asset Management]()

[Maintenance schedule fields for Enterprise Asset Management]()

[Work plan fields for Enterprise Asset Management]()

[Work plan schedule fields for Enterprise Asset Management]()

[Expense line fields for Enterprise Asset Management]()

[Fields inherited from a parent asset group to a sub group]()

[Enterprise asset disposal order stages]()

[Terminology for linear assets]()

[Installed with Enterprise Asset Management for Healthcare]()

[Installed with OT Asset Management]()

[Components installed with Enterprise Asset Management for Data Center and Network Asset Management \(DCNAM\)]()

[Components installed with Enterprise Asset Management for Providers]()

[Scheduled jobs and tables installed with normalization of firmware models]()

[Asset put away task fields]()

[Domain separation for service providers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-security/domain-sep-landing-page.md)

