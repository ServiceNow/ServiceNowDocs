---
title: IBM reconciliation for IBM Authorized SAM Provider \(IASP\) integrations
description: IBM reconciliation keeps your IBM license positions accurate and up-to-date without requiring manual calculations. Reconciliation runs weekly or on-demand.
locale: en-US
release: xanadu
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Authorized SAM Provider \(ASP\) integrations for IBM, Software Asset Management publisher pack for IBM, Supported software publisher licenses, Software Asset Management, IT Asset Management]
---

# IBM reconciliation for IBM Authorized SAM Provider \(IASP\) integrations

IBM reconciliation keeps your IBM license positions accurate and up-to-date without requiring manual calculations. Reconciliation runs weekly or on-demand.

When the Software Asset Management application calculates the number of rights that are required for a processor value unit \(PVU\), resource value unit \(RVU\), or virtual processor core \(VPC\) license, it calculates two different numbers based on whether you are using the license to its full capacity or sub-capacity. The Software Asset Management application uses this information alongside the [daily aggregated peak usage of your IBM software product](../task/view-daily-aggregated-peak-usage-ibm-products.md) and the usage type of your [PVU, RVU](ibm-pvu-rvu-licensing.md), or [VPC](ibm-virtual-processor-core-licensing.md) license to determine the high-water mark, or peak usage, of your IBM software product over a 90 day period.

**Note:** You can determine the high-water mark of your IBM software product per region, including the Americas, EMEA, and APAC.

The Software Asset Management application then uses the high-water mark value to reconcile your IBM software product so that you can determine if your license is in compliance.

**Parent Topic:**[Authorized SAM Provider \(ASP\) integrations for IBM](ibm-asp-integration.md)

