---
title: View supplier metrics using FedEx Dataworks
description: FedEx Dataworks supplier performance benchmarking retrieves FedEx Dataworks logistics performance metrics for a matched supplier, displayed on the supplier profile page to support supplier evaluation.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/supplier-lifecycle-operations/fedex-supplier-performance-benchmarking.html
release: australia
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
keywords: [performance benchmarking, supplier performance, FedEx metrics]
breadcrumb: [FedEx Dataworks Integration, Integrate, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# View supplier metrics using FedEx Dataworks

FedEx Dataworks supplier performance benchmarking retrieves FedEx Dataworks logistics performance metrics for a matched supplier, displayed on the supplier profile page to support supplier evaluation.

## Before you begin

Role required: sn\_slm.manager

The supplier must have a valid FedEx Dataworks Supplier ID. Supplier validation must be completed during the onboarding process in the Registration phase.

## About this task

FedEx Dataworks supplier performance benchmarking is accessible from the supplier profile page in the Source-to-Pay Workspace for suppliers that have a FedEx Dataworks Supplier ID. Relationship managers can retrieve FedEx Dataworks logistics performance metrics for those suppliers on demand.

**Note:** The **FedEx Dataworks - supplier performance benchmarking** section is only visible for suppliers that have a FedEx Dataworks Supplier ID. Suppliers who haven't completed FedEx Dataworks validation won't see this section.

## Procedure

1.  Open the supplier profile page for a supplier with a FedEx Dataworks Supplier ID.

    Navigate to the supplier list, search for the supplier by name, and open the supplier record.

2.  Navigate to the **Performance** tab.

3.  Locate the **FedEx Dataworks - supplier performance benchmarking** section.

    This section only appears for suppliers with a valid FedEx Dataworks Supplier ID.\[Omitted image "fedex-supplier-performance-result.png"\] Alt text: Performance metrics result

    The FedEx Dataworks performance metrics are presented as key-value pairs that show logistics performance data for the selected supplier.

    Performance metrics are defined and supplied by FedEx Dataworks. Metrics are returned as key-value pairs and displayed directly from the FedEx Dataworks response. The specific metrics available depend on FedEx Dataworks' latest data and may vary by supplier.

    |Performance metrics|Description|Rating scale|
    |-------------------|-----------|------------|
    |Customs Delay Rate|Peer group average percentage for similar industry suppliers, indicates the average percent of shipments that were held or delayed during customs clearance processes over the past year.|0% – 100%|
    |Shipment Claims Rate|Peer group average percentage for similar industry suppliers, indicates the average percent of shipments that had associated claims over the past year.|0% – 100%|

4.  Review other performance metrics including supplier score, supplier risk, domain scores, Overall ESG score, and KPI performance data.

    \[Omitted image "fedex-supplier-performance-result2.png"\] Alt text: Supplier metrics showing overall scores and Domain scores for ESG, Quality, and Speed performance

    \[Omitted image "fedex-supplier-performance-result3.png"\] Alt text: Supplier metrics showing overall scores for ESGand KPI metrics


## What to do next

Use the performance metrics to evaluate supplier performance and make informed decisions about supplier relationships and risk management.

**Parent Topic:**[FedEx Dataworks Integration for Supplier Lifecycle Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/fedex-dataworks-overview.md)

**Related topics**  


[FedEx Dataworks Integration for Supplier Lifecycle Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/fedex-dataworks-overview.md)

[Install the S2P Integration FedEx Connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/install-fedex-connector.md)

[Validate supplier using FedEx Dataworks supplier validation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/fedex-supplier-validation.md)

[Evaluate supplier risk using FedEx Dataworks risk assessment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/fedex-risk-assessment.md)

