---
title: FedEx Dataworks Integration for Supplier Lifecycle Operations
description: FedEx Dataworks brings logistics intelligence into Supplier Lifecycle Operations, surfacing shipping patterns and delivery data to support supplier onboarding and risk decisions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/supplier-lifecycle-operations/fedex-dataworks-overview.html
release: australia
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: concept
last_updated: "2026-08-24"
reading_time_minutes: 5
breadcrumb: [Integrate, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# FedEx Dataworks Integration for Supplier Lifecycle Operations

FedEx Dataworks brings logistics intelligence into Supplier Lifecycle Operations, surfacing shipping patterns and delivery data to support supplier onboarding and risk decisions.

## About FedEx Dataworks

FedEx Dataworks combines unmatched, proprietary real-world data signals with advanced analytics to power ServiceNow's Source-to-Pay workflows. Relationship managers can use these signals during supplier onboarding to validate suppliers, evaluate risk, and benchmark supplier performance — without leaving the supplier workspace.

**Important:** Check your entitlements to determine whether you have access to FedEx Dataworks for Supplier Lifecycle Operations. This integration is available from the Australia September 2026 release onwards.

## How the FedEx Dataworks integration works

The integration uses an outbound request table owned by the Source-to-Pay integration framework scope. The FedEx Dataworks app on the platform listens to this table and populates responses. No direct API configuration is required on the Supplier Lifecycle Operations side beyond installing the S2P Integration FedEx Connector app.

The integration introduces a new data collection type called Integration for KPI templates and KPIs. This collection type enables automated data retrieval from external sources such as FedEx Dataworks. When you install the S2P Integration FedEx Connector app, demo data is loaded that includes KPI templates configured with the Integration data collection type.

## Key features

The FedEx Dataworks integration includes the following features:

-   **Supplier validation in supplier onboarding Registration stage**

    Verifies a supplier's details against FedEx Dataworks records to establish a FedEx Dataworks Supplier ID. This step is part of the supplier onboarding playbook and is required before risk assessment or performance benchmarking data can be retrieved. For more information, see [Validate supplier using FedEx Dataworks supplier validation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/fedex-supplier-validation.md).

-   **FedEx Dataworks risk assessment in supplier onboarding Qualification stage**

    Returns risk factor ratings for a matched supplier, covering customs risk, restricted country screening, and dangerous goods risk. Risk assessment is available in the supplier onboarding playbook after a successful supplier match. For more information, see [Evaluate supplier risk using FedEx Dataworks risk assessment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/fedex-risk-assessment.md).

-   **Supplier performance benchmarking**

    Retrieves FedEx Dataworks logistics performance metrics for a matched supplier, displayed in a dedicated section on the supplier profile page. For more information, see [View supplier metrics using FedEx Dataworks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/fedex-supplier-performance-benchmarking.md).


## Demo data

The S2P Integration FedEx Connector app includes demo data that provides a foundation for using FedEx Dataworks features. The demo data includes:

-   Two KPI templates: Customs delay rate and Shipments claim rate
-   Threshold sets for each KPI template with four default thresholds
-   A Shipping performance domain record
-   Threshold values for the KPI templates
-   An ERP source record for FedEx Dataworks

The KPI templates use the Integration data collection type and reference FedEx Dataworks as the external source. When FedEx Dataworks sends performance data, KPIs are created for specific suppliers based on these templates.

## Prerequisites

Confirm that the following apps are installed:

-   Source-to-Pay integration framework
-   Supplier Operations
-   Supplier Relationship and Performance Management

For more information about installing Supplier Lifecycle Operations applications, see [Configure Supplier Lifecycle Operations](https://www.servicenow.com/docs/r/source-to-pay-operations/supplier-lifecycle-operations/config-supp-mgmt.html).

To use FedEx Dataworks for Supplier Lifecycle Operations, install the S2P Integration FedEx Connector app and load the demo data. For more information, see [Install the S2P Integration FedEx Connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/install-fedex-connector.md).

-   **[Install the S2P Integration FedEx Connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/install-fedex-connector.md)**  
Install the S2P Integration FedEx Connector app to enable the FedEx Dataworks integration in Supplier Lifecycle Operations.
-   **[Validate supplier using FedEx Dataworks supplier validation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/fedex-supplier-validation.md)**  
Supplier validation connects a supplier's location to a FedEx Dataworks record, returning a FedEx Dataworks Supplier ID that unlocks risk assessment and performance benchmarking data for that supplier.
-   **[Evaluate supplier risk using FedEx Dataworks risk assessment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/fedex-risk-assessment.md)**  
FedEx Dataworks risk assessment returns logistics-based risk factor ratings for a matched supplier, helping relationship managers evaluate supplier risk during onboarding.
-   **[Fetch KPI data using FedEx Dataworks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/fedex-fetch-kpi-data.md)**  
FedEx Dataworks integration lets you retrieve KPI data metrics for a given supplier, using which KPIs are created.
-   **[View supplier metrics using FedEx Dataworks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/fedex-supplier-performance-benchmarking.md)**  
FedEx Dataworks supplier performance benchmarking retrieves FedEx Dataworks logistics performance metrics for a matched supplier, displayed on the supplier profile page to support supplier evaluation.

**Parent Topic:**[Integrate Supplier Lifecycle Operations with other applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/integrate-slo.md)

**Related topics**  


[Supplier Lifecycle Operations integration framework]()

[Craft.co Integration for Supplier Lifecycle Operations]()

[News Integration for Supplier Lifecycle Operations]()

[Relish Integration for Supplier Lifecycle Operations]()

[Install the S2P Integration FedEx Connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/install-fedex-connector.md)

[Validate supplier using FedEx Dataworks supplier validation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/fedex-supplier-validation.md)

[Evaluate supplier risk using FedEx Dataworks risk assessment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/fedex-risk-assessment.md)

[View supplier metrics using FedEx Dataworks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/fedex-supplier-performance-benchmarking.md)

