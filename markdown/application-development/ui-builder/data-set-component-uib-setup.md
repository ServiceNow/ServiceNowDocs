---
title: Data set component setup
description: Data set is a list of records within a portal that offer users configurable view types and filter options.Configure the data, size, and view of the Data set component.Select event handlers to configure the actions \(events\) provided with the Data set component.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/data-set-component-uib-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 5
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Data set component setup

Data set is a list of records within a portal that offer users configurable view types and filter options.

## Before you begin

This task assumes you have placed the component on the page and are ready to configure the properties and events. For instructions on accessing and using features in UI Builder, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

**Note:** This document describes the latest component functionality. Go to the store to make sure you have the latest version of the component.

Role required: admin or ui\_builder\_admin

## Procedure

1.  Define a label for your data set that differentiates it from other components in the content tree.

    A label makes finding the component easier in a large list of components. For instructions on using the content tree, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md).

    \[Omitted image "data-set-config-content-tree.png"\] Alt text: Component with label displayed in the content tree

2.  Select the Data set component, using one of these methods:

    -   Click anywhere within the component.
    -   Select the Data set label you created for your component in the content tree.
    The property fields appear in the **Config** tab in the setup panel on the right.


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## Data Set component properties

Configure the data, size, and view of the Data set component.

To configure the properties, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Creates dynamic property values from multiple sources. Sources include state variables \(@state\), URL variables \(@context\), or data resource payloads \(@data\). For details, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-data-resources.md).
-   **Scripting**: Creates a scripted property value. For details on scripted values, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).

<table id="table_a2h_hlr_nnb"><thead><tr><th>

Field

</th><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Title

</td><td>

title

</td><td>

Text to introduce the data set.

</td></tr><tr><td>

Data

</td><td>

data

</td><td>

Data to populate the cards in the data set. You can populate the content dynamically by binding to a data resource, or you can manually enter the content in a code editor.-   To dynamically populate the content, click the data icon \(\[Omitted image "data-icon.png"\] Alt text: Data icon\) and select a data resource. This returns a response object containing metadata and an array of items.
-   To manually enter the content, click **Edit**. In the code editor, define the information needed to render each card, including its fields and actions. For example, to populate one card, you would enter the following:

 ```
{ 
  "page_cursor": "e2JlY2E4ZTYyNWIwMjEwMTA4NDhiMjg1ODJkODFjNzYzPTI5LCA3NDRiODJhMjViMDIxMDEwODQ4YjI4NTgyZDgxYzc1Zj0yMDAsIDAxYjQzNWEwNzMyMTEwMTBjMzQyZDVmZGJkZjZhN2UzPTExfQ", 
  "page_size": 20, 
  "page_number": 0, 
  "is_last_page": false, 
  "all_actions": [ 
    { 
      "assignmentId": "d46f400473211010c342d5fdbdf6a7cf", 
      "name": "navigation", 
      "label": "Navigation", 
      "actionType": "uxf_client_action", 
      "actionDispatch": "NAVIGATION", 
      "actionPayload": "{\r\n \"table\": \"{{table}}\",\r\n \"sysId\": \"{{sys_id}}\",\r\n \"url\": \"{{navigation_url}}\"\r\n}" 
    }, 
    { 
      "assignmentId": "e3a173c073151010c342d5fdbdf6a7a2", 
      "name": "call_number", 
      "label": "Call Number", 
      "actionType": "uxf_client_action", 
      "actionDispatch": "HOME_PHONE_CALL", 
      "actionPayload": "{\r\n\t\"phoneNumber\": \"{{home_phone}}\"\r\n}" 
    } 
  ], 
  "selected_filter": "", 
  "items": [ 
    { 
      "template": "now-card-evam-record", 
      "propValues": { 
        "highlightedHeaderLabel": "Vice President", 
        "textHeaderLabel": "Development", 
        "titleLabel": "Manifah Masood", 
        "imageURL": "1792fbe1d701120035ae23c7ce6103e4.iix", 
        "subtitle": "manifah.masood", 
        "subtitleAvatarName": "Manifah Masood", 
        "subtitleAvatarURL": "ab490666c312120048f4d5dc64d3aee8.iix", 
        "detailValueOne": "manifah.masood@example.com", 
        "detailValueTwo": "", 
        "detailValueThree": "", 
        "highlightedHeaderIcon": "clock-outline", 
        "highlightedHeaderBkgColor": "moderate", 
        "subtitleIcon": "calendar-fill", 
        "imageType": "image", 
        "subtitleImageType": "avatar", 
        "detailLabelOne": "Email address", 
        "detailLabelTwo": "Works for", 
        "detailLabelThree": "Location/address", 
        "mainActions": [ 
          { 
            "assignmentId": "42fd3e5273511010c342d5fdbdf6a70e", 
            "name": "activate_user", 
            "label": "Activate", 
            "actionType": "server_script", 
            "icon": "Button", 
            "buttonType": "primary", 
            "actionDispatch": "", 
            "serverScript": "current.active = true;\ncurrent.update();", 
            "confirmationRequired": false, 
            "confirmationMessage": "", 
            "actionPayload": "", 
            "actionPayloadMap": [] 
          }, 
          { 
            "assignmentId": "e3a173c073151010c342d5fdbdf6a7a2", 
            "name": "call_number", 
            "label": "Call Number", 
            "actionType": "uxf_client_action", 
            "icon": "", 
            "buttonType": "primary", 
            "actionDispatch": "HOME_PHONE_CALL", 
            "serverScript": "", 
            "confirmationRequired": false, 
            "confirmationMessage": "", 
            "actionPayload": { 
              "phoneNumber": "" 
            } 
          } 
        ], 
        "clickAction": { 
          "assignmentId": "d46f400473211010c342d5fdbdf6a7cf", 
          "name": "navigation", 
          "label": "Navigation", 
          "actionType": "uxf_client_action", 
          "icon": "", 
          "buttonType": "primary", 
          "actionDispatch": "NAVIGATION", 
          "serverScript": "", 
          "confirmationRequired": false, 
          "confirmationMessage": "", 
          "actionPayload": { 
            "table": "sys_user", 
            "sysId": "1832fbe1d701120035ae23c7ce610369", 
            "url": "" 
          } 
        }, 
        "model": { 
          "name": "Manifah Masood", 
          "email": "manifah.masood@example.com", 
          "avatar": "ab490666c312120048f4d5dc64d3aee8.iix", 
          "mobile_phone": "", 
          "time_zone": "Europe/London", 
          "title": "Vice President", 
          "photo": "1792fbe1d701120035ae23c7ce6103e4.iix", 
          "user_name": "manifah.masood", 
          "location.name": "", 
          "company.name": "", 
          "department.name": "Development", 
          "sysId": "1832fbe1d701120035ae23c7ce610369", 
          "sys_id": "1832fbe1d701120035ae23c7ce610369", 
          "table": "sys_user" 
        } 
      }, 
      "buttonType": "primary", 
      "actionDispatch": "NAVIGATION", 
      "serverScript": "", 
      "confirmationRequired": false, 
      "confirmationMessage": "", 
      "actionPayload": { 
        "table": "sc_cat_item", 
        "sysId": "f514e9e64fcf42c0bde324af0210c766", 
        "url": "" 
      }, 
      "model": { 
        "name": "OS X Mavericks", 
        "price": "$0.00", 
        "category.title": "Software", 
        "vendor.name": "", 
        "icon": "0f823d404f889200086eeed18110c70f.iix", 
        "picture": "616db9444f889200086eeed18110c70e.iix", 
        "short_description": "OS X Mavericks (version 10.9.x) is Apple's tenth\n\t\t\tmajor release of OS X, for Macs\n\t\t", 
        "model.display_name": "", 
        "sys_class_name": "Catalog Item", 
        "delivery_time": "2 Days", 
        "sysId": "f514e9e64fcf42c0bde324af0210c766", 
        "sys_id": "f514e9e64fcf42c0bde324af0210c766", 
        "table": "sc_cat_item" 
      } 
    } 
  ], 
  "available_filters": [ 
    { 
      "sys_id": "", 
      "label": "Default" 
    }, 
    { 
      "sys_id": "c10d1e42737e10108d991e666bf6a761", 
      "label": "Active entities" 
    }, 
    { 
      "sys_id": "808ed682737e10108d991e666bf6a793", 
      "label": "Assigned to me" 
    }, 
    { 
      "sys_id": "1213fb41733210108d991e666bf6a77a", 
      "label": "Recently updated" 
    } 
  ] 
} 
```

