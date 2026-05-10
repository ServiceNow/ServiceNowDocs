---
title: Considerations for activating Next Experience
description: Next Experience delivers a next generation, intuitive, personalized experience to drive productivity, improve engagement, and surface insights across the ServiceNow AI Platform. Your path to activating Next Experience may depend on your instance's level of customization.How to enable or disable the Next Experience UI.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
keywords: [enable next experience, activate next experience]
breadcrumb: [Configure, Next Experience UI, Configure UIs and portals, Configure user experiences]
---

# Considerations for activating Next Experience

Next Experience delivers a next generation, intuitive, personalized experience to drive productivity, improve engagement, and surface insights across the ServiceNow AI Platform. Your path to activating Next Experience may depend on your instance's level of customization.

Guidance and support from the engineers who helped you customize your instance, or another certified partner, will help to ensure that your move to Next Experience goes smoothly.

**Note:** You must have UI16 installed before activating the Next Experience.

## New customer starting on the Australia release

If you're a new customer, you automatically have Next Experience enabled and you don't need to modify the UI to get the newest user interface.

## Existing customer upgrading instance without UI customization

If you're an existing customer, but haven't implemented UI customizations or invested significantly in adopting Workspace, the Next Experience UI is turned on when you upgrade.

## Existing customer upgrading instance with UI customization

If you're an existing customer who has made any of the following modifications to your instance, you might need assistance from the modification authors, or an established partner, to ensure a seamless activation.

-   Customized your user interface. For example, if you created hard-coded styles or implemented UI scripts.
-   Adopted a classic Workspace and want to adopt a new configurable workspace alternative.
-   Created custom components in a classic Workspace and want to adopt a new configurable workspace alternative.

You can use the following tools and APIs with your implementation partner to help adjust your customizations to work well with the new Next Experience theme:

-   [Scriptable PolarisUI API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/server-api-reference/PolarisUIScopedAPI.md)
-   [Next Experience client scripting globals](../reference/next-exp-client-script-globals.md)
-   [Jelly tags](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/scripts/r_JellyTags.md)

## Existing customer opting out of the Next Experience UI prior to an upgrade

If you are an existing ServiceNow customer and decide that you do not want to turn on the Next Experience UI during an upgrade, you can create a system property called **glide.ui.next\_experience.opt\_out** and set the value to **true**.

During the upgrade, the Next Experience UI is not turned on.

## Functionality not supported

**Important:**

Connect Chat is not available in Next Experience. Starting with Australia, certain Connect Chat functions are available in Next Experience by using Sidebar. See [KB1123615 – Moving from Connect Chat to Sidebar](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1123615) for more information about the differences between Connect Chat and Sidebar.

Connect Support is not available in Next Experience and is scheduled to be completely deprecated in Utah. If you want to automatically assign chat requests and other work items to agents in Next Experience, you must migrate to Advanced Work Assignment and Agent Chat. For details, see [Move from Connect Support to Advanced Work Assignment and Agent Chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/advanced-work-assignment/migrate-from-connect-support.md).

These features and products are not currently supported with Next Experience:

-   The functionality found in homepages, arranging information from your instance to tell a story about your data, is found in dashboards on new instances. On upgraded instances with Next Experience enabled, users can view existing homepages if they have a direct URL, but they can't create or edit them. Responsive dashboards and Analytics Overview dashboards take over homepage functionality. Use the [Homepage deprecation help tool](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/performance-analytics/homepage-deprecation-help-tool.md) to convert the homepages on your instance to responsive dashboards.
-   [Live Feed](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/live-feed/c_GetStartedWithLiveFeed.md) is not supported.
-   The JavaScript console log isn't supported in the Next Experience framework.
-   ATF doesn't support these elements of Next Experience, but support for these features is planned for future releases:

    -   Pages built with UI Builder, including pages with lists and form components.
    -   Configurable Workspaces
    -   Landing pages
    **Note:** ATF still supports the Core UI, including Classic Environment \(such as classic lists and forms\).


For more information, see:

-   [KB1156736 – Moving from Connect Chat to AWA and Agent Chat](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1156736)
-   [KB1123615 – Moving from Connect Chat to Sidebar](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1123615)
-   [KB1157068 – Live Feed Is Not Supported in Next Experience](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1157068)

**Parent Topic:**[Configuring the Next Experience UI](next-experience-ui-admin.md)

## Enable Next Experience

How to enable or disable the Next Experience UI.

### Before you begin

Role required: admin

### About this task

As an administrator, you can enable Next Experience for all users on your Australia instance, or let users enable or disable unified navigation for themselves.

If you're a new customer running the Australia release, Next Experience is enabled by default. If you're upgrading, see the information at [Considerations for activating Next Experience](next-experience-adoption-paths.md#) before you enable Next Experience.

**Warning:** It's not recommended that you enable or disable the Next Experience UI until you've learned the impact of how that might affect your instance functionality. You might need assistance from the modification authors or an established partner to ensure a seamless activation.

### Procedure

1.  On login, the **Turn on Next Experience** modal displays. ![Next experience modal.](../image/turn-on-next-experience-modal.png)

2.  Select **Get started**.

3.  Read and determine if Next Experience is for your users.![Turn on next experience page.](../image/turn-on-next-experience-page.png)

    **Note:** Be aware that enabling the Next Experience UI will affect all users on your instance, not just the system administrator.

    Note also that if the admin is on a production instance, a warning appears to notify them of functionalities not supported in Next Experience.

4.  Select **Turn on Next Experience**.

    A banner displays to notify you that Next Experience is successfully turned on.![Next experience turned on banner.](../image/next-experience-turned-on-banner.png)

5.  Log out and back into your instance.

6.  To disable Next Experience in your instance, do the following:

    1.  Navigate to **sys\_properties.list**.

    2.  Set the value of the **glide.ui.polaris.experience** property to **false** to disable Next Experience.

    3.  Reload your instance.


