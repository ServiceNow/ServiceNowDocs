---
title: Define ADAM user accounts
description: Define user accounts in ADAM. One user account is used for the instance to connect with and the other user account is for ADAMSync.
locale: en-US
release: australia
product: LDAP integration
classification: ldap-integration
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Use ADAMSync to populate ADAM, Active Directory Application Mode \(ADAM\), LDAP integration, Authentication, Access Management]
---

# Define ADAM user accounts

Define user accounts in ADAM. One user account is used for the instance to connect with and the other user account is for ADAMSync.

## Before you begin

Role required: admin

## About this task

These accounts can be local ADAM User objects, UserProxy objects, or a Windows account from a trusted domain.

The **ADAM User** account requires read-only access to the directory structure you are importing to your instance. The best way to accomplish this is to add the account to the member attribute on the Readers group found in cn=roles,dc=myCompany,dc=adam.

New ADAM User accounts are disabled by default. You will need to enable the new accounts and set a password.

## Procedure

1.  Enable users by changing the attribute msDS-UserAccountDisabled to FALSE.

2.  Right-click the user object and reset the password.

3.  Test the new accounts by using LDP as defined in [Active Directory Application Mode \(ADAM\)](../concept/c_ActiveDirectoryApplicationMode.md) to make sure they can connect.

    Use the **LDAP** &gt; **View/Tree** option, leaving the Base DN blank to make sure that you can view the objects in the directory by using the new accounts. The Configuration, Schema, and the domain partition should be visible in the left pane. Traverse the domain partition. If you are using a new local ADAM account, it will show ‘No Children’ which means that you don’t have read access to the objects. Verify the Setup group memberships and re-test.

    ADAMSync uses the **ADAMSync User** account to manage objects in the ADAM partition. This account requires admin level rights since it will create, update, and delete ADAM objects.

    ADAMSync uses the **ADAMSync AD** account to read the AD objects that will be synchronized to ADAM.


