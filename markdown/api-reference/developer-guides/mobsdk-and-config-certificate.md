---
title: Configure certificate and create an OAuth Entity
description: You must configure your ServiceNow instance to accept and exchange a JSON Web Token \(JWT\) for an OAuth access token. To enable this functionality you must install a certificate that matches the JWT provider’s private key on the ServiceNow instance that you will use as the JWT Token consumer and create an OAuth Entity on that instance.
locale: en-US
release: australia
product: Developer Guides
classification: developer-guides
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Get started with Mobile SDK - Android, Mobile SDK Developer Guide - Android, Developer guides, API implementation and reference]
---

# Configure certificate and create an OAuth Entity

You must configure your ServiceNow instance to accept and exchange a JSON Web Token \(JWT\) for an OAuth access token. To enable this functionality you must install a certificate that matches the JWT provider’s private key on the ServiceNow instance that you will use as the JWT Token consumer and create an OAuth Entity on that instance.

## Before you begin

Role required: admin

## Procedure

1.  If not already configured, configure your ServiceNow instance as an OAuth JWT provider.

    For details, see Create an OAuth JWT API endpoint for external clients \(machine to machine integration\).

2.  Navigate to **System Definition** &gt; **Certificates**.

3.  Select **New** and then create a new public certificate as shown in the following image.

    ![Mobile SDK iOS X.509 certificate](../../image/mobile_sdk-image-x509-cert.png)

    For details on creating this certificate, see Update your X.509 certificate.

4.  Create an OAuth Entity.

    For details, see Create an OAuth JWT API endpoint for external clients \(machine to machine integration\).

5.  Add and select the **Public Client** field to the form.

    **Note:** This field is not shown by default.

6.  Save the record.

7.  Add a JWT Verifier Map entry.

    After the record is saved, a new section called **Jwt Verifier Maps** appears at the bottom of the form.

    1.  Add a name in the **Name** field, this can be whatever name you choose, and select the certificate that was added.

        The other fields, **Kid** and **Shared key**, can be left blank, as they are auto-filled.

8.  Ensure that the form contains information similar to the following once you are finished with your configuration:

    ![OAuth JWT](../../image/mobile_sdk-oauth_entity_form.png)


