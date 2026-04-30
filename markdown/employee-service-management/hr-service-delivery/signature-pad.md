---
title: Signature pad for HR
description: Signature pad is a feature that any application can use. It captures an electronic signature that can be associated with a document or a task.
locale: en-US
release: yokohama
product: HR Service Delivery
classification: hr-service-delivery
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [HR document templates, E-signature applications of HR Service Delivery, HR Service Delivery, Employee Service Management]
---

# Signature pad for HR

Signature pad is a feature that any application can use. It captures an electronic signature that can be associated with a document or a task.

**Important:**

Starting with the Yokohama release, HR Document Templates is being prepared for future deprecation. It will be hidden and no longer activated on new instances, but will continue to be supported.

Use [Document Templates](../../human-resources/concept/document-templates-overview.md) that provides the latest experience for this functionality. For migration guidelines, see [Migrating from HR Document Templates to Document Templates](../../human-resources/concept/migration-hrdt-dt.md#).

For deprecation details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0867184) article in the Now Support knowledge base.

The HR Service Delivery application uses signature pad with onboarding documents like offer letters, background check approval, company policy acknowledgements, and more.

The Human Resources Scoped App: Core \[com.sn\_hr\_core\] plugin activates the Signature Pad \[com.snc.signaturepad\] plugin. The Signature Image \[signature\_image\] table installs with this plugin.

Ensure **Yes** is checked in the **com.snc.signaturepad.retrieveSignature** field on HR properties. See [HR properties](../../human-resources/task/t_HRProperties.md).

**Note:** [E-signature](https://www.servicenow.com/docs/access?context=e-signature&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US)

-   **Use**

    You can send your employees documents that require a user verification such as a digital signature or by typing their name.

    When signature pad is associated with a document or a task, it captures the drawn signature as an image and stores it in the Signature Image \[signature\_image\] table.

    **Note:** Typing a signature provides acknowledgement, but does not capture an image that is stored.

    For **HR document templates**, use the **Insert Signature** button to insert a variable that prompts a user to sign the document. For **HR PDF document templates**, use the **Employee Signature** field name and **PDF Template Mappings** to prompt a user to sign the document. Refer to [HR document templates](../../human-resources/concept/c_HRDocumentTemplates.md).

    **Note:** Check the generate document UI action condition to ensure this feature works correctly.

    -   **Examples**

        The HR Delivery System uses PDF documents for various scenarios. An example of the code used to call a UI page or dialog box for the signature pad:![PDF code snippet example that calls UI page.](../images/PDF_code_snippet.png)

        An example of the code used in a document after a signature has been accepted and a final PDF document is created:![Code when signature is accepted.](../images/signature_pad_snippet.png)


