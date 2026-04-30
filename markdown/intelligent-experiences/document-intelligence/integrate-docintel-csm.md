---
title: Integrate with Customer Service Management
description: Document Intelligence provides document extraction capabilities to Customer Service Management \(CSM\). Extract relevant information from email and case attachments, such as credit card numbers or customer addresses, and add that information to cases.
locale: en-US
release: zurich
product: Document Intelligence
classification: document-intelligence
topic_type: concept
last_updated: "2026-01-27"
reading_time_minutes: 2
breadcrumb: [Integrate, Document Intelligence, Enable AI experiences]
---

# Integrate with Customer Service Management

Document Intelligence provides document extraction capabilities to Customer Service Management \(CSM\). Extract relevant information from email and case attachments, such as credit card numbers or customer addresses, and add that information to cases.

**Important:** Starting with the Zurich release, Document Intelligence is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported. For details, see the Deprecation Process article \[[KB0867184](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0867184)\] in the Now Support Knowledge Base. Instead, you can extract information from documents using the Now Assist in Document Intelligence application. For more information, see [Now Assist in Document Intelligence](docintel-nowassist-landing.md).

Agents can review values for extracted fields and make corrections as needed by accessing the Document Intelligence interface directly from the case. From this interface, agents can confirm correct values, fix incorrect values, and continue to train the model. This Human In the Loop \(HITL\) interaction of verifying the recommended values enables agents to refine the model and continually improve performance.

Create use cases that identify the information to extract from attachments, such as invoices, and automatically add that information to case fields, depending on the configuration. Labels identify the extracted fields on the case form.

For more information, see [Document Intelligence for CSM](https://www.servicenow.com/docs/access?context=csm-document-intelligence&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US).

## How Document Intelligence works with CSM

When a case is created, the Document Intelligence for CSM feature checks to see:

-   If the case has one or more attachments
-   If the attachment types are specified in the sn\_csm\_ml\_task.case.docintel.parsing\_supported\_types system property

If the case meets those requirements, the feature:

-   Identifies the right use case to use based on the case or case type and the use case filters.
-   Creates a task using the use case, the sys\_id of each attachment, and the case reference.
-   Sends the task, attachment sys\_ids, and case reference as inputs to the prediction model.
-   Uses optical character recognition \(OCR\) solutions to extract data from the documents.
-   Sets the status of the task to Done after the solution has completed.
-   If the extraction mode in the use case is set to Fully automated \(straight through processing\), the extracted field values are added to the case.
-   If the extraction mode is set to Auto-fill or Recommendation, the agent can validate the field values in the Document Intelligence interface.

## Enable Document Intelligence for CSM

Set the system properties and activate the required flows to enable Document Intelligence for CSM.

See [Document Intelligence for Customer Service](https://www.servicenow.com/docs/access?context=csm-document-intelligence&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US).

**Parent Topic:**[Integrating Document Intelligence with other applications](integrating-docintel.md)

