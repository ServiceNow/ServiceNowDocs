---
title: Populating ADAM Objects
description: ADAM Objects include User Objects, UserProxy Object, and Group Objects.
locale: en-US
release: xanadu
product: LDAP integration
classification: ldap-integration
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Active Directory Application Mode \(ADAM\), LDAP integration, Authentication, Access Management]
---

# Populating ADAM Objects

ADAM Objects include User Objects, UserProxy Object, and Group Objects.

## User Objects

Users can be created using the ADAM ADSI Edit console just as we did for OU creation. Users can also be administered using AD command line tools, which is beyond the scope of this document. The only mandatory attribute for new user objects is the **cn**, which is a short name or the user’s full name. There are also a wide range of optional attributes similar to Active Directory user attributes. You can access the full list of attributes by selecting properties from the user object.

## UserProxy Objects

For ServiceNow LDAP integration we recommend you use UserProxy objects in ADAM which creates a proxy account that links to the related AD user account. This allows you to have ADAM authenticate logon credentials using AD usernames and passwords from the domain without ServiceNow directly connecting to the Domain Controller. UserProxy objects are very similar to AD and ADAM User objects except that do not store passwords and has an objectSID attribute that contains the SID from the linked AD User object. This is how the proxy works. UserProxy objects are created using the ADSIEdit console or command line tools, but this can be tedious. It is recommended that you use an automated process as defined below.

## Group Objects

Groups are created using the ADSIEdit console and AD command-line tools. Group concepts are similar to AD and are used to integrate groups and members to ServiceNow. The biggest difference is ADAM groups can contain members from ADAM or from trusted AD Domains.

## Automating ADAM Object Creation

If you are interested in synchronizing Active Directory accounts to ADAM, we recommend you use [Microsoft ADAMSync](http://technet.microsoft.com/en-us/library/cc786455(WS.10).aspx) tool. This is the most common use of ADAM for ServiceNow LDAP integration.

## About Permission Delegation

ADAM contains some built-in groups with default permissions. These groups are found in the container cn=roles,dc=myCompany,dc=adam. These are similar to domain level groups and have rights to objects in the current partition. Similar to AD Forests you can also set a higher level of permissions using the default groups in cn=roles,cn=configuration,dc=myCompany,dc=adam. You must connect to the configuration partition in ADSIEdit. The Administrators group by default includes the account specified during the setup. This member is not always visible since it’s inherited through the configuration groups. Administrators have full control of all partition objects. The Readers group does not contain any members by default and has read access to all objects in the partition. The Users group is a dynamic group just as it is in Active Directory. Transitively it includes all ADAM users created in the partition.

**Related topics**  


[http://www.microsoft.com/downloads/en/details.aspx?familyid=9688f8b9-1034-4ef6-a3e5-2a2a57b5c8e4&amp;displaylang=en%7C](http://www.microsoft.com/downloads/en/details.aspx?familyid=9688f8b9-1034-4ef6-a3e5-2a2a57b5c8e4&displaylang=en%7C)

