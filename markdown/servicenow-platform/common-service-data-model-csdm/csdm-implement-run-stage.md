---
title: CSDM implementation stages — Run
description: In the Run stage, you set up the relationship between a technology and the business that sells and/or consumes the technology.
locale: en-US
release: xanadu
product: Common Service Data Model \(CSDM\)
classification: common-service-data-model-csdm
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Implement, CSDM, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# CSDM implementation stages — Run

In the Run stage, you set up the relationship between a technology and the business that sells and/or consumes the technology.

## ITSM considerations during the Run stage

When you use ITSM, you must understand the impact that a technology can have on your business. For example, your business might perform the following actions:

-   Consume the technology.
-   Sell the technology \(as is the case with Customer Service Management\).
-   Both sell the technology and consume it.

## Benefits of the operations that you perform in the Run stage

-   Run-stage operations ensure impact assessment for Incident Management and Change Management. Within an incident or change, you can identify the impacted business, assuming relationships exist between the selected CI and the impacted businesses.
-   Run-stage operations provide a foundation for using Service Portfolio Management in the Digital Portfolio Management \(DPM\). Service owners can monitor service portfolios and understand service-related information including service trends, improvement initiatives, service performance, and outage monitoring.
-   Run-stage operations provide a foundation for ITSM capabilities. This foundation populates the related “Subscribe by” table on a service offering to identify the business and subscribers affected. Business service offerings can identify subscribers by user, company, location, department, and group.

## Tables that you work on during the Run stage

![Tables that you work on during the Run stage.](../image/run-stage.png)

**Note:** Some of the classes that you implement in this stage are logical CIs. Logical CIs aren’t created through Discovery, so their **Model ID** values might not refer to product model \(application model, service model, or software model\) records. To help you to migrate to a product-centric management paradigm, each instance of a logical CI should be associated with a product model. See [Auto-generate product models for logical CIs](../task/csdm-auto-create-prod-model-for-ci.md).

-   **Business service portfolio table \[service\_portfolio\]**

    **Note:** The Business service portfolio is not a CMDB table.

    A business service portfolio is not a CMDB table. A business service portfolio is a hierarchical collection of business services \(products and services\) that define a business objective.

-   **Business service table \[cmdb\_ci\_service\_business\]**

    The business service table is a base-system CMDB table. This table identifies a business objective that uses \(and depends on\) the infrastructure that technology uses.

    This dependency means that the business service must sell or consume that infrastructure.

-   **Business service offering table \[service\_offering\] \(service offering classified as a "business service"\)**

    Business service offerings are the starting point for configuring Service Portfolio Management. Business service offerings consist of one or more service commitments. These service commitments uniquely define the level of service in terms of availability, scope, pricing, and other factors.

    The business service offering comes from the service. The business service offering is fine-tuned based on how the parent serves a specific technical need.

    Every business service should have at least one business service offering.

-   **Service catalog**

    A service catalog \(sometimes called a request catalog or service request catalog\) is a set of business and technical products, services, service commitment options, and offerings that users can order on a self-service basis. You can manage a catalog to present your available products and services to users as catalog items. Catalogs are described in detail in [Service Catalog](../../service-catalog-management/concept/service-catalog.md).


**Parent Topic:**[Implementing the CSDM framework in stages](csdm-implementation-stages.md)

