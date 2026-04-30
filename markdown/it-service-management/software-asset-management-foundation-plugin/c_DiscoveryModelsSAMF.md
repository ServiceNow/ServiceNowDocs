---
title: Software Asset Management Foundation plugin discovery models and software installations
description: Software discovery models are automatically created during discovery so you can manually normalize the software installed in your environment.
locale: en-US
release: yokohama
product: Software Asset Management Foundation plugin
classification: software-asset-management-foundation-plugin
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Exploring Software Asset Management Foundation plugin, Software Asset Management Foundation plugin, ITSM Software Asset Management, Asset Management, IT Service Management]
---

# Software Asset Management Foundation plugin discovery models and software installations

Software discovery models are automatically created during discovery so you can manually normalize the software installed in your environment.

Software discovery models are stored in the Software Discovery Model \[cmdb\_sam\_sw\_discovery\_model\] table.

There is a difference between [software models](../task/t_AddASoftwareModelSAMF.md) and software discovery models.

-   A software model is a specific version or configuration of software that is purchased and/or available to users.
-   A software discovery model is a model created when a version of software is discovered in a network environment.

Multiple software discovery models can be associated to one software model. For example, a software model can be defined as follows:

-   Publisher = X
-   Product = Y
-   Version = Starts with 10

If there are two separate installs of this product \(version 10.1 and version 10.2\), two discovery models are created. One of the discovery models has the discovered version set to 10.1, and the other discovery model has the discovered version set to 10.2. The reconciliation process associates both of these discovery models to the same software model since they both meet the version criterion of `Starts with 10`.

## Discovery Models

Software discovery models cannot be created manually. The following field combination, called the primary key, is used to match new software installations to a new or existing software discovery model.

Primary key: **Publisher**, **Display Name**, and **Version**

**Note:** When analyzing version numbers, an exact match is always searched for first, but rounds down to a major version number when an exact match is not found.

For example, if no match is found for version number 8.0.4, but version 8.0 is found, then version 8.0 is used in the **Software model** field.

<table id="table_cql_sx5_hp"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Display name

</td><td>

Name of the discovery model as it appears in record lists. This value is generated automatically using the discovered publisher, discovered product, and discovered version.

</td></tr><tr><td>

Normalization status

</td><td>

[Status](c_SAMDiscoverySAMF.md) of the normalization process:-   Manually Normalized
-   New

</td></tr><tr><td>

Publisher

</td><td>

Publisher of the software.

</td></tr><tr><td>

Product

</td><td>

Product name of the software.

</td></tr><tr><td>

Version

</td><td>

Version of the software product.

</td></tr><tr><td>

Discovered publisher

</td><td>

Discovered publisher of the software.

</td></tr><tr><td>

Discovered product

</td><td>

Discovered name of the software.

</td></tr><tr><td>

Discovered version

</td><td>

Discovered version of the software.

</td></tr><tr><td class="sub-head" colspan="2">

Additional Information

</td></tr><tr><td>

Product type

</td><td>

-   Child: A subcomponent of main software \(not licensable\).
-   Driver: A software product that controls a device.
-   Licensable: A software product that is licensable.
-   Not Licensable: A software product that is not licensable.
-   Patch: A software product designed to update, fix, or improve an existing computer program.
-   Unknown: Not discovered.

For unknown product types, the product type can be changed to another value.

When the product type is changed, the normalization status of the discovery model is updated to Manually Normalized.


 The reconciliation process only considers software discovery models that are licensable.

</td></tr><tr><td>

Platform

</td><td>

Platforms include:-   Windows
-   Mac
-   Unix

</td></tr><tr><td>

Language

</td><td>

-   Dutch
-   English
-   French
-   German
-   Italian
-   Spanish

 Additional languages are generated if discovered.

</td></tr><tr><td>

Edition

</td><td>

Edition of the software.

</td></tr><tr><td>

Full version

</td><td>

Full version of the software.

</td></tr></tbody>
</table>**Note:** If a normalized discovery model has a missing version, edition, language, or platform value, those field values can be set by the user. Once a new value is set, the normalization status changes form New to Manually Normalized.

## Software Installations

The Software Installations list contains the software installed in your organization and is automatically populated by discovery.

Installed software is placed in the Software Installation \[cmdb\_sam\_sw\_install\] table by Discovery, and a primary key is built \(using **Publisher**, **Display Name**, and **Version** fields\).

Discovery automatically matches the discovered software installation with a new or existing software discovery model using the primary key.

<table id="table_rgq_jnk_fbb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Display name.

</td><td>

Name of the software installation as it appears in the record lists. Can be a combination of the discovered product name and edition.

</td></tr><tr><td>

Discovery model

</td><td>

Software discovery model that represents the installed software.

</td></tr><tr><td>

Publisher

</td><td>

Publisher of the software.

</td></tr><tr><td>

Version

</td><td>

Version of the software.

</td></tr><tr><td>

Edition Override

</td><td>

Override of the software edition setting.If the edition for the software was not discovered, you can edit this field to set the edition, if known, so reconciliation can be performed successfully.

 For more information, see [Manually override SAM Foundation edition value in classic](../task/t_ManOverrideEditionSAMF.md).

</td></tr><tr><td class="sub-head" colspan="2">

Installation

</td></tr><tr><td>

Prod id

</td><td>

Unique ID for the product assigned by the manufacturer. Found through discovery.

</td></tr><tr><td>

Install location

</td><td>

Path under which the software is installed.

</td></tr><tr><td>

Install date

</td><td>

Date that the software was installed.

</td></tr><tr><td>

Revision

</td><td>

Revision of the software.

</td></tr><tr><td>

Instance key

</td><td>

Unique ID for the instantiation of the software. Automatically generated when the software is installed.

</td></tr><tr><td>

Installed on

</td><td>

Hardware on which the software is installed.

</td></tr><tr><td>

Uninstall string

</td><td>

Identifier used to uninstall the software.

</td></tr><tr><td>

ISO serial number

</td><td>

ISO number of the software.

</td></tr><tr><td class="sub-head" colspan="2">

Reconciliation

</td></tr><tr><td>

Entitlement

</td><td>

The entitlement found to use with this installation.

</td></tr><tr><td>

Inferred suite

</td><td>

The inferred suite model this installation belongs to.

</td></tr><tr><td>

Omit from suites

</td><td>

Check box for not counting the software install as a component of a suite during reconciliation.

</td></tr></tbody>
</table>**Parent Topic:**[Exploring Software Asset Management Foundation plugin](exploring-sam-foundation.md)

