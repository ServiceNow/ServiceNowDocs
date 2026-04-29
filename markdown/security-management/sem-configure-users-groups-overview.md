---
title: Configure users and groups in Security Exposure Management Workspace
description: Administrators can manage user and group access directly from the Security Exposure Management Workspace using centralized assignment of product-specific roles through a consistent, workspace-based experience.
locale: en-us
release: australia
topic_type: concept
last_updated: "2026-03-25"
reading_time_minutes: 2
keywords: [Security Exposure Management Workspace, user management, group management, role assignment, explicit roles, Security Exposure Management]
breadcrumb: [Implement, Unified Security Exposure Management, Security Operations]
---

# Configure users and groups in Security Exposure Management Workspace

Administrators can manage user and group access directly from the Security Exposure Management Workspace using centralized assignment of product-specific roles through a consistent, workspace-based experience.

The Users and Groups capability in the Security Exposure Management Workspace provides a centralized interface for managing product-specific role assignments. This workspace-based experience enables administrators to control access to security management products without navigating to multiple configuration pages.

## Scope of role management

The Users and Groups page manages only explicit role assignments. This means:

-   Only users and groups directly assigned to a role through this interface are displayed and managed.
-   Role inheritance through other roles or group membership is not modified or displayed on this page.
-   Users who inherit a role through group membership or role hierarchy are excluded from the view.
-   The interface provides a focused view of direct assignments for clarity and control.

## Required roles

Access to the Users and Groups page varies based on role assignment:

-   **System Administrator \(admin\)** – Required to add or remove users and groups from roles. This role provides full administrative access to modify role assignments.
-   **Application Admin / Persona Roles** – Provides read-only access to view role assignments. Users with these roles can review existing assignments but cannot make modifications.

## Supported products

The Users and Groups page displays products and roles based on installed plugins and feature configuration. Supported products include:

-   Security Exposure Management
-   Vulnerability Response
-   Application Vulnerability Response
-   Container Vulnerability Response
-   Configuration Compliance

Each product provides multiple role options specific to its functional requirements, such as admin, analyst, remediation owner, and other specialized roles.

## Read-only access

Users who have application-specific persona roles but do not have the system administrator role can view role assignments in a read-only mode. These users can view supported products, role listings, and assigned users and groups, but cannot add or remove assignments. This provides transparency while maintaining security controls around role modifications.

## View inherited roles

To view the granular roles inherited by a persona role, navigate to **All** &gt; **User Administration** &gt; **Roles**. Open the role record and review the Contains Roles related list.

-   **[Add groups to a role](sem-add-groups-to-role.md)**  
Assign groups to product-specific roles in the Security Exposure Management Workspace. Only explicit assignments are managed through this interface.
-   **[Add users to a role](sem-add-users-to-role.md)**  
Assign users to product-specific roles using the interface in the Security Exposure Management Workspace.

**Related topics**  


[Supported products and roles in](../reference/sem-supported-products-roles.md)

