---
title: Create an X.509 Certificate
description: Create an X.509 certificate record in ServiceNow by uploading a Java Key Store \(JKS\) file and configuring the certificate settings. This enables secure authentication and encryption for Card Data Security applications.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/financial-services-operations/dispute-management/create-an-x-509-certificate.html
release: australia
product: Dispute Management
classification: dispute-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [create x.509 certificate, x509 certificate, java key store certificate, upload jks file, validate certificate, system definition certificates, key store password, card data security certificate, certificate record creation]
breadcrumb: [Set up OAuth for Card Data Security, Configure, Card Data Security, Dispute Management, Banking applications, Financial Services Operations \(FSO\)]
---

# Create an X.509 Certificate

Create an X.509 certificate record in ServiceNow by uploading a Java Key Store \(JKS\) file and configuring the certificate settings. This enables secure authentication and encryption for Card Data Security applications.

## Before you begin

Role required: admin

This task requires a JKS file created for Card Data Security. See [Create a JKS file](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-management/create-a-jks-file.md) for more information.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Certificates**.

2.  Select **New**.

3.  Enter the following field values.

    |Field|Value|
    |-----|-----|
    |**Name**|&lt;Name of the certificate&gt;|
    |**Type**|Java Key Store|
    |**Key store password**|&lt;The key store password defined when generating the JKS file&gt;|

4.  Select the attachments \[Omitted image "Form\_Attachment.png"\] icon.

5.  Select the JKS file to attach the file to the record.

6.  Select the related link **Validate Stores/Certificates**.

    An information message saying "Valid key\_store" displays if validation is successful.

7.  Select **Update**.


## Result

A certificate record is created.

## What to do next

[Set up a JWT key](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-management/set-up-a-jwt-key.md).

