---
title: Service Catalog API - ServiceNow Fluent
description: The Service Catalog API defines catalog items \[sc\_cat\_item\], record producers \[sc\_cat\_item\_producer\], and related aspects of service catalogs.Create a catalog item \[sc\_cat\_item\] that users can request from a service catalog.Create a record producer \[sc\_cat\_item\_producer\] for users to create task-based records, such as incident or change request records, from the service catalog.Configure a catalog UI policy \[catalog\_ui\_policy\] to control variable behavior on catalog item forms based on conditions.Configure the variable actions \[catalog\_ui\_policy\_action\] that a catalog UI policy performs on variables when its conditions are met.Configure a catalog client script \[catalog\_script\_client\] that runs on the client side to control the behavior of a catalog item form.Create a variable set \[item\_option\_new\_set\] that groups reusable variables for use across multiple catalog items and record producers.
locale: en-US
release: australia
product: ServiceNow SDK
classification: servicenow-sdk
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 36
keywords: [servicenow fluent, fluent api, servicenow fluent, fluent api, servicenow fluent, fluent api, servicenow fluent, fluent api, servicenow fluent, fluent api, servicenow fluent, fluent api, servicenow fluent, fluent api]
breadcrumb: [ServiceNow Fluent API reference, Reference, ServiceNow SDK, Building applications in source code, Building pro-code applications, Developing your application, Building applications]
---

# Service Catalog API - ServiceNow Fluent

The Service Catalog API defines catalog items \[sc\_cat\_item\], record producers \[sc\_cat\_item\_producer\], and related aspects of service catalogs.

