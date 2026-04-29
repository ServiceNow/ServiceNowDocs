---
title: Define LDAP organizational units
description: An organizational unit \(OU\) definition specifies the LDAP source directories available to the integration.
locale: en-US
release: australia
product: LDAP integration
classification: ldap-integration
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [LDAP integration setup, LDAP integration, Authentication, Access Management]
---

# Define LDAP organizational units

An organizational unit \(OU\) definition specifies the LDAP source directories available to the integration.

## Before you begin

Role required: admin.

## About this task

OU definitions can contain locations, people, or user groups. Every LDAP server definition contains two sample OU definitions: one for importing groups into the system and the other for users.

## Procedure

1.  Navigate to **All** &gt; **System LDAP** &gt; **LDAP Servers**.

2.  Select the LDAP server to configure.

3.  In the **LDAP OU Definitions** related list, select either the **Groups** or **Users** sample OU definition.

4.  Complete the LDAP OU Definition form \(see table\).

5.  Click **Update**.

    The system automatically tests the connection to the LDAP server.

6.  Under **Related Links**, click **Browse** to view the LDAP directory records that the OU definition returns.

    ![LDAP OU definition form](../image/LDAPOUdefinition.png)

<table id="table_frt_c1c_wp"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td id="entry_LdapServerName">

Specify the name the integration uses when referencing this OU. The name you enter here becomes an LDAP target in the data source record.

</td></tr><tr><td>

RDN

</td><td>

Specify the relative distinguished name of the subdirectory you want to search. This RDN is combined with the start-searching directory from the LDAP server definition to identify the subdirectory containing information for this organizational unit. For example, the sample OU definition uses the RDN value of `CN=Users` to search the LDAP directory `CN=Users,DC=service-now,DC=com` and any directory below this point. This field must match a subdirectory in your LDAP system.

</td></tr><tr><td>

Query field

</td><td id="entry_LdapQueryField">

Specify the name of the attribute within the LDAP server to query for records. The query field must be unique in both single and multiple domain instances. For best results, use email addresses or other credentials that uniquely identify the user in a multiple domain instance. Active Directory uses the **sAMAccountName** attribute. Other LDAP servers tend to use the **cn** attribute.**Note:** The **Query field** must map to the **User ID** field in the User \[sys\_user\] table. For example, if an Active Directory user logs in as `joe.example`, there must be a user record with a **User ID** value of **joe.example** and an LDAP record with an **sAMAccountName** value of **joe.example**.

</td></tr><tr><td>

Active

</td><td>

Select this check box to activate the OU definition and to allow administrators to test importing data. However, the integration can only bring data into the system from active OU definitions.

</td></tr><tr><td>

Table

</td><td id="entry_LdapTable">

Specify the table that receives the mapped data from your LDAP server. For users, select **User \(sys\_user\)**, and for groups, select **Group \(sys\_group\)**.

</td></tr><tr><td>

Filter

</td><td id="entry_LdapFilter">

Enter an LDAP filter string to select specific records to import from the OU. The more specific the LDAP filter query, the more efficient the query is. For example, the Users LDAP OU definition uses the following filter to select records that are classified as a person, have an **sn** attribute value, are not computers, and are not flagged as inactive:

 `(&(objectClass=person)(sn=*)(!(objectClass=computer)) (!(userAccountControl:1.2.840.113556.1.4.803:=2)))`

 You can find a description of LDAP filter syntax by searching the internet for `LDAP Filters RFC`.

</td></tr></tbody>
</table>
## Example organizational unit definitions

Suppose you have an LDAP server with the following directory structure:

dc=my-domain,dc=com

-   ou=Groups
    -   cn=Development
    -   cn=HR
    -   cn=Sales
-   ou=Users
    -   ou=Development
    -   ou=HR
    -   ou=Sales

Further suppose that you want to exclude the HR group and HR users from the application. Do the following:

1.  Create an LDAP server record with a starting search directory of dc=my-domain,dc=com.
2.  Create an OU definition record for ou=Groups with a filter to exclude cn=HR.
3.  Create an OU definition record for ou=Users with a filter to exclude ou=HR.

If you do not specify additional attributes or filters with an OU definition, the LDAP query returns the entire sub-tree from the starting directory and RDN.

In these examples, an OU definition with the RDN value of ou=Groups and no filter would have returned all groups. Likewise, an OU definition with the RDN value of ou=Users and no filter would have returned all users and child organizational units.

