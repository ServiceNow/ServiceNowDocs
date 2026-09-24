---
title: Manage capabilities maps
description: Explore and manage the usage status for the capabilities you are entitled to use.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/impact/impact-product-adoption-roadmap/manage-capability-maps.html
release: brazil
product: Impact Product Adoption Roadmap
classification: impact-product-adoption-roadmap
topic_type: task
last_updated: "2026-09-21"
reading_time_minutes: 3
breadcrumb: [Entitlements and usage using capabilities, Product adoption, Using Impact, Impact]
---

# Manage capabilities maps

Explore and manage the usage status for the capabilities you are entitled to use.

## Before you begin

Role required: Impact\_platform\_owner, impact\_admin, impact\_executive, or impact\_user

## About this task

Use the capabilities map to track which entitled capabilities your organization is using, planning to use, or not using. Update usage status, add notes, and organize the view to support product adoption planning.

**Note:** Starting with the Brazil release, the Impact Store Application displays 375 entitled and non-entitled capabilities, compared to 1,155 capabilities in previous releases.

## Procedure

1.  Navigate to **Impact Workspace** &gt; **Product Adoption** &gt; **Capabilities map**.

2.  From the **View by** list, select your product.

    The Product Adoption Summary displays capabilities that your organization is planning or actively using, along with percentage usage trends over time.

    To adjust the time period for **% in use capabilities**, select \[Omitted image "ellipsis-vertical-fill-24.svg"\] Alt text: time period icon icon.

    **Note:**

    Even if your Impact Store Application instance is not integrated with Impact Delivery Instance using Service Exchange, you can view the capabilities map with a list of applications, and their entitlement status.

    \[Omitted image "image.capabilities\_withoutservicebridge"\] Alt text: Capabilities map showing applications and entitlement status without Service Bridge connection

    To view the complete capabilities map experience, connect to ServiceNow Impact Delivery Instance. For more information see,

    -   [Service Exchange](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/service-exchange/tmt-service-bridge-both-landing-page.md)
    -   [Use manual registration to establish the connection to the provider instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/connect-instance-impact-store-app.md)
3.  In the **Capabilities** section, you can expand the products lines to view capabilities that are of type application their entitled status, usage status, related accelerators, available notes, and last updated date.

    By default, you can only view entitled and non-hidden capabilities. Adjust the filters to change the view.

    In the **Capabilities** section header, you can view the details of the user who last updated the capabilities map along with the timestamp.

4.  Navigate to a product to view its capabilities.

5.  To view capabilities recommended by your Squad, see the **Squad prioritized** column.

    Squad prioritized capabilities are identified by your Impact squad team as most relevant for your organization based on your entitlements and goals.

    **Note:** To filter by Squad prioritized capabilities, select the \[Omitted image "filter-icon.png"\] Alt text: filter icon filter icon in the **Capabilities** section and then select **Squad Prioritized** from the filter options.

    Without an active Service Exchange integration, the **Squad prioritized** column displays an icon and a message in place of squad recommendations.

6.  To update a capability's usage status, use one of the following methods:

    -   Double-click the **Usage Status** column for the capability.
    -   Select \[Omitted image "ellipsis-horizontal-fill-24.svg"\] Alt text: for the capability and then select **Change Status** from the list.
    The capabilities map reflects your updates to usage status, notes, and visibility settings. Use these updates to track product adoption and plan capability implementation.

    **Note:** Usage status is shown with a \[Omitted image "image.capabilities\_notconnected"\] Alt text: Usage not displayed icon for all applications, and you can manually edit usage status without an active Service Exchange connection.

7.  Select a usage status from the list in the Edit Usage Status Pop-up window.

8.  Select a capability to display the Capability Details Page **About** tab with the **Related Resources**.

9.  To hide the capability from appearing in the default view of the capabilities map, select the check box beside the capability, then select **Hide** button.

    \[Omitted image "hide-capabilities.png"\] Alt text: Hide one or more capabilities if you do not want to view them in the table.

    You can bulk hide capabilities by selecting the check box for multiple capabilities, then select the **Hide** button.

    **Note:** Starting with the Brazil release, capabilities aren’t hidden by default. You can hide or unhide capabilities based on your preferences.

10. To edit capability notes, select the capability to open its details window, then select **Edit** next to the **Capability notes** section under the **About** tab.

    \[Omitted image "capabilities-edit-notes.png"\] Alt text: Add or edit notes related to the capability.

    **Note:** If there are no capability notes, select **Add** to add them.

11. To add a capability manually, select the **Add manual capability** button and enter the required information in the **Add manual capability** window.

12. To view the related accelerators for a capability, select the count of **Related accelerator** column.

    The capability details and its related accelerators are displayed.


