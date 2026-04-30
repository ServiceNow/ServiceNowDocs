---
title: Sales promotion campaign data model
description: A sales promotion is a marketing strategy of implementing new ideas to increase sales, raise brand awareness, and provide discounts to the customers.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Data model, Reference, Manufacturing Commercial Operations]
---

# Sales promotion campaign data model

A sales promotion is a marketing strategy of implementing new ideas to increase sales, raise brand awareness, and provide discounts to the customers.

## Introduction to sales promotion campaign claims

Manufacturers or Original equipment manufacturers \(OEMs\) announce the sales promotion discounts or offers to the dealers. These promotions are applicable to a set of customers or all the customers based on the OEM marketing strategies. The dealer agents can raise the promotion claims to OEMs for the reimbursement of the discounts or offers provided during the sales process. The sales promotion feature enables the dealer to raise the claims post sales, which can be approved or rejected by the OEM depending on the claim case.

Sales promotion has three main parts:

-   Creation of sales promotion by the OEM
-   Creation of claim against the promotion by the dealer
-   Review and reimbursement of the claim by the OEM

The following diagram shows the entities and their relationships within the Sales promotion campaign claim application.

![Decorative](../image/Data-model-sales-promotion.png "Sales promotion campaign data model")

## Bulk Import Sales Promotion claim

The sales promotion supports bulk import functionality, where the dealer sales agents can import a spreadsheet with multiple claims for review and approval. To enable bulk import, you must customize it on the Customer Service Management \(CSM\) or Business Location Service Portal \(BLSP\) portals.

To learn more about the Business Location Service Portal, see [Using the Business Location Service Portal](https://www.servicenow.com/docs/access?context=using-blsp-portal&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US).

-   **[Sales Promotion Campaign Claim tables](sales-promotion-campaign-claim-table.md)**  
This section explains the sales promotion campaign claims tables in Manufacturing Commercial Operations.

**Parent Topic:**[Data model](data-model.md)

