---
title: Navigate portfolio types in Digital Portfolio Management
description: Navigate three types of enterprise portfolios in the Digital Portfolio Management \(DPM\) application — service, business applications, and service instance. The way to create a portfolio depends on the type. As of May 2025, Enterprise portfolios are created directly in DPM. Business application and Service instance portfolios are created using the enterprise portfolios tables in the DPM module in UI16.
locale: en-US
release: australia
product: Digital Portfolio Management
classification: digital-portfolio-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 9
breadcrumb: [Enterprise portfolios, Work with portfolios, Digital Portfolio Management, IT Service Management]
---

# Navigate portfolio types in Digital Portfolio Management

Navigate three types of enterprise portfolios in the Digital Portfolio Management \(DPM\) application — service, business applications, and service instance. The way to create a portfolio depends on the type. As of May 2025, Enterprise portfolios are created directly in DPM. Business application and Service instance portfolios are created using the enterprise portfolios tables in the DPM module in UI16.

Enterprise portfolios are structured in a nesting content tree format so you can easily navigate each type of enterprise portfolio. Access Enterprise portfolios using the Enterprise portfolio icon \(![Enterprise portfolios icon.](../image/enterprise-portfolio-gray.png)\). For more information about accessing enterprise portfolios, see [Navigate enterprise portfolios in Digital Portfolio Management](../task/dpm-enterprise-portfolio.md).

