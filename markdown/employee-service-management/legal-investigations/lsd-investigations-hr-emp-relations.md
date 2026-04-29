---
title: Better together solution: Legal Investigations and HR Service Delivery Employee Relations
description: Employees can submit complaints through the Employee Center portal without worrying about who should investigate the complaint. During the triaging or investigation process, fulfillers working on these issues can transfer them back and forth between the Legal and HR departments as necessary for resolution.
locale: en-US
release: australia
product: Legal Investigations
classification: legal-investigations
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Explore, Legal Investigations, Legal Service Delivery Practice Applications, Legal Service Delivery, Legal and Contract Operations, Employee Service Management]
---

# Better together solution: Legal Investigations and HR Service Delivery Employee Relations

Employees can submit complaints through the Employee Center portal without worrying about who should investigate the complaint. During the triaging or investigation process, fulfillers working on these issues can transfer them back and forth between the Legal and HR departments as necessary for resolution.

## Key features

Using Legal Investigations and HR Service Delivery Employee Relations with Universal Request together for the following key features:

-   Omnichannel modes for submitting complaints via Employee Center portal, and Anonymous Report Center \(ARC\) portal.
-   Single triaging queue for all complaints through Universal Request.
-   Interdepartmental transfer of basic case details between Legal Service Delivery Legal Investigations and HR Service Delivery Employee Relations.

## Setting up Legal Investigations and HR Service Delivery Employee Relations to work together

Complete the following configurations to integrate Legal Investigations with HR Service Delivery Employee Relations.

-   [Set up Legal Investigations with HR Service Delivery Employee Relations](../task/integrate-lsd-hrsd.md)
-   [Configure Universal Request for legal services](../../legal-request-management/task/configure-universal-request-legal.md)

## Data mapping

When information related to HR [Employee Relations](../../human-resources/concept/hr-case-employee-relations.md) and related legal ethics matters is transferred between HR and the Legal departments, a complete data copy with appropriate data mapping is performed. For the Legal to HR transfer, activate the `HRERDepartmentTransferPostProcessor` script to enable copying. For more information, see [Data mapping fields](../reference/deep-data-copy-mapping.md).

To perform additional customizations for deep copying, edit the following scripts:

-   Legal to HR: `HRERDepartmentTransferPostProcessor` \(Employee Relations scope\)
-   HR to Legal: `LegalDepartmentTransferPostProcessor` \(Legal Investigations scope\)

In the **Evidence of type link** table, for a Legal to HR transfer, if external storage is enabled for the legal matter, the artifacts are copied into evidences with the URL field containing the document URL. If external storage is turned off, the matter artifact is copied as an evidence with all the attachments.

If external storage is enabled for the legal matter, all the attachments or documents are copied as evidences with an external documents link. For a Legal to HR transfer, no association exists between the interviews and evidences.

In the **Corrective/Recommended Actions** table, for a Legal to HR transfer, attachments in matter and artifacts linked to the Recommended action task are copied as attachments to the HR Corrective Action. If external storage is enabled for the legal matter, all the attachments or documents are copied as evidences with an external documents link.

## Workflow for handling complaints

The following workflow example explains how routing agents, legal fulfillers, and HR agents can use the applications together to resolve complaint requests submitted by employees.

1.  Employees who observe an ethical violation or similar incident report it by submitting a universal request. See [Submit a complaint through the Quick Link in Employee Center](../task/submit-complaint-employee-center.md#).
2.  A universal request routing agent can triage these complaint requests and create tickets for the appropriate department to work on. See [Triaging universal requests for legal investigation complaints](manage-legal-investigations-uni-request.md).

    **Note:** When the routing agent creates a legal ticket for complaints from the universal request, an ethics legal matter is created directly to handle and resolve the complaint.

3.  The fulfiller from the respective department who is assigned the ticket can work on it and close it, transfer it to another department, or transfer to the universal request. See [Work on a legal matter for a complaint](../task/work-legal-investigations-matter.md).
4.  When a ticket is transferred from the Legal department to the HR department, the details in the legal ticket, such as the description, short description, and comments, are copied to the HR Case. The legal ticket is closed, and an HR case is created, which is then handled by an HR agent. See [Transfer a legal ticket to another department](../../legal-request-management/task/transfer-legal-request-universal-request.md). Similarly, an HR agent working on an HR case can transfer it to the Legal department, which creates an ethics legal matter.

