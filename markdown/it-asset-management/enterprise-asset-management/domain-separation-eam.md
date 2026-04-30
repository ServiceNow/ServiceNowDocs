---
title: Domain separation and Enterprise Asset Management
description: Domain separation is supported in Enterprise Asset Management. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
release: zurich
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [References, Enterprise Asset Management, IT Asset Management]
---

# Domain separation and Enterprise Asset Management

Domain separation is supported in Enterprise Asset Management. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

## Support level: Standard

-   Includes all aspects of **Basic** level support.
-   Application properties are domain-aware as needed.
-   Business logic: The service provider \(SP\) creates or modifies processes per customer. The use cases reflect proper use of the application by multiple SP customers in a single instance.
-   The instance owner must configure the minimum viable product \(MVP\) business logic and data parameters per tenant as expected for the specific application.

Sample use case: An Admin must be able to make comments required when a record closes for one tenant, but not for another.

For more information on support levels, see [Application support for domain separation](https://www.servicenow.com/docs/access?context=domain-separated-apps&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

## Overview

Domain separation support in the product enables service providers to offer managed services for enterprise asset management to their customers. This feature also caters to large organizations who manage their subsidiaries as independent domains.

## How domain separation works in Enterprise Asset Management

In Enterprise Asset Management, domain separation occurs in two stages: data separation and process separation. There are two system properties that are used to enable or disable the separation. In the Tokyo release, both data and process are domain-separated.

**Note:**

The [Recommended practice](https://www.servicenow.com/docs/access?context=bp-domain-sep-recommended&version=zurich&pubname=zurich-platform-security&ft:locale=en-US) is to avoid customizing the base system domain configuration record.

## Required plugins

-   Domain separation extension \(com.glide.domain.msp\_extensions.installer\)
-   Performance Analytics – Domain Support \(com.snc.pa.domain\_support\)
-   Work management \(com.snc.work\_management\)

## Other supported plugins

-   Service Catalog – Domain Separation \(com.glideapp.servicecatalog.domain\_separation\)
-   Procurement \(com.snc.procurement\)

To learn more, see [Domain separation explained](https://www.servicenow.com/docs/access?context=bp-what-is-domain-separation&version=zurich&pubname=zurich-platform-security&ft:locale=en-US), [Contains queries and domain access](https://www.servicenow.com/docs/access?context=bp-contains-domain-visibility&version=zurich&pubname=zurich-platform-security&ft:locale=en-US), and [Importance of Default domain](https://www.servicenow.com/docs/access?context=bp-default-domain&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

**Parent Topic:**[Enterprise Asset Management reference](reference-enterprise-asset-management.md)

**Related topics**  


[Enterprise Asset Management roles](../reference/eam-roles.md)

[OT Asset Workspace roles](../reference/ot-workspace-roles.md)

[Asset fields for enterprise assets](../reference/asset-fields-eam.md)

[Asset audit fields for enterprise assets](../reference/asset-audit-record-fields-eam.md)

[Audit results](../reference/audit-results-eam.md)

[Enterprise model categories and corresponding classes](../reference/enterprise-model-categories.md)

[Mandatory fields in the bulk import spreadsheets](../reference/mandatory-bulk-fields.md)

[Normalization status for enterprise models](../reference/norm-status-eam.md)

[Model fields for Enterprise Asset Management](../reference/eam-model-fields.md)

[Contract fields for Enterprise Asset Management](../reference/contract-fields-eam.md)

[Maintenance plan fields for Enterprise Asset Management](../reference/maintenance-plan-fields-eam.md)

[Maintenance schedule fields for Enterprise Asset Management](../reference/maintenance-schedule-fields-eam.md)

[Work plan fields for Enterprise Asset Management](../reference/wp-fields-eam.md)

[Work plan schedule fields for Enterprise Asset Management](../reference/work-plan-schedule-fields-eam.md)

[Expense line fields for Enterprise Asset Management](../reference/expense-line-fields-eam.md)

[Fields inherited from a parent asset group to a sub group](../reference/subgroups-parent-fields-eam.md)

[Enterprise asset disposal order stages](../reference/eamasset-disposalorder-stages.md)

[Terminology for linear assets](../reference/terms-eam.md)

[Installed with Enterprise Asset Management for Healthcare](../reference/installed-with-eam-healthcare.md)

[Installed with OT Asset Management](../reference/installed-with-otam.md)

[Components installed with Enterprise Asset Management for Data Center and Network Asset Management \(DCNAM\)](../reference/installed-with-eam-dcnam.md)

[Components installed with Enterprise Asset Management for Providers](../reference/installed-with-eam-providers.md)

[Scheduled jobs and tables installed with normalization of firmware models](../reference/firmware-tables-jobs-ot.md)

[Asset put away task fields](../reference/put-away-task-form-eam.md)

[Domain separation for service providers](https://www.servicenow.com/docs/access?context=domain-sep-landing-page&version=zurich&pubname=zurich-platform-security&ft:locale=en-US)

