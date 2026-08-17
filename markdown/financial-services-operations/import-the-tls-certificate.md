---
title: Import the TLS Certificate
description: The Verifi API endpoint is HTTPS-only. ServiceNow must trust the Verifi/Visa CA certificate chain to establish a secure connection. This section covers importing the certificate into the ServiceNow certificate store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/financial-services-operations/import-the-tls-certificate.html
release: australia
topic_type: task
last_updated: "2026-04-02"
reading_time_minutes: 1
breadcrumb: [Configure, Verifi, Integrate, Financial Services Operations \(FSO\)]
---

# Import the TLS Certificate

The Verifi API endpoint is HTTPS-only. ServiceNow® must trust the Verifi/Visa CA certificate chain to establish a secure connection. This section covers importing the certificate into the ServiceNow® certificate store.

## Before you begin

Role required: admin

## Procedure

1.  Obtain the certificate by performing the following steps:

    1.  Request the Verifi CA root certificate and any required intermediates from the Verifi Integration Team.

        The certificates will be provided in PEM format \(.pem or .cer extension\).

    2.  Confirm the certificate covers both verifiapi.visa.com \(Production\) and verifiapitest.visa.com \(UAT\).

    3.  If the certificate chain contains multiple files \(root + intermediate\), import each one separately.

2.  Import the certificate into ServiceNow® by performing the following steps:

    1.  Navigate to the System Definition &gt; Certificates.

    2.  Select **New**.

    3.  Set the type field to PEM.

    4.  Paste the full certificate content \(including **-----BEGIN CERTIFICATE-----** and **-----END CERTIFICATE-----** delimiters\) into the PEM Certificate field.

    5.  Set the **Name** field to a recognizable label, for example:

        |Certificate|Suggested Name|
        |-----------|--------------|
        |Visa/Verifi Root CA|Verifi — Visa Root CA|
        |Intermediate CA|Verifi — Visa Intermediate CA|

    6.  Select **Submit**.

    7.  Repeat all the steps for each certificate in the chain.

3.  Associate with the REST Endpoint by performing the steps given below:

    1.  Open the Verifi CDRN REST Message record \(UAT or Production\).

    2.  Locate the Mutual Authentication field group.

    3.  In the **Trust Store** field, reference the imported certificates.

    4.  Populate the Keystore and Keystore Password fields with the client certificate provided during onboarding if the client certificate authentication is required by Verifi.

    5.  Save the record.

    **Note:** To verify the certificate import, use the Test link on the REST Message record. A successful response confirms that TLS handshaking is working correctly. A "PKIX path building failed" error typically indicates a missing intermediate certificate.

4.  Set a calendar reminder at least 30 days before the certificate expiration date to obtain a renewal from the Verifi Integration Team.

    Expired certificates will cause all API calls to fail with a TLS handshake error. Verifi certificates are subject to periodic renewal.


**Parent Topic:**[Configuring Financial Services Operations Integration with Verifi](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/configure-financial-services-integration-with-verifi-cdrn.md)