**Note:** For the latest ServiceNow Fluent API documentation and examples, see the [ServiceNow Fluent API reference](https://servicenow.github.io/sdk/) and [ServiceNow SDK examples repository](https://github.com/ServiceNow/sdk-examples) on GitHub.

For general information about service catalogs, see Service Catalog.

**Parent Topic:**[ServiceNow Fluent API reference](servicenow-fluent-api-reference.md)

**Related topics**  


[ServiceNow Fluent](../concept/servicenow-fluent.md)

## CatalogItem object

Create a catalog item \[sc\_cat\_item\] that users can request from a service catalog.

A catalog item must reference a flow, workflow, or execution plan that defines how the item request is fulfilled.

<table id="table_rsp_5rh_33c" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

$id

</td><td>

String or Number

</td><td>

Required. A unique ID for the metadata object. When you build the application, this ID is hashed into a unique sys\_id. For more information, see [ServiceNow Fluent language constructs](fluent-constructs.md).Format: `Now.ID['String' or Number]`

</td></tr><tr><td>

name

</td><td>

String

</td><td>

Required. A name for the item that appears in the catalog.

</td></tr><tr><td>

active

</td><td>

Boolean

</td><td>

Flag that indicates whether the item is active and available to be ordered.Default: true

</td></tr><tr><td>

availability

</td><td>

String

</td><td>

The type of device on which the item displays.Valid values:

-   desktopOnly: The item displays only on desktop devices.
-   mobileOnly: The item displays only on mobile devices.
-   both: The item displays on both desktop and mobile devices.

Default: desktopOnly

</td></tr><tr><td>

checkedOut

</td><td>

Boolean

</td><td>

Flag that indicates whether the item is checked out for editing.Default: false

</td></tr><tr><td>

description

</td><td>

String

</td><td>

A detailed description of the item that displays in the catalog when a user selects the item or the associated **Preview** link.You can embed videos, images, links to internal knowledge base \(KB\) articles, and links to external sources of information and instruction documentation.

</td></tr><tr><td>

meta

</td><td>

Array

</td><td>

A list of metadata tags used to aid in searches related to the item.**Note:** The meta property is used only for Zing text indexing and search engine and not for AI Search.

</td></tr><tr><td>

model

</td><td>

Reference or String

</td><td>

The variable identifier or sys\_id of a product model \[cmdb\_model\] associated with the item. To define a product model, use the [Record API - ServiceNow Fluent](record-api-now-ts.md#).

</td></tr><tr><td>

order

</td><td>

Number

</td><td>

The order in which the item appears within its category.Default: 0

</td></tr><tr><td>

owner

</td><td>

Reference or String

</td><td>

The variable identifier or sys\_id of a user \[sys\_user\] who owns the item and has edit access to it​. To define a user, use the [Record API - ServiceNow Fluent](record-api-now-ts.md#).

</td></tr><tr><td>

roles

</td><td>

Array

</td><td>

A list of variable identifiers of Role objects or sys\_ids of roles \[sys\_user\_role\] that can access the item.​ For more information, see [Role API - ServiceNow Fluent](role-api-now-ts.md#).

</td></tr><tr><td>

shortDescription

</td><td>

String

</td><td>

A short description of the item that appears on the catalog home page, search results, and the title bar of the order form.

</td></tr><tr><td>

showVariableHelpOnLoad

</td><td>

Boolean

</td><td>

Flag that indicates whether the item displays variable help text by default.Default: false

</td></tr><tr><td>

startClosed

</td><td>

Boolean

</td><td>

Flag that indicates whether to start the item in a collapsed state.Default: false

</td></tr><tr><td>

state

</td><td>

String

</td><td>

The publication state of the item, such as draft or published.

</td></tr><tr><td>

variables

</td><td>

Object

</td><td>

The variable definitions for the item that provide options for requesting it. Each variable type has a specific function. For example:```javascript
variables: {
    laptopType: SelectBoxVariable({
      question: "Laptop Type",
      choices: {
        standard: { label: "Standard Laptop", sequence: 1 },
        developer: { label: "Developer Workstation", sequence: 2 }
      },
      mandatory: true,
      order: 100
    }),
    justification: MultiLineTextVariable({
      question: "Business Justification",
      mandatory: true,
      order: 200
    })
}
```

For general information about catalog variables, see Service catalog variables.

</td></tr><tr><td>

version

</td><td>

Number

</td><td>

A version of the item.Default: 1

</td></tr><tr><td>

image

</td><td>

String

</td><td>

Deprecated. An image for the item.

</td></tr><tr><td>

icon

</td><td>

String

</td><td>

An image file that displays as an icon beside the item name in the catalog.Use a 27x27 pixel image. If no image is uploaded, the default icon appears.

</td></tr><tr><td>

picture

</td><td>

String

</td><td>

An image file to display as a picture of the item.

</td></tr><tr><td>

mobilePicture

</td><td>

String

</td><td>

An image to display as a picture of the item on mobile devices.This property applies only if the value of the mobilePictureType is `mobilePicture`.

</td></tr><tr><td>

mobilePictureType

</td><td>

String

</td><td>

The type of picture to display for the item on mobile devices.Valid values:

-   desktopPicture: Use the image from the picture property.
-   mobilePicture: Use the image from the mobilePicture property.
-   noPicture: The item doesn't display a picture on mobile devices.

Default: desktopPicture

</td></tr><tr><td>

hideAddToCart

</td><td>

Boolean

</td><td>

Flag that indicates whether to hide the **Add to Cart** button.Default: false

</td></tr><tr><td>

hideAddToWishList

</td><td>

Boolean

</td><td>

Flag that indicates whether to hide the **Add to Wishlist** button.Default: false

</td></tr><tr><td>

hideDeliveryTime

</td><td>

Boolean

</td><td>

Flag that indicates whether to hide the delivery time.Default: false

</td></tr><tr><td>

hideQuantitySelector

</td><td>

Boolean

</td><td>

Flag that indicates whether to hide the **Quantity** field.Default: false

</td></tr><tr><td>

hideSaveAsDraft

</td><td>

Boolean

</td><td>

Flag that indicates whether to hide the **Save as Draft** button.Default: false

</td></tr><tr><td>

hideSP

</td><td>

Boolean

</td><td>

Flag that indicates whether to hide an item on Service Portal.Default: false

</td></tr><tr><td>

mandatoryAttachment

</td><td>

Boolean

</td><td>

Flag that indicates whether to require adding an attachment to submit a request.Default: false

</td></tr><tr><td>

hideAttachment

</td><td>

Boolean

</td><td>

Flag that indicates whether to hide the attachment section and not support adding attachments.Default: false

</td></tr><tr><td>

assignedTopics

</td><td>

Array

</td><td>

A list of sys\_ids of existing taxonomy topics that control the visibility of the item in the Employee Center portal. For more information, see Associate a catalog item with a taxonomy topic in Employee Center.**Note:** This property is available only when the Employee Experience Taxonomy plugin \(sn\_ect\) is active.

</td></tr><tr><td>

availableFor

</td><td>

Array

</td><td>

A list of sys\_ids of user criteria \[user\_criteria\] that define who can access the item.

</td></tr><tr><td>

notAvailableFor

</td><td>

Array

</td><td>

A list of sys\_ids of user criteria \[user\_criteria\] that define who can't access the item.This property overrides the availableFor property.

</td></tr><tr><td>

variableSets

</td><td>

Array

</td><td>

A list of variable identifiers of VariableSet objects or sys\_ids of variable sets \[item\_option\_new\_set\] to attach to the item. For more information, see [VariableSet object](fluent-service-catalog-api.md#).Format: `{ variableSet, order }`

</td></tr><tr><td>

flow

</td><td>

Reference or String

</td><td>

The variable identifier of a Flow object or sys\_id of a flow \[sys\_hub\_flow\] that defines how the request is fulfilled. To define a flow, use the [Flow API - ServiceNow Fluent](fluent-flow-api.md#).**Note:** You should use flows as the fulfillment method for catalog items. When flow, workflow, and executionPlan are all specified, the system uses the flow.

</td></tr><tr><td>

executionPlan

</td><td>

Reference or String

</td><td>

The variable identifier or sys\_id of an execution plan \[sc\_cat\_item\_delivery\_plan\] that defines how the request is fulfilled. To define an execution plan, use the [Record API - ServiceNow Fluent](record-api-now-ts.md#).

</td></tr><tr><td>

workflow

</td><td>

String

</td><td>

The sys\_id of a legacy workflow \[wf\_workflow\] that defines how the item request is fulfilled. Use the flow property for new implementations.

</td></tr><tr><td>

accessType

</td><td>

String

</td><td>

The user access required to request the item.Valid values:

-   restricted: Only users who have access to the item can request the item.
-   delegated: Users who don't have access to the item can request the item on behalf of someone else using the delegated request experience. For more information, see Delegated request experience.

**Note:** This functionality is only applicable when the item has a Requested For variable.

Default: restricted

</td></tr><tr><td>

location

</td><td>

Reference or String

</td><td>

The variable identifier or sys\_id of a location \[cmn\_location\] where the item is provided. To define a location, use the [Record API - ServiceNow Fluent](record-api-now-ts.md#).

</td></tr><tr><td>

vendor

</td><td>

Reference or String

</td><td>

The variable identifier or sys\_id of a vendor associated with the item. To define a vendor, use the [Record API - ServiceNow Fluent](record-api-now-ts.md#).

</td></tr><tr><td>

deliveryPlanScript

</td><td>

Script

</td><td>

Deprecated. Use the executionPlan property instead.

</td></tr><tr><td>

deliveryTime

</td><td>

Object

</td><td>

The estimated time to deliver the item.Format: `deliveryTime: { days: Number, hours: Number })`

</td></tr><tr><td>

entitlementScript

</td><td>

Script

</td><td>

A script that defines entitlement for the item.

</td></tr><tr><td>

makeItemNonConversational

</td><td>

Boolean

</td><td>

Flag that indicates whether to prevent the ability to request the item from a conversational experience such as Virtual Agent. If true, the item can be requested from a conversational experience.Default: false

</td></tr><tr><td>

visibleBundle

</td><td>

Boolean

</td><td>

Flag that indicates whether item is visible in saved bundles.Default: true

</td></tr><tr><td>

visibleGuide

</td><td>

Boolean

</td><td>

Flag that indicates whether item is visible in order guides.Default: true

</td></tr><tr><td>

visibleStandalone

</td><td>

Boolean

</td><td>

Flag that indicates whether the standalone view is visible.Default: true

</td></tr><tr><td>

fulfillmentAutomationLevel

</td><td>

String

</td><td>

The level of fulfillment automation for requests.Valid values:

-   unspecified: Automation level of item isn’t specified.
-   manual: Catalog item isn’t automated.
-   semiAutomated: Catalog item is semi-automated.
-   fullyAutomated: Catalog item is automated completely.

</td></tr><tr><td>

fulfillmentGroup

</td><td>

Reference or String

</td><td>

The variable identifier or sys\_id of the group \[sys\_user\_group\] responsible for delivering the item. To define a user group, use the [Record API - ServiceNow Fluent](record-api-now-ts.md#).

</td></tr><tr><td>

catalogs

</td><td>

Array

</td><td>

A list of sys\_ids of the catalogs \[sc\_catalog\] in which the item appears.

</td></tr><tr><td>

categories

</td><td>

Array

</td><td>

A list of sys\_ids of the categories \[sc\_category\] to which the item belongs. A catalog must be specified in the catalogs property before categories can be assigned.In the Service Portal, catalog searches find only items that are assigned to a category. In Employee Center, catalog searches find only items that are associated with a taxonomy topic. For more information, see Associate a catalog item with a taxonomy topic in Employee Center.

</td></tr><tr><td>

cost

</td><td>

Number

</td><td>

A number indicating the one-time cost of the item.Default: 0

</td></tr><tr><td>

displayPriceProperty

</td><td>

String

</td><td>

The system property that controls how the item price is displayed.

</td></tr><tr><td>

ignorePrice

</td><td>

Boolean

</td><td>

Flag that indicates whether to hide the item price in the cart and in the catalog listing.Default: true

</td></tr><tr><td>

mobileHidePrice

</td><td>

Boolean

</td><td>

Flag that indicates whether to hide the item price on mobile devices.Default: false

</td></tr><tr><td>

omitPrice

</td><td>

Boolean

</td><td>

Flag that indicates whether to omit the price entirely from all views of the item.Default: false

</td></tr><tr><td>

billable

</td><td>

Boolean

</td><td>

Flag that indicates whether the item is billable.Default: false

</td></tr><tr><td>

pricingDetails

</td><td>

Array

</td><td>

A list of pricing entries for the item. Valid values:

-   price: A one-time price for the item.
-   recurring\_price: A price that recurs at a regular interval. When using this value, the recurringFrequency property is required.

Format: `{ amount, currencyType, field }`

</td></tr><tr><td>

recurringFrequency

</td><td>

String

</td><td>

The time interval at which the recurring price repeats, such as monthly or yearly.This property is required when pricingDetails contains a `recurring_price` field entry.

</td></tr><tr><td>

requestMethod

</td><td>

String

</td><td>

The label for the submission button and the order submission experience.Valid values:

-   order: Displays an **Order Now** button. A confirmation dialog is shown and delivery information is editable.
-   request: Displays a **Request** button. A confirmation dialog is shown but delivery information isn’t displayed. Use for scenarios where delivery information is pre-determined, such as a code access request.
-   submit: Displays a **Submit** button. No confirmation dialog or delivery information is displayed. Use for scenarios where no further request information is required, such as a password reset.

Default: order

</td></tr><tr><td>

customCart

</td><td>

Reference or String

</td><td>

The variable identifier or sys\_id of a custom UI macro to use for cart rendering. To define a custom cart, use the [Record API - ServiceNow Fluent](record-api-now-ts.md#).

</td></tr><tr><td>

useScLayout

</td><td>

Boolean

</td><td>

Flag that indicates whether the item uses the Service Catalog layout for display.Default: true

</td></tr><tr><td>

noCart

</td><td>

Boolean

</td><td>

Deprecated. Flag that indicates whether to hide the shopping cart.Default: false

</td></tr><tr><td>

noOrder

</td><td>

Boolean

</td><td>

Deprecated. Flag that indicates whether to hide the **Order** option.Default: false

</td></tr><tr><td>

noOrderNow

</td><td>

Boolean

</td><td>

Deprecated. Flag that indicates whether to hide the **Order Now** option.Default: false

</td></tr><tr><td>

noProceedCheckout

</td><td>

Boolean

</td><td>

Deprecated. Flag that indicates whether to hide the checkout process.Default: false

</td></tr><tr><td>

noQuantity

</td><td>

Boolean

</td><td>

Deprecated. Flag that indicates whether to hide the **Quantity** field.Default: false

</td></tr><tr><td>

noSearch

</td><td>

Boolean

</td><td>

Deprecated. Flag that indicates whether to hide search.Default: false

</td></tr><tr><td>

$meta

</td><td>

Object

</td><td>

Metadata for the application metadata.With the installMethod property, you can map the application metadata to an output directory that loads only in specific circumstances.

```javascript
$meta: {
      installMethod: 'String'
}
```

Valid values for installMethod:

-   demo: Outputs the application metadata to the `metadata/unload.demo` directory to be installed with the application when the **Load demo data** option is selected.
-   first install: Outputs the application metadata to the `metadata/unload` directory to be installed only the first time an application is installed on an instance.

</td></tr></tbody>
</table>```javascript
import { CatalogItem } from "@servicenow/sdk/core";

export const softwareLicenseRequest = CatalogItem({
  $id: Now.ID["software_license_request"],
  name: "Software License Request",
  shortDescription: "Request a software license",

  catalogs: [serviceCatalog],
  categories: [softwareCategory],

  // Attach reusable variable sets
  variableSets: [
    { variableSet: contactInfoSet, order: 100 },
    { variableSet: approvalInfoSet, order: 200 }
  ],

  // Item-specific variables
  variables: {
    software_name: SingleLineTextVariable({
      question: "Software Name",
      mandatory: true,
      order: 100
    }),
    license_type: SelectBoxVariable({
      question: "License Type",
      choices: {
        individual: { label: "Individual", sequence: 1 },
        team: { label: "Team (5 seats)", sequence: 2 },
        enterprise: { label: "Enterprise (unlimited)", sequence: 3 }
      },
      mandatory: true,
      order: 200
    }),
    number_of_licenses: SingleLineTextVariable({
      question: "Number of Licenses",
      defaultValue: "1",
      order: 300
    }),
    justification: MultiLineTextVariable({
      question: "Business Justification",
      mandatory: true,
      order: 400
    })
  },

  // Pricing with recurring charges
  pricingDetails: [
    { amount: 0, currencyType: "USD", field: "price" },
    { amount: 99, currencyType: "USD", field: "recurring_price" }
  ],
  recurringFrequency: "monthly",

  flow: "523da512c611228900811a37c97c2014",
  deliveryTime: { days: 3, hours: 0 }
})
```

## CatalogItemRecordProducer object

Create a record producer \[sc\_cat\_item\_producer\] for users to create task-based records, such as incident or change request records, from the service catalog.

You can create a record producer for tables and database views that are in the same scope as the record producer. You can also create a record producer for tables that allow create access from applications in other scopes.

<table id="table_rsp_5rh_33c" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

$id

</td><td>

String or Number

</td><td>

Required. A unique ID for the metadata object. When you build the application, this ID is hashed into a unique sys\_id. For more information, see [ServiceNow Fluent language constructs](fluent-constructs.md).Format: `Now.ID['String' or Number]`

</td></tr><tr><td>

table

</td><td>

Reference or String

</td><td>

Required. The variable identifier of a Table object or name of a table in which the record producer creates records, such as incident or change\_request.

</td></tr><tr><td>

name

</td><td>

String

</td><td>

Required. A name for the item that appears in the catalog.

</td></tr><tr><td>

active

</td><td>

Boolean

</td><td>

Flag that indicates whether the item is active and available to be ordered.Default: true

</td></tr><tr><td>

availability

</td><td>

String

</td><td>

The type of device on which the item displays.Valid values:

-   desktopOnly: The item displays only on desktop devices.
-   mobileOnly: The item displays only on mobile devices.
-   both: The item displays on both desktop and mobile devices.

Default: desktopOnly

</td></tr><tr><td>

checkedOut

</td><td>

Boolean

</td><td>

Flag that indicates whether the item is checked out for editing.Default: false

</td></tr><tr><td>

description

</td><td>

String

</td><td>

A detailed description of the item that displays in the catalog when a user selects the item or the associated **Preview** link.You can embed videos, images, links to internal knowledge base \(KB\) articles, and links to external sources of information and instruction documentation.

</td></tr><tr><td>

meta

</td><td>

Array

</td><td>

A list of metadata tags used to aid in searches related to the item.**Note:** The meta property is used only for Zing text indexing and search engine and not for AI Search.

</td></tr><tr><td>

model

</td><td>

Reference or String

</td><td>

The variable identifier or sys\_id of a product model \[cmdb\_model\] associated with the item. To define a product model, use the [Record API - ServiceNow Fluent](record-api-now-ts.md#).

</td></tr><tr><td>

order

</td><td>

Number

</td><td>

The order in which the item appears within its category.Default: 0

</td></tr><tr><td>

owner

</td><td>

Reference or String

</td><td>

The variable identifier or sys\_id of a user \[sys\_user\] who owns the item and has edit access to it​. To define a user, use the [Record API - ServiceNow Fluent](record-api-now-ts.md#).

</td></tr><tr><td>

roles

</td><td>

Array

</td><td>

A list of variable identifiers of Role objects or sys\_ids of roles \[sys\_user\_role\] that can access the item.​ For more information, see [Role API - ServiceNow Fluent](role-api-now-ts.md#).

</td></tr><tr><td>

shortDescription

</td><td>

String

</td><td>

A short description of the item that appears on the catalog home page, search results, and the title bar of the order form.

</td></tr><tr><td>

showVariableHelpOnLoad

</td><td>

Boolean

</td><td>

Flag that indicates whether the item displays variable help text by default.Default: false

</td></tr><tr><td>

startClosed

</td><td>

Boolean

</td><td>

Flag that indicates whether to start the item in a collapsed state.Default: false

</td></tr><tr><td>

state

</td><td>

String

</td><td>

The publication state of the item, such as draft or published.

</td></tr><tr><td>

variables

</td><td>

Object

</td><td>

The variable definitions for the item that provide options for requesting it. Each variable type has a specific function. For example:```javascript
variables: {
    laptopType: SelectBoxVariable({
      question: "Laptop Type",
      choices: {
        standard: { label: "Standard Laptop", sequence: 1 },
        developer: { label: "Developer Workstation", sequence: 2 }
      },
      mandatory: true,
      order: 100
    }),
    justification: MultiLineTextVariable({
      question: "Business Justification",
      mandatory: true,
      order: 200
    })
}
```

For general information about catalog variables, see Service catalog variables.

</td></tr><tr><td>

version

</td><td>

Number

</td><td>

A version of the item.Default: 1

</td></tr><tr><td>

view

</td><td>

Reference or String

</td><td>

Required. The variable identifier or name of the UI view \[sys\_ui\_view\] which applies, or the default view. To define a UI view, use the [Record API - ServiceNow Fluent](record-api-now-ts.md#).To use the default view \(`default_view`\), you must import it:

```javascript
import { default_view } from '@servicenow/sdk/core'
```

</td></tr><tr><td>

icon

</td><td>

String

</td><td>

An image file that displays as an icon beside the item name in the catalog.Use a 27x27 pixel image. If no image is uploaded, the default icon appears.

</td></tr><tr><td>

picture

</td><td>

String

</td><td>

An image file to display as a picture of the item.

</td></tr><tr><td>

mobilePicture

</td><td>

String

</td><td>

An image to display as a picture of the item on mobile devices.This property applies only if the value of the mobilePictureType is `mobilePicture`.

</td></tr><tr><td>

mobilePictureType

</td><td>

String

</td><td>

The type of picture to display for the item on mobile devices.Valid values:

-   desktopPicture: Use the image from the picture property.
-   mobilePicture: Use the image from the mobilePicture property.
-   noPicture: The item doesn't display a picture on mobile devices.

Default: desktopPicture

</td></tr><tr><td>

assignedTopics

</td><td>

Array

</td><td>

A list of sys\_ids of existing taxonomy topics that control the visibility of the item in the Employee Center portal. For more information, see Associate a catalog item with a taxonomy topic in Employee Center.**Note:** This property is available only when the Employee Experience Taxonomy plugin \(sn\_ect\) is active.

</td></tr><tr><td>

availableFor

</td><td>

Array

</td><td>

A list of sys\_ids of user criteria \[user\_criteria\] that define who can access the item.

</td></tr><tr><td>

notAvailableFor

</td><td>

Array

</td><td>

A list of sys\_ids of user criteria \[user\_criteria\] that define who can't access the item.This property overrides the availableFor property.

</td></tr><tr><td>

variableSets

</td><td>

Array

</td><td>

A list of variable identifiers of VariableSet objects or sys\_ids of variable sets \[item\_option\_new\_set\] to attach to the item. For more information, see [VariableSet object](fluent-service-catalog-api.md#).Format: `{ variableSet, order }`

</td></tr><tr><td>

hideAddToCart

</td><td>

Boolean

</td><td>

Flag that indicates whether to hide the **Add to Cart** button.Default: false

</td></tr><tr><td>

hideAddToWishList

</td><td>

Boolean

</td><td>

Flag that indicates whether to hide the **Add to Wishlist** button.Default: false

</td></tr><tr><td>

hideDeliveryTime

</td><td>

Boolean

</td><td>

Flag that indicates whether to hide the delivery time.Default: false

</td></tr><tr><td>

hideQuantitySelector

</td><td>

Boolean

</td><td>

Flag that indicates whether to hide the **Quantity** field.Default: false

</td></tr><tr><td>

hideSaveAsDraft

</td><td>

Boolean

</td><td>

Flag that indicates whether to hide the **Save as Draft** button.Default: false

</td></tr><tr><td>

hideSP

</td><td>

Boolean

</td><td>

Flag that indicates whether to hide an item on Service Portal.Default: false

</td></tr><tr><td>

mandatoryAttachment

</td><td>

Boolean

</td><td>

Flag that indicates whether to require adding an attachment to submit a request.Default: false

</td></tr><tr><td>

hideAttachment

</td><td>

Boolean

</td><td>

Flag that indicates whether to hide the attachment section and not support adding attachments.Default: false

</td></tr><tr><td>

allowEdit

</td><td>

Boolean

</td><td>

Flag that indicates whether users can edit the created record after submission.Default: false

</td></tr><tr><td>

canCancel

</td><td>

Boolean

</td><td>

Flag that indicates whether to display a Cancel button on the record producer form. Users can select Cancel to cancel the record producer and return to the last-viewed screen.Default: false

</td></tr><tr><td>

postInsertScript

</td><td>

Script

</td><td>

A server-side script that runs after the record is inserted in the associated table. You can call `current.update()` in this script.**Note:** This script overrides the target record values and record producer template values.

This property supports inline JavaScript or a reference to another file in the application that contains a script.

Format:

-   To use text content from another file, refer to a file in the application using the following format: `Now.include('path/to/file')`. For more information, see [ServiceNow Fluent language constructs](fluent-constructs.md).
-   To provide an inline script, use string literals or template literals for multiple lines of code: `'Script' or `Script``.

Default:

```javascript
/**
* This script is executed after the record is generated. 
* `current` Is the GlideRecord produced by Record Producer. Use `current.update()` to update the record
* To access the variables, use `producer.var1` where var1 is the name of the variable
* To access the Record Producer use `cat_item`
*/
```

</td></tr><tr><td>

redirectUrl

</td><td>

String

</td><td>

The redirect destination after the record is generated.Valid values:

-   generatedRecord: Redirects to the task record created by the record producer.
-   catalogHomePage: Redirects to the service catalog.

Default: generatedRecord

</td></tr><tr><td>

saveOptions

</td><td>

String

</td><td>

Advanced configuration options for saving the record producer.

</td></tr><tr><td>

saveScript

</td><td>

Script

</td><td>

A script that runs at every step save in Catalog Builder. This property supports inline JavaScript or a reference to another file in the application that contains a script.Format:

-   To use text content from another file, refer to a file in the application using the following format: `Now.include('path/to/file')`. For more information, see [ServiceNow Fluent language constructs](fluent-constructs.md).
-   To provide an inline script, use string literals or template literals for multiple lines of code: `'Script' or `Script``.

Default:

```javascript
/**
* This script is executed at every step save in Catalog Builder. 
* This script is executed before `Script` is executed.
* `current` Is the GlideRecord produced by Record Producer. 
* To access the variables, use `producer.var1` where var1 is the name of the variable
* To access the Record Producer use `cat_item`
*/
```

</td></tr><tr><td>

script

</td><td>

Script

</td><td>

A server-side script that runs before the record is created. Use this script to assign values to fields on the record dynamically. Don't call `current.update()` or `current.insert()` in this script.This property supports inline JavaScript or a reference to another file in the application that contains a script.

Format:

-   To use text content from another file, refer to a file in the application using the following format: `Now.include('path/to/file')`. For more information, see [ServiceNow Fluent language constructs](fluent-constructs.md).
-   To provide an inline script, use string literals or template literals for multiple lines of code: `'Script' or `Script``.

Default:

```javascript
/** This script is executed before the Record is generated
* `current`- GlideRecord produced by Record Producer
* Don't use `current.update()` or `current.insert()` as the record is generated by Record Producer
* Don't use `current.setValue('sys_class_name', 'xxx')` as this will trigger reparent flow and can cause data loss
* Avoid `current.setAbortAction()` and generate a separate record
* Use `producer.var1` to access variables
*/
```

</td></tr><tr><td>

image

</td><td>

String

</td><td>

Deprecated. An image for the item.

</td></tr><tr><td>

$meta

</td><td>

Object

</td><td>

Metadata for the application metadata.With the installMethod property, you can map the application metadata to an output directory that loads only in specific circumstances.

```javascript
$meta: {
      installMethod: 'String'
}
```

Valid values for installMethod:

-   demo: Outputs the application metadata to the `metadata/unload.demo` directory to be installed with the application when the **Load demo data** option is selected.
-   first install: Outputs the application metadata to the `metadata/unload` directory to be installed only the first time an application is installed on an instance.

</td></tr></tbody>
</table>```javascript
import { CatalogItemRecordProducer } from "@servicenow/sdk/core";

const serviceCatalog = "e0d08b13c3330100c8b837659bba8fb4";
const itServicesCategory = "d258b953c611227a0146101fb1be7c31";

export const comprehensiveIncidentProducer = CatalogItemRecordProducer({
  $id: Now.ID["comprehensive_incident_producer"],
  name: "Report Incident with Full Configuration",
  shortDescription: "Complete incident producer with variables and scripts",
  table: "incident",

  catalogs: [serviceCatalog],
  categories: [itServicesCategory],

  variables: {
    short_description: SingleLineTextVariable({
      question: "Brief Summary",
      mandatory: true,
      mapToField: true,
      field: "short_description",
      order: 100
    }),
    urgency: SelectBoxVariable({
      question: "Urgency",
      mandatory: true,
      mapToField: true,
      field: "urgency",
      choices: {
        "1": { label: "High", sequence: 1 },
        "2": { label: "Medium", sequence: 2 },
        "3": { label: "Low", sequence: 3 }
      },
      order: 200
    }),
    assignment_group: ReferenceVariable({
      question: "Assignment Group",
      mapToField: true,
      field: "assignment_group",
      referenceTable: "sys_user_group",
      order: 300
    })
  },

  script: Now.include("../../scripts/rp-pre-insert.js"),
  postInsertScript: Now.include("../../scripts/rp-post-insert.js"),

  redirectUrl: "generatedRecord",
  view: "ess",
  allowEdit: true
})
```

## CatalogUiPolicy object

Configure a catalog UI policy \[catalog\_ui\_policy\] to control variable behavior on catalog item forms based on conditions.

Catalog UI policies can make variables mandatory, read-only, visible, or hidden when specified conditions are met. For validation, calculations, or asynchronous calls, use catalog client scripts instead.

<table id="table_rsp_5rh_33c" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

$id

</td><td>

String or Number

</td><td>

Required. A unique ID for the metadata object. When you build the application, this ID is hashed into a unique sys\_id. For more information, see [ServiceNow Fluent language constructs](fluent-constructs.md).Format: `Now.ID['String' or Number]`

</td></tr><tr><td>

shortDescription

</td><td>

String

</td><td>

Required. A short description of what the catalog UI policy does.

</td></tr><tr><td>

catalogItem

</td><td>

Reference or String

</td><td>

Required only if the variableSet property isn’t used. The variable identifier of a CatalogItem or CatalogItemRecordProducer object or sys\_id of the catalog item \[sc\_cat\_item\] or record producer \[sc\_cat\_item\_producer\] to which the UI policy applies. For more information, see [CatalogItem object](fluent-service-catalog-api.md#) or [CatalogItemRecordProducer object](fluent-service-catalog-api.md#).

</td></tr><tr><td>

variableSet

</td><td>

Reference or String

</td><td>

Required only if the catalogItem property isn’t used. The variable identifier of a VariableSet object or sys\_id of the variable set \[item\_option\_new\_set\] to which the UI policy applies. For more information, see [VariableSet object](fluent-service-catalog-api.md#).

</td></tr><tr><td>

appliesTo

</td><td>

String

</td><td>

The scope to which the UI policy applies.Valid values:

-   item: The policy applies to a catalog item.
-   set: The policy applies to a variable set.

Default: item

</td></tr><tr><td>

active

</td><td>

Boolean

</td><td>

Flag that indicates whether the catalog UI policy is active.Default: true

</td></tr><tr><td>

global

</td><td>

Boolean

</td><td>

Flag that indicates on which views of the table the Catalog UI Policy runs.Default: true

</td></tr><tr><td>

onLoad

</td><td>

Boolean

</td><td>

Flag that indicates whether the catalog UI policy runs when the form loads. If false, the policy applies only when variable values change.Default: true

</td></tr><tr><td>

reverseIfFalse

</td><td>

Boolean

</td><td>

Flag that indicates whether to reverse the UI policy actions when the catalog condition evaluates to false.Default: true

</td></tr><tr><td>

inherit

</td><td>

Boolean

</td><td>

Flag that indicates whether the Catalog UI Policy is inherited.Default: false

</td></tr><tr><td>

isolateScript

</td><td>

Boolean

</td><td>

Flag that indicates whether the policy scripts run in an isolated scope.Default: true

</td></tr><tr><td>

catalogCondition

</td><td>

String

</td><td>

The encoded query conditions based on catalog item variable values that trigger the UI policy. For example:```javascript
catalogCondition: `${catalogItem.variables.singleLineText}=catalogitem^${catalogItem.variables.reference}ISNOTEMPTY^EQ`
```

</td></tr><tr><td>

appliesOnCatalogItemView

</td><td>

Boolean

</td><td>

Flag that indicates whether the UI policy applies to catalog items displayed in the order screen. This view is available to requesters.Default: true

</td></tr><tr><td>

appliesOnTargetRecord

</td><td>

Boolean

</td><td>

Flag that indicates whether the UI policy applies to records created for task-extended tables via record producers.Default: false

</td></tr><tr><td>

appliesOnCatalogTasks

</td><td>

Boolean

</td><td>

Flag that indicates whether the UI policy applies to catalog task forms. This view is available to fulfillers.Default: false

</td></tr><tr><td>

appliesOnRequestedItems

</td><td>

Boolean

</td><td>

Flag that indicates whether the UI policy applies to requested item forms. This view is available to fulfillers.Default: false

</td></tr><tr><td>

runScripts

</td><td>

Boolean

</td><td>

Flag that indicates whether to run the executeIfTrue and executeIfFalse scripts for this UI policy. Use scripts to apply behaviors beyond read-only, mandatory, or visible, such as targeting a specific role.Default: false

</td></tr><tr><td>

executeIfTrue

</td><td>

String

</td><td>

A client-side script that runs when the catalog condition evaluates to true. The script must be wrapped in a `function onCondition() {}` function.

</td></tr><tr><td>

executeIfFalse

</td><td>

String

</td><td>

A client-side script that runs when the catalog condition evaluates to false. The script must be wrapped in a `function onCondition() {}` function.

</td></tr><tr><td>

runScriptsInUiType

</td><td>

String

</td><td>

The UI type on which the policy scripts run.Valid values:

-   desktop: Scripts run on the desktop interface.
-   mobileOrServicePortal: Scripts run on the mobile and Service Portal interfaces.
-   all: Scripts run on all interfaces.

Default: desktop

</td></tr><tr><td>

vaSupported

</td><td>

Boolean

</td><td>

Flag that indicates whether the UI policy is supported in Virtual Agent conversations.Default: false

</td></tr><tr><td>

actions

</td><td>

Array

</td><td>

A list of variable actions to perform when the catalog condition is met. For more information, see [actions array](fluent-service-catalog-api.md#).

</td></tr><tr><td>

$meta

</td><td>

Object

</td><td>

Metadata for the application metadata.With the installMethod property, you can map the application metadata to an output directory that loads only in specific circumstances.

```javascript
$meta: {
      installMethod: 'String'
}
```

Valid values for installMethod:

-   demo: Outputs the application metadata to the `metadata/unload.demo` directory to be installed with the application when the **Load demo data** option is selected.
-   first install: Outputs the application metadata to the `metadata/unload` directory to be installed only the first time an application is installed on an instance.

</td></tr></tbody>
</table>```javascript
import { CatalogUiPolicy } from "@servicenow/sdk/core";
import { hardwareRequestItem } from "./catalog-items/HardwareRequest.now";

export const managerApprovalPolicy = CatalogUiPolicy({
  $id: Now.ID["manager_approval_policy"],
  shortDescription: "Show manager approval when high priority selected",
  catalogItem: hardwareRequestItem,
  catalogCondition: `${hardwareRequestItem.variables.priority}=high^EQ`,
  actions: [
    {
      variableName: hardwareRequestItem.variables.manager_approval,
      visible: true,
      mandatory: true
    }
  ]
})
```

### actions array

Configure the variable actions \[catalog\_ui\_policy\_action\] that a catalog UI policy performs on variables when its conditions are met.

Each action in the array specifies a variable and the property changes to apply to that variable when the UI policy condition evaluates to true.

<table id="table_pm4_ysh_33c" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

variableName

</td><td>

String

</td><td>

Required. The variable to which the action applies.

</td></tr><tr><td>

visible

</td><td>

Boolean

</td><td>

Flag that indicates whether to make the variable visible.Default: false

</td></tr><tr><td>

disabled

</td><td>

Boolean

</td><td>

Flag that indicates whether to turn off the variable.Default: false

</td></tr><tr><td>

mandatory

</td><td>

Boolean

</td><td>

Flag that indicates whether to make the variable required.Default: false

</td></tr><tr><td>

cleared

</td><td>

Boolean

</td><td>

Flag that indicates whether to clear the variable value when the condition is met.Default: false

</td></tr><tr><td>

variableMessage

</td><td>

String

</td><td>

A message to display on the variable when the condition is met.This property applies only if the variableMessageType property has a value.

</td></tr><tr><td>

variableMessageType

</td><td>

String

</td><td>

The type of field message.Valid values:

-   info
-   warning
-   error

</td></tr><tr><td>

value

</td><td>

String

</td><td>

The value to set on the variable when the condition is met. This property applies only if the valueAction property is set to `setValue`.

</td></tr><tr><td>

valueAction

</td><td>

String

</td><td>

The action to take on the variable value when the condition is met.Valid values:

-   setValue: Sets the variable to the value specified in the value property.
-   clearValue: Clears the variable value.

</td></tr><tr><td>

order

</td><td>

Number

</td><td>

The order in which the action is evaluated relative to other actions.Default: 100

</td></tr><tr><td>

readOnly

</td><td>

Boolean

</td><td>

Flag that indicates whether to make the variable read only.Default: false

</td></tr></tbody>
</table>```javascript
actions: [
    {
      variableName: laptopRequest.variables.justification,
      mandatory: true,
      variableMessage: "Justification required for urgent requests",
      variableMessageType: "info",
      order: 100
    },
    {
      variableName: laptopRequest.variables.manager_approval,
      visible: true,
      mandatory: true,
      order: 200
    },
    {
      variableName: laptopRequest.variables.delivery_date,
      visible: true,
      order: 300
    }
]
```

## CatalogClientScript object

Configure a catalog client script \[catalog\_script\_client\] that runs on the client side to control the behavior of a catalog item form.

Use catalog client scripts to validate user input, auto-populate fields, or display alerts on catalog item forms. For simple show/hide, mandatory, and read-only logic, use catalog UI policies instead.

<table id="table_rsp_5rh_33c" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

$id

</td><td>

String or Number

</td><td>

Required. A unique ID for the metadata object. When you build the application, this ID is hashed into a unique sys\_id. For more information, see [ServiceNow Fluent language constructs](fluent-constructs.md).Format: `Now.ID['String' or Number]`

</td></tr><tr><td>

name

</td><td>

String

</td><td>

Required. A unique name for the catalog client script.

</td></tr><tr><td>

script

</td><td>

Script

</td><td>

The client-side script to run on the catalog item form. This property supports inline JavaScript or a reference to another file in the application that contains a script.Format:

-   To use text content from another file, refer to a file in the application using the following format: `Now.include('path/to/file')`. For more information, see [ServiceNow Fluent language constructs](fluent-constructs.md).
-   To provide an inline script, use string literals or template literals for multiple lines of code: `'Script' or `Script``.

</td></tr><tr><td>

type

</td><td>

String

</td><td>

The event that triggers the client script to run.Valid values:

-   onLoad: Runs when the form loads. Use for initial setup such as setting field states, default values, and visibility.
-   onChange: Runs when a specific variable changes. Include an `if (isLoading) return;` guard.
-   onSubmit: Runs when the form is submitted. Return `false` to block submission. Avoid using GlideAjax in this type because of asynchronous issues.

</td></tr><tr><td>

uiType

</td><td>

String

</td><td>

The UI type on which the client script runs.Valid values:

-   desktop: Applies to the desktop interface.
-   mobileOrServicePortal: Applies to the mobile and Service Portal interfaces.
-   all: Applies to all interfaces.

Default: desktop

</td></tr><tr><td>

active

</td><td>

Boolean

</td><td>

Flag that indicates whether the client script is enabled.Default: true

</td></tr><tr><td>

appliesTo

</td><td>

String

</td><td>

Required if using the variableSet property. The scope to which the catalog client script applies.Valid values:

-   item: The script applies to a catalog item.
-   set: The script applies to a variable set.

Default: item

</td></tr><tr><td>

catalogItem

</td><td>

Reference or String

</td><td>

Required only if the variableSet property isn’t used. The variable identifier of a CatalogItem or CatalogItemRecordProducer object or sys\_id of the catalog item \[sc\_cat\_item\] or record producer \[sc\_cat\_item\_producer\] to which the client script applies. For more information, see [CatalogItem object](fluent-service-catalog-api.md#) or [CatalogItemRecordProducer object](fluent-service-catalog-api.md#).

</td></tr><tr><td>

variableSet

</td><td>

Reference or String

</td><td>

Required only if the catalogItem property isn’t used. The variable identifier of a VariableSet object or sys\_id of the variable set \[item\_option\_new\_set\] to which the UI policy applies. For more information, see [VariableSet object](fluent-service-catalog-api.md#).

</td></tr><tr><td>

variableName

</td><td>

String

</td><td>

Required if the value of the type property is `onChange`. The name of the catalog variable that triggers the script when its value changes.

</td></tr><tr><td>

appliesOnCatalogItemView

</td><td>

Boolean

</td><td>

Flag that indicates whether the client script applies to catalog items displayed in the order screen of the service catalog. This view is available to requesters.Default: true

</td></tr><tr><td>

appliesOnRequestedItems

</td><td>

Boolean

</td><td>

Flag that indicates whether the client script applies to requested item forms after the item is requested. This view is available to fulfillers.Default: false

</td></tr><tr><td>

appliesOnCatalogTasks

</td><td>

Boolean

</td><td>

Flag that indicates whether the client script applies to catalog task forms for the item. This view is available to fulfillers.Default: false

</td></tr><tr><td>

appliesOnTargetRecord

</td><td>

Boolean

</td><td>

Flag that indicates whether the client script applies to records created for task-extended tables via record producers.Default: false

</td></tr><tr><td>

global

</td><td>

Boolean

</td><td>

Flag that indicates whether the client script runs in the global scope.Default: true

</td></tr><tr><td>

vaSupported

</td><td>

Boolean

</td><td>

Flag that indicates whether the client script is supported in Virtual Agent conversations.Default: false

</td></tr><tr><td>

publishedRef

</td><td>

String

</td><td>

The sys\_id of a published catalog item \[sc\_cat\_item\] or record producer \[sc\_cat\_item\_producer\] that this client script references.

</td></tr><tr><td>

$meta

</td><td>

Object

</td><td>

Metadata for the application metadata.With the installMethod property, you can map the application metadata to an output directory that loads only in specific circumstances.

```javascript
$meta: {
      installMethod: 'String'
}
```

Valid values for installMethod:

-   demo: Outputs the application metadata to the `metadata/unload.demo` directory to be installed with the application when the **Load demo data** option is selected.
-   first install: Outputs the application metadata to the `metadata/unload` directory to be installed only the first time an application is installed on an instance.

</td></tr></tbody>
</table>```javascript
import { CatalogClientScript } from "@servicenow/sdk/core";
import { laptopRequest } from "../catalog-items/laptop-request.now";

CatalogClientScript({
  $id: Now.ID["laptop_onload"],
  name: "Laptop Request - OnLoad",
  script: Now.include("../../client/laptop-onload.js"),
  type: "onLoad",
  catalogItem: laptopRequest,
  active: true,
  appliesOnCatalogItemView: true
});
```

The client script is defined in the `laptop-onload.js` file referenced from the script property. For example:

```javascript
function onLoad() {
  // Set initial field states
  g_form.setReadOnly("estimated_cost", true);
  g_form.setValue("estimated_cost", "$0");
  g_form.setMandatory("justification", true);
}
```

## VariableSet object

Create a variable set \[item\_option\_new\_set\] that groups reusable variables for use across multiple catalog items and record producers.

Variable sets are reusable collections of variables that can be attached to catalog items and record producers. Catalog UI policies and client scripts can be scoped to a variable set by setting the `appliesTo` property to `set`.

**Note:**

-   Variable sets within a catalog item can’t have the same internal name.
-   Within a catalog item, the name of a variable can’t be the same as the title or internal name of a variable set.
-   Catalog client scripts and catalog UI policy scripts must refer to the internal name of a variable set, not the title or display name.

<table id="table_rsp_5rh_33c" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

$id

</td><td>

String or Number

</td><td>

Required. A unique ID for the metadata object. When you build the application, this ID is hashed into a unique sys\_id. For more information, see [ServiceNow Fluent language constructs](fluent-constructs.md).Format: `Now.ID['String' or Number]`

</td></tr><tr><td>

title

</td><td>

String

</td><td>

Required. The display title of the variable set. This title appears only if the the displayTitle property is set to true.

</td></tr><tr><td>

internalName

</td><td>

String

</td><td>

The internal name of the variable set used for programmatic access through the g\_form API and server-side scripts. If not provided, the internal name is automatically generated from the title property.

</td></tr><tr><td>

description

</td><td>

String

</td><td>

A description of the variable set and its intended use.

</td></tr><tr><td>

type

</td><td>

String

</td><td>

The type of the variable set.Valid values:

-   singleRow: Variables are arranged in a single row.
-   multiRow: Variables are arranged in multiple rows that users can add or remove.

Default: singleRow

</td></tr><tr><td>

layout

</td><td>

String

</td><td>

The column layout for the variable set.Valid values:

-   normal: Variables are displayed in a single column.
-   2down: Variables are displayed in two columns, one side then the other.
-   2across: Variables are displayed in two columns with alternating sides.

Default: normal

</td></tr><tr><td>

order

</td><td>

Number

</td><td>

The order in which a variable set displays relative to other variable sets on the form.Default: 100

</td></tr><tr><td>

displayTitle

</td><td>

Boolean

</td><td>

Flag that indicates whether to display a collapsible section header for the variable set. If true, the value of the title property is displayed as a collapsible header.**Note:** Check box variables are grouped under a default title of Options. To use a custom title, add a Label variable with an order value that places it directly above the check box variables.

Default: false

</td></tr><tr><td>

setAttributes

</td><td>

String

</td><td>

Additional configuration attributes for the variable set as a comma-separated string, such as `max_rows=10,collapsible=true`. Use the `max_rows` attribute to set the maximum number of rows for a multi-row variable set.**Note:** AttachmentVariable, ContainerVariable, HtmlVariable, and CustomVariable types aren’t supported in multi-row variable sets.

</td></tr><tr><td>

readRoles

</td><td>

Array

</td><td>

A list of variable identifiers of Role objects or sys\_ids of roles \[sys\_user\_role\] that can view the variable set.​ For more information, see [Role API - ServiceNow Fluent](role-api-now-ts.md#).

</td></tr><tr><td>

writeRoles

</td><td>

Array

</td><td>

A list of variable identifiers of Role objects or sys\_ids of roles \[sys\_user\_role\] that can modify variable values in the set. For more information, see [Role API - ServiceNow Fluent](role-api-now-ts.md#).

</td></tr><tr><td>

createRoles

</td><td>

Array

</td><td>

A list of variable identifiers of Role objects or sys\_ids of roles \[sys\_user\_role\] that can create row instances. For more information, see [Role API - ServiceNow Fluent](role-api-now-ts.md#).This property applies only if the value of the type property is `multiRow`.

</td></tr><tr><td>

variables

</td><td>

Object

</td><td>

The variable definitions for the item that provide options for requesting it. Each variable type has a specific function. For example:```javascript
variables: {
    laptopType: SelectBoxVariable({
      question: "Laptop Type",
      choices: {
        standard: { label: "Standard Laptop", sequence: 1 },
        developer: { label: "Developer Workstation", sequence: 2 }
      },
      mandatory: true,
      order: 100
    }),
    justification: MultiLineTextVariable({
      question: "Business Justification",
      mandatory: true,
      order: 200
    })
}
```

For general information about catalog variables, see Service catalog variables.

</td></tr><tr><td>

name

</td><td>

String

</td><td>

An optional name for additional identification of the variable set.

</td></tr><tr><td>

version

</td><td>

Number

</td><td>

The version of the variable set.Default: 0

</td></tr><tr><td>

$meta

</td><td>

Object

</td><td>

Metadata for the application metadata.With the installMethod property, you can map the application metadata to an output directory that loads only in specific circumstances.

```javascript
$meta: {
      installMethod: 'String'
}
```

Valid values for installMethod:

-   demo: Outputs the application metadata to the `metadata/unload.demo` directory to be installed with the application when the **Load demo data** option is selected.
-   first install: Outputs the application metadata to the `metadata/unload` directory to be installed only the first time an application is installed on an instance.

</td></tr></tbody>
</table>```javascript
import {
  VariableSet,
  EmailVariable,
  SingleLineTextVariable,
  ReferenceVariable
} from "@servicenow/sdk/core";

export const contactInfoSet = VariableSet({
  $id: Now.ID["contact_info_set"],
  title: "Contact Information",
  description: "Standard contact information fields",
  type: "singleRow",
  layout: "2across",
  order: 100,
  displayTitle: true,
  variables: {
    email: EmailVariable({
      question: "Email Address",
      mandatory: true,
      order: 100
    }),
    phone: SingleLineTextVariable({
      question: "Phone Number",
      mandatory: true,
      order: 200
    }),
    department: ReferenceVariable({
      question: "Department",
      referenceTable: "cmn_department",
      referenceQualCondition: "active=true",
      order: 300
    })
  }
})
```