Each type of enterprise portfolio offers unique data pertinent to its type. See [the DPM Academy](https://www.servicenow.com/community/itsm-articles/digital-portfolio-management-learning-resources/ta-p/2896465) Learning Resources, especially the video series, for more information about the difference between each portfolio, how they should be used, and who they are for.

## Service portfolios

As of May 2025, you can create service enterprise portfolios directly in the DPM Workspace. Service enterprise portfolios are structured in a nested content tree with the taxonomy node, and then services that are in the service portfolio. You can create a portfolio from scratch or use one of the provided templates. For more information on service enterprise portfolio templates, see [Navigate service enterprise portfolio templates in DPM](dpm-enterprise-portfolio-templates.md).

<table id="table_iw3_hzw_2yb"><thead><tr><th>

Section

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Taxonomy node

</td><td>

-   The first level in the content tree under the service enterprise portfolio.
-   The following information is provided for the taxonomy node:
    -   Header with a short description, owned by name, and total subscribers.
    -   Performance snapshot metrics for availability, open incidents, incidents not updated for 5 days, and new requests.
    -   Needs attention cards for critical incidents, outages, and changes.
-   The **View details** link provides the following information about the taxonomy node.
    -   Header with the service portfolio name, manager name, and total subscribers.
    -   **Overview** tab with performance snapshot metrics and the breakdown of services in the category.

**Note:** DPM versions prior to 2.2.15 may have duplicate services showing in the Service breakdown section. For information, see [KB1123710](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1182501).

    -   **Taxonomy node** tab with all the taxonomy nodes related to the portfolio.
    -   **Services** tab that lists all services in the portfolio, with their parent, classification \(business or technical\), phase, status, criticality, and owned by name. You can also select **Create business service** or **Create technology management service** to perform those tasks in Service Builder.
    -   **Info** tab with a description and general information about the taxonomy node.
    -   **Needs attention** panel that lists critical incidents, outages, and changes.

</td></tr><tr><td>

Service and service offering

</td><td>

-   The next two levels in the content tree under the taxonomy node. Services and service offerings can be either technical or business.
-   The header:

    -   Short description.
    -   Owned by name.
    -   Delivery manager name.
    -   Total subscribers.
    -   Phase \(if using CSDM fields, then life-cycle Stage\)
    -   Status \(if using CSDM fields, then life-cycle Status\)
**Note:** For information about CSDM life-cycle field names, see [Apply the CSDM guidelines to Digital Portfolio Management](../reference/dpm-csdm.md).

-   The performance snapshot metrics for availability, open incidents, incidents not updated for 5 days, and new requests.
-   The Needs attention cards for critical incidents,outages, and changes.
-   The **More menu** icon \(![More menu icon](../../configurable-workforce-optimization-itsm/image/menu-icon.png)\) enables you to:
    -   Add the service or service offering to a personal portfolio. For more information, see [Create a personal portfolio in Digital Portfolio Management](../task/dpm-create-personal-portfolios.md).
    -   Add the service to your DPM homepage. For more information, see [Digital Portfolio Management Workspace homepage](dpm-explore-landing.md).
    -   Edit the service or service offering in Service Builder. For more information, see [Create a service in Service Builder](../../service-builder/task/create-service.md).
-   The **View details** link launches the service or service offering details. For more information, see the Service and service offerings section in [Digital Portfolio Management related applications and data sources](../reference/dpm-related-products.md).

</td></tr></tbody>
</table>## Business application portfolios

The DPM Workspace displays enterprise portfolios in a nested content tree starting with the enterprise taxonomy node at the top level \(there could be more than one\). After the top node, it lists the business applications that are in the enterprise portfolio. Here’s an example of a business application enterprise portfolio content tree.

![Business application enterprise portfolio content tree example](../image/dpm-enterprise-portfolio-example.png "Business application enterprise portfolio content tree example")

**Important:** The image shows the **Portfolio** field as Enterprise business applications. To select a different type of enterprise portfolio from the one you're in, delete the value in the **Portfolio** field, and then select the field \(again\) to see the other portfolio types \(service, business, or service instance\).

<table id="table_wc1_vz4_2yb"><thead><tr><th>

Section

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Enterprise taxonomy node

</td><td>

-   The first level in the content tree under the business application enterprise portfolio. Could contain a second or third level if it has child enterprise taxonomy nodes.
-   The header:
    -   Short description.
    -   Owned by name.
    -   Managed by name.
    -   Total subscribers
-   The portfolio success metrics for availability, incidents with a breached service level agreement \(SLA\), incidents caused by changes, and successful changes.
-   Needs attention cards for critical incidents, outages, changes,alerts, risks, and audits.
-   The **View details** link provides the following information about the enterprise taxonomy node.
    -   Header with the Owned by name and the Managed by name.
    -   **Overview** tab with portfolio success metrics and the breakdown of business applications in the enterprise taxonomy node.
    -   **Taxonomy nodes** tab that lists all the related taxonomy nodes.
    -   **Business applications** tab with a list of the business applications that are in the enterprise taxonomy node.
    -   **Info** tab with a description and general information about the enterprise taxonomy node.
    -   **Needs attention** panel that lists critical incidents, outages, changes, alerts, risks, and audits, for the enterprise taxonomy node.

</td></tr><tr><td>

Business application

</td><td>

-   The next level in the content tree under the enterprise taxonomy node.
-   The header:
    -   Short description.
    -   Application owner name.
    -   Business owner name.
    -   Total subscribers.
    -   Status.

The Overall risk is empty.

-   The portfolio success metrics for availability, incidents with a breached SLA, incidents caused by changes, and successful changes.
-   The Needs attention cards for critical incidents, changes, risks, and audits.
-   The **More menu** icon \(![More menu icon](../../configurable-workforce-optimization-itsm/image/menu-icon.png)\) enables you to add the business application to a personal portfolio. For more information, see [Create a personal portfolio in Digital Portfolio Management](../task/dpm-create-personal-portfolios.md).
-   The **View details** link launches the business application details. For more information, see the Business applications section in [Digital Portfolio Management related applications and data sources](../reference/dpm-related-products.md).

</td></tr></tbody>
</table>## Service instance portfolios

The information in service instance portfolios is similar to that of business application portfolios with some differences that pertain to service instances.

For information about KPI groups in service instance portfolios, see [View service instance details](dpm-app-service-details.md).

<table id="table_xxm_g5w_2yb"><thead><tr><th>

Section

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Enterprise taxonomy node

</td><td>

-   The first level in the content tree under the service instance enterprise portfolio. Could contain a second or third level if it has child enterprise taxonomy nodes.
-   The header:
    -   Short description.
    -   Owned by name.
    -   Managed by name.
    -   Total subscribers.
-   The portfolio success metrics for availability, mean days to resolve \(MTTR\), incidents caused by changes, and successful changes.
-   The Needs attention cards for critical incidents, outages, changes, alerts, risks, and audits.
-   The **View details** link provides the following information about the enterprise taxonomy node.
    -   Header with the Owned by name and the Managed by name.
    -   **Overview** tab with portfolio success metrics and the breakdown of service instances in the enterprise taxonomy node.
    -   **Service instances** tab with a list of the service instances that are in the enterprise taxonomy node.
    -   **Info** tab with a description and general information about the enterprise taxonomy node.
    -   **Needs attention** panel that lists critical incidents, outages, changes, alerts, risks, and audits for the enterprise taxonomy node.

</td></tr><tr><td>

Service instance

</td><td>

-   The next level in the content tree under the enterprise taxonomy node.
-   The header:
    -   Short description.
    -   Owned by name.
    -   Managed by name.
    -   Operational status.

The Overall risk is empty.

-   The portfolio success metrics for availability, incidents with a breached SLA, incidents caused by changes, and successful changes.
-   The Needs attention cards for critical incidents, changes, outages, risks, and alerts.
-   The **More menu** icon \(![More menu icon](../../configurable-workforce-optimization-itsm/image/menu-icon.png)\) enables you to add the service instance to a personal portfolio. For more information, see [Create a personal portfolio in Digital Portfolio Management](../task/dpm-create-personal-portfolios.md).
-   The **View details** link launches the service instance details. For information on what this screen includes, see the Service instances section in [Digital Portfolio Management related applications and data sources](../reference/dpm-related-products.md).

</td></tr></tbody>
</table>**Parent Topic:**[Enterprise portfolios](dpm-enterprise-portfolios.md)

**Related topics**  


[Enterprise portfolios](dpm-enterprise-portfolios.md)

[Navigate enterprise portfolios in Digital Portfolio Management](../task/dpm-enterprise-portfolio.md)