</td></tr><tr><td>

Show grid/list toggle

</td><td>

toggleView

</td><td>

Option to allow users to switch between the list and grid views

</td></tr><tr><td>

Default view

</td><td>

defaultView

</td><td>

View in which the data set is displayed by default. You can select **List** or **Grid**. If left blank, the list view is the default.

</td></tr><tr><td>

Card height \(grid view\)

</td><td>

cardHeight

</td><td>

Size of the cards to display. You can select **Small**, **Medium**, or **Large**. This configuration applies only to the grid view.

</td></tr><tr><td>

Max. cards per row \(grid view\)

</td><td>

maxCardPerRow

</td><td>

Maximum number of cards to display in a row. You can select a minimum of 1 and a maximum of 6. This configuration applies only to the grid view.

</td></tr><tr><td>

Min. card width

</td><td>

minCardWidth

</td><td>

Minimum card width, in pixels. For best readability of the card content, use a minimum card width of 150 pixels.

</td></tr><tr><td>

Empty state message

</td><td>

emptyMessage

</td><td>

Message to display when there is no data to show.

</td></tr><tr><td>

Hide filter

</td><td>

hideFilter

</td><td>

Option to hide the filter element.

</td></tr><tr><td>

Hide pagination

</td><td>

hidePaginationControls

</td><td>

Option to hide pagination buttons to view the next or previous page of the data set.

</td></tr></tbody>
</table>## Data Set component events

Select event handlers to configure the actions \(events\) provided with the Data set component.

The Events tab shows the events used by the Data set component. To view the available events, select **+ Add event mapping**. Select the event in the list to add one or more event handlers.

### Event handlers

Event handlers work with data resources to link the Data set actions to the data you want to display to your users. Select the event in the list to add one or more event handlers.

For instructions on adding event handlers to an event, see [Configure an event handler](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/event-handler.md).

### Event descriptions

|Event|Description|
|-----|-----------|
|NOW\_DATA\_SET\_PAGINATION\_BUTTON\_CLICKED|User clicks a pagination button, such as selecting to view the next page of content.|
|NOW\_DATA\_SET\_FILTER\_ITEM\_CLICKED|User clicks an item that is listed in the filter dropdown.|
|NOW\_DATA\_SET\_ACTION\_SUCCEEDED|Server completes a component action successfully. The event also dispatches a payload containing information of the component action.|
|NOW\_DATA\_SET\_ACTION\_FAILED|Server completes a component action unsuccessfully. The event also dispatches a payload containing information of the component action.|

