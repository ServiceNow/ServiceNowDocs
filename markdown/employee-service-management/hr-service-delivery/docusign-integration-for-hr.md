---
title: Integrating with the DocuSign service
description: Request electronic signatures through the DocuSign service with the DocuSign integration.
locale: en-US
release: australia
product: HR Service Delivery
classification: hr-service-delivery
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [HR Integrations, Integration of HR Service Delivery with third-party systems, HR Service Delivery, Employee Service Management]
---

# Integrating with the DocuSign service

Request electronic signatures through the DocuSign service with the DocuSign integration.

**Important:**

Starting with the Australia release, HR Document Templates is being prepared for future deprecation. It will be hidden and no longer activated on new instances, but will continue to be supported.

Use [Document Templates](document-templates-overview.md) and [Document Template integration with Docusign](docusign-doc.md) that provide the latest experience for this functionality. For migration guidelines, see [Migrating from HR Document Templates to Document Templates](migration-hrdt-dt.md#).

For deprecation details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0867184) article in the Now Support knowledge base.

This integration depends on the DocuSign spoke in IntegrationHub, and is enabled for the signing of ad hoc documents \(HR PDF document templates\) and DocuSign templates. A preconfigured HR service, flow, and HR case template for both the ad hoc document flow and DocuSign template flow are available to use.

## DocuSign spoke

The DocuSign integration depends on the DocuSign spoke in IntegrationHub. Before you begin, an admin must have set up the DocuSign spoke, including registering as an OAuth provider and creating credential and connection records. You must also synchronize DocuSign with your ServiceNow instance.

-   Set up DocuSign spoke. See [Docusign eSignature Spoke](https://www.servicenow.com/docs/access?context=docusign-spoke&version=australia&pubname=australia-integrate-applications&ft:locale=en-US).
-   [Sychronize DocuSign with ServiceNow](https://www.servicenow.com/docs/access?context=sync-docusign-servicenow&version=australia&pubname=australia-integrate-applications&ft:locale=en-US)

    **Note:**

    -   You must synchronize each time you need to get new or updated DocuSign templates. To synchronize, navigate to **DocuSign** &gt; **Accounts** and click the **Get Accounts** related link.
    -   If your organization has more than one DocuSign account, the ad hoc document flow uses the first available account.

## DocuSign integration setup

Once the DocuSign spoke is set up and synchronized, you can configure the integration for HR. Depending on whether the user is signing an ad hoc document \(HR PDF document template\) or a DocuSign template, the integration has two flows that you can use. For each document that you want to make available for signing through the DocuSign service, configure as follows.

<table id="table_d5t_hrj_b3b"><thead><tr><th>

Flow

</th><th>

Configuration requirements

</th></tr></thead><tbody><tr><td>

Ad hoc document flow

</td><td>

1.  Create a managed document that you want to make available for signing. See [Managed Documents](https://www.servicenow.com/docs/access?context=c_ManagedDocuments&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US) for more information.
2.  [Configure an HR PDF document template for an ad hoc document](../task/configure-hr-pdf-document-template-for-docusign-ad-hoc-document.md)
3.  [Configure an HR service for the DocuSign integration](../task/configure-hr-service-for-docusign-integration.md)

</td></tr><tr><td>

DocuSign template flow

</td><td>

1.  Create a DocuSign template that you want to make available for signing. See the [DocuSign eSignature User Guide](https://support.docusign.com/en/guides/ndse-user-guide) for more information.
2.  [Configure an HR PDF document template for a DocuSign template](../task/configure-docusign-template-for-hr-document-template.md)
3.  [Configure an HR service for the DocuSign integration](../task/configure-hr-service-for-docusign-integration.md)

</td></tr></tbody>
</table>The ad hoc document flow is for the signing of static documents that originate from a managed document in the ServiceNow system. Each ad hoc document is configured as a standard HR PDF document template. You can add signers to the document with **Mark Signatures**, and then map each signature field to an appropriate user field in a table. \(The positioning of the markings are not used, and the DocuSign integration allows the signer to sign anywhere in the document.\) You can also parse the PDF to map document fields to corresponding table fields to auto-populate the document when it is generated for signing. The generated document is static, which means that it is read-only and the signatory cannot update any of the fields.

The DocuSign template flow is for the signing of dynamic documents that originate from the DocuSign system. Each DocuSign template is brought into the ServiceNow system, and then configured into an HR PDF document template to enable mappings. You must map each signature field from the DocuSign template to an appropriate user field in a table. You can also map fields from the DocuSign template to corresponding table fields to auto-populate the document for signing. The generated document is dynamic, which means that the signatory can write in editable fields, such as to update an address or provide W-4 information. However, any updates made are saved to the document only. They are not mapped back to the source table.

## Requesting electronic signatures through the DocuSign service

Once the integration setup is complete, HR agents from your organization can request electronic signatures through the DocuSign service.

For more information, see [Request an electronic signature through the Docusign service](../task/request-e-signature-through-docusign-service.md).

-   **[Configure an HR PDF document template for an ad hoc document](../task/configure-hr-pdf-document-template-for-docusign-ad-hoc-document.md)**  
If you are using the DocuSign integration, configure an HR PDF document template for each ad hoc document that you want to make available for signing.
-   **[Configure an HR PDF document template for a DocuSign template](../task/configure-docusign-template-for-hr-document-template.md)**  
If you are using the DocuSign integration, configure an HR PDF document template for each DocuSign template that you want to make available for signing.
-   **[Configure an HR service for the DocuSign integration](../task/configure-hr-service-for-docusign-integration.md)**  
Create or modify an HR service to request electronic signatures through the DocuSign service. Preconfigured flows to collect signatures for either an ad hoc document \(HR PDF document template\) or a DocuSign template are available to use. You must also configure an associated HR case template to set a default ad hoc document or DocuSign template for signing.

**Parent Topic:**[HR Integrations](scoped-hr-third-party-integrations.md)

