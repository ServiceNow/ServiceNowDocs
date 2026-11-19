---
title: Skill inputs for ServiceNow Otto for Accounts Payable Operations \(APO\)
description: Skill inputs for the invoice case summarization skill, including the base input table and fields used to generate invoice case summaries.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/source-to-pay-operations/accounts-payable-operations/skill-input-now-assist-apo.html
release: zurich
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [APO, Accounts Payable Operations, ServciceNow Otto, Invoice case, Supplier, invoice case summarization skill]
breadcrumb: [Configure ServiceNow Otto for Accounts Payable Operations \(APO\), ServiceNow Otto for APO, Accounts Payable Operations, Finance and Supply Chain]
---

# Skill inputs for ServiceNow Otto for Accounts Payable Operations \(APO\)

Skill inputs for the invoice case summarization skill, including the base input table and fields used to generate invoice case summaries.

## Overview of skills

Inputs identify the data that is used for a skill. Inputs include the table and fields that are used to generate a record summary.

You can modify the inputs, but you can't modify a skill's data source. The data source contains the tables and fields that the skill relies on.

## Skills for ServiceNow Otto for Accounts Payable Operations \(APO\)

The ServiceNow Otto for APO application includes the invoice case summarization skill.

## Invoice case summarization skill

The inputs for the invoice case summarization skill identify the table and fields that are used when the summary is generated for an invoice case.

The following table lists the inputs for the case summarization from the Choose input for procurement case page in the AI Admin Hub console.

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