---
title: Using document types with HR document templates
description: Document types limit the choices for allowable documents based on HR service. For organizations with large amounts of documents, document types help categorize and make finding the correct document easier.
locale: en-US
release: zurich
product: HR Service Delivery
classification: hr-service-delivery
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
keywords: [Document Types]
breadcrumb: [HR document templates, HR Documents, HR Service Delivery, Employee Service Management]
---

# Using document types with HR document templates

Document types limit the choices for allowable documents based on HR service. For organizations with large amounts of documents, document types help categorize and make finding the correct document easier.

**Important:**

Starting with the Zurich release, HR Document Templates is deprecated and no longer supported or available for new activation.

Use [Document Templates](document-templates-overview.md) that provides the latest experience for this functionality. For migration guidelines, see [Migrating from HR Document Templates to Document Templates](migration-hrdt-dt.md#).

For deprecation details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0867184) article in the Now Support knowledge base.

For example, you can have multiple employee verification letters depending on if the employee is full-time, part time, or contingent. HR criteria on an HR service determines which letter to send.

When an HR case is created for an HR service, it checks:

-   HR case template for the HR service
-   The document type for the HR case template
-   HR criteria

Verifying this information allows the case to narrow the search for the correct letter or auto-populate the exact letter required.

-   **Setting up document types**

    To use this feature:

    -   Add a document type to your document templates.
    -   Add the document type to an HR case template. From the HR template classic environment, you can add a specific PDF template, but cannot specify a document type. Adding a specific PDF template automates populating the HR case form, but eliminates flexibility when you have multiple documents.
    -   Add the HR case template to an HR service.
    -   Add HR criteria to the HR service.
        -   Using HR criteria provides flexibility in choosing or auto-populating a document for an HR service.
        -   When defining conditions like case sensitivity or null values, see API [GlideFilter - Scoped, Global](https://www.servicenow.com/docs/access?context=c_GlideFilterScopedAPI&version=zurich&pubname=zurich-api-reference&ft:locale=en-US).
-   **How it works**

    When an HR case is created from an HR service:![Flow chart of how HR case is created from HR service.](../image/doctype_flow.png)

    The HR case template looks for a document type to determine what **Document template** or **PDF document template** to a case. It tries to automatically place a document template on an HR case by:

    -   Checking if there are documents associated with the document type.
    -   If there is only one document associated with the document type and the HR criteria is empty, place that document on the **HR case** form.
    -   If there is HR criteria on the document template, verify the **Subject person** on the **HR case** form matches the criteria. If yes, place the document template on the **HR case** form.
    -   If there are multiple document templates for the document type, check for **HR criteria**. When a single document matches, populate the document template on the **HR case** form. When multiple documents match, do not populate, but list documents in the Document type list in the **HR case** form.
    -   When **HR criteria** is not available on any document templates, list documents in the Document type list in the **HR case** form.

        **Note:** There is HR criteria on the HR service and HR document templates. On HR services, HR criteria narrows the allowable services for an employee. For example, you can provide 401 \(k\) services to US employees, but not to non-US employees. On HR document templates, HR criteria narrows what employees the document is for. For example, when you have employee verification letters for US employees and non-US employees, use HR criteria to determine the correct document.


