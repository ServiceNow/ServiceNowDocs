---
title: Step 5. Add Access Control Lists \(ACLs\) for Major Security Incident Management workspace users
description: Add Access Control Lists \(ACLs\) for Major Security Incident Management workspace users.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/security-incident-response/adding-access-control-lists-for-msim-workspace-users.html
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Rollup example use case implementation for a Security Case, Rollup Framework for MSIM, Major Security Incident Management, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Step 5. Add Access Control Lists \(ACLs\) for Major Security Incident Management workspace users

Add Access Control Lists \(ACLs\) for Major Security Incident Management workspace users.

## Before you begin

Role required: admin

**Note:** The permissions required to linking and unlinking capabilities are controlled by the sn\_msi.linkedsivi\_read role.

Major Security Incident Management persona contains sn\_msi.linkedsivi\_read role.

1.  sn\_msi.workspace\_admin \(MSIM Workspace admin\)
2.  sn\_msi.workspace\_manager \(MSIM Workspace manager\)
3.  sn\_msi.workspace\_responder \(MSIM Workspace responder\)

**Note:** For any source table, you must make sure that the required roles are added to the sn\_msi.linkedsivi\_read role.

## Procedure

1.  Navigate to **User Administration** &gt; **Roles** and search for **sn\_msi.linkedsivi\_read** role.

2.  Select **Edit** in the Contains Roles related list section.

    \[Omitted image "contains-roles-step4.png"\] Alt text: Roles.

3.  Make sure that your source table roles are added under the Contains Roles section.

    The Edit Members page is displayed to configure the roles required for a security case.

    \[Omitted image "edit-roles-step5.png"\] Alt text: Edit roles.

4.  Search for the source table roles, in the Collections section.

    Select the required roles that allow read and write access on the source table for a security case.

    **Note:**

    -   For a Security case, two separate roles for read and write are needed.
    -   Write access on tables for the ability to select source record from Major Security Incident Management workspace linked Record modal.
5.  Select **Save** to add roles.

6.  Verify that the roles are added successfully to the **Contains Roles** related list section.


**Parent Topic:**[Rollup example use case implementation for a Security Case](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/use-case-for-a-security-case.md)

