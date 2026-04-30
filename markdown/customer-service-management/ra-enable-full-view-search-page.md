---
title: Enable full view search for Recommended Actions in a configurable workspace
description: The full view search feature displays the AI search results in a new subtab with an expanded view. Use the following information to enable this feature in any configurable workspace.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configuring AI search, Recommended Actions configuration, Implement Intelligence, Configure, Customer Service Management]
---

# Enable full view search for Recommended Actions in a configurable workspace

The full view search feature displays the AI search results in a new subtab with an expanded view. Use the following information to enable this feature in any configurable workspace.

## Before you begin

Role required: admin

## About this task

AI search results appear in the Recommended Actions tab in the contextual side panel in the form of guidances that you can act on. Selecting the Full view search icon displays the AI search results in a new subtab with an expanded view.

When a user selects the Full view search icon, the Recommended Actions application dispatches an event called **RECOMMENDED\_ACTIONS\#ACTION\_CLICKED** with a type of **raExpandedSearch**. This event needs to be handled in the corresponding team layer that wants to uptake the full view search page. The following code snippet provides an example about how to navigate to the page with the correct properties.

```
if (event.payload.actionProps.type == 'raExpandedSearch') {
          const { contextTable, contextId, contextSysId,
searchTerm,selectedFilterTab,selectedFacetOptions, 
selectedSortOption,actionConfigurations } = event.payload.actionProps;
          helpers.navigate.to('ra-expanded-search', { 'contextTable':
contextTable, 'contextId': contextId }, {'contextSysId': contextSysId,
'searchTerm': searchTerm, 'selectedFilterTab': selectedFilterTab,
'selectedFacetOptions': selectedFacetOptions, 'selectedSortOption':
selectedSortOption, 'actionConfigurations': 
JSON.stringify(actionConfigurations)}, false, false, 'current');
      }
```

Use the following steps to define the full view search page in a configurable workspace.

## Procedure

1.  Navigate to UI Builder and select your workspace experience.

2.  Create a new page with the following URL path: **ra-expanded-search**.

    This is the path that you will use in the above script to open the full view search page. For more information, see [Create a blank page](https://www.servicenow.com/docs/access?context=learn-by-example-create-blank-page&version=zurich&pubname=zurich-application-development&ft:locale=en-US) in the UI Builder documentation.

3.  Select the following required parameters for the page.

    -   contextTable
    -   contextId
4.  Select the following optional parameters for the page.

    -   contextSysId
    -   searchTerm
    -   selectedFilterTab
    -   selectedFacetOptions
    -   selectedSortOptions
    -   actionConfigurations
5.  Open the page variant that you created in step 2 by navigating to the **sys\_ux\_screen.list** and selecting the page variant from the UX Screens list.

6.  Use a copied version of the page definition created by RA for full view search.

    For example, **Recommended Actions Expanded Search Default \(sysId - b646da9443a8c2108d82c8641ab8f2f3**.

    **Note:** It's not advised to use the mentioned page definition directly.

7.  Create a viewport inside the page variant to load the guidance detailed experience to make it work in the full view search page.

    1.  Create an app route record by navigating to **sys\_ux\_app\_route.list** and selecting **New**.

    2.  Fill in the fields based on how you have configured the full view search page.

    3.  Select **Submit**.

    **Note:** Be sure to use a different route/parent macroponent composition element ID to avoid any conflicts with the CSM Recommended Actions Full View Search page.


