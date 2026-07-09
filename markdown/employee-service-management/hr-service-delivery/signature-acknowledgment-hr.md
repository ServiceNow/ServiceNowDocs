---
title: Adding a signature acknowledgment for HR documents
description: You can add an acknowledgement check box with customized text on HR documents associated with an HR task.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/employee-service-management/hr-service-delivery/signature-acknowledgment-hr.html
release: zurich
product: HR Service Delivery
classification: hr-service-delivery
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [HR document templates, HR Documents, HR Service Delivery, Employee Service Management]
---

# Adding a signature acknowledgment for HR documents

You can add an acknowledgement check box with customized text on HR documents associated with an HR task.

**Important:**

Starting with the Zurich release, HR Document Templates is deprecated and no longer supported or available for new activation.

Use [Document Templates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/hr-service-delivery/document-templates-overview.md) that provides the latest experience for this functionality. For migration guidelines, see [Migrating from HR Document Templates to Document Templates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/hr-service-delivery/migration-hrdt-dt.md).

For deprecation details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0867184) article in the Now Support knowledge base.

Signature acknowledgements are a way to capture the meaning of the signature, such as review, approval, responsibility, or authorship.

For the e-signatures task type, you can show a check box and clarifying text about the meaning of the signature. \[Omitted image "ack-e-signature.png"\] Alt text: E-signature acknowledgment

For the sign document task type, you can show a check box and clarifying text about the meaning of the signature.\[Omitted image "ack-sign-document.png"\] Alt text: Sign document acknowledgment

For acknowledgments, you can show a check box and clarifying text about using login credentials.\[Omitted image "ack-credential.png"\] Alt text: Credential acknowledgment

There are multiple ways to add the check box and text for the different task types.

-   **Create signature acknowledgment from an HR task**

    Using this method creates the acknowledgment check box and text one time for the specific HR task. It does not save it for future HR tasks of the same type.

    -   From an existing HR case, add an HR task.
    -   From the HR task, select an HR Task Type of:

        E-Signature.

    -   Select an E-signature template.
    **Note:** See [Adding an HR task to an HR case](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/hr-service-delivery/t_ViewAnHRTask.md).

-   **Create or modify an HR template \(task\)**

    Using this method creates an acknowledgment check box and text every time the HR service is requested for an HR case.

    -   Table: Select an HR task table.
    -   HR task type: Select one:
        -   E-Signature
        -   Sign Document

            **Note:** The parent HR case requires a PDF document.

        -   Credential
    -   Acknowledgment document: Attach a document.
    -   Acknowledgment text: \(Add this field\) Enter text to appear next to check box.
    **Note:** See [Configure an HR task template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/hr-service-delivery/configure-hr-task-template.md).

-   **Create or modify an HR document template**

    Using this method creates an acknowledgment check box and text every time the document is associated with an HR case.

    From the HR document template, add text in the **Acknowledgment text** field.

    **Note:** See [Configure an HR document template \(HTML\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/hr-service-delivery/t_AddHRPDFDocumentTemplate.md) or [Configure an HR PDF document template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/hr-service-delivery/PDFTemplate.md).

-   **Automate signing requests using templates**

    For more information on using DocuSign templates and automating signing requests using templates, see [How to automate signing requests using templates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/integrate-applications/automate-docusign-templates.md).


