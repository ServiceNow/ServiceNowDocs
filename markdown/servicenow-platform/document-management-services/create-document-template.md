---
title: Set up a document template for signing documents using a CAC or PIV smart card
description: Set up a document template for PDF using a Common Access Card \(CAC\) or Personal Identification Verification \(PIV\) card. Set up certificates to automate and simplify the process of filling, reviewing, and signing a document online.
locale: en-US
release: australia
product: Document Management Services
classification: document-management-services
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Digital signature for PDF documents using CAC or PIV smart cards, Use, Document Management, Document Services, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Set up a document template for signing documents using a CAC or PIV smart card

Set up a document template for PDF using a Common Access Card \(CAC\) or Personal Identification Verification \(PIV\) card. Set up certificates to automate and simplify the process of filling, reviewing, and signing a document online.

## Before you begin

Adobe Acrobat Reader must be installed on your desktop.

The Document Templates application must be installed. For more information, see [Configuring Document Templates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/hr-service-delivery/set-up-doc-temp.md).

Role required: sn\_doc.admin, sn\_doc.reader, or admin

## Procedure

1.  Create a document template.

    1.  [Configure a PDF document template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/hr-service-delivery/configure-editable-pdf.md).

        **Note:** The **Signing type** field should be **Digital Signature Smart Cards**.

    2.  [Map fields for the PDF document template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/hr-service-delivery/edit-pdf-mappings.md)

    3.  Select **Edit Document Preview** to define the label and placement of the button to submit the signature.

    4.  [Create participants for the PDF document template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/hr-service-delivery/create-participant.md).

    5.  To map templates to participants, go to the **Template Mapping** tab, select the field name, and add the participant name, and to map fields, select the field from the **Mapping field** drop-down menu.

        **Note:** The text fields can have pre-filled values mapped, and the digital signature field types should be mapped to the participants.

    6.  Select **Update**.

    7.  Select **Publish**.

2.  [Set up Certificate-based authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/certificate-based-authentication/set-up-mutual-auth.md).

3.  Configure your browser settings to automatically open the downloaded PDF documents in Adobe Acrobat Reader.

    For Google Chrome, see [PDF download setting for Google Chrome](https://support.google.com/chrome/answer/95759?hl=en&co=GENIE.Platform%3DDesktop#zippy=%2Cchange-default-pdf-download-permissions).

    For Mozilla Firefox and Apple Safari, see [Configure browser to use the Adobe PDF plug-in to open online PDF files](https://helpx.adobe.com/in/acrobat/kb/pdf-browser-plugin-configuration.html).

4.  Configure Adobe Acrobat Reader to add your download location as your Privileged Location.

    1.  In Adobe Acrobat Reader, go to **Preferences** &gt; **Security \(Enhanced\)**.

    2.  Select **Add Folder Path** and add your download location as your Privileged Location.

    3.  Select **OK**.


## What to do next

[Sign document templates for PDF documents using CAC or PIV smart card](sign-pdf-documents-cac-piv.md)

-   **[Assign a custom signing domain for CAC/PIV digital signatures](configure-domain-api-signing.md)**  
Improve signing traffic management by assigning a custom domain for CAC/PIV digital signatures by setting an optional system property to override the default **glide.servlet.uri** setting.
-   **[Property value for digital signature using CAC or PIV smart cards](../reference/property-value-cac-piv-signing.md)**  
Specify the method that will be used to identify and validate the user who has signed the PDF using the **com.snc.pdfsigning.validation.method** property.

**Parent Topic:**[Digital signature for PDF documents using CAC or PIV smart cards](../concept/digital-signature.md)

