---
title: Configuring Next Experience start page options
description: Multiple start page options help you determine where best to start your day in Next Experience. Configure the landing page so that you and your users start on a page tailored to your needs in ServiceNow.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
keywords: [next experience start page options]
breadcrumb: [Working in Next Experience, Next Experience UI, Configure UIs and portals, Configure user experiences]
---

# Configuring Next Experience start page options

Multiple start page options help you determine where best to start your day in Next Experience. Configure the landing page so that you and your users start on a page tailored to your needs in ServiceNow.

There are several options for the page that opens when you launch ServiceNow® or select the logo at the top of the screen.

## Start page options

Any page can have redirect rules as the page is loading to take the user to a different page.

-   **Next Experience default landing page**

    The default landing page provides information to help orient you to your tasks in an instance enabled with Next Experience. Variants of this page are available, depending on your setup. For more information, see [Exploring your Next Experience default landing page](../../../get-started/servicenow-overview/concept/exploring-your-next-experience-homepage.md).

-   **Configurable workspace home**

    Any page within a configurable workspace can be the start page. For more information about configurable workspace options, see [Configuring Configurable Workspace](../../configurable-workspace/concept/c_set-up-configurable-workspace.md).

-   **User-selected landing page**

    You can select any page on the platform to be your start, based on a user preference. A user-selected landing page can be any page inside a configurable workspace as well. For more information, see [Configure a user-selected start page](../task/configure-user-selected-start-page-preference.md).

-   **Admin-selected landing page**

    This option can be any page inside a workspace, but also a classic dashboard. The admin can include role-based logic to direct users to configurable workspaces. For more information, see

    -   [Configure a Core UI global landing page in Next Experience enabled instances](../task/use-ui16-landing-page-in-next-experience.md)
    -   [Configure per-user landing pages in Next Experience](../task/configure-per-user-ui16-landing-page-in-next-experience.md)
-   **Responsive dashboards**

    You can start with a responsive dashboard created in the classic environment to use an existing dashboard that isn't available in a configurable workspace. For more information, see [Set responsive dashboards as your home](https://www.servicenow.com/docs/access?context=t_SetDashboardsAsHome&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US).

-   **Homepages**

    Homepages are a deprecated feature. Homepages from earlier releases are read-only from the Tokyo release. For information on converting homepages to Responsive dashboards, see [Homepage deprecation](https://www.servicenow.com/docs/access?context=homepage-deprecation-help-tool&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US).


## How to choose a start page

The different options for start pages serve different purposes. For example, choose a responsive dashboard for your start page if most of your data is in the classic environment, rather than in configurable workspaces.

## Upgrade considerations

When you upgrade to an instance with Next Experience enabled, it's best to convert homepages to responsive dashboards, so that you don't lose editing capabilities. Homepages are turned off by default when Next Experience is enabled. For more information, see [Homepage deprecation](https://www.servicenow.com/docs/access?context=homepage-deprecation-help-tool&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US).

