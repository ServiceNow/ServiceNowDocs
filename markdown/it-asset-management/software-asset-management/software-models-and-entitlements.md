---
title: Software models and Software entitlements
description: A software model is a profile of the software that you've purchased, including information about the publisher, version, and discovery map. Software entitlements are used to relate the software model to the rights that you've purchased.
locale: en-US
release: xanadu
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Exploring Software Asset Management, Software Asset Management, IT Asset Management]
---

# Software models and Software entitlements

A software model is a profile of the software that you've purchased, including information about the publisher, version, and discovery map. Software entitlements are used to relate the software model to the rights that you've purchased.

## Software models

Software models are used to record publisher information and create a profile. You can link multiple entitlements to one software model.

If you delete a software model, all records related to the software model, in the Downgrade Rights \[samp\_sw\_downgrade\_model and samp\_downgrade\_model\] tables, are automatically deleted. For detailed information on downgrade rights, see [Downgrade Rights](downgrade-rights.md).

For details on manually creating software models, see [Create software models in workspace](../task/create-swmodels-workspace.md). For details on automatic creation of software models, see [Automatic creation of software models](duplicate-sw-models.md).

## Software Product Lifecycle report

You can also track a software lifecycle phase for use with the [Technology Portfolio Management](https://www.servicenow.com/docs/access?context=technology-portfolio-management&version=xanadu&pubname=xanadu-application-portfolio-management&ft:locale=en-US).

The Software Product Lifecycle \[sam\_sw\_product\_lifecycle\] table holds the information of the software product, its lifecycle type \(internal or external\), full version, lifecycle phases, start date of the phase, and the risk.

The Content active column in the Software Product lifecycle \[sam\_sw\_product\_lifecycle\] table is set to the value true by the Software Asset Management content service if the lifecycle records are valid. If you do not want a lifecycle phase to be rendered on the Technology Portfolio Management \(TPM\) timeline, then set the **Active** column to false. For example, you can have **General Availability**, **End of Extended Support**, and **End of Support** lifecycle phases as three records for Oracle DB Server software model in the Software Product Lifecycles list. However, if you do not want **General Availability** phase to be shown on the timeline, you can clear the **Active** check box in the Software Product Lifecycle form for that lifecycle phase record. As a result, the timeline starts with the **End of Support** phase. Although the lifecycle phase record exists for the software product lifecycle, the lifecycle data will not be rendered on the timeline. Because only active lifecycle records are considered and plotted in the TPM timeline.

View the Software Product Lifecycle report to be informed about the products nearing end-of-life, end-of-support, and end-of-extended support. View the report by navigating to **Reports** &gt; **View/Run**. The report is based on the scheduled job, **SAM - Generate Data For Software Lifecycle Report**.

## Software Lifecycle Report

The Software Lifecycle Report \[sam\_sw\_product\_lifecycle\_report\] table calculates the current and upcoming lifecycle phases from the lifecycle phases mentioned in the Software Product Lifecycle \[sam\_sw\_product\_lifecyle\] table.

For records with the same publisher, product, version, full version, and edition, there's a single record for different lifecycle phases. This helps in avoiding duplicate software installation count for each lifecycle phase. You can export lifecycles from the Software Installation \[cmdb-sam-sw-install\] table. The software installation records are linked to lifecycles via the **Installs associated to lifecycle** column in the Software Installation \[cmdb-sam-sw-install\] table.

Five new columns have been added to Software Lifecycle Report \[sam\_sw\_product\_lifecycle\_report\] table:

|New column label and name|Description|
|-------------------------|-----------|
|Current phase \[current\_lifecycle\_phase\]|The lifecycle phase that is currently underway.|
|Current lifecycle phase start date \[current\_lifecycle\_phase\_start\_date\]|The start date of the current lifecycle phase.|
|Upcoming lifecycle phase \[upcoming\_lifecycle\_phase\]|The lifecyle phase that is soon coming up.|
|Upcoming lifecycle phase start date \[upcoming\_lifecycle\_phase\_start\_date\]|The start date of the upcoming lifecycle phase.|
|Owners \[owners\]|The person responsible for the software model.|

**Note:** The lifecycle phase column is removed from the Software Lifecycle Report \[sam\_sw\_product\_lifecycle\_report\] table.

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

