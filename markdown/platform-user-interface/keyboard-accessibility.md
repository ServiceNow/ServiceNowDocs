---
title: Using accessibility features
description: Accessibility features include keyboard navigation, color and style settings, using a screen reader, and search methods.Skip links allow users to quickly navigate to the main content on a page, list, or form, bypassing icons, banner text, navigation links, and other elements. Skip links are not visible until you tab to them.There are several color and style changes that make the platform more accessible.Screen elements in the platform have enhancements that make them accessible to screen readers.There are several ways to search for information in the user interface.With accessibility mode enabled, tab through cards in a task board. Use the card details button to view task card details.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-05-08"
reading_time_minutes: 6
breadcrumb: [User interface configuration, Working in Core UI, Configure UIs and portals, Configure user experiences]
---

# Using accessibility features

Accessibility features include keyboard navigation, color and style settings, using a screen reader, and search methods.

## Keyboard accessibility

The ServiceNow AI Platform is designed to be as accessible as possible without user modification or setting changes. Users can tab through the platform UI without enabling accessibility. However, without accessibility enabled, tabbing goes from input to input and skips other items on a form, such as reference icons.

Tab-through provides the following options:

-   Use skip links to shift focus to different parts of the page without tabbing through every element.
-   On edit pages such as forms, the keyboard focus starts at the first editable field on the page.
-   If the **glide.ui.focus\_first\_element** user preference is enabled, page focus starts at the first input field at the top of the page content section. In a table, this field is usually the search option. In a form, the field is the first input field in the form. For more information about disabling initial field focus to improve accessibility, see [Turn off first field focus](c_SetUpSect508ComplianceFeature.md#).
-   Use tab-through and arrow keys to move items around in a slushbucket.
-   When focused on tabs, use right/left arrow keys to switch tabs.
-   Arrows keys work within menus to navigate between entries.
-   On tab-through for a list, the option to enable the **Edit table data inline** appears, so you can use the list editor, rather than opening the form.
    -   When inline edit mode is enabled, screen focus shifts to the first cell in the table.
    -   Press the Escape key while a cell is selected to exit inline edit mode. Focus remains on the cell.
    -   Press the spacebar to open the context menu for the selected item.
    -   Use the arrow keys \(in addition to tabbing\) to move around the list in inline edit mode.
-   Properties pages, such as **System Properties** &gt; **UI Properties**, include an icon with the property name. Screen readers read the property name when the icon is in focus.
-   Fields on a form include a tooltip icon. Screen readers read the tooltip when the icon is in focus.
-   In the application navigator when accessibility is enabled, tabbing moves you through each element for every module, including the **Edit application/module** and **Add to favorites** icons. Use the arrow keys to move through the application navigator without focusing on these additional elements.
-   If accessibility mode is enabled, a help icon appears with the HTML field. The help icon indicates how to access and escape the HTML field toolbar.

**Parent Topic:**[User interface configuration](../../core-configuration/concept/p_NavigationAndUIConfiguration.md)

## Use skip links

Skip links allow users to quickly navigate to the main content on a page, list, or form, bypassing icons, banner text, navigation links, and other elements. Skip links are not visible until you tab to them.

### Before you begin

Role required: none

### About this task

The user interface includes skip links to the navigation menu, and the main content pane. If accessibility is not enabled, users can also use skip links to activate accessibility.

![Skip link for the navigator](../image/SkipLink.png "Skip link")

-   **Enable Accessibility**: Enables accessibility. This skip link only appears if the user has not yet enabled accessibility. Pressing enter prompts you to reload the page with accessibility mode enabled.
-   **Skip to navigator**: Skips to the navigation filter in the application navigator.
-   **Skip to main content**: Skips to the main content page.
-   **Edit table data inline**: Skips to the first field in a table. When the field is selected, press Enter to edit the field. Press the spacebar to open the field context menu. Press the Escape key to exit inline edit mode.

Skip links are usually the first item in the tab order for a page or frame.

### Procedure

-   Use the Tab and Shift+Tab keys to move forward and back through the skip links and other selectable fields.

-   When a skip link receives focus, press Enter to select the link.


## Color and style accessibility

There are several color and style changes that make the platform more accessible.

### Enable the Contrast UI theme

In the system settings, on the themes tab, select the Contrast UI theme. The Contrast UI theme provides a higher contrast range of colors for the platform UI.

In Service Portal, you can apply the Stock — High Contrast theme to a portal for a higher contrast color range. Portal users can enable a contrast theme using the **Accessibility** option in the User Profile widget.

### Patterned charts and graphs

View charts and graphs that rely heavily on color with patterns in addition to colors. Navigate to **System settings** &gt; **General**, then select **Data visualization patterns enabled**.

![Two graphs, one in the standard mode which relies only on color, and an overlay of the second graph with patterns.](../image/AccessibilityEnabledStyleEx.png "Accessibility enabled graph")

## Screen reader accessibility

Screen elements in the platform have enhancements that make them accessible to screen readers.

Use NVDA, JAWS, or VoiceOver for non-visual access to the platform.

Skip links allow you to tab straight to the main content instead of tabbing through all the other elements on the page.

When a page reloads or search results display, screen readers inform the user.

Important images and field indicators \(for example, status indicators for avatars in list v3\) have alternative text for screen readers to read.

To reduce confusion when tabbing through modules, the edit application/edit module and add to favorites icons are accessible to screen readers by tabbing. To skip the **Edit application/module** and **Add to favorites** icons, use the up and down arrows on the keyboard.

In Service Portal, users can add alternative text to containers in their own portal for screen readers to read.

Elements such as links or button are listed as such for screen reader awareness.

Properties pages, such as **System Properties** &gt; **UI Properties**, include an icon with the property name. Screen readers read the property name when the icon is in focus.

Forms include accessible tooltips that screen readers read when the tooltip is in focus.

## Accessibility search methods

There are several ways to search for information in the user interface.

-   When a list opens, focus starts in the search field. Press the Tab key or the shift+tab keys to navigate away from the search, or start typing while focus is in the search field.
-   List views include a **Go to** search field in the list title bar. Using the \* wildcard character in the search text allows you to perform a **contains** search rather than a **starts with** search. This type of query may take longer to run but can save keystrokes. You can also use several other wildcards with list searches.
-   The navigation filter in the application navigator filters the applications and modules that appear in the navigator based on the entered text. Tab through or use skip links to navigate directly to the navigation filter. To open a module, click the module name, or press the Down Arrow to highlight the module name, and then press Enter.

See [Available search options](https://www.servicenow.com/docs/access?context=c_IntroductionToSearching&version=australia&pubname=australia-platform-administration&ft:locale=en-US) for more information about these search methods.

## View card details in a Visual Task Board

With accessibility mode enabled, tab through cards in a task board. Use the card details button to view task card details.

### Before you begin

Enable accessibility from the General tab of the system settings menu.

Role required: none

### Procedure

1.  Navigate to **All** &gt; **Self-Service** &gt; **Visual Task Boards**.

2.  Open an existing task board.

3.  Press the Tab key to navigate through the board to get to a task card.

4.  Press the Tab key to navigate through the card until the Open Card Details button appears.

    ![Task board card with the View Card Details button enabled and highlighted](../image/viewcarddetails.png "Card details")

5.  Press **Enter** to open the card.

6.  To exit the card, press **Escape**.


