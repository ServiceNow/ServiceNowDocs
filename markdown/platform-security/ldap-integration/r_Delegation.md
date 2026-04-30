---
title: Delegation with ADAM
description: Once the OU structure is created, define the permission delegations to properly secure the objects to limited users.
locale: en-US
release: xanadu
product: LDAP integration
classification: ldap-integration
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Active Directory Application Mode \(ADAM\), LDAP integration, Authentication, Access Management]
---

# Delegation with ADAM

Once the OU structure is created, define the permission delegations to properly secure the objects to limited users.

As with Active Directory, there are two general ways to grant permissions:

-   Add users to a group that already has the appropriate permissions assigned.
-   Define new permissions on the ADAM objects.

For this task, we discuss object level permissions. Refer to the Group Administration section for information on group memberships.

Since we don’t have a Users and Computers console for ADAM, all object level permissions are defined using the Active Directory utility DSACLS.exe. This file is found in the ADAM program directory. When running ADAM utilities it is best to launch the ADAM Tools Command Prompt. This ensures the proper versions of the tools. DSALCS is used to view and set object access rights.

Example: "`dsacls \\localhost:50010\dc=myCompany,dc=adam`" displays the permissions assigned to the root of partition **dc=myCompany,dc=adam** running on the localhost, port 50010. DSACLS is a complex tool used to create complex delegation. Run "DSACLS /?" for usage notes.

**Related topics**  


[Create containers and organizational units for ADAM](../task/t_CreateContainersAndOrgUnits.md)

[Use ADAMSync to populate ADAM](../concept/c_UsingADAMSyncToPopulateADAM.md)

[http://www.microsoft.com/downloads/en/details.aspx?familyid=9688f8b9-1034-4ef6-a3e5-2a2a57b5c8e4&amp;displaylang=en%7C](http://www.microsoft.com/downloads/en/details.aspx?familyid=9688f8b9-1034-4ef6-a3e5-2a2a57b5c8e4&displaylang=en%7C)

