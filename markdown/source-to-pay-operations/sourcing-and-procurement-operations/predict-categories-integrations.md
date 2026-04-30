---
title: Predict categories for PRLs and POLs imported through integrations
description: Automatically predict and assign product and spend categories for imported purchase requisition lines and purchase order lines using scheduled on-demand scripts.
locale: en-US
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Automatically assign categories during SR and PR creation, Explore Now Assist for Sourcing and Procurement Operations \(SPO\), Now Assist for SPO, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Predict categories for PRLs and POLs imported through integrations

Automatically predict and assign product and spend categories for imported purchase requisition lines and purchase order lines using scheduled on-demand scripts.

The Spend categorization agent automatically predicts and assigns product and spend categories for imported purchase requisition lines \(PRLs\) and purchase order lines \(POLs\) using scheduled on-demand scripts.

The following scheduled on-demand scripts have been added:

-   **Product and spend category prediction for purchase line**: Updates the spend and product category fields on PRLs imported through integration from third-party systems.
-   **Product and spend category prediction for purchase order line**: Updates the spend and product category fields on POLs imported through integration from third-party systems.

After the PRLs and POLs are imported into your instance, open the appropriate scheduled on-demand script and select **Execute Now** to run the script and update the spend and product category fields.![Scheduled Script Execution page showing the product and spend category prediction script with Execute Now button.](../image/prl-on-demand.png)

## How product and spend category updates work for imported PRLs and POLs

-   Predictions are applied automatically when category fields are empty.
-   Only users with admin role can run on demand jobs for bulk updates.
-   You receive an email confirmation once a job completes.
-   Jobs resume from where the previous run ended.
-   POLs linked to PRLs inherit the spend category from the associated PRLs, while standalone POLs receive AI-predicted categories.

**Parent Topic:**[Automatically assign categories during SR and PR creation](automatically-assign-categories.md)

