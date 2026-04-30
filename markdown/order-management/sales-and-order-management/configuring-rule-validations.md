---
title: Configuring matrix validation rules
description: As a product catalog admin or pricing admin, you can manage the system-defined matrix validation rules that automatically check the mandatory rule inputs or outputs in matrix decision tables. You can also define your own custom validations.
locale: en-US
release: xanadu
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring product pricing, Configuring Sales Customer Relationship Management applications, Sales Customer Relationship Management]
---

# Configuring matrix validation rules

As a product catalog admin or pricing admin, you can manage the system-defined matrix validation rules that automatically check the mandatory rule inputs or outputs in matrix decision tables. You can also define your own custom validations.

The product eligibility and pricing matrices included with the Product and Pricing Rules application have system-defined matrix validation rules, which are identified in the Details tab for each matrix. Each validation rule has a validation definition, which is a script that identifies the context variables to be validated in the matrix decision table and the corresponding error or warning messages to be displayed. The validations are run when you save your matrix decision row changes. The **Validation Status** field indicates whether the change is valid. If the change is not valid, error or warning messages are displayed in the **Validation Message** columns of the decision table.

Some system-defined validation rules are applicable to all decision tables, while others apply to only certain types of matrices:

-   DuplicateCondition: Checks for duplicate conditions in decision rules.
-   MissingMandatoryInputs: Checks for missing required inputs.
-   MissingMandatoryOutputs: Checks for missing required outputs.
-   EligibilityResultValidation: Checks the product eligibility results.
-   MandatoryCostBookForTypeExistingCostBook: Checks the cost book type.
-   MandatoryPriceListForTypeExistingPriceList: Checks the price list type.
-   ProductOfferCharsWithoutProdOffer: Checks for product offer characteristics without product offering.

![System-defined rule validations provided with the Product Catalog Eligibility Matrix](../image/matrix-rule-validation.png "Rule validations in Product Offering Category Eligibility Matrix") ![System-defined rule validations set for the matrix]( "Rule validations in Product Offering Category Eligibility Matrix")

From the Details tab for a matrix, you can also run rule validations for the entire matrix by selecting the **More actions** icon and selecting **Validate rule**.

