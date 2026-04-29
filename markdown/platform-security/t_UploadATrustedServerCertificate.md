---
title: Uploading a trusted server certificate
description: By uploading the service provider's trusted server certificate, the instance ensures it is connecting to a valid and secure service.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Uploading a certificate to an instance, Certificates, Encryption]
---

# Uploading a trusted server certificate

By uploading the service provider's trusted server certificate, the instance ensures it is connecting to a valid and secure service.

## Before you begin

Role required: admin

## About this task

The instance validates outbound Web Service calls by using the certificate provided by the service provider.

## Procedure

1.  Create a new Certificate record with the type **Trust Store Cert**.

2.  Do one of the following actions:

    -   Attach the service provider's DER formatted certificate.
    -   Copy and paste the service provider's PEM format certificate into the **PEM Certificate** field.

**Parent Topic:**[Uploading a certificate to an instance](t_UploadACertificateToAnInstance.md)

