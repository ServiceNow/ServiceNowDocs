---
title: Set up ServiceNow CPQ Configurator without guided setup
description: Plan and configure your implementation of the ServiceNow CPQ Configurator. Product catalog admins and agents use the Configurator in the CSM Configurable Workspace, while users using self-service features use it in the Business Portal.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/configuring-servicenow-cpq.html
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [configure]
breadcrumb: [ServiceNow CPQ Configurator, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Set up ServiceNow CPQ Configurator without guided setup

Plan and configure your implementation of the ServiceNow CPQ Configurator. Product catalog admins and agents use the Configurator in the CSM Configurable Workspace, while users using self-service features use it in the Business Portal.

## Configuration overview

1.  Install the following applications using the Application Manager:

    -   FSM CSM and Configurable Workspace Foundation \(sn\_cwf\_wrkspc\)
    -   Order Management \(sn\_ind\_tmt\_orm\)
    -   Product Catalog Management Core \(sn\_prd\_pm\)
    -   Price Management \(sn\_csm\_pricing\)
    -   Quote Management Application \(sn\_quote\_mgmt\)
    -   Product Configurator \(sn\_prd\_config\_ui\)
    -   Customer Life Cycle Management Workflows \(sn\_l2c\_cust\_flows\)
    -   Product and pricing rules \(sn\_csm\_price\_mtrx\)
    -   Opportunity Management Application \(sn\_opty\_mgmt\)
    -   Product Offering Recommendations \(sn\_prd\_pm\_ra\)
    -   Order Management Portal \(sn\_ord\_mgmt\_portal\)
    -   Order Operations Case Management \(sn\_order\_case\)
    -   Case Management for Invoice Operations \(sn\_csm\_invoice\)
    -   Sales Cart \(sn\_sales\_cart\)
    -   Customer Life Cycle Management Self Service \(sn\_clm\_selfservice\)
    -   Contracts and Entitlement Workflows \(sn\_contract\_ent\_wf\)
    -   Sales Quota Application \(sn\_quota\_app\)
    -   Customer Service Portal \(sn\_csm\_portal\)
    -   CPQ Integration \(sn\_cpq\_intg\)
    -   CPQ Configurator \(sn\_cpq\_config\)
    **Note:** Other applications, such as Product Catalog Management Core v17.1.0, and Pricing Management v15.0.0 are installed automatically with the preceding applications.

2.  [Set up instance for ServiceNow CPQ integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/cpq-integration-create-certificates.md).
3.  [Request a ServiceNow CPQ tenant](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/set-up-logik-instance.md)
4.  [Connect your instance with ServiceNow CPQ instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/connect-sn-instance-logik.md).
5.  [Set up an external connection in ServiceNow CPQ](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/set-up-external-connection-logik.md).
6.  [Enable the ServiceNow CPQ Configurator](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/enable-advanced-configurator.md).

    If you're currently using the Sales Customer Relationship Management product configurator and want to use the ServiceNow CPQ Configurator, enable the **enable\_advanced\_configuration** system property.


