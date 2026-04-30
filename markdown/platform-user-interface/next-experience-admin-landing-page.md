---
title: Next Experience default admin landing page
description: Use the default admin landing page to see your admin-specific work at a glance and identify items that need attention including open tasks, security issues, and approvals.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Next Experience landing pages, Configuring the Next Experience UI, Next Experience UI, Configure UIs and portals, Configure user experiences]
---

# Next Experience default admin landing page

Use the default admin landing page to see your admin-specific work at a glance and identify items that need attention including open tasks, security issues, and approvals.

As an admin, a variant of the landing page for admins displays for you. Admin landing pages might include the following items:

-   Number of installed apps that have updated versions available
-   Number of entitled but not activated or not installed apps
-   Real-time security notifications
-   Lists and visualizations of your assignments
-   More resources to learn about features

![Default admin landing page.](../image/Admin_Landing_Page.png)

## New Customers

New customers launching on San Diego or customers that have performed a zBoot on their instance will have the Next Experience UI automatically enabled on their instance. These customers also have the Default landing page that ships with the Next Experience UI automatically enabled.

## Existing Customers

Existing customers upgrading from a previous release will not see the default landing page upon activating the Next Experience UI. Existing customers will continue to see their existing start page \(Homepage or Dashboard\). By utilizing existing start pages, this provides administrators the ability to turn on the Next Experience UI and allow for users to begin using the new user interface, and provides administrators the time to create organization specific landing pages. Existing customers can use the Default Landing Page by modifying the **glide.login.home** system property, though it is recommended to perform testing on the Default Landing Page in a sub-product instance to verify it meets current user needs.

**Parent Topic:**[Next Experience landing pages](next-experience-landing-pages.md)

