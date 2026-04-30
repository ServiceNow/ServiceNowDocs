---
title: Assign the certificate to ADAM
description: Install an SSL certificate on the server and any LDAP client to support secure binds and encrypt the user and password information being transmitted.
locale: en-US
release: yokohama
product: LDAP integration
classification: ldap-integration
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Use LDAPS with ADAM, Active Directory Application Mode \(ADAM\), LDAP integration, Authentication, Access Management]
---

# Assign the certificate to ADAM

Install an SSL certificate on the server and any LDAP client to support secure binds and encrypt the user and password information being transmitted.

## Before you begin

Role required: admin

## About this task

Because there is limited and controlled uses to the ADAM service, it is feasible to use a self-signed certificate to meet your needs without incurring certificate costs or building a Certificate Authority \(CA\) infrastructure.

## Procedure

1.  Open the Certificates MMC console and create two console connections, one for Local Computer Certificates, and the other for Local Computer Services Certificates on the new ADAM service.

    The new certificate can be found under `Certificates (Local Computer)\Personal\Certificates`.

2.  Copy the certificate to the container for the ADAM service `Certificates – Service (ADAM Service Name)\ADAM_ADAM Service Name\Trusted Root Certificates\Certificates` and copy the certificate to `Certificates – Service (ADAM Service Name)\ADAM_ADAM Service Name\Personal\Certificates`.

3.  Open the details tab on the certificate that you copied, note the Valid from date stamp, and assign read access to the certificate key file.

    Go to `C:\Documents and Settings\All Users\Application Data\Microsoft\Crypto\RSA\MachineKeys` and identify the certificate with the matching time stamp. Assign Read &amp; Execute rights to the service account running ADAM. By default, this is **Network Service**.

4.  Restart the ADAM service to activate the new certificate.


**Related topics**  


[http://www.microsoft.com/downloads/en/details.aspx?familyid=9688f8b9-1034-4ef6-a3e5-2a2a57b5c8e4&amp;displaylang=en%7C](http://www.microsoft.com/downloads/en/details.aspx?familyid=9688f8b9-1034-4ef6-a3e5-2a2a57b5c8e4&displaylang=en%7C)

