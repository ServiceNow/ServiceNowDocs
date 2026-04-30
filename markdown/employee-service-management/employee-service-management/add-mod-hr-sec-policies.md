---
title: Add or modify document security policies
description: Many employee documents contain confidential and personal information. Use document security policies to define access to employee documents and ensure that they are secure.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
---

# Add or modify document security policies

Many employee documents contain confidential and personal information. Use document security policies to define access to employee documents and ensure that they are secure.

## Before you begin

Role required: sn\_hr\_ef.admin

## About this task

You can determine who can read, write, or authorize purging of documents by adding or modifying document security policies.

**Note:** You can provide employees visibility into their own employee documents through their HR profile. Check the **Employee access** box on the **Document type** form. See [Define policies for a document type](../concept/hr-doc-management-config.md#).

Users are granted access to employee documents by:

-   Groups
-   Roles
-   Both groups and roles

The security policy can require authorization to purge and requires a user to belong to a group that has purge authorization.

See [Manage HR Groups](t_ManageHRGroups.md) and [Manage HR roles](../concept/c_ManageRoles.md). Or see [Groups](t_ManageHRGroups.md) and [Roles](../concept/c_ManageRoles.md).

## Procedure

1.  Navigate to **All** &gt; **HR Administration** &gt; **Employee Documents** &gt; **Security Policies**.

2.  Click **New** or an existing security policy to edit.

3.  Fill in the fields as appropriate.

<table id="table_cgc_tlf_d2b"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Description

</td><td>

Phrase that describes the HR employee document security policy.

</td></tr><tr><td>

Application type

</td><td>

Application associated with the security policy.

</td></tr><tr><td>

Active

</td><td>

Option for enabling or disabling the security policy. When you disable a security policy, it implies that the security policy will be associated with the document type, but will not be considered for evaluation.

</td></tr><tr><td>

Applies when

</td><td>

Filters defining additional conditions on a security policy.

</td></tr></tbody>
</table>    Use the three tabs to determine what groups or roles are required to search, access, and edit meta data for an employee document by document type. You can also define what groups receive purge notifications or can authorize purging of employee documents.

<table id="table_vgf_nmf_d2b"><thead><tr><th>

Tabs

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Read

</td><td>

Groups: Groups a user must belong to search and read an employee document with the associated document type and security policy.Roles: Roles a user must have to search and read an employee document with the associated document type and security policy.

**Note:** Users with the Employee Document Management Reader \[sn\_hr\_ef.document\_reader\] role must also be added here to search and read documents associated with the document type and security policy.

 Match all: Determines if both the conditions for groups and roles must be met for access.

**Note:** If you leave unchecked, the user only has to meet conditions from either Groups or Roles, not both.

</td></tr><tr><td>

Write

</td><td>

Groups: The groups a user must belong to access.Roles: Roles a user must have to search, read, and create an employee document with the associated document type and security policy.

 **Note:** Users with the Employee Document Management Writer \[sn\_hr\_ef.document\_writer\] role must also be added here to search, read, and create documents associated with the document type and security policy.

 Match all: Determines if both the conditions for groups and roles must be met for write access.

**Note:** If you leave unchecked, the user only has to meet conditions from either Groups or Roles, not both.

</td></tr><tr><td>

Authorize Purge

</td><td>

Authorization is required to purge documents, or send a notification before the purge process runs.Groups: Group a user must belong to authorize or be notified of an upcoming purge.

**Note:** Only one person in the group is required to authorize.

</td></tr></tbody>
</table>4.  Click **Save** and the **Document Types** related list appears.

5.  Click **New** and you can create a document type to be associated with the security policy.

6.  Click **Submit** or **Update**.


