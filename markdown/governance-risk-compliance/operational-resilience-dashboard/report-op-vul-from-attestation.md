---
title: Report an operational vulnerability from the Self-attestation module
description: Report an Operational vulnerability from the Self-attestation module in the Operational Resilience Workspace.
locale: en-US
release: xanadu
product: Operational Resilience Dashboard
classification: operational-resilience-dashboard
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Reporting Operational vulnerability, Managing Operational vulnerability, Manage, Operational Resilience, Governance, Risk, and Compliance]
---

# Report an operational vulnerability from the Self-attestation module

Report an Operational vulnerability from the Self-attestation module in the Operational Resilience Workspace.

## Before you begin

Role required: sn\_oper\_res.manager

## Procedure

1.  Navigate to **Workspaces** &gt; **Operational Resilience Workspace** &gt; **Self-attestations**.

    A list of the available Self-attestations is displayed.

2.  Select a Self-attestation record from the list.

    If you create a Self-attestation record and save it, the Operational vulnerabilities related list is displayed.

    The Self-attestation record with the Operational vulnerabilities related list is displayed.

3.  Check the state of the Self-attestation record.

    If the self-attestation is in the **Attestation received** state, you cannot add or remove a vulnerability at this stage.

4.  Add a service to the self-attestation record.

5.  Open the Service record, select **More** and add the **Operational vulnerabilities** related list.

6.  Select **New** in the Operational vulnerabilities related list and add an operational vulnerability.

7.  On the Vulnerability New record form, fill in the fields.

    The source of the vulnerability is the Self-attestation. Therefore, the **Source** field on the form shows the source as Self attestation and the **Source table** field on the form shows the table as Self attestation. The **Source table** field is auto-filled.

    To view more information on the fields, see the [Create New Operational vulnerability form](../reference/create-new-op-vul-form.md).

8.  Select **Save**.

    The following example shows how the Self-attestation record is displayed in the Operational vulnerabilities related list and the Operational vulnerability is associated with the Self-attestation for critical services.

    ![Attestation record.](../image/op-vul-added-for-service-attest-record.png)

9.  Select **Save**.

    The Self-attestation record is saved.


