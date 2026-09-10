---
title: Set up ServiceNow CPQ Configurator without guided setup
description: Plan and configure your implementation of the ServiceNow CPQ Configurator. Product catalog admins and agents use the Configurator in the CRM Workspace, while users using self-service features use it in the Business Portal.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/configuring-servicenow-cpq.html
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [configure]
breadcrumb: [Set up CPQ Configurator, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Set up ServiceNow CPQ Configurator without guided setup

Plan and configure your implementation of the ServiceNow CPQ Configurator. Product catalog admins and agents use the Configurator in the CRM Workspace, while users using self-service features use it in the Business Portal.

## Configuration overview

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.
2.  Install the following plugins searching by name or ID; if the plugin does not appear in the results, request it from the ServiceNow Store. Select a version and **Load demo data** as required.

    -   CSM and FSM Workspace Foundation\(sn\_cwf\_wrkspc\)
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
    -   Customer Life Cycle Managment Self Service \(sn\_clm\_selfservice\)
    -   Customer Service Portal \(sn\_csm\_portal\)
    -   CPQ Integration \(sn\_cpq\_intg\)
    -   CPQ Configurator \(sn\_cpq\_config\)
    -   Contracts and Entitlement Workflows \(sn\_contract\_ent\_wf\)
    -   Sales Quota Application \(sn\_quota\_app\)
    The following are dependent plugins that are installed with the above mentioned plugins. Review and install the plugins if they aren't installed already.

    -   Product Catalog Management Core \(sn\_prd\_pm\) - installed with Price Management, Product Configurator, Product Offering Recommendations
    -   Customer Life Cycle Management Workflows \(sn\_l2c\_cust\_flows\) - installed with Order management and Quote Management Application, Contracts and Entitlement Workflows
    -   Price Management \(sn\_csm\_pricing\) - installed with Product and pricing rules, Sales Cart
    -   Order Management \(sn\_ind\_tmt\_orm\) - installed with Order Management Portal, Order Operations Case Management
    -   CPQ Integration \(sn\_cpq\_intg\) - installed with CPQ Configurator
3.  [Set up instance for CPQ integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/cpq-integration-create-certificates.md).
4.  [Request a CPQ tenant](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/set-up-logik-instance.md)
5.  [Connect your instance with CPQ instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/connect-sn-instance-logik.md).
6.  [Set up an external connection in CPQ](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/set-up-external-connection-logik.md).
7.  [Enable the CPQ Configurator](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/enable-advanced-configurator.md).

    If you're currently using the Sales Customer Relationship Management product configurator and want to use the ServiceNow CPQ Configurator, enable the **enable\_advanced\_configuration** system property.


