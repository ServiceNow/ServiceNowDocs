---
title: Tax integration in playbook
description: The Accounts Payable Operations playbook enables AP specialists and tax specialists to perform invoice tax validation using tax engine integration. Use the playbook for implementing and viewing the different stages of tax validation using the tax engine integration.
locale: en-US
release: yokohama
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: task
last_updated: "2026-02-23"
reading_time_minutes: 4
breadcrumb: [Tax Engine Integration, Integrating APO with other applications, Accounts Payable Operations, Finance and Supply Chain]
---

# Tax integration in playbook

The Accounts Payable Operations playbook enables AP specialists and tax specialists to perform invoice tax validation using tax engine integration. Use the playbook for implementing and viewing the different stages of tax validation using the tax engine integration.

## Before you begin

Role required: AP specialist, tax specialist

## Procedure

1.  Navigate to **Workspaces** &gt; **Source-to-Pay Workspace**.

2.  Select the list icon \(![List icon](../../supplier-lifecycle-operations/image/cases-list-icon.png)\).

    A list of options within the workspace is displayed.

3.  Select **Invoices &gt;****All invoices.**

    You can create an invoice manually. For more information on invoices, see [Work with invoices](../concept/work-with-invoices.md). Invoices can be entered manually or extracted using DocIntel. For more information on invoice extraction, see [Configure data extraction modes](set-up-extraction-modes-di.md).

4.  Select **View Invoice processing case**.

5.  Select **Validate invoice**.

    1.  Select the **Review header** details.

        Review the invoice header details and make any required changes. Tax mentioned in the invoice copy is entered or extracted as supplier tax \(editable\) at header level and the system tax is the sum total of system tax \(read only, derived from external tax engine\) for all the tax lines.

    2.  Select **Save**.

    3.  Select **Continue** to move to the next activity in the playbook.

    4.  Select the **Review invoice lines** activity and manually review the invoice lines associated with the invoice.

        **Note:** When tax integration is disabled, you can create tax lines from related list of invoice lines or invoice case. For more information on tax lines in related list see [Using Playbook in Accounts Payable Operations](how-to-use-playbook.md). If tax integration is enabled, you can add tax lines using the related list but the tax lines are deleted and new tax lines are added as a response from external tax engine. Tax mentioned for each invoice line in the invoice copy is entered or extracted as supplier tax \(editable\) at invoice line level and the system tax \(read only, derived from external tax engine\) is the sum total of system tax \(read only\) for all the tax lines of that particular invoice line.

    5.  Select **Add new invoice lines** to create invoice lines.

    6.  Select **Continue** to move to the next activity in the playbook.

    7.  Select **Submit invoice**.

        **Note:** During invoice processing \(straight-through processing\), when the invoice is sent to tax engine for validation, you can view the progress in the **Review compliance** swim lane. You will be prompted with a message "No action is needed. The system automatically runs a tax validation using a third-party tax engine. This verifies tax details from the invoice and ensures compliance by validating tax rates and jurisdictions. After tax validation is complete, the system moves to the next step automatically.![Tax validation in progress](../image/tax-validation-in-progress.png)

        Tax Validation in progress.

        ![Tax validation success](../image/tax-validation-success.png)

        Tax Validation successful.

        ![Tax validation failed](../image/tax-validation-failed.png)

        Tax Validation in failed.

<table id="table_fgw_ctv_j3c"><thead><tr><th>

Scenario

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Tax validation successful

</td><td>

If tax response is successful, the tax validation page will display the tax lines \(Review compliance - tax validation lane\) created automatically from the tax response.

</td></tr><tr><td>

Tax not validated due to integration error

</td><td>

Tax validation fails, exception is raised. **Note:** The revalidate Timed‑Out Tax Validations scheduled job identifies invoices that have remained in the In Progress tax status beyond the configured threshold \(as defined by the system property Maximum time to wait for tax validation from the external tax integration in minutes\) and updates their tax status to **Integration Error**.

</td></tr><tr><td>

Tax validation failed

</td><td>

Tax validation cannot be completed due to missing required invoice attributes for tax calculation or If tax response fails then Tax validation failed exception is raised. AP specialist manually verifies the invoice and selects **Validate tax** to re-calculate the tax.

</td></tr><tr><td>

Tax validation expired

</td><td>

Invoice header or line-level information is changed after the invoice execution \(post tax integration response\) then Tax validation expired exception is raised. AP specialist manually verifies the invoice and selects **Validate tax** to re-calculate the tax.

</td></tr><tr><td colspan="2">

System validates the supplier taxes by comparing the taxes calculated from the external tax engine and creates over or under tax exceptions.

</td></tr><tr><td>

Under tax amount variance \(invoice line\)

</td><td>

Tax amount on an invoice line is lesser than the tax response \(considering the variance\) received for the line item through tax engine.

</td></tr><tr><td>

Under tax amount variance \(invoice header\) exception

</td><td>

Total tax amount on the invoice header is lesser than the total tax \(considering the variance\) for the invoice received through tax engine

</td></tr><tr><td>

Over tax amount variance \(invoice header\)

</td><td>

Total tax amount on the invoice header is greater than the total tax \(considering the variance\) of the invoice received through tax engine

</td></tr><tr><td>

Over tax amount variance \(invoice line\)

</td><td>

Tax amount on the invoice line is greater than the tax \(considering the variance\) of the invoice line item of the invoice received through tax engine

</td></tr></tbody>
</table>6.  Select **Review exceptions**.

    The list of exceptions raised for the invoice is listed. For more information on exceptions, see [Invoice exceptions](../concept/work-with-invoice-exceptions.md) and [Using Playbook in Accounts Payable Operations](how-to-use-playbook.md).

    The invoice tax validation is successful.


