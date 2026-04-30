---
title: Prefilling variable values on the catalog item form in the portal and Next Experience UIs
description: When catalog item requesters want to order items on portals or Next Experience UI, you can set the catalog items to use the key-value pairs, which prefill the variable values. The requesters can finish forms faster.
locale: en-US
release: zurich
product: Service Catalog
classification: service-catalog
topic_type: concept
last_updated: "2025-08-19"
reading_time_minutes: 3
breadcrumb: [Service catalog variables, Service Catalog Reference, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Prefilling variable values on the catalog item form in the portal and Next Experience UIs

When catalog item requesters want to order items on portals or Next Experience UI, you can set the catalog items to use the key-value pairs, which prefill the variable values. The requesters can finish forms faster.

The values set by this method are applied as if they were user-given values. That means dynamic behaviors \(Catalog UI policies, catalog client scripts, and so on\) work for these values.

This feature is enabled by default. To turn off this feature, you can set the **glide.sc.enable\_url\_prefill** property to false.

## Prefilling forms on portals

You can configure catalog items in portals like Service Portal or Employee Center to prefill forms by modifying the URL.

**Note:** In portals, you can find widget instance option called **Disable URL prefill**. This check box is turned off by default. Select this option to disable URL prefill on that specific portal.

To configure prefill, you can do the following actions:

1.  Use a URL parameter, **sysparm\_variable\_values**, to construct the key-value pairs. In the key-value pair, key is the name of the variable and value is the value of that variable.

    **Note:** The value for a reference variable must be a sys\_id.

2.  Provide the value as a URL parameter of **sysparm\_variable\_values**. For example, if you want to set **Department** as “Sales” and **Business justification** as “employee onboarding”, then use the following URL.

    **/sp?id=sc\_cat\_item&amp;sys\_id=e56a7ffe41011300964ff05369414ebd&amp;sysparm\_variable\_values=\{"business\_justification":"employee onboarding", "department":"221db0edc611228401760aec06c9d929"\}**

3.  To test the URL, you can add the URL in the browser’s address bar and open it.

    You can observe that the **Department** field is prefilled with the value “Sales” and the **Business Justification** field is prefilled with the value as “employee onboarding” on load.

    The following variables aren’t supported for prefill:

    -   Attachment
    -   Custom
    -   Custom with label
    -   Non-input taking variable types such as label, container
    -   Masked
    -   UI page
    -   Multi-row variable set \(MRVS\)
    The order in which these variable values are prefilled is the order in which the variables are defined on the catalog item form.


## Prefilling forms on Next Experience UIs

Configure key-value pairs to prefill catalog item request forms on Next Experience UIs. For the Next Experience UIs, the key-value pairs are sent directly to the component as an input property.

When the catalog item or form is rendered after the user selects the item, these key-value pairs are passed to the component as an object. The component then parses the object and prefills the form accordingly.

To configure the key-value pairs, perform these steps:

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **Experiences**.
2.  Select the UX application for which you want to set prefill values.
3.  Select **Open in UI Builder**.
4.  Open the page with the catalog item that you want to set the prefill values for.
5.  On the catalog item macroponent, use the variableValues property.
6.  Edit the property to add a key-value pair as shown in the following image.![key-value pair example](../image/key-value-pair.png)
7.  After providing the key-value pair, save the item and select **Preview** &gt; **Open URL path**.

## Prefilling forms for inline catalog items in Virtual Agent

You can set prefill values for the inline catalog item form used in Virtual Agent.

To configure prefilling forms for inline catalog items, perform these steps:

1.  Open the topic, for example, Request Catalog Item Inline-seismic.
2.  In the variableValues property, provide the key-value pairs as a stringed JSON object.

There are two ways of configuring this feature. You can provide a stringed JSON object or you can write a script.

In this example, as shown in the image, there are two variables, Department and Business justification. Set the value to true for both the variables. You can specify "Department" as “Sales” and "Business justification" as “employee onboarding”.![Prefilled variable values for inline catalog items in Virtual Agent](../image/script-dept.png)

Once you configure this, when requesters request items, they would see the forms prefilled.

**Parent Topic:**[Service catalog variables](c_ServiceCatalogVariables.md)

