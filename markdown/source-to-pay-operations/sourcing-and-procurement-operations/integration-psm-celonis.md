---
title: Sourcing and Procurement Operations integration with Celonis
description: Identify inefficiencies in your customer business process, understand their business impact, and gain insights into the root causes, by integrating Sourcing and Procurement Operations with Celonis.
locale: en-US
release: yokohama
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 6
breadcrumb: [Integrating Sourcing and Procurement Operations with other applications, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Sourcing and Procurement Operations integration with Celonis

Identify inefficiencies in your customer business process, understand their business impact, and gain insights into the root causes, by integrating Sourcing and Procurement Operations with Celonis.

Some insights provided by Celonis are listed here.

-   Inconsistent payment terms: Where the payment terms agreed with the supplier is Net 45 on the supplier primary record, but invoices have an earlier payment term like Net 15 or Net 30. Such inconsistent payment terms, if not recognized, may lead to an inefficient usage of the working capital and the days payable outstanding of the customer may get reduced.
-   Duplicate suppliers: Where a same supplier is wrongly created twice, for example, “California Academy of Sciences” and “The California Academy of Sciences.” Such duplicate records may confuse end users, with some invoices getting created for the first supplier and some for the second. This makes supplier account reconciliation difficult and prone to frauds, where the same invoice may be recorded for both the suppliers.
-   Duplicate invoices: Where the same supplier invoice gets recorded twice. This could be because it has been entered once based on the invoice that was emailed, and reentered by another payables specialist later when the physical copy of the invoice was received from the inward mail department. Such invoices, if not identified, may result in overbooking of an invoice and double payment to the supplier.
-   Invoices for late payment risk: Where some invoices are on hold as the price billed is marginally greater than the tolerance defined, for example, 0.5% above tolerance. In such cases, the has to be released so that the payment can be made on time.
-   Supplier bank account missing: Where the payment method setup on the supplier is electronic, but the bank account is missing. Payments for such suppliers are identified during the payment batch run that happens around the due date. This eventually delays the payment to the supplier and impacts the relationship with the supplier. Ideally, such issues must be identified beforehand so that the missing information can be gathered from the supplier well before the due date.

These insights are valuable and have a direct impact on business, in terms of inefficient usage of money, overspending, or having an adverse impact on supplier relationship. With this integration, these insights provided by Celonis are easily consumed by the Now platform’s intuitive low-code workflow to create playbook experiences that guide users through the processes on how to resolve these issues.

## Workflow and playbook experience for Celonis integration

Workflows for the various insights provided by Celonis are built with the help of the Playbooks component provided by the Now platform. For more information on this component, see [Process Automation Designer](https://www.servicenow.com/docs/access?context=process-automation-designer&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US).

Here's an example of an inconsistent payment term insight provided by Celonis, and an end-to-end system built to automate the work for the users.

Create a flow in Playbooks:

-   Ingest the data from the Celonis API, create a procurement case, and assign it to a user or group. These cases are displayed in the assigned user's Source-to-Pay Workspace landing page.
-   Customers can configure various options like updating the ERP directly from the case playbook, or manually logging in to the ERP to update the data.
-   Customers can configure the closure steps like sending an email to the supplier with the information that the payment terms have been updated to the original agreed term recorded in the primary record. Customers can also mark a copy of this email to their manager with the case closure information.

Configure your playbook experience to include the following relevant information:

-   Steps to resolve the case.
-   Displaying the relevant information in the playbook so that users can take appropriate decisions.
-   Ability to perform searches so that the case owner can search for knowledge articles on similar cases and learn how they were resolved.
-   Embedded tasks in the playbook like directly updating the ERP, which ensures that all the work that must be done can be done from the playbook itself without the need to log in to any other ERP system.

For more information, see [About Playbook Experience](https://www.servicenow.com/docs/access?context=playbook-ui&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US).

## Celonis triggers for Sourcing and Procurement Operations

A sample payload from Celonis for payment term mismatch is provided.

```
{
    "Supplier": "PolyTec",
    "Supplier City": "Munich",
    "Supplier Country": "DE",
    "Purchase Order": "PO10008760",
    "Invoice Number": 9350035113,
    "Payment Block Reason": "Payment Term Mismatch",
    "Due Date": "5/15/21",
    "Priority Vendor": "Yes",
    "Invoice Amount": 160725.03,
    "Payment Term (Invoice)": "NET 30",
    "Payment Term (Master Data)": "NET 60"
  }

```

The incoming payload from Celonis is stored in a custom staging table, from where it is processed via a business rule or flow designer to create a case and corresponding case lines. You can leverage existing case types or create a new case type as need be, which you can then assign to users or groups. Create a new case type by adding a new choice to the Case type column. A corresponding playbook can be triggered for this case type to assist in case fulfilment, as explained above.

**Parent Topic:**[Integrating Sourcing and Procurement Operations with other applications](integrating-spo.md)

**Related topics**  


[Sourcing and Procurement Operations integration with IT Asset Management](spo-itam-better-together.md)

[Sourcing and Procurement Operations integration with Employee Center](employee-center-integration-psm.md)

[Sourcing and Procurement Operations integration with third-party sourcing solutions](psm-integration-third-party-sourcing.md)

[Sourcing and Procurement Operations integration with Third-party Risk Management](better-together-with-vrm.md)

[Sourcing and Procurement Operations integration with Project Management](integration-psm-ppm.md)

[Sourcing and Procurement Operations integration with Field Service Management](integration-psm-fsm.md)

[Source-to-Pay Operations integration with Contract Management Pro](integration-spo-cmpro.md)

[ERP source validation on Sourcing and Procurement Operations objects](../reference/erp-source-val-spo-objects.md)

[Spendint API](../../../integrate/inbound-rest/concept/spendint-api.md)

[Procurement File Transfer Framework](procurement-file-transfer-framework.md)

