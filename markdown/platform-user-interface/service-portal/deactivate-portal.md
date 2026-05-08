---
title: Deactivate a portal
description: Turn off access to a portal that you no longer want users to visit and optionally redirect them to another portal.
locale: en-US
release: australia
product: Service Portal
classification: service-portal
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Managing portal access, Configuring Service Portal, Service Portal, Configure UIs and portals, Configure user experiences]
---

# Deactivate a portal

Turn off access to a portal that you no longer want users to visit and optionally redirect them to another portal.

## Before you begin

Role required: sp\_admin or admin

## About this task

After you deactivate a portal, users are either redirected to an alternate portal that you configure, or they receive a message that the portal is inactive.

If an alternate portal is selected, pages are redirected by replacing the URL suffix of the inactive portal with the suffix of the alternate portal. To confirm that users are redirected to the correct page, complete the following steps:

-   Verify that all necessary resources, such as knowledge base articles and catalog items, are available on the alternate portal.
-   If different pages are used on each portal, set up page route maps to map pages from the inactive portal to the alternate portal. For more information, see [Redirect a reference to a page ID](reroute-page.md).
-   If customizations exist for page redirects using the SPEntryPage script include or other methods, test these customizations thoroughly to confirm that there are no conflicts or remove the customizations. For more information, see [Single sign-on, logins, and URL redirects](../concept/c_SPSSOLoginAndRedirects.md#).

To support deactivating and reactivating public portals without search engines deindexing their pages, temporary HTTP 302 redirects are used for inactive portals.

## Procedure

1.  Navigate to **All** &gt; **Service Portal** &gt; **Portals**.

2.  Select a portal.

    **Note:** You can't deactivate the default portal on an instance or any portal configured as an alternate portal for an inactive portal. You can't deactivate or redirect to the Mobile Employee Service Portal \(/mesp\).

3.  Select **Inactive**.

4.  In the **Alternate portal** field, select an active portal to which to redirect users who attempt to access the inactive portal.

    Multiple inactive portals can redirect to the same alternate portal.

5.  Select **Update**.


## Result

If you selected an alternate portal, users attempting to access the inactive portal are redirected to the alternate portal. They receive a message informing them that they've been redirected. For example:

![Message for users who attempt to visit an inactive portal and are redirected to an alternate portal.](../image/inactive-portal-message.png)

If you don’t specify an alternate portal, users receive a message that the portal has been deactivated. You can customize these messages from the Message \[sys\_ui\_message\] table. For more information see, Message table.

To reactivate a portal, clear the **Inactive** option.

**Parent Topic:**[Managing portal access](../concept/portal-security.md)

