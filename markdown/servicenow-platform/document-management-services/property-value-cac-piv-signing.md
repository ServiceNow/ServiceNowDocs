---
title: Property value for digital signature using CAC or PIV smart cards
description: Specify the method that will be used to identify and validate the user who has signed the PDF using the com.snc.pdfsigning.validation.method property.
locale: en-US
release: australia
product: Document Management Services
classification: document-management-services
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Set up a document template for signing documents, Digital signature for PDF documents using CAC or PIV smart cards, Use, Document Management, Document Services, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Property value for digital signature using CAC or PIV smart cards

Specify the method that will be used to identify and validate the user who has signed the PDF using the **com.snc.pdfsigning.validation.method** property.

The property value **com.snc.pdfsigning.validation.method** is used for identifying and validating the user who has signed the PDF. Identifying the user is necessary to validate whether the correct user has signed the PDF. The IT team of a customer can define the way to validate a PDF depending on their policies and issued certificates.

|Value|Action|
|-----|------|
|common\_name|Uses the Common Name \(CN\) field in the Subject of the certificate to check if a certificate exists in the sys\_user\_certificate table that is associated with a user.​|
|email|Uses the email IDs in the certificate to locate a user in ServiceNow with a matching email ID.|
|any \(default value\)|Utilizes both of the above validation methods to resolve a user.|
|ignore|No user validation is performed on the signing fields.|

**Parent Topic:**[Set up a document template for signing documents using a CAC or PIV smart card](../task/create-document-template.md)

