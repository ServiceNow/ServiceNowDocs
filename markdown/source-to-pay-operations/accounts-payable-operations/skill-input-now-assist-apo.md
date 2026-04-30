---
title: Skill inputs for Now Assist for Accounts Payable Operations \(APO\)
description: You can configure some of the inputs for a generative AI skill. Inputs permit you to determine how and when a skill is used.
locale: en-US
release: australia
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure Now Assist for Accounts Payable Operations \(APO\), Now Assist for APO, Accounts Payable Operations, Finance and Supply Chain]
---

# Skill inputs for Now Assist for Accounts Payable Operations \(APO\)

You can configure some of the inputs for a generative AI skill. Inputs permit you to determine how and when a skill is used.

## Overview of skills

Inputs identify the data that is used for a skill. Inputs include the table and fields that are used to generate a record summary.

You can modify the inputs, but you can't modify a skill's data source. The data source contains the tables and fields that the skill relies on.

## Skills for Now Assist for APO

The Now Assist for APO application includes the invoice case summarization skill.

## Invoice case summarization skill

The inputs for the invoice case summarization skill identify the table and fields that are used when the summary is generated for an invoice case.

The following table lists the inputs for the case summarization from the Choose input for procurement case page in the Now Assist Admin console.

<table id="table_qcd_hl2_pdc"><thead><tr><th>

Input

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Base input table

</td><td>

Invoice case \[sn\_ap\_cm\_ap\_case\] table

</td></tr><tr><td>

Base input fields

</td><td>

-   Description
-   Supplier
-   Invoice due date
-   Invoice supplier number
-   Invoice date
-   Short description
-   Requested by
-   Caller email
-   Sub category
-   State
-   Closed at
-   Closed by
-   Closure code
-   Closure details

</td></tr></tbody>
</table>