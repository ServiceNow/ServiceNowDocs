---
title: Roles installed with Code Signing
description: Code Signing includes the following roles.Use the code signing admin role to assign codesigning\_manager and codesigning\_auditor roles to other users.Use the code signing manager role to create and update signature configuration, and create and run code signing jobs.Use the code signing auditor role to view signature configurations, signing jobs, and Code Signing change audit data. The auditor role does not have create or write access to code signing assets.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/cs-role-landing.html
release: brazil
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Administer and Troubleshoot, Code Signing, Platform Security]
---

# Roles installed with Code Signing

Code Signing includes the following roles.

**Parent Topic:**[Code Signing reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/code-signing-reference.md)

## Code signing admin \[codesigning\_admin\]

Use the code signing admin role to assign codesigning\_manager and codesigning\_auditor roles to other users.

### Contains Roles

List of roles contained within the role.

None.

### Groups

List of groups this role is assigned to by default.

None.

### Special considerations

Avoid granting an admin role when more specialized roles are available.

## Code signing manager \[codesigning\_manager\]

Use the code signing manager role to create and update signature configuration, and create and run code signing jobs.

### Contains Roles

List of roles contained within the role.

None.

### Groups

List of groups this role is assigned to by default.

None.

### Special considerations

None.

## Code signing auditor \[codesigning\_auditor\]

Use the code signing auditor role to view signature configurations, signing jobs, and Code Signing change audit data. The auditor role does not have create or write access to code signing assets.

### Contains Roles

List of roles contained within the role.

None.

### Groups

List of groups this role is assigned to by default.

None.

### Special considerations

This role grants read and reporting access to the **sn\_cse\_vault\_codesigning\_audit\_data** table, which records changes to protected records. No role grants create, update, or delete access to this table. For more information, see [Code Signing change audit data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/cs-vault-audit-data.md).

