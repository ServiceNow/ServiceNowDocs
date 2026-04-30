---
title: Enable guided tours
description: Enable guided tours for Service Portal pages as well as the standard platform UI.
locale: en-US
release: yokohama
product: Adoption Services
classification: adoption-services
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Configuring Guided Tours, Guided Tours, Adoption services, Configure user experiences]
---

# Enable guided tours

Enable guided tours for Service Portal pages as well as the standard platform UI.

## Before you begin

Role required: admin

## About this task

The Guided Tour Designer was first introduced in the Jakarta release. For new instances that were created in Jakarta and beyond, guided tours are active by default. For instances that originate from pre-Jakarta, guided tours are inactive by default.

With the Yokohama release, you can also enable guided tours to run on Service Portal pages. When you upgrade your instance to Yokohama, the following results occur:

-   For instances that are new in Yokohama, the Guided Tours for Service Portal feature is active by default.
-   For pre-Yokohama instances that you upgrade to Yokohama, the Guided Tours for Service Portal feature is inactive by default.

**Note:** The [Service Portal](../../service-portal/concept/c_ServicePortal.md) application provides a framework that enables you to customize your portal so that your users can access specific platform features in a custom context. You can create a guided tour for a Service Portal page to guide your users through its content step by step.

## Procedure

1.  In the application navigator, enter `sys_properties.list`.

2.  From the System Properties list, find the following properties and set their values to **True**.

    |Property|Description|
    |--------|-----------|
    |com.snc.guided\_tours.standard\_ui.enable|Enables guided tours across your instance to run on the standard platform UI and Workspaces.|
    |com.snc.guided\_tours.sp.enable|Enables guided tours across your instance to run on Service Portal pages. You can create and publish tours for standard UI pages regardless of this property setting.|
    |com.snc.guided\_tours.custom\_ui.enable|Enables guided tours across your instance to run on the Custom UI pages.|


## Result

You can create, update, and play guided tours that reference both standard platform UI elements and tours that reference custom UI elements on a Service Portal page. Your users can play these tours.

## What to do next

Start planning, outlining, and drafting your guided tours. If you are drafting Service Portal guided tours, refer to these items.

<table id="table_mjh_zsr_zdb"><thead><tr><th>

Item

</th><th>

Details

</th></tr></thead><tbody><tr><td>

Guided tour callout steps

</td><td>

Guided tours must be able to recognize every element that they point to so they can locate it after a callout step is created on the element. Therefore, Service Portal page creators must ensure that every custom element they create has a unique name to help validate it as a record in the database. For example, if you create two widgets on a Service Portal page, you must assign them with unique names, such as Widget1 and Widget2.You can customize the elements further by appending additional attributes to the HTML and unique values to their properties. For example, the system currently uses **data-gtd-eid** and **data-id** attributes to identify the elements as unique.

</td></tr><tr><td>

Service Portal pages

</td><td>

In the base system, you can only launch tours from pages that use the SP Header Menu. Manually launched tours do not display on pages with custom header menus.

 If your guided tour is on a Service Portal page that does not use the SP Header Menu, you must configure your tour for auto-launch so the tour is visible to your users. To ensure this type of tour is visible to your users, see [Configure auto-launch for guided tours](auto-launch-guided-tours.md).

 If your Service Portal uses Page Route Maps, tours may not show when expected. For example, your users may not see a tour when expected if the tour is configured for a redirected page. For more information, see [Redirect a reference to a Page ID](../../service-portal/task/reroute-page.md) .

</td></tr><tr><td>

Service Portal branding

</td><td>

When you update the branding for a Service Portal page, the callouts in the guided tour for that page also update accordingly. For example: You update your Service Portal panel background theme color to yellow, and its primary color to red. Result: Your guided tour callout panel background becomes yellow and the callout text field becomes red.

</td></tr></tbody>
</table>|Service Portal guided tour callout colors|
|-----------------------------------------|
|You can customize your guided tour callout colors or use the guided tour defaults.|
|**Parameter**|**Default**|**Custom**|
|Guided tour callouts use the following Service Portal properties:|To set the callout color independently of the Service Portal colors, apply the following CSS variables:|
|**Callout background color**|Panel background color|$gtd-callout-background|
|**Callout text color**|Text color|$gtd-callout-content-color|
|**Callout number color \(Example: 2/5\)**|Text muted|$gtd-callout-number-color|
|**Callout close button \(X\) color**|Text muted|$gtd-callout-close-color|
|**Callout primary button color**|Primary button background color|$gtd-callout-active-color|

**Parent Topic:**[Configuring Guided Tours](../concept/configuring-guided-tours.md)

