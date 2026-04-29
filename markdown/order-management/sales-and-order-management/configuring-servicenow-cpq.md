---
title: Configuring CPQ Configurator
description: Plan and configure your implementation of the CPQ Configurator. Product catalog admins and agents run CPQ Configurator in the CSM Configurable Workspace, while customers using self-service features use it in the Business Portal.
locale: en-US
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [configure]
breadcrumb: [Configure, price, quote apps, Configure, Sales and Order Management]
---

# Configuring CPQ Configurator

Plan and configure your implementation of the CPQ Configurator. Product catalog admins and agents run CPQ Configurator in the CSM Configurable Workspace, while customers using self-service features use it in the Business Portal.

## Configuration overview

1.  Install the following applications using the Application Manager:

    -   Order Management v15.3.0
    -   Product configurator v1.0.1
    -   CPQ Integration v2.1.0
    -   CPQ Configurator v1.2.5
    -   Quote Management v9.1.0
    -   Customer Life Cycle Management Workflows v5.1.1
    -   Product and Pricing Rules v9.0.0
    -   Opportunity Management v8.0.0
    -   Sales Cart v2.1.0
    **Note:** Other applications, such as Product Catalog Management Core v17.1.0, and Pricing Management v15.0.0 are installed automatically with the preceding applications.

2.  [Set up a ServiceNow instance for CPQ Integration](../task/cpq-integration-create-certificates.md).
3.  [Provision a Logik.ai instance](../task/set-up-logik-instance.md)
4.  [Set up a ServiceNow instance connection with a Logik.ai instance](../task/connect-sn-instance-logik.md).
5.  [Set up an external connection in CPQ](../task/set-up-external-connection-logik.md).
6.  [Enable the CPQ Configurator](../task/enable-advanced-configurator.md).

    If you're currently using the Sales and Order Management product configurator and want to use the CPQ Configurator, use the **enable\_advanced\_configuration** system property to enable the CPQ Configurator.


