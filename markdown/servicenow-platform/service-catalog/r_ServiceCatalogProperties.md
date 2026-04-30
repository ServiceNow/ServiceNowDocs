---
title: Service Catalog properties
description: The Service Catalog application contains properties used to configure various settings in the application.
locale: en-US
release: yokohama
product: Service Catalog
classification: service-catalog
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 19
breadcrumb: [Service Catalog Reference, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Service Catalog properties

The Service Catalog application contains properties used to configure various settings in the application.

To configure Service Catalog system properties, navigate to **Service Catalog** &gt; **Catalog Administration** &gt; **Properties**. The properties are categorized into the following sections.

-   **Homepage**: Configure settings for the Service Catalog homepage, and control the behavior of the categories and the items displayed on the homepage.
-   **Catalog Items**: Configure settings for catalog items and record producers.
-   **Order Guides** &gt; **General**: Configure settings for the order guide.
-   **Order Guides** &gt; **Scriptable Order Guides**: Configure settings for scriptable order guides.
-   **Cart**: Control the behavior of the shopping cart and checkout screens.
-   **Request Fulfillment**: Configure settings for request fulfillment processes.
-   **Search**: Configure search settings for the Service Catalog homepage.
-   **Security**: Configure security settings for the Service Catalog.
-   **Pricing**: Configure settings for the pricing engine and pricing display.
-   **Portal**: Configure settings for catalog portal widgets.
-   **Virtual Agent**: Configure settings for request submission in Virtual Agent.

    This section is visible only when you activate the Service Management Virtual Agent Topic Blocks  plugin \(com.glideapp.cs.sm\_topic\_blocks\) .

-   **Mobile**: Configure settings for Now Mobile.
-   **Other**: Additional settings for the Service Catalog.

<table id="table_nn5_t4f_qbb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Homepage

</td></tr><tr><td>

Number of Catalog Items/Categories to preview in a section \(**glide.sc.max\_items**\)

</td><td>

Number of catalog items or categories to preview in a section:-   **Type:** integer
-   **Default value:** 5

</td></tr><tr><td>

Show category descriptions in the category view page \(**com.glide.servicecatalog.view\_includes\_category\_descriptions**\)

</td><td>

Show category descriptions in the category view page: -   **Type:** yes \| no
-   **Default value:** yes

</td></tr><tr><td>

In category view display subcategories in a panel \(**glide.sc.use\_sub\_cat\_section**\)

</td><td>

In category view, display subcategories in a panel: -   **Type:** true \| false
-   **Default value:** true

</td></tr><tr><td>

Toggle whether the expand/collapse icon is rendered for category widgets on the service catalog homepage \(**glide.sc.homepage.show.collapse**\)

</td><td>

Toggle whether the expand/collapse icon is rendered for category widgets on the service catalog homepage:-   **Type:** true \| false
-   **Default value:** false

</td></tr><tr><td>

When browsing a category use the pop-up icon to show item details \(**glide.sc.cat\_view\_use\_popup\_for\_details**\)

</td><td>

When browsing for a category or a catalog item, use the info icon next to the category or catalog item to preview category or item details: -   **Type:** true \| false
-   **Default value:** false

</td></tr><tr><td>

Number of catalog items to expand in browsing and search when not using pop-up icons to view details \(**glide.sc.auto\_expand**\)

</td><td>

Number of catalog items to expand in browsing and search when not using pop-up icons to view details: -   **Type:** integer
-   **Default value:** 2

</td></tr><tr><td>

Show the additional categories section when viewing a catalog item \(**glide.sc.show\_additional\_cats**\)

</td><td>

Show the additional categories section when viewing a catalog item: -   **Type:** true \| false
-   **Default value:** true

</td></tr><tr><td>

Limit descriptions in category and item listings to two rows in the Mobile UI \(**glide.sc.mobile.limit.description**\)

</td><td>

Limit descriptions in the category and item listings to two rows in the Classic Mobile UI: -   **Type:** true \| false
-   **Default value:** true

</td></tr><tr><td>

List of content types \(comma-separated\) to allow on the catalog homepage. Blank allows all content types. \(**glide.sc.home.filter**\)

</td><td>

List of content types \(comma-separated\) to allow on the catalog homepage. Blank indicates all content types.

</td></tr><tr><td>

Name of placeholder picture for items that don't have a picture defined \(**glide.sc.placeholder.image**\)

</td><td>

Name of the placeholder picture for items that don't have a picture defined. Applicable only to Classic Mobile and not Desktop.By default, two images are available: **sc\_placeholder\_image.png** and **sc\_placeholder\_image-01.png**. In addition, the default can be replaced with a custom image:

 **Default value:** sc\_placeholder\_image.png

</td></tr><tr><td class="sub-head" colspan="2">

Catalog Items

</td></tr><tr><td>

Specifies the default behavior of record producer after record generation \(**glide.sc.producer.redirect\_url**\)

</td><td>

Default redirect behavior of the record producer after its generation.Possible values:

 -   **Generated Task record**: Redirects to the task record created using the record producer.
-   **Catalog Homepage**: Redirects to the service catalog where the order for the record producer is placed.

 Override this behavior by editing the value of the **Redirect To** field of the record producer or defining the redirect code in the **Script** field of the record producer.

</td></tr><tr><td>

Enabling this makes sure that the attachments uploaded to the attachment variable are deleted from the system if and when they are replaced/deleted on the form \(**glide.sc.variable.attachment.delete.v2**\)

</td><td>

Automatically deletes a sys\_attachment record from the system when you replace or delete an attachment from a catalog item attachment variable.

</td></tr><tr><td>

List of class names for catalog items that can't be added to an existing request \(**glide.sc.item.cannot\_add\_to\_request**\)

</td><td>

List of class names for catalog items that can’t be added to an existing request: -   **Type:** string
-   **Default value:** sc\_cat\_item\_guide, sc\_cat\_item\_producer, sc\_cat\_item\_wizard

</td></tr><tr><td>

List of class names for catalog items that don’t use the default "Try It" UI action \(**glide.sc.item.cannot\_try\_it**\)

</td><td>

List of class names for catalog items that don't use the default "Try It" UI action: -   **Type:** string
-   **Default value:** sc\_cat\_item\_guide, sc\_cat\_item\_producer, sc\_cat\_item\_wizard, sc\_cat\_item\_service

</td></tr><tr><td>

List of class names for catalog items that don’t generate a normal cart item \(**glide.sc.item.not\_normal\_cart\_item**\)

</td><td>

List of class names for catalog items that don't generate a normal cart item:-   **Type:** string
-   **Default value:** sc\_cat\_item\_guide, sc\_cat\_item\_producer, sc\_cat\_item\_wizard

</td></tr><tr><td>

Relationship tables which should be part of 'Copy Item' action. Table Name should be comma-separated \(**glide.sc.item.copy.include\_relationship**\)

</td><td>

Specify the tables in which the records having a reference to a catalog item are also copied when you copy the catalog item using the **Copy** UI action:**Note:** Table names should be comma-separated without any spaces.

</td></tr><tr><td>

Disables clickthrough via the info-icon on a reference variable. Set value to true to enable this functionality \(**glide.sc.variable.reference.clickthrough**\)

</td><td>

Disable clickthrough via the info icon on a reference variable. Set the value to true to enable this functionality.

</td></tr><tr><td class="sub-head" colspan="2">

Order Guides

</td></tr><tr><td class="sub-head" colspan="2">

General

</td></tr><tr><td>

List of class names for catalog items that can’t be included in an order guide \(**glide.sc.item.order\_guide\_exclusion**\)

</td><td>

Comma-separated list of class names for catalog items that can’t be included in an order guide. For example, sc\_cat\_item\_guide and sc\_cat\_item\_content.

</td></tr><tr><td>

Validate mandatory fields when switching tabs in 'Choose Options' section of Order Guides \(**glide.sc.guide.tab.validate**\)

</td><td>

Validate mandatory fields when switching tabs in the **Choose Options** section of order guides: -   **Type:** true \| false
-   **Default value:** true

</td></tr><tr><td>

Render order guide on cart preview and order status page \(**glide.sc.render\_order\_guide\_column**\)

</td><td>

Render the order guide on cart preview and order status page. If an item is part of an order guide, the order guide is listed next to the item. If a user attempts to delete an item belonging to an order guide, a confirmation message appears.

</td></tr><tr><td>

On an order guide, reset cascading or assigned variable values on an item when a user goes back using the "describe needs" button \(**glide.sc.reset\_cascade**\). **Note:** This property is supported in Platform only, not in the portal.

</td><td>

On an order guide, reset cascading variable values on an item when a user navigates by clicking **Describe Needs**.

</td></tr><tr><td>

On an order guide, reset all variables when cascading variables or assigned variable values are reset on an item after a user goes back using the "describe needs" button \(**glide.sc.reset\_cascade\_all**\)**Note:** This property is supported in Platform only, not in the portal.

</td><td>

In an order guide, reset the values of cascading variables and non-cascading values on an item when a user navigates back and forth between the **Described Needs** and **Choose Options** screens. If set to **false**, only the values for the cascading variables are reset.

</td></tr><tr><td class="sub-head" colspan="2">

Scriptable Order Guides

</td></tr><tr><td>

During the processing of a scriptable order guide, create a failure record when the JSON payload is empty \(**glide.sc.sog.empty\_payload**\)

</td><td>

If selected, creates a failure record when the JSON payload is empty during the processing of a scriptable order guide.

</td></tr><tr><td>

During the processing of a scriptable order guide, create a failure record when the order guide is inactive \(**glide.sc.sog.inactive\_order\_guide**\)

</td><td>

If selected, creates a failure record when the order guide is inactive during the processing of a scriptable order guide.

</td></tr><tr><td>

During the processing of a scriptable order guide, create a failure record when the order guide sys\_id is invalid \(**glide.sc.sog.invalid\_order\_guide\_id**\)

</td><td>

If selected, creates a failure record when the order guide sys\_id is invalid during the processing of a scriptable order guide.

</td></tr><tr><td>

During the processing of a scriptable order guide, create a failure record when there is a general JSON parsing error \(**glide.sc.sog.json\_parsing**\)

</td><td>

If selected, creates a failure record when there is a general JSON parsing error during the processing of a scriptable order guide.

</td></tr><tr><td>

During the processing of a scriptable order guide, create a failure record when JSON parameters are missing \(**glide.sc.sog.mandatory\_json\_parameters**\)

</td><td>

If selected, creates a failure record when JSON parameters are missing during the processing of a scriptable order guide.

</td></tr><tr><td class="sub-head" colspan="2">

Cart

</td></tr><tr><td>

Enable cloning requests during checkout. Deprecated by sc\_layout; if sc\_layout is enabled then this property is not used \(**glide.sc.allow.checkout.clone**\)

</td><td>

Enable cloning requests during checkout.**Note:** This property is deprecated when cart layouts are enabled.

</td></tr><tr><td>

List of roles \(comma-separated\) that can use bulk ordering functionality. Blank means all users \(**glide.sc.allow.clone.roles**\)

</td><td>

Roles \(comma-separated\) that can clone requests for other users. Blank value indicates all users can clone requests.

</td></tr><tr><td>

Show the 'Back to Catalog' button on the two-step checkout screen \(**glide.sc.checkout.twostep.back**\)

</td><td>

Show the **Back to Catalog** button on the two-step checkout screen.

</td></tr><tr><td>

Use the two-step catalog checkout model \(default false\) \(**glide.sc.checkout.twostep**\)

</td><td>

Use the two-step catalog checkout model.**Default value:** false

</td></tr><tr><td>

Condition under which users may cancel a request \(previous property must also be true\). For example, current.opened\_by == gs.getUserID\(\) \|\| current.caller\_id == gs.getUserID\(\) \(**glide.sc.checkout.cancel.condition**\)

</td><td>

Condition under which users can cancel a request. Requires **Allow ess users the option to cancel their requests from the checkout screen** to be **True**.

</td></tr><tr><td>

Allow ess users the option to cancel their requests from the checkout screen. In conjunction with sc\_layout feature, if either is set to true the cancel button becomes visible \(**glide.sc.checkout.cancel**\)

</td><td>

Enable Employee Self-Service \(ESS\) portal users the option to cancel their requests from the checkout screen.

</td></tr><tr><td>

Use the two-step checkout model when placing a Catalog Order from a Wizard \(default true\) \(**glide.expert.checkout.twostep**\)

</td><td>

Use the two-step checkout model when placing a catalog order from a wizard:**Default value:** true

</td></tr><tr><td>

List of roles \(comma-separated\) that can update the "Requested for" widget in the service catalog. Blank means all users. If the user doesn't have privileges to change requested for, they will not have ability to get other user address details \(**glide.sc.req\_for.roles**\)

</td><td>

List of users with the roles \(comma-separated\) provided here can request items for other users. If no role is specified, then the default behavior is defined by the **glide.sc.req\_for.roles.default** property. For information about configuring the **glide.sc.req\_for.roles.default** property, see [Configure the default behavior to request items for other users](../task/config-default-behavior-request-other-user.md).Controls access to the **Requested For** widget on the catalog homepage. Users with access to this widget can request items for another person. Users without access can place orders in their own name only.

</td></tr><tr><td>

Ordering of matches for the "request for" service catalog widget. Choose fields in the sys\_user table \(**glide.sc.request\_for.order\_by**\)

</td><td>

Ordering of matches for the "request for" Service Catalog widget. Choose fields in the user `[sys_user]` table.

</td></tr><tr><td>

Show the request item number for each line item on the checkout screen \(default false\). Deprecated by sc\_layout; if sc\_layout is enabled then this property is not used \(**glide.sc.checkout.request.number**\)

</td><td>

Show the request item number for each line item on the checkout screen:**Default value:** false

 **Note:** This property is deprecated when cart layouts are enabled.

</td></tr><tr><td>

Field name to use for the description column of the checkout form. If blank, the default \(short\_description\) is used \(**glide.sc.ess.description**\)

</td><td>

Field name for the description column of the checkout form. If blank, the default is used:**Default value:** short\_description

</td></tr><tr><td>

Additional columns for the "request for" service catalog widget. Choose fields in the sys\_user table. Must be semicolon separated \(**glide.sc.request\_for.columns**\)

</td><td>

Additional columns for the "request for" Service Catalog widget. Choose fields in the user `[sys_user]` table. Must be semicolon separated.

</td></tr><tr><td>

Automatically update the delivery address for catalog carts when the details of a users location changes \(**glide.sc.auto.cart.address.reset**\)

</td><td>

Automatically update the delivery address for catalog carts when the user location details change. If enabled, when changes are made to a user's address, and the user has an active cart, updates the user's address in the cart. If not enabled, the old address is retained in the cart:

 -   **Type:** true \| false
-   **Default value:** false

</td></tr><tr><td>

When determining the address of a user prioritize the details on an associated location record over the details on the user record itself \(**glide.sc.prioritise.user.location**\)

</td><td>

If selected, when determining the address of a user, prioritizes the details on an associated location record over the details on the user record itself.

</td></tr><tr><td>

Determines whether 'Order Now' button exhibits new or old behavior. If this property is true, clicking "Order Now" button in the service catalog, only orders the item currently selected, any items saved in user's shopping cart is left untouched for future ordering. Old 'Order Now' feature is deprecated, 'Order Item' button is deprecated too \(**glide.sc.enable\_order\_now**\)

</td><td>

Determines whether the **Order Now** button exhibits new or old behavior. If this property is **true**, clicking **Order Now** in the service catalog only orders the item currently selected. Any items saved in the shopping cart are left untouched for future ordering. The legacy Order Now feature and the **Order Item** button are deprecated.

</td></tr><tr><td>

List of roles \(comma-separated\) that can use the quantity selector in the shopping cart. Blank means all users \(**glide.sc.allow.quantity**\)

</td><td>

List of roles \(comma-separated\) that can use the quantity selector in the shopping cart. Blank means all users.

</td></tr><tr><td>

Enable removal of inactive catalog items from cart \(**glide.sc.remove\_inactive\_cat\_items\_from\_cart**\)

</td><td>

Enable removal of inactive catalog items from cart. If enabled, automatically removes all deactivated catalog items from the shopping cart. Avoids users ordering items which are placed in the cart while active and are then made inactive:

 -   **Type:** true \| false
-   **Default value:** false

</td></tr><tr><td>

Use the sc\_layout driven cart macros \(default: true\) \(**glide.sc.use\_cart\_layouts**\)

</td><td>

Use the sc\_layout driven cart macros. Activates the new cart layout mechanism, which enables customization of cart and checkout-related widgets and pages without the need to own the UI macros or pages:

 -   **Type:** true \| false
-   **Default value:** true

</td></tr><tr><td>

Show tasks related to requests on the order status page \(the screen you see in the service catalog after a successful order is placed\) \(**glide.sc.checkout.task.display**\)

</td><td>

Show tasks related to requests on the Order Status page, the screen that you see in the service catalog after a successful order is placed.

</td></tr><tr><td>

Round all delivery plans &gt; 1 day to the nearest day \(true\) or display the precise time \(false\) \(**glide.sc.round.delivery.times**\)

</td><td>

Round all delivery plans &gt; 1 day to the nearest day \(true\) or display the precise time \(false\).

</td></tr><tr><td class="sub-head" colspan="2">

Request Fulfillment

</td></tr><tr><td>

Prevent changes to requested item quantity when approved \(except for catalog\_admin users\) \(**glide.sc.restrict.quantity.changes**\)

</td><td>

Prevent changes to the requested item quantity \(except for catalog\_admin users\).

</td></tr><tr><td>

Show the current pending approver's name in the stage widget mouseover \(**glide.sc.approval.hover**\)

</td><td>

Show the current pending approver's name in the stage widget mouseover.

</td></tr><tr><td>

Service catalog tasks approval engine \(**glide.approval\_engine.sc\_task**\)

</td><td>

Service Catalog Tasks approval engine.

</td></tr><tr><td>

Audit changes to service catalog variables \(**glide.sc.audit.variables**\)

</td><td>

Audit changes to Service Catalog variables.

</td></tr><tr><td>

Hide the border and background in variable editor ui \(**glide.sc.hide\_variable\_editor\_background**\)

</td><td>

If selected, hides the border and background in variable editor UI. The default value is false.

</td></tr><tr><td>

Use delivery task name instead of short\_description for the delivery plan summarizer field. Default is false \(uses the short\_description\) \(**glide.sc.delivery\_summary.name**\)

</td><td>

Use the delivery task name instead of the short description for the delivery plan summarizer field:**Default value:** false \(uses the short description\)

</td></tr><tr><td>

Render variables on a request item as they appear on the order panel, followed by the delivery plan variables \(true\), or merge the two based on their order values \(false\) \(**glide.sc.variable.snapshot**\)

</td><td>

Render variables on a request item as they appear on the order panel, followed by the delivery plan variables \(true\), or merge the two based on their order values \(false\).

</td></tr><tr><td>

Service Catalog Requests approval engine \(**glide.approval\_engine.sc\_request**\)

</td><td>

Service Catalog requests approval engine.

</td></tr><tr><td class="sub-head" colspan="2">

Search

</td></tr><tr><td>

List of class names for catalog items that don't have the search field displayed \(**glide.sc.item.cannot\_show\_search**\)

</td><td>

List of class names for catalog items that don’t have the search field displayed: -   **Type:** string
-   **Default value:** sc\_cat\_item\_guide, sc\_cat\_item\_producer, sc\_cat\_item\_wizard

</td></tr><tr><td>

Allow empty service catalog searches \(**glide.sc.search.allow\_empty\_search**\)

</td><td>

If selected, an empty query in the search bar displays all items. This query is performance-heavy.

</td></tr><tr><td>

List of roles \(comma-separated\) that can search the service catalog. Blank means all users \(**glide.sc.can\_search**\)

</td><td>

List of roles \(comma-separated\) that can search the Service Catalog. Blank means all users.

</td></tr><tr><td>

Show breadcrumbs for the categories associated with items when they are displayed in browse and search listings \(**glide.sc.show\_listing\_breadcrumbs**\)

</td><td>

If selected, display breadcrumbs for the categories associated with items when they are displayed in browse and search results.

</td></tr><tr><td>

Service catalog searches return items in inactive categories \(**glide.sc.search.disabled\_cats**\)

</td><td>

Service Catalog searches return items in inactive categories. Search results can include catalog items in non-accessible categories, as specified by the active flag or by security constraints:

 -   **Type:** true \| false
-   **Default value:** true

</td></tr><tr><td>

List of catalog sys\_ids \(comma-separated\) that are excluded from catalog item search \(**glide.sc.search.exclude\_catalogs**\)

</td><td>

List of catalog sys\_ids \(comma-separated\) that are excluded from catalog item search.

</td></tr><tr><td>

Number of service catalog matches returned for global searches \(**glide.sc.search.rowcount**\)

</td><td>

Number of the service catalog matches returned for global searches. Limits the number of results returned by a catalog search to improve search performance.

</td></tr><tr><td>

Specify whether search suggestions should be enabled \(**glide.sc.search.suggestions**\)

</td><td>

Specify whether search suggestions are enabled:-   **Type:** true \| false
-   **Default value:** true

</td></tr><tr><td class="sub-head" colspan="2">

Security

</td></tr><tr><td>

Use "User Criteria" to define access to catalog items and categories \(**glide.sc.use\_user\_criteria**\)

</td><td>

Use user criteria to define access to catalog items and categories. Entitlements are not honored if set to true:-   **Type:** true \| false
-   **Default value:** true

</td></tr><tr><td>

Enable both "User Criteria" and "Entitlement" related lists for catalog items and categories when migrating from entitlements \(**glide.sc.user\_criteria\_migration**\)

</td><td>

Enable User Criteria related lists for catalog items and categories when migrating from entitlements. Set to **true** to display the user criteria related lists without needing to switch to user criteria functionality:

 -   **Type:** true \| false
-   **Default value:** false

</td></tr><tr><td>

List of roles \(comma-separated\) that can override normal entitlement checking inside the catalog. A role of "itil" means that the itil role can order any catalog item, even one protected by entitlement restrictions \(**glide.sc.entitlement.override**\)

</td><td>

List of roles \(comma-separated\) that can override normal entitlement checking inside the catalog. A role of "itil" means that the itil role can order any catalog item, even one protected by entitlement restrictions.

</td></tr><tr><td>

List of roles \(comma-separated\) that override entitlements so that they can view any category within the service catalog \(**glide.sc.category.canview.override**\)

</td><td>

List of roles \(comma-separated\) that override entitlements to enable viewing of any category within the Service Catalog.**Default value:** admin and catalog\_admin

</td></tr><tr><td class="sub-head" colspan="2">

Pricing

</td></tr><tr><td>

Append pricing information to option labels \(**glide.sc.enhance.labels**\)

</td><td>

Append pricing information to option labels. This is also applicable in Service Portal.

</td></tr><tr><td>

List of class names for catalog items that don't show the price in listings \(**glide.sc.item.cannot\_show\_price**\)

</td><td>

List of class names for catalog items that do not show the price in listings.

</td></tr><tr><td>

When to show prices and sub-totals on the service catalog cart \(overrides sc\_layout record settings\) \(**glide.sc.price.display**\)

</td><td>

When to show prices and sub-totals in the service catalog cart.

</td></tr><tr><td>

When set to true then the two script includes CatalogPriceCalculator and CatalogRecurringPriceCalculator are used generate prices \(enabling custom functionality\) \(**glide.sc.use\_custom\_pricegenerator**\)

</td><td>

When set to **true**, the script includes, CatalogPriceCalculator and CatalogRecurringPriceCalculatorare used to generate prices, which enables custom functionality. To use your own price calculation logic, set this property to **Yes**. Then edit the **calcPrice** method inside the **CatalogPriceCalculator** and **CatalogRecurringPriceCalculator** script includes, using your own price calculation algorithm:

 -   **Type:** yes \| no
-   **Default value:** no

</td></tr><tr><td class="sub-head" colspan="2">

Portal

</td></tr><tr><td>

Show order confirmation pop-up in checkout process \(**glide.sc.sp.twostep**\)

</td><td>

If selected, displays the order confirmation window during the two-step checkout process inService Portal.

</td></tr><tr><td>

Use Cart V2 widget in Header Menu widget \(**glide.sc.portal.use\_cart\_v2\_header**\)

</td><td>

If selected, the Cart V2 \(SC Shopping Cart widget \(ID: sc-shopping-cart-v2\)\) widget is enabled in the Header Menu widget of Service Portal.

</td></tr><tr><td class="sub-head" colspan="2">

Virtual AgentThis section is visible only when you activate the Service Management Virtual Agent Topic Blocks  plugin \(com.glideapp.cs.sm\_topic\_blocks\) .

</td></tr><tr><td>

Specifies the upper limit for the number of questions beyond which the item doesn’t support conversational requests, default value of the property is 10 \(**glide.sc.conversational.request.question.limit**\)

</td><td>

Maximum number of questions for a catalog item for it to be eligible for request submission in the conversation mode in Virtual Agent.

</td></tr><tr><td class="sub-head" colspan="2">

Mobile

</td></tr><tr><td>

Catalog category sort option in Now Mobile \(**glide.sc.mobile.category.order\_by**\)

</td><td>

Sort option for categories in Now Mobile.-   Title: Categories are sorted by their title. By default, categories are sorted alphabetically by their title.
-   Order: Categories are sorted by their order.

</td></tr><tr><td>

Include 'Desktop only' Items in Now Mobile \(**glide.sc.mobile.include\_desktop\_only\_items**\)

</td><td>

Option to include the catalog item with **Availability** set to `Desktop only` in Now Mobile.

</td></tr><tr><td>

Catalog item classes not available in Now Mobile \(comma separated list\) \(**glide.sc.mobile.item\_class\_not\_supported**\)

</td><td>

Catalog item types to exclude in Now Mobile. For example, `sc_cat_item_content, sc_cat_item_producer`

</td></tr><tr><td>

Experience for items not available in Now Mobile \(**glide.sc.mobile.unsupported\_discover**\)

</td><td>

Option to define the non-availability behavior of a catalog item. Possible options:-   Discoverable-show message that item is not viewable in Now mobile: Item is discoverable in the search and browse experience but not viewable.
-   Not discoverable-do not show in search and browse experience: Item is neither discoverable in the search and browse experience nor viewable.

 **Note:**

-   If AI Search is enabled for Now Mobile, this property is not applicable.
-   This property is supported only when one of the following properties are applicable:
    -   Include 'Desktop only' Items in NOW Mobile \(**glide.sc.mobile.include\_desktop\_only\_items**\)
    -   Catalog item classes not available in Now Mobile \(comma-separated list\) \(**glide.sc.mobile.item\_class\_not\_supported**\)

</td></tr><tr><td>

Primary color for buttons in the catalog request experience in Now Mobile \(**glide.sc.mobile.primary\_color**\). If Next Experience is turned on, the property will be ignored.

</td><td>

Color for buttons in the catalog request experience.

</td></tr><tr><td class="sub-head" colspan="2">

Other

</td></tr><tr><td>

Log all client-side actions on variable \(**glide.sc.log.variable\_actions**\)

</td><td>

If set to **true**, captures the variable log in the [Variable Action Logger](../task/debug-actions-on-catalog-item-variables.md) window: -   **Type:** true \| false
-   **Default value:** false

</td></tr><tr><td>

Use links for breadcrumbs rendered in service catalog pages accessed via a CMS site \(**glide.sc.use\_breadcrumb\_links.cms**\)

</td><td>

Use links for breadcrumbs rendered in Service Catalog pages accessed via a CMS site. Enables users with the CMS administrator \(content\_admin\) role to choose whether service catalog breadcrumbs are displayed with or without links for greater navigation control:

 -   **Type:** true \| false
-   **Default value:** false

</td></tr><tr><td>

Enable the ui policies related to variable set to be run first \(**glide.sc.ui\_policy.variable\_set\_run\_first**\)

</td><td>

Enable the UI policies related to the variable set to run first.If enabled, UI policies related to the variable set are run first, then the UI policies on items:

-   **Type:** true \| false
-   **Default value:** false

</td></tr><tr><td>

The maximum number of orphan sc\_item\_option records to delete when any sc\_req\_item record is deleted \(**sc\_orphan\_item\_option\_delete\_limit**\)

</td><td>

Maximum number of orphan sc\_item\_option records to delete when any sc\_req\_item record is deleted.

</td></tr></tbody>
</table>**Parent Topic:**[Service Catalog Reference](../concept/service-catalog-reference.md)

