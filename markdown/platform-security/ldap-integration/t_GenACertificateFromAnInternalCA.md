---
title: Generate a certificate from an internal certificate authority
description: When you configure Microsoft Active Directory for SSL access, you must generate an internal certificate and request the external certificate.
locale: en-US
release: xanadu
product: LDAP integration
classification: ldap-integration
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configure Microsoft Active Directory for secure LDAPS communication, LDAP integration, Authentication, Access Management]
---

# Generate a certificate from an internal certificate authority

When you configure Microsoft Active Directory for SSL access, you must generate an internal certificate and request the external certificate.

## Before you begin

Role required: admin

## About this task

These steps apply to Microsoft CA services. If you have a different internal CA platform, see your local CA administrator for assistance.

## Procedure

1.  From the domain controller \(DC\) you want to create a certificate for, browse to `http://localhost/certsrv` or specify the CA server name if it is on a remote server.

2.  From the Welcome page, click **Request a certificate** and select advanced certificate request.

3.  On the Advanced Certificate Request page, select **Create** and submit a request to this CA.

4.  Complete the Advanced Certificate Request as follows:

    |Field|Entry|
    |-----|-----|
    |Name|The fully qualified domain name \(FQDN\) of the DC that is requesting the certificate.|
    |E-Mail|The email address of the person responsible for the certificate.|
    |Company|Your company name.|
    |Key Options settings|
    |Create new key set|Select it.|
    |CSR|Microsoft RSA SChannel Cryptographic Provider.|
    |Key Usage|Exchange.|
    |Key Size|1024 is recommended. The instance supports up to 2048.|
    |Automatic key container name|Select it.|
    |Store certificate in the local computer certificate store|Select it.|

5.  Click **Submit**.

    You are directed to a page that provides your **Request ID**, make note of this ID.

6.  To process the pending request, complete the following:

    1.  Open the Certificate Authority management console.

    2.  Expand the server node and select **Pending Requests**.

    3.  Locate the Request ID for the request you just submitted, right-click, and select All Tasks/Issue to approve the request and issue the certificate.

7.  To retrieve the issued certificate, complete the following:

    1.  From the DC you made the request from, browse to `http://localhost/certsrv`, or specify the CA server name if it is on a remote server.

    2.  Select `View the status of a pending certificate request`.

    3.  Select the link to the new certificate.

    4.  Select the link to **Install this certificate**.


## What to do next

You need to request a third party certificate. Certificates from external CAs can be purchased for as little as $30 per year. For detailed procedures on requesting a certificate from an external CA, see Microsoft article [321051](http://support.microsoft.com/kb/321051). After it is received, installed, and tested, follow the export procedure.

