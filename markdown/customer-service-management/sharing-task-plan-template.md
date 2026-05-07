---
title: Sharing task plan templates
description: Sharing task plan templates ensures that only authorized users can create, edit, and manage templates. It involves setting access controls, defining roles and responsibilities.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-05-06"
reading_time_minutes: 2
breadcrumb: [Task Plan Templates, Case management, Organize agent workspaces, Configure, Customer Service Management]
---

# Sharing task plan templates

Sharing task plan templates ensures that only authorized users can create, edit, and manage templates. It involves setting access controls, defining roles and responsibilities.

## Sharing task plan template overview

Effective sharing of task plan templates helps organizations manage ownership, sharing, and access securely and efficiently. It defines the responsibilities of admin and owner, and supports a seamless experience for users interacting with templates.

The sharing task plan template capability provides secure, efficient template management, and role-based controls for all member types involved.

Sharing task plan template features include;

-   Role-based access control
-   Ownership and sharing rules
-   Global template settings
-   Notifications when access is granted
-   API and ACL configurations for automated access provisioning

Templates can be marked as global or non-global, activated, or deactivated, and shared with users, groups, or service organizations.

**Note:** Query rules can be used with the CSM plugin to grant access to tables within Task Plan templates. Alternatively, non-query rules are available for scenarios where the CSM plugin is used independently.

## Template sharing and access management

Sharing task plan templates is designed to ensure that only authorized users can access, edit, or share templates, maintaining operational integrity and avoid misuse. Access is managed at multiple levels—user, group, service organization, and organization criteria—with each entity able to receive read, write permissions. Member Type is a key field when sharing templates with service organizations or based on organization criteria.

Task plan admin role: \(sn\_task\_plan.admin\)

The task plan admin role is responsible for overseeing and managing templates within the system. Admins can set templates as global or non-global, activate, or deactivate templates. Admins can assign access to users, groups, service organizations, or based on organization criteria. Admins have the authority to update template owners and they can apply global sharing rules and validations.

<table id="table_xds_vst_ghc"><thead><tr><th>

Field Names

</th><th>

Descriptions

</th></tr></thead><tbody><tr><td>

Owner field

</td><td>

Task plan template owners are responsible for sharing templates with users, groups, or service organizations, granting read, write access. They can view and manage access permissions and publish, clone, or deactivate shared templates. Owners can change the owner of a template and to switch a template’s status between global and non-global.

</td></tr><tr><td>

User, Groups, Service Org, Service Org Criteria, and Member type fields

</td><td>

Users, groups, service org, and service orgs filtered by organization criteria are able to view and write to shared templates. They can filter and search for templates and receive notifications whenever access is granted. Member Type is a key field enabled only when sharing templates with service organizations or based on organization criteria. Member type enables owners and admins to specify the exact role or type of members like Location Agent, Listed Member. These member type should have access to a template.

</td></tr></tbody>
</table>