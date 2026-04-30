---
title: Configure page security by role
description: Set up pages to be public or filter them by role.
locale: en-US
release: yokohama
product: Service Portal
classification: service-portal
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Managing portal access, Configuring Service Portal, Service Portal, Configure UIs and portals, Configure user experiences]
---

# Configure page security by role

Set up pages to be public or filter them by role.

## Before you begin

Role required: admin or sp\_admin

## About this task

Public pages won't require a user login; anyone can access them. All other options require user authentication.

## Procedure

1.  In the Service Portal configuration page \(**Service Portal** &gt; **Service Portal Configuration**\), open the Page Editor.

2.  In the Select Page list, search for the page to apply page security to.

3.  Select the highest level node in the tree view.

4.  Configure page security.

    -   To make a page public, select the **Public** check box. All users can access pages marked as **Public**.
    -   To limit access to a certain role, add roles in a comma separated list. Users without the role listed can see links to the page if they appear in the portal. Trying to open the page results in a "page not found" error.

        **Note:** If you select **Public** and add a list of roles, the page is still accessible by any user.

    -   To create a draft page that only administrators can see while the page is still in development, select **Draft**. Users must have the admin role to see any pages in draft. Everyone else sees a "page not found" error.
5.  Click **Save**.


## Example

![Doc page in the Page Editor with the admin,advanced_users,sp_admin roles entered in the Roles field](../image/PageSecurityExample.png "Page with limited access by role")

## What to do next

Follow the steps in [Configure widget security](configure-widget-security.md) to configure security for the widgets on your page.

**Parent Topic:**[Managing portal access](../concept/portal-security.md)

