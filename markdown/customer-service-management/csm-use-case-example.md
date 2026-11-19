---
title: Customer Service Management examples
description: In this example, the CSDM helps the fictitious ACME technology company use CSM to manage network monitoring services for customers.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/customer-service-management/csm-use-case-example.html
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [CSDM guidelines, Data models, Set up your environment, Configure, Customer Service Management]
---

# Customer Service Management examples

In this example, the CSDM helps the fictitious ACME technology company use CSM to manage network monitoring services for customers.

## Example scenario: Key personas and how they benefit

ACME offers a network monitoring service to its enterprise customers who can purchase either the Platinum, Gold, or Silver offering. A customer, Boxeo, has purchased the network monitoring Platinum offering \(Sold Product\) and is using it in development and production environments \(Install Base Item\).

\[Omitted image "csm-data-model-example-v5.png"\] Alt text: CSM data model example.

The key personas \(customer service agents, network operations center \(NOC\) engineers, service owners, and customers\) can complete the following tasks:

**Customer service agents can**:

-   View the products and services that the customer has purchased \(Sold Product\) and installed \(Install Base\).

    \[Omitted image "csm-agents-identify-products.png"\] Alt text: CSM agents view products customers have purchased and installed by customers.

-   View the service offering associated with the sold product. The sold product references the service offering.

    \[Omitted image "csm-agents-sold-products.png"\] Alt text: CSM agents view service offering details for sold products.

-   View the health status of Install Base Items

    \[Omitted image "csm-agents-view-health.png"\] Alt text: CSM agents can view the health status of Install Base Items.


**NOC engineers can**: View customers affected by a service issue and inform customer service. Specifically, they can perform the following operations:

-   View the affected Install Base Items and add it to or remove it from an Account. The Install Base item references the application service \(CI\). The CI it depends on should be one of the CIs affected. The CI should also be referenced in the Alert to show that Install Base Item \(and therefore the Account or Consumer\) as affected.

-   Create a proactive case from an alert and inform the customer service team of the service issue or outage.

\[Omitted image "noc-engineers.png"\] Alt text: NOC engineers can view the customers affected by the service issue.

**Service owners can**: View the customers that are subscribed to a service offering.\[Omitted image "svc-owners-view.png"\] Alt text: Service owners can view customers subscribed to a service offering.

**Customers can**:

-   View the install base items and details.
-   View outages and service issues.

    \[Omitted image "customer-view-install-base.png"\] Alt text: Customers can view the install base and outages from the customer portal.

-   View products they have purchased.
-   Request services related to the products they’ve purchased.

    \[Omitted image "customer-view-prod.png"\] Alt text: Customers can view products purchased and request related services.


## Example CSM and CSDM use cases

-   **Service with multiple packages**

    ACME offers a Credit Check Service to its enterprise customers. They can purchase the Platinum, Gold, or Silver offering.

    \[Omitted image "svcs-with-multiple-packages.png"\] Alt text: Service with multiple packages.

-   **Service with optional components**

    ACME offers a Billing Service to its enterprise customers. They can purchase the bundle or one or more of the component offerings \(for example, invoices, payments, or discounts\).

    \[Omitted image "svcs-optional-components.png"\] Alt text: Service with optional components.

-   **Service with a physical product**

    ACME offers a Digital Printing Solution. Customers can purchase either the bundle or the printer along with one more service offering \(for example, Scan and Email Monitoring\).

    \[Omitted image "svc-with-physical-prod.png"\] Alt text: Service with a physical product.

-   **Service sold to multiple customers**

    ACME sells a Pharmacy Manager Service to two customers: Boxeo and Avid Inc.

    \[Omitted image "svc-sold-multiple-customers.png"\] Alt text: Service sold to multiple customers.

-   **Service used by multiple customers**

    ACME deploys both Boxeo and Avid on the same production instance \(multi-tenant model\).

    \[Omitted image "svc-used-by-multiple-customers.png"\] Alt text: Service used by multiple customers.

-   **Service used on-premises**

    ACME offers an Order Management service. This purchase is tracked in the ServiceNow AI Platform but is used on-premises.

    \[Omitted image "svc-on-premise.png"\] Alt text: Service used on-premise.


## Additional information

For more information about the relevant CSM features and tasks, see the following topics:

[Configure form views for Service Portfolio Management integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/configure-form-views-spm-csm.md)

[View product information from the Customer Service Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/view-product-info-csp.md)

[Create a proactive case from an alert](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/case-alert-workspace.md)

[Create a case for install base from the Customer Service homepage](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/create-case-install-base.md)

[Proactive Customer Service Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/proactive-service-operations.md)

[Service health status for install base](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/service-health-pcso.md)

[Configure install base](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/configure-install-base.md)

[Outage tracking for install base](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/outage-tracking-csm.md)

[View install base information from the Customer Service Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/view-install-base-info.md)

[View install base information in Agent Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/install-base-aw-csm.md)

[View product information from the Customer Service Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/view-product-info-csp.md)

[View sold product information in Agent Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/view-sold-product-info-workspace.md)

