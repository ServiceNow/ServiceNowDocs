---
title: Responsive dashboard role examples
description: Your ability to create, edit, view, or share a dashboard depends on your roles. These examples show what you can do with a dashboard based on your roles.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/now-intelligence/performance-analytics/responsive-dashboard-role-examples.html
release: zurich
product: Performance Analytics
classification: performance-analytics
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Dashboard permissions, Administering dashboards, Responsive dashboards in the Core UI, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Responsive dashboard role examples

Your ability to create, edit, view, or share a dashboard depends on your roles. These examples show what you can do with a dashboard based on your roles.

These descriptions of dashboard roles assume base system functionality. It is possible to create roles and assign permissions that override this functionality.

## No role

Users without a role only see dashboards that another user has shared with them. Information on the dashboard, especially list visualizations, may be hidden from the user based on ACLs.

Users without roles cannot create or share dashboards. An admin shared this dashboard with Avery, a user with no role. Much of the data on the dashboard is hidden and there is no sharing option.\[Omitted image "db-role-no-role.png"\] Alt text: Dashboard shared with user who has no role

## Any role

Users with any role can create dashboards and can share dashboards that they create. They can view or view and edit dashboards that are shared with them with the **Can edit** permission. ACLs still apply to what they can view in a dashboard. An admin shared the dashboard with Daniel, a user with the pa\_viewer role, with permission to edit. \[Omitted image "db-share-with-role-edit-perm.png"\] Alt text: Dashboard shared with user who has a non-admin, non-power user role

Daniel created this dashboard and therefore they can share, configure, edit, and delete it.\[Omitted image "db-share-config-edit.png"\] Alt text: Dashboard created by user without admin role. They can edit and share it.

## pa\_admin and pa\_power\_user

Users with pa\_admin and pa\_power\_user roles can manage users, groups, and roles on any dashboard that they can edit. Marisa has the pa\_power\_user role. When they click the Sharing icon \(\[Omitted image "SharingIcon.png"\] Alt text:\), they see all three options for people to share the dashboard with.\[Omitted image "db-share-pa-admin.png"\] Alt text: Dashboard viewed by user with pa\_admin or pa\_power\_user role who can share with groups, users, and roles.

## dashboard\_admin or admin

Users with the dashboard\_admin or admin role have these abilities:

-   Edit and manage users, groups, and roles for any dashboard
-   Change the owner of any dashboard
-   Delete any dashboard

Taylor has the dashboard\_admin role and selected **Dashboard Properties** from the context menu \(\[Omitted image "ContextMenu.png"\] Alt text:\). Both the **Owner** and **Delete** options are available to them.\[Omitted image "db-share-db-admin.png"\] Alt text: Dashboard properties for dashboard owned by user with role but accessed by ad user with the dashboard\_admin role.

