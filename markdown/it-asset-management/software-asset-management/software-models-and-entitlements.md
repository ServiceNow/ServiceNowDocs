---
title: Software models and Software entitlements
description: A software model is a profile of the software that you've purchased, including information about the publisher, version, and discovery map. Software entitlements are used to relate the software model to the rights that you've purchased.
locale: en-US
release: zurich
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Explore, Software Asset Management, IT Asset Management]
---

# Software models and Software entitlements

A software model is a profile of the software that you've purchased, including information about the publisher, version, and discovery map. Software entitlements are used to relate the software model to the rights that you've purchased.

## Software models

Software models are used to record publisher information and create a profile. You can link multiple entitlements to one software model.

If you delete a software model, all records related to the software model, in the Downgrade Rights \[samp\_sw\_downgrade\_model and samp\_downgrade\_model\] tables, are automatically deleted. For detailed information on downgrade rights, see [Downgrade Rights](downgrade-rights.md).

For details on manually creating software models, see [Create a software model in the Software Asset Workspace](../task/create-swmodels-workspace.md). For details on automatic creation of software models, see [Automatic creation of software models](duplicate-sw-models.md).

## Software entitlements

To track the software rights for your software, create a software entitlement that can be linked back to the publisher information.

A software entitlement records the terms of your software license. By using software entitlements, you can:

-   Rapidly address if license allotment has been exceeded and return to compliant status by removing unauthorized software or ordering more licenses.
-   If the license allotment is not being used completely, lower the number of future licenses purchased.

For example, a company purchases a software entitlement for 100 rights. From the software entitlement, 100 employee or machine allocations are created that are rightfully assigned a license. If Discovery finds the software installed on 200 machines, the software asset manager must identify the employees or machines that have the software installed without a license, and remediate the situation.

For details on creating software entitlements, see [Create entitlements in workspace](../task/create-entitlements-workspace.md).

## Import software entitlements

You can import bulk software entitlements at one go.

If a Publisher Part Number \(PPN\) is specified for the entitlements that you import, the PPN is matched to PPN in the Content Service Library and the data is used to create a software model automatically.

**Note:** If a `Publisher Part Number not found` error occurs during import of the software entitlement \(product, publisher, version, edition, platform, and language\) but a discovery map is found, then a [custom publisher part number](../task/sam-add-custom-part-number.md) is automatically created. If a discovery map is not found, you can create a discovery map to be associated with the publisher part number.

If the import spreadsheet contains a conflicting \(or missing\) PPN, the PPN value is set to the value in the existing product definition, when available.

**Note:** If you import a batch of Microsoft entitlements and the **License Duration** field is set to **Contractual**, you must specify both a start and end date.

The step-up license type is only available if the publisher is Microsoft. If you try to specify another publisher, an error message is displayed.

-   **[Automatic creation of software models](duplicate-sw-models.md)**  
Software models are automatically created for software installations if one doesn't already exist.
-   **[Custom publisher part numbers \(PPN\)](customppn-swap.md)**  
Propagate changes to entitlements and software models by replacing your custom PPNs and custom discovery maps \(DMAPs\) with the Software Asset Management Content Service PPNs and DMAPs.

**Parent Topic:**[Exploring Software Asset Management](explore-sam-workspace.md)

