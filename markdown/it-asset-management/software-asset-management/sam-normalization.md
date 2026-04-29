---
title: Software normalization
description: Standardize discovered software model data within the Software Asset Management application through the process of software model normalization.
locale: en-US
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
keywords: [Software model normalization, software model normalization rule, software normalization statuses,]
breadcrumb: [Software discovery and normalization, Exploring Software Asset Management, Software Asset Management, IT Asset Management]
---

# Software normalization

Standardize discovered software model data within the Software Asset Management application through the process of software model normalization.

When a new software discovery model is found in the Configuration Management Database \(CMDB\), the normalization process compares the discovered software publisher, product, and version, and edition values against the Software Asset ManagementContent Library.

When the normalization process completes, matches are added to the corresponding normalized columns \(Publisher, Product, Version, and Edition\) of the Software Discovery Model \[cmdb\_sam\_sw\_discovery\_model\] table. The normalized ﬁelds are then used in various downstream processes and use-cases across Software Asset Management, such as reconciliation of entitlements purchase, calculation of license position and management of software llifecycle. For example, the discovered publisher Microsoft Corp could be normalized to Microsoft for the normalized Publisher column.

## Benefits of normalization

-   Normalization establishes a definitive inventory of all software discovered within your organization. Maintaining a comprehensive and accurate list of installed software is essential for both software audit readiness and effective IT operations. Without normalization, your organization encounters many different names for the same software publisher, which creates confusion and requires substantial effort to rationalize the data.
-   By implementing normalization, you streamline your software inventory, improve data consistency, and enhance the reliability of your reporting processes.
-   Normalization makes software reconciliation more accurate and efficient. It uses standard values to match software found with entitlements you own. This leads to more accurate reconciliation results. You can plan and complete software audits more easily because the counts are correct and match your records.
-   The normalization process enables standardizing installation data from multiple discovery tools.

## Scheduled jobs

To standardize software discovery models, they must be normalized. You can either manually update the records with normalization content or let the normalization capability within Software Asset Management Professional to compare and standardize your records against Software Asset Management Content Library.

The scheduled job **SAM - Normalize discovery models using content library rules** runs daily to normalize discovery models based on content rules and assign a normalization status to the discovery model record. For more information about the different normalization statuses, see [Normalization statuses](../reference/normalization-status.md).

**Note:** You can also opt in for Machine Learning normalization by activating the Software Asset Management – Machine Learning Normalization \(com.sn\_sam\_ml\_normalization\) plugin. For more information, see [Normalization of discovery models using machine learning](ml-learning-sam.md).

The scheduled job, **SAM - Discovery Model Normalization job** runs daily to update the normalization trend charts on the Normalization and content dashboard. For more information about normalization trend charts, see [Normalization and content dashboard](../reference/norm-content-dashboard-workspace.md).

## Manual normalization

Manual normalization is the process of updating a software discovery model when the platform hasn’t fully normalized it. You can manually normalize a software discovery model when its normalization status is **Partially Normalized**, **Publisher Normalized**, or **Match Not Found**. For more information about manually normalizing a software discovery model, see [Manually normalize a software model in the Software Asset Workspace](../task/manual-normalize-swmodel-workspace.md).

## Normalization suggestion

When a software discovery model is compared against the Software Asset Management plugin Content Library, normalization suggestions are generated for discovery models. These suggestions predict fields such as **Publisher**, **Product**, and **Version** based on the discovery source. You can accept or reject these suggestions. For more information about viewing normalization suggestions, see [View normalization suggestions in the Software Asset Workspace](../task/view-norm-sugg-workspace.md).

## Revert normalization

You can manually revert normalization, which removes all normalized values and sets the discovery model's status to **Match not found**. You can revert the normalization of discovery models with a status of **Normalized**, **Partially Normalized**, or **Publisher Normalized** to **Match Not Found**. For more information about reverting the software discovery model normalization, see [Revert normalization in the workspace](../task/revert-norm-workspace.md).

**Note:** Discovery models with a status of **Manually Normalized** and discovery models that have been normalized using pattern normalization rules can’t be reverted.

## Software model normalization rules

The Software Asset Management application uses the following normalization rules to normalize the software discovery models:

-   **Product Map and Package Map normalization**: The ServiceNow® Content Service creates rules for each distinct discovery model. Even if the difference is minor, a separate normalization rule is developed. For example, if there are 1,000 discovery models, then 1,000 Product Map normalization or Package Map normalization rules are created for normalizing the models.
-   **Pattern normalization**: Creates a single normalization rule that can address multiple discovery models with a specific data pattern. The rule looks for pattern matches between discovered fields and normalized values, and updates the normalized fields accordingly. For instance, to normalize software discovery model that contains Microsoft Office 2019, you can define a pattern normalization rule. Any discovery models starting with Microsoft Office 2019 is treated as equivalent and mapped to Microsoft Office.
-   **Enhanced pattern normalization**: Handles a wide range of complex scenarios encountered during software model discovery and product identification. This normalization rule addresses variations in product names, edition names, and version identifiers by using configured patterns to match and standardize different patterns. For example, if an edition is labeled as standard, STD, stand, or any other variant, a pattern rule can be established to treat such instances as equivalent and map them to the standard edition. The Software Asset Management application enables conditional mapping. The presence or absence of speciﬁc terms determines whether an item is included in or excluded from the enhanced pattern normalization rule coverage. This rule manages the different formats and scenarios encountered in discovery models, confirming consistency and accuracy in normalization.
-   **Wide-net normalization**: If certain software discovery models share similar discovered field values, the Software Asset Management application normalizes them using wide-net normalization principles, which reduces the need for the ServiceNow® Content Service to create separate normalization rules for each product.

    **Note:** Only certain software products are eligible for wide-net normalization. These software products are determined by the ServiceNow® Content Service.


**Parent Topic:**[Software discovery and normalization](c_SAMDiscovery.md)

**Related topics**  


[Manually normalize a software model in the Software Asset Workspace](../task/manual-normalize-swmodel-workspace.md)

[View normalization suggestions in the Software Asset Workspace](../task/view-norm-sugg-workspace.md)

[Revert normalization in the workspace](../task/revert-norm-workspace.md)

[Normalization statuses](../reference/normalization-status.md)

[Normalization of discovery models using machine learning](ml-learning-sam.md)

[Normalization and content dashboard](../reference/norm-content-dashboard-workspace.md)

