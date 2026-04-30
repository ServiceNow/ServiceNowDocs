---
title: Create a contract template from an existing template
description: Create a new contract template from an existing template if you need only a small variation in the content of an existing template.
locale: en-US
release: yokohama
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Manage clauses, tables, and contract templates, Managing Contract Management Pro, Contract Management Pro, Employee Service Management]
---

# Create a contract template from an existing template

Create a new contract template from an existing template if you need only a small variation in the content of an existing template.

## Before you begin

Role required: sn\_cm\_core.contract\_config

## Procedure

1.  Navigate to **All** &gt; **Contracts Core** &gt; **Contract Administration** &gt; **Contract Templates**.

2.  Open the contract template from the list.

3.  Select **Create Revision**.

    Select the option **Copy** when you are creating template in Default View.

    A template revision is created with the data related to participants, imported clauses, and template mappings.

4.  Import clauses and template field mappings from a Microsoft Word document with content controls.

    For more information, see [Add content controls in a Microsoft Word document](cncore-word-doc-tmplt-contls.md).

    1.  In the **Document** field, select **Update**.

    2.  Select **Choose file**.

    3.  Choose a file and select **Ok**.

    4.  Select **Parse document**

        -   The document is parsed.
        -   The metadata that was already present is retained.
        -   The metadata that was present earlier but not found in the recent parsing is deleted.
        -   The metadata that is new is added.
        -   The clause tags that were already present are retained.
        -   The clauses that were present earlier but not found in the recent parsing are deleted.
        -   The clause tags that are new are added.
    A new file is uploaded to the contract template.


## What to do next

-   Map any new meta data found during parsing. For more information, see [Update contract template mappings](cncore-template-mapping.md).
-   Classify new clauses found during parsing. For more information, see [Classify and map imported clauses](cncore-import-clauses.md)

**Parent Topic:**[Manage clauses, tables, and contract templates](../concept/cncore-manage-clauses-ctemplates.md)

**Related topics**  


[Edit a contract clause variation](cncore-edit-cv.md)

[Edit a contract template by manually adding content controls](cncore-edit-ct.md)

[Edit a contract template using Microsoft Word add-in for ServiceNow Contracts](cncore-edit-ct-addin.md)

[Generate and preview a contract document from a template](cncore-preview-template.md)

[Delete a contract template](cncore-delete-template.md)

