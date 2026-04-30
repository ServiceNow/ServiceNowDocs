---
title: Test the LDAPS connections
description: Test the LDAPS connections. There are two console connections, one for Local Computer Certificates, and the other for Local Computer Services Certificates on the new ADAM service.
locale: en-US
release: zurich
product: LDAP integration
classification: ldap-integration
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Active Directory Application Mode \(ADAM\), LDAP integration, Authentication, Access Management]
---

# Test the LDAPS connections

Test the LDAPS connections. There are two console connections, one for Local Computer Certificates, and the other for Local Computer Services Certificates on the new ADAM service.

## Before you begin

Role required: admin

## Procedure

1.  Run LDP.exe from the ADAM install folder `c:\windows\adam`.

    Verify that the ADAM version is selected because this is not the standard Windows LDP client.

2.  Open a new connection by using the **Connection/Connect** menu.

    The server name must match the CN that is assigned to the certificate.

3.  Enter the **LDAPS port** and select the **SSL** check box.

    The results of a successful connection are some general server information and no errors.

4.  Bind \(log in\) to the service.

    To replicate typical LDAP client connections, select the Simple bind option. Enter a valid ADAM user or userProxy distinguished name in the user field and the associated password.

    If you see a return message stating ‘Authenticated as:….’ then you have successfully connected using LDAPS.


**Related topics**  


[http://www.microsoft.com/downloads/en/details.aspx?familyid=9688f8b9-1034-4ef6-a3e5-2a2a57b5c8e4&amp;displaylang=en%7C](http://www.microsoft.com/downloads/en/details.aspx?familyid=9688f8b9-1034-4ef6-a3e5-2a2a57b5c8e4&displaylang=en%7C)

