---
title: Theme Builder release notes
description: The ServiceNow Theme Builder application enables you to tailor the visual experience for your users, helping to update the look and feel to be more like your brand. Theme Builder was enhanced and updated in the Xanadu release.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 4
---

# Theme Builder release notes

The ServiceNow® Theme Builder application enables you to tailor the visual experience for your users, helping to update the look and feel to be more like your brand. Theme Builder was enhanced and updated in the Xanadu release.

## Theme Builder highlights for the Xanadu release

-   Achieve your branding and styling needs by offering multiple themes and alternate color palettes to your users.
-   Add a dark alternate color palette to your newly created themes and edit to refine your theme.
-   As of Theme Builder version 4.1, receive notifications about updates directly from the Theme Builder application.
-   As of Theme Builder version 4.1, organize your themes by priority, purpose, or other criteria, by using the drag-and-drop feature in the List view. With this feature, you can publish and order the themes that are displayed in the Next Experience Theme user preference.

See [Working with themes in Next Experience](https://www.servicenow.com/docs/access?context=next-experience-theming&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US) for more information.

**Important:** Theme Builder is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Xanadu release

-   **[Publish multiple themes with Theme Builder](https://www.servicenow.com/docs/access?context=tb-apply-theme&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US)**

    Publish multiple themes with their alternate color palettes to your web instance. Set a default theme for your users.

-   **[Add a dark alternate color palette](https://www.servicenow.com/docs/access?context=tb-edit-color-palette&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US)**

    Add a dark alternate color palette to your Theme Builder theme. You can edit this alternate color palette to further enhance your brand style.

-   **[Set the presentation order of your themes in Next Experience](https://www.servicenow.com/docs/access?context=configure-presentation-order-of-themes&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US)**

    Define the presentation order of the themes that are displayed in the ServiceNow® Next Experience user preferences.

-   **[Select from multiple themes in Next Experience user preferences](https://www.servicenow.com/docs/access?context=select-a-theme-in-next-experience&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US)**

    View multiple themes and their alternate color palettes in Next Experience user preferences.

-   **[Set the presentation order of your Theme Builder themes](https://www.servicenow.com/docs/access?context=set-presentation-order-themes&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US)**

    As of Theme Builder version 4.1, you can control the order in which the themes created with Theme Builder appear in Next Experience user preferences by using the List view within the Manager page.

-   **[Remove Global Style overrides](https://www.servicenow.com/docs/access?context=tb-edit-theme&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US)**

    As of Theme Builder version 4.1, you can remove any overrides that you made to Global Styles and return to your initial values by using the Remove Override button.

-   **[Use drag-and-drop to publish and unpublish your themes](https://www.servicenow.com/docs/access?context=tb-apply-theme&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US)**

    As of Theme Builder version 4.1, use the drag-and-drop feature in the List view to publish and unpublish your themes for your web instance.

-   **[Adjust a component to meet accessibility standards](https://www.servicenow.com/docs/access?context=tb-adjust-component-wcag&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US)**

    As of Theme Builder version 4.1, the Accessibility Inspector now displays the total number of accessibility errors in your theme and lists the specific components with contrast issues. See the Accessibility section for details.


## UI changes

-   **[Manage web and mobile themes independently](https://www.servicenow.com/docs/access?context=tb-edit-theme&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US)**

    Manage your web and mobile theming experiences separately by using the updated Manager view.

-   **[Manager view now displays each theme and all associated color palettes in one place](https://www.servicenow.com/docs/access?context=tb-edit-theme&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US)**

    Each core theme and all associated alternate color palettes are now located within one theme card.


## Removed in this release

-   Removed the **Apply** button used to apply your theme to web and mobile instances. To publish your theme, use the **Publish** option from the theme card overflow menu. For more information about publishing themes, see [Publish your themes with Theme Builder](https://www.servicenow.com/docs/access?context=tb-apply-theme&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US).

## Activation information

Install Theme Builder by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

**Note:** As of Theme Builder version 4.1, you see when a new Theme Builder update is available from within the Editor page view.

## Accessibility information

Accessibility improvements for Theme Builder include the following updates:

-   Added a dark alternate color palette that makes the display easier for your eyes and less disturbing in low-light settings is available for creation. For more information, see [Add an alternate color palette](https://www.servicenow.com/docs/access?context=tb-edit-color-palette&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US).
-   Updated modal when you publish a theme group for your web instance. A warning appears if there’s an accessibility error within the base theme or the theme's alternate color palettes. A link within the modal navigates you to the correct theme or alternate color palette with accessibility errors.
-   Improved Accessibility Inspector detects and guides you through fixing accessibility issues in your theme. This tool includes the total number of violations and a list of specific components with accessibility issues. For more information, see [Adjust a component to meet accessibility standards](https://www.servicenow.com/docs/access?context=tb-adjust-component-wcag&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US).
-   Updated reflow feature ensures the content within the Component Editor view automatically adjusts when the screen size is reduced. This improvement eliminates the need for horizontal scrolling.

## Related ServiceNow applications and features

-   **[Build apps using App Engine Studio](https://www.servicenow.com/docs/access?context=aes-overview&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US)**

    Use ServiceNow® App Engine Studio for developing rich web applications to store information, automate business processes, and solve business problems.

-   **ServiceNow®[UI Builder](https://www.servicenow.com/docs/access?context=ui-builder-overview&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US)**

    Use ServiceNow® UI Builder to build pages for workspaces generated with App Engine Studio or custom web experiences using Next Experience Components and custom web components.


**Parent Topic:**[ServiceNow AI Platform user interface release notes](now-platform-ui-rn-landing.md)

