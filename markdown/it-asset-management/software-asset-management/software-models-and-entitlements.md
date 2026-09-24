---
title: Software models and software entitlements
description: A software model is a profile of the software that you have purchased, including information about the publisher, version, and discovery map. Software entitlements are used to relate the software model to the rights that you have purchased.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/software-asset-management/software-models-and-entitlements.html
release: brazil
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 5
breadcrumb: [Exploring Software Asset Management, Software Asset Management, IT Asset Management, Asset Management]
---

# Software models and software entitlements

A software model is a profile of the software that you have purchased, including information about the publisher, version, and discovery map. Software entitlements are used to relate the software model to the rights that you have purchased.

## Software models

Software models are used to record publisher information and create a profile. You can link multiple entitlements to one software model.

If you delete a software model, all records related to the software model, in the Downgrade Rights \[samp\_sw\_downgrade\_model and samp\_downgrade\_model\] tables, are automatically deleted. For detailed information on downgrade rights, see [Downgrade Rights](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-asset-management/downgrade-rights.md).

For details on manually creating software models, see [Create a software model in the Software Asset Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-asset-management/create-swmodels-workspace.md). For details on automatic creation of software models, see [Automatic creation of software models](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-asset-management/duplicate-sw-models.md).

## Software entitlements

To track the software rights for your software, create a software entitlement that can be linked back to the publisher information.

A software entitlement records the terms of your software license. By using software entitlements, you can:

-   Rapidly address if license allotment has been exceeded and return to compliant status by removing unauthorized software or ordering more licenses.
-   If the license allotment is not being used completely, lower the number of future licenses purchased.

For example, a company purchases a software entitlement for 100 rights. From the software entitlement, 100 employee or machine allocations are created that are rightfully assigned a license. If Discovery finds the software installed on 200 machines, the software asset manager must identify the employees or machines that have the software installed without a license, and remediate the situation.

For details on creating software entitlements, see [Create entitlements in workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-asset-management/create-entitlements-workspace.md).

## Import software entitlements

Import bulk software entitlements at one go.

If a Publisher Part Number \(PPN\) is specified for the entitlements that you import, the PPN is matched to PPN in the Content Service Library and the data is used to create a software model automatically.

**Note:** If a `Publisher Part Number not found` error occurs during import of the software entitlement \(product, publisher, version, edition, platform, and language\), open the record and correct the error. To generate a custom part number, select **Create PPN**. If a discovery map is not found, you can create a discovery map to be associated with the publisher part number.

If the import spreadsheet contains a conflicting \(or missing\) PPN, the PPN value is set to the value in the existing product definition, when available.

**Note:** If you import a batch of Microsoft entitlements and the **License Duration** field is set to **Contractual**, you must specify the start and end date.

The step-up license type is only available if the publisher is Microsoft. If you try to specify another publisher, an error message is displayed.

## PPN and software model resolution in entitlement imports

The system uses different resolution strategies depending on:

-   Whether a PPN is provided in the import row.
-   Whether the import is standard \(custom\) or MLS \(Multi-License Service\).
-   Whether the automatic software model creation property is enabled.

## Scenario 1: PPN field is blank

For standard \(custom\) imports, the system attempts to identify a software model through a matching process:

1.  The system tries to identify a software model using the **Publisher**, **Product**, **Version**, **Edition**, **Platform**, and **Language** fields provided in the import row.
2.  If an exact match is found, the software model is assigned, and the import proceeds normally.
3.  If no exact match is found, the system tries a relaxed search, allowing any platform or any language, to find the closest match.
4.  If a match is found through the relaxed search, the software model is assigned and there is no error.
5.  If no match is found:
    -   If the automatic software model creation property is enabled \(the default\), and both publisher and product are identified, the system automatically creates a new software model and the import proceeds.
    -   If the automatic software model creation property is disabled, or publisher or product can't be identified, an error record is created: `PPN and SM not found`.

For MLS imports, the system doesn't attempt to find a software model from other fields when the PPN is blank. The import row continues to other validation checks but will likely fail at downstream validations \(such as license metric resolution\) that depend on PPN or software model.

## Scenario 2: PPN is provided

PPN exists in the Content Library:

1.  The system looks up the associated software model.
2.  If exactly one software model is found, it is assigned and there is no error.
3.  If multiple software models are found, an error record is created: `Multiple software models found for the Publisher Part Number. Please choose a software mode`l.

PPN doesn't exist in the Content Library or is marked Inactive:

1.  The system searches for a software model using **Publisher**, **Product**,**Version**, **Edition**, **Platform**, and **Language** \(exact match only; no relaxed search in this scenario\).
2.  If software model is found:
    -   The PPN not found issue is noted internally.
    -   If no other validation errors exist on the row, the entitlement is created without a PPN reference.
    -   If other validation errors exist, such as invalid license type, missing purchased rights, an error record is created including `Publisher Part Number not found` alongside other errors.
3.  If software model isn't found:
    -   If automatic software model creation is enabled, the import is standard \(custom\), and both publisher and product can be identified, the system automatically creates a software model.
    -   Else, an error record is created: `PPN and SM not found`.

-   **[Automatic creation of software models](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-asset-management/duplicate-sw-models.md)**  
Software models are automatically created for software installations if one doesn't already exist.
-   **[Custom publisher part numbers \(PPN\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-asset-management/customppn-swap.md)**  
Propagate changes to entitlements and software models by replacing your custom PPNs and custom discovery maps \(DMAPs\) with the Software Asset Management Content Service PPNs and DMAPs.

**Parent Topic:**[Exploring Software Asset Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-asset-management/explore-sam-workspace.md)

