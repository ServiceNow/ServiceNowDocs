---
title: Create a remediation action
description: Create a remediation action in Cloud Configuration Governance for the remediations that doesn’t require any additional input parameters.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Remediation, Using Cloud Configuration Governance, Cloud Configuration Governance, ITOM Cloud Accelerate, IT Operations Management]
---

# Create a remediation action

Create a remediation action in Cloud Configuration Governance for the remediations that doesn’t require any additional input parameters.

## Before you begin

Role required: sn\_itom\_ccg.ccg\_governer

## About this task

Cloud Configuration Governance uses Integration Hub subflows to perform the remediations.

## Procedure

1.  Navigate to **Cloud Configuration Governance** &gt; **Remediations**.

2.  Select **New**.

3.  On the form, fill in the fields.

<table id="table_mtb_s5f_hsb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Minimum permission required

</td><td>

Minimum cloud permissions required to execute the remediation.Cloud Configuration Governance doesn’t read the permissions information from this field. Use this field to store the permissions information for future reference.

</td></tr><tr><td>

Action

</td><td>

Remediation flow that can fix the selected violation.

</td></tr><tr><td>

Violation

</td><td>

Violation that you want to remediate.

</td></tr><tr><td>

Requires approval

</td><td>

Option to enforce approval for the remediation action. For more information on approvals, see [Approvals](https://www.servicenow.com/docs/access?context=r_Approvals&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US).

</td></tr><tr><td>

Description

</td><td>

Brief description of the remediation action.

</td></tr><tr><td>

Remediation Catalog Item

</td><td>

Name of the remediation catalog item that can be used to raise a remediation request.Select the CCG Remediation Default Catalog.

</td></tr></tbody>
</table>4.  Select **Submit**.


## What to do next

Run the remediation action to fix the identified violation. For more information, see [Run remediation](ccg-run-remediation.md).

