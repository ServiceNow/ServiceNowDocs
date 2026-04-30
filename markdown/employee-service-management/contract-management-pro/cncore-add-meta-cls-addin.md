---
title: Add metadata to a clause using add-in
description: As a contract configurator, add metadata to pre-fill information that will be placed in the contract document.
locale: en-US
release: zurich
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure dynamic clauses for contract templates, Configure contract templates, Configure, Contract Management Pro, Legal and Contract Operations, Employee Service Management]
---

# Add metadata to a clause using add-in

As a contract configurator, add metadata to pre-fill information that will be placed in the contract document.

## Before you begin

Ensure you have configured the Word add-in. For more information, see [Configure the Microsoft Word add-in for ServiceNow Contracts](../task/cncore-config-word-addin.md).

Role required: sn\_cm\_core.contract\_config and canvas\_user

## Procedure

1.  Open a document where you want to mark the content controls in Microsoft Word.

2.  From the Microsoft Word ribbon, select ServiceNow Contracts add-in.

    The add-in login screen is displayed.

3.  Enter the credentials of the ServiceNow instance from where you downloaded the manifest file.

    The add-in screen is displayed with Templates and Clauses tabs.

4.  In the Clauses tab, select a clause.

    The clause variation details are displayed.

5.  Select the clause variation for which you want to add metadata.

6.  In the Microsoft Word, place the cursor at the location where you want to add the metadata.

7.  Select **Create metadata mapping**.

    ![Create metadata for clause variation](../image/cmpro-waddin-cls-metadatanew.png "Create metadata for clause variation")

8.  In the **Field name** field, enter unique name for the metadata.

9.  Select **Create**.

    -   The metadata is added and displayed as a tile with field name as the title. ![Metadata added using Word Add-in](../image/ccore-metadata-tile.png)
    -   The metadata is synced to the ServiceNow instance. You can view the meta data by logging to the ServiceNow instance and navigating to the **Field mapping** related list of a clause variation.
10. Add the created metadata to other locations in the document by clicking on the tag.

11. Select **Complete mapping and upload**.

    The file will be uploaded. If the clause variation is mapped to multiple templates and the variation has metadata, the unmapped metadata is displayed and you must map them for each of the templates.


**Parent Topic:**[Configure dynamic clauses for contract templates](cncore-clause-and-cv.md)

