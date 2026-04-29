---
title: Service Portal and client scripts
description: You can use client scripts and catalog client scripts in the Service Portal if the UI Type is set to Mobile / Service Portal or All. Client scripts and catalog client scripts are used with the Form widget and SC Catalog Item widget, as opposed to a widget client controller.
locale: en-US
release: australia
product: Service Portal
classification: service-portal
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Supported features in Service Portal, Exploring Service Portal, Service Portal, Configure UIs and portals, Configure user experiences]
---

# Service Portal and client scripts

You can use client scripts and catalog client scripts in the Service Portal if the UI Type is set to **Mobile / Service Portal** or **All**. Client scripts and catalog client scripts are used with the Form widget and SC Catalog Item widget, as opposed to a widget client controller.

Before flagging a script as **Mobile/Service Portal** or **All**, make sure that you are only using the mobile APIs. Setting a client script to **Mobile** does not ensure that it will work, it simply flags that the script should be attempted by the mobile app or the Service Portal. Many of your existing client scripts can be set to **All** as long as the API calls are supported by the mobile client scripting environment.

The topics in this section require advanced coding knowledge and an understanding of Service Portal APIs.

## Checking desktop vs mobile runtime

You might want to mark a client script compatible with both desktop and mobile, but include behavior that depends on the runtime. You can use this script:

```
  if (window === null)
    // Write your mobile compatible code here
  else
    // Write your desktop compatible code here
```

## Unsupported client scripting globals

The following globals and APIs are unavailable in client scripts and catalog client scripts used in the Service Portal:

-   $
-   $$
-   $j
-   angular
-   control
-   document
-   jQuery
-   window

**Note:** Widget client controllers are full Angular controllers and are not subject to the unsupported client script globals listed here. Use jQuery and Angular as needed.

## Embedded widgets &amp; g\_form

When using the Service Catalog variable type **Macro** and **Macro with Label**, you can pick a widget to embed in a catalog item form. Within the client controller for the embedded widget you can access the field object and catalog item g\_form instance using:

-   `$scope.page.field`
-   `$scope.page.g_form()`

## Client scripts used with Service Portal

The g\_list global helps you set the filter of a Glide list element or a list collector variable. Use this API in place of the g\_filter API on desktop client scripts.

```
function onLoad() {
  var myListCollector = g_list.get("my_list_collector");
  myListCollector.reset();
  myListCollector.setQuery("active=true^category=8c7b22230b402200b0b02c6317673a62");
  myListCollector.addItem('3a700d39af5f4fc0aab978df90f4c692', 'Power Supply');
  myListCollector.addItem('1cb93419a3a248318da8f814140b42f6', 'Backpack');
}
```

g\_service\_catalog is only available in Service Portal service catalog item scripts. Use this API to know if your catalog item script is run as part of an order guide or on its own.

```
function onLoad() {
  if (window) // if CMS, don't run this
   return;

   // g_service_catalog api for Service Portal and Mobile
   var isOrderGuide = g_service_catalog.isOrderGuide();
   g_form.setValue("is_order_guide", isOrderGuide ? "Yes!" : "Nope :(");
}
```

-   **[Supported client script types and APIs](../reference/client-script-reference.md)**  
Some client scripts are not supported in Service Portal. Others must have a UI type set to **All** or **Mobile / Service Portal**. If using a client script in the Service Portal, only client-side APIs supported in a mobile environment can be used.

**Parent Topic:**[Supported features in Service Portal](../reference/unsupported-features-sp.md)

