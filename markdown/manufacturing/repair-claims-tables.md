---
title: Repair claims tables
description: This section explains the repair claim tables in Manufacturing Commercial Operations.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Repair claims data model, Data model, Reference, Manufacturing Commercial Operations]
---

# Repair claims tables

This section explains the repair claim tables in Manufacturing Commercial Operations.

## Repair claim plugin

The repair claim feature adds or modifies the existing tables:

-   Expense Line \[fm\_expense\_line\]
-   Case \[sn\_customerservice\_case\]
-   Case Line \[sn\_case\_line\]

The repair claim plugin adds the following tables.

<table id="table_yn1_h1l_3fc"><thead><tr><th>

Label

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Repair Claim Case\[sn\_repair\_claim\_mgmt\_case\]

</td><td>

Stores the details of the repair claim request submitted for reimbursement.

</td></tr><tr><td>

Repair Claim Case Line\[sn\_repair\_claim\_mgmt\_case\_line\]

</td><td>

Stores the repair claim job level details of the customers.

</td></tr><tr><td>

Repair Case Line Charge\[sn\_repair\_claim\_mgmt\_case\_line\_charge\]

</td><td>

Stores the specific line item that holds the detailed expenses involved for the repair.

</td></tr><tr><td>

Expense Line\[fm\_expense\_line\]

</td><td>

Stores the expense information for the approved or partially approved claim jobs.

</td></tr><tr><td>

Claim Case\[sn\_claim\_cmn\_case\]

</td><td>

Stores the input provided by the dealer to the manufacturer when the claim request is raised. This information is retrieved from the Promotion input table.

</td></tr><tr><td>

Claim Case Line\[sn\_claim\_cmn\_case\_line\]

</td><td>

Stores the job level details for the claim

</td></tr><tr><td>

Case Line\[sn\_case\_line\]

</td><td>

Stores the case line item records that are created for parent cases.

</td></tr><tr><td>

Claim Case Line Charge\[sn\_claim\_cmn\_case\_line\_charge\]

</td><td>

Stores the charges incurred for each repair job.

</td></tr></tbody>
</table>To learn more about the Case and Case Line, see [Case Lines and Workflows](https://www.servicenow.com/docs/access?context=csm-case-mgmt-case-lines&version=australia&pubname=australia-customer-service-management&ft:locale=en-US).

**Parent Topic:**[Repair claims data model](repair-claims.md)

