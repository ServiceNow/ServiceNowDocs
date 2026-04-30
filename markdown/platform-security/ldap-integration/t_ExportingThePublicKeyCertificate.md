---
title: Export the public key certificate
description: LDAPS clients, including the instance need the public key certificate in order to make a secure connection to ADAM.
locale: en-US
release: xanadu
product: LDAP integration
classification: ldap-integration
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Use LDAPS with ADAM, Active Directory Application Mode \(ADAM\), LDAP integration, Authentication, Access Management]
---

# Export the public key certificate

LDAPS clients, including the instance need the public key certificate in order to make a secure connection to ADAM.

## Before you begin

Role required: admin

## About this task

From the server certificate consoles you used above, export a public key to be used by the clients.

## Procedure

1.  Select the certificate, right-click, and select **all tasks/export**.

    Do not export the private key. Select the default DER encoded binary X.509 format and specify the export file name.

2.  Install the public certificate on the LDAP clients that connect to the server using LDAPS.

    When prompted, add the certificate to the Trusted Root Certificate Authorities store.


**Related topics**  


[http://www.microsoft.com/downloads/en/details.aspx?familyid=9688f8b9-1034-4ef6-a3e5-2a2a57b5c8e4&amp;displaylang=en%7C](http://www.microsoft.com/downloads/en/details.aspx?familyid=9688f8b9-1034-4ef6-a3e5-2a2a57b5c8e4&displaylang=en%7C)

