---
title: View the Playbook activities
description: Playbooks in Accounts Payable Operations displays step by step process involved in processing an invoice processing case through activity views.
locale: en-US
release: yokohama
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Playbook for updating the invoice primary data, Using Accounts Payable Operations, Accounts Payable Operations, Finance and Supply Chain]
---

# View the Playbook activities

Playbooks in Accounts Payable Operations displays step by step process involved in processing an invoice processing case through activity views.

The playbook life cycle provides the context as to where an Accounts Payable specialist is within the playbook, including information for each stage and activity and any dependencies between stages. For stages with multiple activities, the playbook life cycle provides step-by-step guidance for completing the stage.

The figure below displays the playbook workflow.![Playbook workflow](../image/playbook.png)

The stages and activities in a playbook life cycle are configured using [Process Automation Designer](https://www.servicenow.com/docs/bundle/washingtondc-build-workflows/page/administer/process-automation-designer/concept/process-automation-designer.html) \(PAD\). Refer to the table below for the Playbook activity cards.

<table id="table_uts_4h1_51c"><thead><tr><th>

Stage

</th><th>

Activity

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Validate invoice

</td><td>

-   Review header details-Review the invoice header details and make any required changes
-   Review invoice lines- Review the invoice lines associated with the invoice processing case
-   Review tax lines- Review the list of invoice tax lines.

</td><td>

Verify the invoice details. For more information on details of playbook stages, see [Using Playbook in Accounts Payable Operations](../task/how-to-use-playbook.md)

</td></tr><tr><td>

Check duplicates

</td><td>

Review duplicates

</td><td>

Checks if the invoice processing case is a suspected duplicate

</td></tr><tr><td>

Map invoice lines

</td><td>

-   Verify purchase order- Verify the purchase order details associated with an invoice.
-   Review PO line mapping- Review the PO lines associated with the purchase order to identify the lines that is mapped to the invoice line.

</td><td>

Allows you map invoice lines with purchase order lines.

</td></tr><tr><td>

Review exceptions

</td><td>

-   Resolve exceptions- Review and resolve the exceptions generated for the invoice.
-   Review exception tasks-Review and resolve exception tasks if any.

</td><td>

Allows you review list of exceptions raised for the invoice

</td></tr><tr><td>

Await approval

</td><td>

-   View approval plan- Review the approval plan
-   Review approvals-Review the approvals generated for the invoice

</td><td>

Allows you to review approvals generated for the invoice

</td></tr><tr><td>

Pay invoice

</td><td>

-   Review integration errors- Review the integration errors generated for the invoice.
-   Review payments- Review the payment details of the invoice.

</td><td>

Allows you to review the integration errors and the payment details

</td></tr></tbody>
</table>The playbook work area appears in the center part of the playbook section. It displays the action taken for the current activity, depending on the configured activity view.

**Parent Topic:**[Playbook for updating the invoice primary data](playbooks.md)

