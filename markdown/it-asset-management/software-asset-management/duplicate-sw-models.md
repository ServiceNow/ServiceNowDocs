---
title: Automatic creation of software models
description: Software models are automatically created for software installations if one doesn't already exist.
locale: en-US
release: xanadu
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Software models and Software entitlements, Exploring Software Asset Management, Software Asset Management, IT Asset Management]
---

# Automatic creation of software models

Software models are automatically created for software installations if one doesn't already exist.

All software installations need to be associated to software models. Being associated to a software model, helps in remediation and ensures that the software installations are included during cost estimation in order to be compliant.

If a software installation doesn't correspond to any software model, the system automatically creates a software model.

-   To create a software model automatically for licensable products, enable the property **Automatically create software models for all 'licensable' products**.
-   To create a software model for not licensable products, enable the property **Automatically create software models for all 'not licensable' products**.

**Note:** You can update the above mentioned properties by navigating to **Software Asset** &gt; **Administration** &gt; **Properties**.

When reconciliation runs, the system searches if any software model exists for the software installation. The search for an existing software model is based on attributes such as version, edition, language, platform, and install condition. If all conditions for the attributes in an existing software model match, then a software model is not created hence avoiding the creation of duplicate software models.

A software model is only created if no match is found. The software model is created across versions and for the specific edition, if available. However a software model is never created against a specific version.

Discovery maps are associated to software models only if a discovery map exists for that software model. If a corresponding discovery map doesn't exist in the Content Service library, a software model still gets created without a discovery map.

You can identify if a software model is automatically created by the **Automatically create software models for all 'licensable' products** or **Automatically create software models for all 'not licensable' products** property. In the Software Model list view, select the gear icon to display the `Created source` column. If the value in this property says `System property`, then it indicates that the software model was automatically created by one of the properties.

**Parent Topic:**[Software models and Software entitlements](software-models-and-entitlements.md)

**Related topics**  


[Software Asset Management properties](../reference/sam-properties.md)

