---
title: Integrating with the Adobe Sign service
description: Request electronic signatures through the Adobe Sign service with the Adobe Sign integration. This integration depends on the Adobe Sign spoke in IntegrationHub, and is enabled for the signing of adhoc documents \(HR PDF document templates\) and Adobe Sign templates.
locale: en-US
release: australia
product: HR Service Delivery
classification: hr-service-delivery
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [HR Integrations, Integration of HR Service Delivery with third-party systems, HR Service Delivery, Employee Service Management]
---

# Integrating with the Adobe Sign service

Request electronic signatures through the Adobe Sign service with the Adobe Sign integration. This integration depends on the Adobe Sign spoke in IntegrationHub, and is enabled for the signing of adhoc documents \(HR PDF document templates\) and Adobe Sign templates.

**Important:**

Starting with the Australia release, HR Document Templates is being prepared for future deprecation. It will be hidden and no longer activated on new instances, but will continue to be supported.

Use [Document Templates](document-templates-overview.md) and [Document Template integration with AdobeSign](adobe-sign-doc.md) that provide the latest experience for this functionality. For migration guidelines, see [Migrating from HR Document Templates to Document Templates](migration-hrdt-dt.md#).

For deprecation details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0867184) article in the Now Support knowledge base.

A preconfigured HR service, flow, and HR case template for both the adhoc document and Adobe Sign document are available to use.

**Note:** The Adobe Sign Integration flow will be completed \(or not in waiting state\) only after all the HR tasks created for the HR case are signed or expired or cancelled by the users.

## Adobe Sign spoke

The Adobe Sign integration depends on the Adobe Sign spoke in IntegrationHub. Before you begin, your administrator must have:

-   [activated the Adobe Sign spoke](../task/activate-adobe.md)
-   [set up the Adobe Sign spoke](https://www.servicenow.com/docs/access?context=adobe-sign-spoke&version=australia&pubname=australia-integrate-applications&ft:locale=en-US)


## Adobe Sign integration setup

Once the Adobe Sign spoke is set up, you can configure the integration for HR. The integration has a single flow that branches out into sub flows, one for signing an adhoc document \(HR PDF document template\) and another for signing an Adobe Sign template. The sub flow triggered for a document depends on the PDF template type that is configured for that document.

For each document that you want to make available for signing through the Adobe Sign service, configure as follows.

<table id="table_d5t_hrj_b3b"><thead><tr><th>

Type of document

</th><th>

Configuration requirements

</th></tr></thead><tbody><tr><td>

Adhoc document \(HR PDF document template\)

</td><td>

1.  Create a managed document that you want to make available for signing. See [Managed Documents](https://www.servicenow.com/docs/access?context=c_ManagedDocuments&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US) for more information.
2.  Configure an HR service for the adhoc document.
3.  [Configure an HR PDF document template for an adhoc document](../task/configure-hr-pdf-document-adobesign.md).

</td></tr><tr><td>

Adobe Sign document

</td><td>

1.  Create an Adobe Sign template that you want to make available for signing.
2.  [Configure an HR service for the Adobe Sign integration](../task/configure-adobe-sign-template-for-hr-document-template.md).
3.  [Configure an HR PDF document template for an Adobe Sign template](../task/configure-hr-service-for-adobe-sign-integration.md).

</td></tr></tbody>
</table>Each adhoc document is configured as a standard HR PDF document template. You can add signers to the document with **Mark Signatures**, and then map each signature field to an appropriate user field in a table. The positioning of the markings are not used, and the Adobe Sign integration allows the signer to sign anywhere in the document. You can also parse the PDF to map document fields to corresponding table fields to auto-populate the document when it is generated for signing. The generated document is static, which means that it is read-only and the signatory cannot update any of the fields.

Each Adobe Sign template is brought into the ServiceNow system, and then configured into an HR PDF document template to enable mappings. Map each signature field from the Adobe Sign template to an appropriate user field in a table. The generated document is dynamic, which means that the signatory can write in editable fields, such as to update an address or provide W-4 information. However, any updates made are saved to the document only.

## Requesting electronic signatures through the Adobe Sign service

Once the integration setup is complete, HR agents from your organization can request electronic signatures through the Adobe Sign service.

For more information, see [Request an electronic signature through the Adobe Acrobat Sign service](../task/request-e-signature-through-adobe-sign-service.md).

-   **[Activate the Adobe Sign spoke](../task/activate-adobe.md)**  
Activate the Adobe Sign spoke in IntegrationHub from the ServiceNow Store, and enable the signing of adhoc documents \(HR PDF document templates\) and Adobe Sign templates.
-   **[Configure an HR PDF document template for an adhoc document](../task/configure-hr-pdf-document-adobesign.md)**  
If you are using the Adobe Sign integration, configure an HR PDF document template for each ad hoc document that you want to make available for signing.
-   **[Configure an HR PDF document template for an Adobe Sign template](../task/configure-hr-service-for-adobe-sign-integration.md)**  
If you are using the Adobe Sign integration, configure an HR PDF document template for each Adobe Sign template that you want to make available for signing. You must map each signature field from the Adobe Sign template to an appropriate user field in a table.
-   **[Configure an HR service for the Adobe Sign integration](../task/configure-adobe-sign-template-for-hr-document-template.md)**  
Create or modify an HR service to request electronic signatures through the Adobe Sign service. A preconfigured flow to collect signatures for either an adhoc document \(HR PDF document template\) or an Adobe Sign template is available to use.

**Parent Topic:**[HR Integrations](scoped-hr-third-party-integrations.md)

