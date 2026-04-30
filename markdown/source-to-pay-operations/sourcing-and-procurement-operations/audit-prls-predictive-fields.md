---
title: Audit purchase lines automatically when predictive fields change
description: Automated audit compares existing categories with the latest AI prediction when key predictive fields are updated in a service request or purchase requisition, flagging inconsistencies without automatically updating category fields.
locale: en-US
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Automatically assign categories during SR and PR creation, Explore Now Assist for Sourcing and Procurement Operations \(SPO\), Now Assist for SPO, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Audit purchase lines automatically when predictive fields change

Automated audit compares existing categories with the latest AI prediction when key predictive fields are updated in a service request or purchase requisition, flagging inconsistencies without automatically updating category fields.

When key predictive fields in a service request \(SR\) or purchase requisition \(PR\) are updated, the Spend categorization agent runs an automated audit to compare the existing categories with the latest AI prediction. Key predictive fields include Product name, Supplier, Supplier product, Purchase reason, and Short description.

When key predictive fields are updated in a Service Request \(SR\) or Purchase Request \(PR\), the Spend category and Product category fields are automatically populated with AI‑predicted values. A warning message appears on the PRL form informing users to review the AI‑predicted values for accuracy before saving them.

![Purchase request form showing AI prediction warning message and Spend category field populated with "Servers".](../image/spend-product-category-notifications.png)

If the AI‑predicted value does not meet your requirements, you can select a different value from the **Spend category** drop‑down list. The same AI‑predicted and override behavior applies to the **Product category** field as well.

![PRL form showing AI-predicted "Networking" category in drop-down list with other available options.](../image/spend-product-category-ai-prediction.png)

This audit relies on existing categorization rules and taxonomy mappings, along with historical classification data used for training and pattern analysis.

If a category mismatch is detected, the system flags the inconsistency and displays an alert at the line level, without automatically updating the category fields.

The audit runs asynchronously to ensure minimal impact on system performance.

For more information about the prediction logic and flow, refer to the section 'Product and spend category prediction logic' in [Automatically assign categories during SR and PR creation](automatically-assign-categories.md).

**Parent Topic:**[Automatically assign categories during SR and PR creation](automatically-assign-categories.md)

