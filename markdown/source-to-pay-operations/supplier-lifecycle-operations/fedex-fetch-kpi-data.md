---
title: Fetch KPI data using FedEx Dataworks
description: FedEx Dataworks integration lets you retrieve KPI data for a given supplier to create KPIs.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/source-to-pay-operations/supplier-lifecycle-operations/fedex-fetch-kpi-data.html
release: australia
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
keywords: [performance benchmarking, supplier performance, FedEx metrics]
breadcrumb: [FedEx Dataworks Integration, Integrate, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Fetch KPI data using FedEx Dataworks

FedEx Dataworks integration lets you retrieve KPI data for a given supplier to create KPIs.

## Before you begin

Role required: sn\_slm.manager

The supplier must have a valid FedEx Dataworks Supplier ID. Complete supplier validation during the onboarding process in the Registration phase.

## About this task

The **Fetch KPI from FedEx Dataworks** button is accessible from the supplier profile page in the Source-to-Pay Workspace.

**Note:** The **Fetch KPI from FedEx Dataworks** button is only visible for suppliers that have a FedEx Dataworks Supplier ID. Only suppliers with completed supplier validation display this button.

## Procedure

1.  Open the supplier profile page for a supplier with a FedEx Dataworks Supplier ID.

    Navigate to the supplier list, search for the supplier by name, and open the supplier record.

2.  Select **Fetch KPI from FedEx Dataworks**.

    An outbound request for performance evaluation is sent to FedEx Dataworks using the KPI templates provided in the demo data. The demo data includes two KPI templates: Customs delay rate and Shipments claim rate. These templates use the Integration data collection type and reference FedEx Dataworks as the external source.


## Result

KPIs are created for the supplier. You can view the KPIs under the **KPI management** tab.

**Parent Topic:**[FedEx Dataworks Integration for Supplier Lifecycle Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/source-to-pay-operations/supplier-lifecycle-operations/fedex-dataworks-overview.md)

**Related topics**  


[FedEx Dataworks Integration for Supplier Lifecycle Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/source-to-pay-operations/supplier-lifecycle-operations/fedex-dataworks-overview.md)

[Install the S2P Integration FedEx Connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/source-to-pay-operations/supplier-lifecycle-operations/install-fedex-connector.md)

