---
title: Manage software models using the legacy Software Asset Management plugin
description: The legacy Software Asset Management \(com.snc.software\_asset\_management\) plugin uses software models to manage licenses, specifically in software counters and license restrictions, and to track upgrade and downgrade licenses.
locale: en-US
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Legacy Software Asset Management plugin, ITSM Software Asset Management, Asset Management, IT Service Management]
---

# Manage software models using the legacy Software Asset Management plugin

The legacy Software Asset Management \(com.snc.software\_asset\_management\) plugin uses software models to manage licenses, specifically in software counters and license restrictions, and to track upgrade and downgrade licenses.

## Before you begin

Role required: sam or model\_manager

## About this task

Create software models for all of the software your organization wants to monitor. Software models can also be imported from another source such as the Discovery application.

**Note:** Software does not create configuration items. If the discovery tool you use supports and finds ISO information, details such as ISO ID and ISO serial number are added to the Software Model form for compliance purposes.

## Procedure

1.  Navigate to **All** &gt; **Software Asset** &gt; **Software Models**.

    Users with the model\_manager role can navigate to **Product Catalog** &gt; **Product Model** &gt; **Software Models**, but cannot administer all aspects of software models.

2.  Click **New**.

3.  Complete the form.

<table id="table_nr2_nd1_y4"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Display name

</td><td>

\[Read-only\] Name of the model. A system property called **glide.cmdb\_model.display\_name.shorten** controls how software model display names are generated. Administrators can configure the property.

</td></tr><tr><td>

Manufacturer

</td><td>

The company that built the model.

</td></tr><tr><td>

Name

</td><td>

The manufacturer-assigned name of the model or an abstract name specified by the model manager, such as Field Agent Laptop.

</td></tr><tr><td>

Edition

</td><td>

The edition of the software model, such as Professional.

</td></tr><tr><td colspan="2">

General

</td></tr><tr><td>

Short description

</td><td>

A brief description of the model.

</td></tr><tr><td>

Model categories

</td><td>

\[Read-only\] The category the model is assigned to. The system automatically sets the value to **Software License**. This field is a glide list.

</td></tr><tr><td>

Asset tracking strategy

</td><td>

The process the model should be tracked by. Choose from the following:-   **Leave to Category**: model is transparent and the asset class is defined solely by the category.
-   **Create Consumable Asset**: model forces the asset class to be consumable, regardless of what the category defines as the asset class.
-   **Don't create assets**: model blocks asset instantiation, regardless of what the category defines as the asset class.


</td></tr><tr><td>

Acquisition method

</td><td>

The method for purchasing the model. Options are **Both**, **Buy**, and **Lease**.

</td></tr><tr><td>

Cost

</td><td>

The cost a single unit of the model.

</td></tr><tr><td>

Depreciation

</td><td>

The depreciation scheme for the model.

</td></tr><tr><td>

Model number

</td><td>

The specific model number assigned to the item by the manufacturer.

</td></tr><tr><td>

Barcode

</td><td>

The barcode number assigned to the model. Barcodes are usually assigned by the manufacturer.

</td></tr><tr><td>

Owner

</td><td>

The person responsible for the model.

</td></tr><tr><td>

Status

</td><td>

The current status of the model. Options are **In Production**, **Retired**, and **Sold**.

</td></tr><tr><td>

Certified

</td><td>

The option that determines whether the model is approved for use.

</td></tr><tr><td>

Comments

</td><td>

Information about the model that would be helpful for others to know.

</td></tr><tr><td colspan="2">

License

</td></tr><tr><td>

Version

</td><td>

The exact version of the software. For example, Version 2.

</td></tr><tr><td>

Major

</td><td>

The ISO major version number of the software.

</td></tr><tr><td>

Minor

</td><td>

The ISO minor version number of the software.

</td></tr><tr><td>

Build

</td><td>

The build number of the software.

</td></tr><tr><td>

Software category

</td><td>

A category name for grouping software with similar characteristics.

</td></tr><tr><td>

Single or multi license

</td><td>

Defines whether this model uses a single license or multiple licenses.

</td></tr><tr><td>

Maximum socket count

</td><td>

Maximum number of CPU sockets that a computer must have for the software to be installed.

</td></tr><tr><td>

License type

</td><td>

