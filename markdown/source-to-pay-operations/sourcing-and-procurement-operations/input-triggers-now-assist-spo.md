---
title: Skill inputs for Now Assist for Sourcing and Procurement Operations \(SPO\)
description: You can configure some of the inputs for a generative AI skill. Inputs permit you to determine how and when a skill is used.
locale: en-US
release: xanadu
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
keywords: [Now Assist Security Operations]
breadcrumb: [Configuring Now Assist for Sourcing and Procurement Operations \(SPO\), Now Assist for Sourcing and Procurement Operations \(SPO\), Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Skill inputs for Now Assist for Sourcing and Procurement Operations \(SPO\)

You can configure some of the inputs for a generative AI skill. Inputs permit you to determine how and when a skill is used.

## Overview of skills

Inputs identify the data used for a skill. Inputs include the table and fields used to generate a record summary.

You can modify inputs, but you can't modify a skill's data source. The data source contains the tables and fields that the skill relies on.

## Now Assist skills for Now Assist for SPO

The Now Assist for SPO includes the following skills

-   Sourcing request summarization
-   Purchase requisition summarization
-   Procurement case summarization

## Sourcing request summarization skill

Inputs for the Sourcing request summarization skill identify the table and fields used when the summary is generated for a sourcing request.

The following table lists the inputs for the Sourcing request summarization skill from the Choose input for sourcing request page in the Now Assist Admin console.

<table id="table_arz_fk3_1cc"><thead><tr><th>

Input

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Base input table

</td><td>

Sourcing Request \[sn\_shop\_sourcing\_activity\] table.

</td></tr><tr><td>

Base input fields

</td><td>

-   Business owner
-   Short description
-   Request type
-   Product category
-   Product name
-   Max budget
-   Purchased quantity
-   Supplier responses close
-   Sourcing request details
-   Product type
-   Status

</td></tr></tbody>
</table>## Purchase requisition summarization skill

Inputs for the Purchase requisition summarization skill identify the table and fields that are used when the summary is generated for a purchase requisition.

The following table lists the inputs for the Purchase requisition summarization from the Choose input for purchase requisition page in the Now Assist Admin console.

<table id="table_mc2_fqw_tcc"><thead><tr><th>

Input

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Base input table

</td><td>

Purchase Requisition \[sn\_shop\_purchase\_requisition\] table.

</td></tr><tr><td>

Base input fields

</td><td>

-   Number
-   Short description
-   Description
-   State
-   Business owner
-   Order type
-   Requisition type
-   Supplier
-   Total amount
-   Work notes
-   Additional comments

</td></tr></tbody>
</table>## Procurement case summarization skill

Inputs for the Procurement case summarization skill identify the table and fields that are used when the summary is generated for a procurement case.

The following table lists the inputs for the Procurement case summarization from the Choose input for procurement case page in the Now Assist Admin console.

<table id="table_il3_sfj_1cc"><thead><tr><th>

Input

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Base input table

</td><td>

Procurement Case \[sn\_spend\_psd\_procurement\_request\] table.

</td></tr><tr><td>

Base input fields

</td><td>

-   State
-   Short description
-   Description
-   Due date
-   Case type
-   Related case
-   Requested by
-   Supplier
-   Assigned to
-   Work notes
-   Additional comments

</td></tr></tbody>
</table>