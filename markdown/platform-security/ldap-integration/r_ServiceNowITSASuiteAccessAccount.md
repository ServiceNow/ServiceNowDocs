---
title: Active Directory Application Mode \(ADAM\) Access Account
description: The system requires a user account to read the Active Directory Application Mode \(ADAM\) object information that is imported into the application instance.
locale: en-US
release: zurich
product: LDAP integration
classification: ldap-integration
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Active Directory Application Mode \(ADAM\), LDAP integration, Authentication, Access Management]
---

# Active Directory Application Mode \(ADAM\) Access Account

The system requires a user account to read the Active Directory Application Mode \(ADAM\) object information that is imported into the application instance.

Create the account by using one of the following methods:

-   Create a local ADAM user account and assign it a password and assign permissions.
-   Assign permission to a Windows domain account on the ADAM partition.
-   Use a userProxy account.

When using ADAM as an LDAP source, you must specify the fully qualified distinguished name \(FQDN\) of the ADAM account in the instance's LDAP server's **Login distinguished name** field.

**Related topics**  


[Active Directory Application Mode \(ADAM\)](../concept/c_ActiveDirectoryApplicationMode.md)

[http://www.microsoft.com/downloads/en/details.aspx?familyid=9688f8b9-1034-4ef6-a3e5-2a2a57b5c8e4&amp;displaylang=en%7C](http://www.microsoft.com/downloads/en/details.aspx?familyid=9688f8b9-1034-4ef6-a3e5-2a2a57b5c8e4&displaylang=en%7C)

