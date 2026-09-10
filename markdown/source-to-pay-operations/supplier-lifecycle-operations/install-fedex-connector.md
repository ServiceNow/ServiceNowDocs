---
title: Install the S2P Integration FedEx Connector
description: Install the S2P Integration FedEx Connector app to enable the FedEx Dataworks integration in Supplier Lifecycle Operations.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/supplier-lifecycle-operations/install-fedex-connector.html
release: australia
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: task
last_updated: "2026-08-24"
reading_time_minutes: 2
keywords: [installation, FedEx Dataworks, S2P Integration]
breadcrumb: [FedEx Dataworks Integration, Integrate, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Install the S2P Integration FedEx Connector

Install the S2P Integration FedEx Connector app to enable the FedEx Dataworks integration in Supplier Lifecycle Operations.

## Before you begin

A basic authentication profile must be created using the FedEx Dataworks guidelines.

Role required: admin

## About this task

The S2P FedEx Integration Connector is a Store app that enables Supplier Lifecycle Operations to communicate with FedEx Dataworks. The app includes demo data that must be loaded for the integration to work correctly. After installation and demo data loading, FedEx Dataworks features become available in the supplier onboarding playbook and on the supplier profile page.

## Procedure

1.  Navigate to the ServiceNow Store and search for **S2P FedEx Integration Connector**.

2.  Select **Get** to install the app on your instance.

3.  Verify that the installation completed without errors.

    The installation process typically completes within a few minutes. You can monitor progress in the System Logs.

4.  Load the demo data by navigating to **System Applications** &gt; **Applications**, locating the S2P Integration FedEx Connector app, and selecting **Load Demo Data**.

    The demo data includes KPI templates, threshold sets, a Shipping performance domain, and an ERP source record for FedEx Dataworks. This data is required for the FedEx Dataworks to function correctly.

    The demo data is loaded into your instance.

5.  Verify that the demo data loaded correctly by navigating to **Supplier Lifecycle Operations** &gt; **Performance Management** &gt; **KPI Templates** and confirming that the Customs delay rate and Shipments claim rate templates are present.

6.  For each FedEx Dataworks-related KPI template, verify that the **External source** field is populated with FedEx Dataworks.

    The **External source** field is hidden by default on the KPI template form. To view this field, customize the form layout. If the field is empty for FedEx Dataworks-related templates, populate it manually with FedEx Dataworks from the ERP source table to prevent integration failures.


## Result

The FedEx Dataworks features are now available in the supplier onboarding playbook and on the supplier profile page for suppliers. The demo data provides KPI templates that FedEx Dataworks uses to create supplier-specific KPIs.

## What to do next

To start using the FedEx Dataworks integration, initiate a supplier's onboarding and match their details to establish a FedEx Dataworks Supplier ID. For more information, see [Validate supplier using FedEx Dataworks supplier validation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/fedex-supplier-validation.md).

**Parent Topic:**[FedEx Dataworks Integration for Supplier Lifecycle Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/fedex-dataworks-overview.md)

**Related topics**  


[FedEx Dataworks Integration for Supplier Lifecycle Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/fedex-dataworks-overview.md)

[Validate supplier using FedEx Dataworks supplier validation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/fedex-supplier-validation.md)

[Evaluate supplier risk using FedEx Dataworks risk assessment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/fedex-risk-assessment.md)

[View supplier metrics using FedEx Dataworks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/fedex-supplier-performance-benchmarking.md)

