---
title: Using Supplier Collaboration Portal in APO
description: The Supplier Collaboration Portal enables suppliers to interact with Accounts Payable specialists to submit invoices, create inquiry cases, and manage tasks.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/accounts-payable-operations/using-supplier-collaboration-portal.html
release: australia
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
keywords: [APO, Accounts Payable Operations, invoice exception, supplier, supplier portal, invoice inquiry case]
breadcrumb: [Use, Accounts Payable Operations, Finance and Supply Chain]
---

# Using Supplier Collaboration Portal in APO

The Supplier Collaboration Portal enables suppliers to interact with Accounts Payable specialists to submit invoices, create inquiry cases, and manage tasks.

## Supplier and supplier contact management

APO grants supplier contacts access to the Supplier Collaboration Portal to manage invoices and invoice inquiries, handle tasks, and submit invoices or inquiries through the portal, Virtual Agent, or Live Agent chat.

APO does not include workflows to onboard suppliers or to add and update supplier contacts. These workflows are part of SLO. If your instance has APO without SLO, import supplier and supplier contact records into ServiceNow from your ERP or other system of record instead of using the SLO onboarding workflow. For more information, see [Manage supplier contacts from the Source-to-Pay Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/managing-contacts-smw.md) and [Add a supplier contact from the Source-to-Pay Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/add-supplier-contact.md).

Each supplier contact record requires a linked user record. When you import a supplier contact, create a corresponding user record that stores the contact's user ID and password so the contact can log in to the Supplier Collaboration Portal with credentials set up outside ServiceNow.

## Supplier Portal Collaboration header

The portal header is located at the top-right corner of the home page contains the following options.

|Option|Description|
|------|-----------|
|My Tasks|Lists all the tasks that are assigned to the logged-in user. For more information on tasks, see [Working with tasks in Supplier Collaboration Portal header](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/work-supplier-collaboration-portal-header.md).|
|My Requests|Opens the My Requests page, which lists all the requests assigned to you.|
|Submit a request|Supplier raises invoice requests.|

For more information regarding the Supplier Portal Collaboration header options, see [Working with tasks in Supplier Collaboration Portal header](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/work-supplier-collaboration-portal-header.md).

## Supplier Collaboration Portal widgets

The Supplier Collaboration Portal integrated with Accounts Payable Operations consists of the following widgets. For more information on Supplier Collaboration Portal widgets, see [Supplier Collaboration Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/supplier-central.md).

## My active items widget

As a supplier contact, you can view specific items from the following tiles in the **My active items** widget:

<table id="table_pbp_yqy_zxb"><thead><tr><th>

Item

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Tasks

</td><td>

Opens the **My Tasks** list page, which lists all the tasks that are assigned to the supplier. For more information on tasks, see [Working with tasks in Supplier Collaboration Portal header](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/work-supplier-collaboration-portal-header.md).

</td></tr><tr><td>

Requests

</td><td>

Lists all the invoice inquiry cases for the supplier. For more information on inquiry requests, see [Working with My Requests](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/work-with-my-requests.md).

</td></tr><tr><td>

Invoices

</td><td>

Lists the invoices for supplier to view the invoice details and raise invoice related inquiry case. For more information on invoice inquiry see [Submit an Invoice Inquiry](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/submit-invoice-inquiry-case.md).**Note:** From the invoice form, you can submit an inquiry case. For more details on inquiry case, see [Submit an Invoice Inquiry](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/submit-invoice-inquiry-case.md)

.

</td></tr></tbody>
</table>## My Requests widget

Displays a list of invoice inquiry cases that you have submitted. Selecting a case directly opens the **My Requests** page so that you can work on that inquiry case. Select **View All** to view the list of all inquiry cases that you have submitted. For more information on **My Requests** widget, see [Working with My Requests](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/work-with-my-requests.md).

For more information on installing Supplier Collaboration Portal, see [Configure Supplier Lifecycle Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/config-supp-mgmt.md).

**Important:** After you install Supplier Collaboration Portal, approve the restricted caller access privileges that installation generates. If these privileges remain unapproved, suppliers encounter errors when they use the portal. For more information, see [Restricted caller access approvals for Supplier Collaboration Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/rca-approvals.md).

-   **[Explicit roles plugin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/explicit-roles-plugin.md)**  
The Explicit Roles plugin controls which users can access APO by requiring every user to have at least one explicit role assignment.
-   **[Working with tasks in Supplier Collaboration Portal header](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/work-supplier-collaboration-portal-header.md)**  
View and manage exception tasks and invoice inquiry requests assigned to your supplier account using the Tasks menu in the Supplier Collaboration Portal header.
-   **[Working with My Requests](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/work-with-my-requests.md)**  
View and manage invoice inquiry cases assigned to you as a supplier, including responding to requests from the Accounts Payable team.
-   **[Create Universal Request from Supplier portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/create-ur-from-supplier-portal.md)**  
Create a Universal Request \(UR\) from the Supplier Collaboration Portal to submit invoice inquiries directly to the Source-to-Pay Workspace for processing.
-   **[Working with Supplier Catalog](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/working-with-supplier-catalog.md)**  
Suppliers use the Supplier Catalog to submit invoice inquiries and new invoices to the Accounts Payable Operations team for evaluation and resolution.
-   **[Virtual agent flows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/virtual-agent-flows.md)**  
Suppliers can check the invoice and inquiry statuses, create inquiry cases in the supplier portal using the chat channel. Suppliers can also use the virtual agent to view predefined chatbot topics.

**Parent Topic:**[Accounts Payable Operations overview](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/use-acc-pay-mgmt.md)

**Related topics**  


[Create a knowledge base article about invoice]()

[Invoice case categories and subcategories]()

[Using Invoice Case Management]()

[Using Accounts Payable Invoice Processing]()

[Advanced Work Assignment in Accounts Payable Operations]()

[Configure Advanced Work Assignment for Accounts Payable Operations]()

[Using Advanced Work Assignment for Accounts Payable Operations]()

[Working with Advanced Work Assignment]()

[Interaction management in Accounts Payable Operations]()

[Composing emails with predefined content from the Source-to-Pay Workspace]()

[Universal Request in Accounts Payable Operations]()

[Playbook for updating the invoice primary data]()

