---
title: Skill inputs for Now Assist for Accounts Payable Operations \(APO\)
description: You can configure some of the inputs for a generative AI skill. Inputs permit you to determine how and when a skill is used.
locale: en-US
release: yokohama
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configure Now Assist for Accounts Payable Operations \(APO\), Now Assist for Accounts Payable Operations \(APO\), Accounts Payable Operations, Finance and Supply Chain]
---

# Skill inputs for Now Assist for Accounts Payable Operations \(APO\)

You can configure some of the inputs for a generative AI skill. Inputs permit you to determine how and when a skill is used.

## Overview of skills

Inputs identify the data that is used for a skill. Inputs include the table and fields that are used to generate a record summary.

You can modify the inputs, but you can't modify a skill's data source. The data source contains the tables and fields that the skill relies on.

## Skills for Now Assist for APO

The Now Assist for APO application includes the invoice case summarization skill.

**Important:** These Now Assist skills are now turned on by default. The skills will be automatically available to appropriate role users for the application. This change simply activates the skills and does not touch the roles that are needed to use them. The new default behavior works as follows:

-   **New customers**

    When you install a Now Assist product , designated skills are turned on automatically.

-   **Existing customers who are upgrading \(starting with Zurich Patch 4\)**

    Any previously unconfigured skill is turned on automatically \(the skill was never turned on, then off again\).

    There is no change to Now Assist skills that are currently enabled and customized.

    Previously configured skills that were turned on, then off, remain inactive.


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
</table>**Related topics**  


[Using Invoice Case Management](../concept/use-invoice-case-mgmt.md)