The tracking type for the license. For example, by number of users, per workstation, per installation with IBM PVU or per Oracle processors. If you select the **By number of users** option, you can create a software counter and specify the number of installations per license.

</td></tr><tr><td>

Activation status

</td><td>

The activation state of the software model. Options are **None** and **Activated**.

</td></tr><tr><td>

ISO id

</td><td>

The unique ISO identification number of the software product.

</td></tr><tr><td>

ISO serial number

</td><td>

The serial number issued by ISO for the software.

</td></tr><tr><td>

Application model

</td><td>

Application associated with this software.

</td></tr><tr><td>

Rights

</td><td>

Number of licenses granted to this software.

</td></tr><tr><td>

Minimum users

</td><td>

Minimum number of user licenses required for this software.

</td></tr><tr><td>

Maximum users

</td><td>

Maximum number of user licenses required for this software.

</td></tr><tr><td colspan="2">

Suite Components

</td></tr><tr><td>

Inference percent

</td><td>

The percentage of suite components that need to be present on a system to count as a suite. Used for suite management. For example, Suite A consists of 5 products. If the inference percent is set to 60% and a discovery tool finds three of the products on the system, the software is flagged for possible purchase as a suite.

</td></tr><tr><td>

Components

</td><td>

The child product or products of the suite. For example, Microsoft Word and Microsoft Excel are child products of Microsoft Office.

</td></tr><tr><td colspan="2">

Suite Parents

</td></tr><tr><td>

Parents

</td><td>

The parent suites to which the software is assigned. For example, the parent suite for several common Microsoft products is a version of Microsoft Office.

</td></tr><tr><td colspan="2">

Upgrade

</td></tr><tr><td>

Upgrades

</td><td>

An alternative version license to which you have rights. For example, if you purchase version 4 of a software product shortly before version 5 is released, your version 4 license may include a free upgrade to version 5 when it is released.

</td></tr><tr><td colspan="2">

Downgrade

</td></tr><tr><td>

Downgrades

</td><td>

An alternative version license to which you have rights. For example, if you purchase version 4 of a software product, your version 4 license may include downgrade rights to version 3.

</td></tr><tr><td colspan="2">

Licenses

</td></tr><tr><td>

Software Licenses

</td><td>

The software licenses that should be created automatically from this model. **Note:** This embedded list shows all assets created from this model, whether or not they are software licenses, in versions prior to this release.

</td></tr><tr><td colspan="2">

Catalog Item

</td></tr><tr><td>

Product Catalog

</td><td>

The information about the model as it appears in the product catalog and service catalog. Information only appears if the model has been published to the product catalog.

</td></tr><tr><td>

Description

</td><td>

Description of the software model as it appears in the product catalog.

</td></tr><tr><td>

Picture

</td><td>

An image of the software logo.

</td></tr></tbody>
</table>    Any software licenses you create and assign to the new model are displayed in the **Licenses** embedded list on the Software Model form.


-   **[Create and manage software suites using the legacy Software Asset Management plugin](../concept/c_CreateAndManageSWSuite.md)**  
Software uses the concept of suites instead of bundles.

**Parent Topic:**[Legacy Software Asset Management plugin](../concept/c_SoftwareAssetManagement.md)

**Related topics**  


[Legacy Software Asset Management plugin Overview module](../concept/c_SWAssetMgmtOverviewMod.md)

[Legacy Software Asset Management plugin setup process](../concept/c_SetupProcess.md)

[Determine where software is installed using the legacy Software Asset Management plugin](../concept/c_DeterminWhereSWInstalled.md)

[Software licenses in the legacy Software Asset Management plugin](../concept/c_SoftwareLicenses.md)

[License calculations with the legacy Software Asset Management plugin](../concept/c_UseLicenseCalculations.md)

[Software discovery models in the legacy Software Asset Management plugin](../concept/c_UsingSoftwareDiscoveryModels.md)

[Legacy Software License Compliance Checker](../concept/c_SoftwareLicenseComplianceChecker.md)

[Software license reconciliation counters for the legacy Software Asset Management plugin](../concept/c_UseCountersSWLicenseReconcil.md)

[Legacy IBM PVU Process Pack](../concept/c_IBMPVUProcessPack.md)

[Software contracts for the legacy Software Asset Management plugin](../concept/c_SoftwareContracts.md)

[Legacy Oracle process pack](../concept/c_OracleProcessPack.md)

