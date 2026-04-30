---
title: Theme Builder release notes
description: The ServiceNow Theme Builder application enables you to tailor the visual experience for your users, helping to update the look and feel to match your brand. Theme Builder was enhanced and updated in the Yokohama release.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 3
---

# Theme Builder release notes

The ServiceNow® Theme Builder application enables you to tailor the visual experience for your users, helping to update the look and feel to match your brand. Theme Builder was enhanced and updated in the Yokohama release.

## Theme Builder highlights for the Yokohama release

-   Edit and style the Unified Navigation component to better suit your brand.
-   Make individual style edits on a component by double-clicking it to quickly access the Component Editor.
-   As of Theme Builder version 5.1, customize the colors of empty state illustrations from within Theme Builder.
-   As of Theme Builder version 5.1, use your own custom images by overriding the default empty state illustrations.

See [Working with themes in Next Experience](https://www.servicenow.com/docs/access?context=next-experience-theming&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US) for more information.

**Important:** Theme Builder is available by default starting in the Yokohama release and upgrades are available in ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Yokohama release

-   **[Align with your brand by using the Unified Navigation component](https://www.servicenow.com/docs/access?context=edit-unified-navigation-component&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US)**

    Customize the Unified Navigation component from within Theme Builder by using the following new features:

    -   Quickly view how the Unified Navigation component will look in your theme by using the Preview pane.
    -   Use the Component Configuration menu to view any shared styling between subcomponents.
    -   View the background color of your subcomponent and see how it renders in relation to the Unified Navigation component by using the updated canvas color feature.
-   **[Use the double-click feature to quickly access the Component Editor](https://www.servicenow.com/docs/access?context=tb-edit-components&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US)**

    Double-click a component tile to access the Component Editor where you can continue to make style adjustments to subcomponents, variants, or interactions.

-   **[Adjust the Unified Navigation component to meet accessibility standards](https://www.servicenow.com/docs/access?context=tb-adjust-component-wcag&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US)**

    As of Theme Builder version 5.1, the Accessibility Inspector now displays the total number of accessibility errors with contrast issues for the Unified Navigation component and subcomponents. See the Accessibility section for details.

-   **[Adapt the theme-able illustrations to seamlessly integrate with your brand](https://www.servicenow.com/docs/access?context=working-with-image-styles&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US)**

    As of Theme Builder version 5.1, use the new Image styles feature to enhance your theme in the following ways:

    -   Edit the colors of the empty state illustrations from within Theme Builder. When a part of your Next Experience web page doesn't contain data, an empty state illustration appears. Empty state illustrations are theme-able and adapt to your theme colors.
    -   Override empty state illustrations with your own custom images to uniquely align with your branding style.

## UI changes

-   **[Navigation updated](https://www.servicenow.com/docs/access?context=tb-edit-components&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US)**

    The **Return to component overview** link within the Component Editor is replaced with breadcrumb-style navigation for a more contextual navigation experience.

-   **[Component Editor button replaced](https://www.servicenow.com/docs/access?context=tb-edit-components&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US)**

    The **Go to Component Editor** button is now labeled either **Style variants**, **Style subcomponents**, or **Style interactions** depending on the selected component. The Component Editor behaves in the same way despite this UI change.

-   **[Component Editor Interactions States panel updated](https://www.servicenow.com/docs/access?context=tb-edit-components&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US)**

    The Interaction States panel within the Component Editor now refers to either **Interactions** or **Subcomponents**.

-   **[New Image styles tab added to Editor page](https://www.servicenow.com/docs/access?context=working-with-image-styles&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US)**

    As of Theme Builder version 5.1, the Editor page has the following additional options:

    -   The general styles panel, which includes Global and Component styles, now features Image styles. The Image styles tab displays all illustrations available for editing.
    -   When you select an empty state illustration for editing from the Image styles tab, the property panel opens with two additional tabs: Images and Colors. The Images tab displays which image files are applied to an empty state illustration. The Colors tab displays which theme colors are applied to an illustration.

## Activation information

Starting with the Yokohama release, Theme Builder is included as a core plugin with the Next Experience application and is available by default. You can update to the latest version of Theme Builder from ServiceNow Store.

## Accessibility information

-   **[Adjust the Unified Navigation component to meet accessibility standards](https://www.servicenow.com/docs/access?context=tb-adjust-component-wcag&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US)**

    The Accessibility Inspector, which detects and guides you through fixing contrast issues in your theme, now includes accessibility errors for the Unified Navigation component and subcomponents.


## Related ServiceNow applications and features

-   **[Build apps using App Engine Studio](https://www.servicenow.com/docs/access?context=aes-overview&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US)**

    Use ServiceNow® App Engine Studio for developing rich web applications to store information, automate business processes, and solve business problems.

-   **[UI Builder](https://www.servicenow.com/docs/access?context=ui-builder-overview&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US)**

    Use ServiceNow® UI Builder to build pages for workspaces that are generated with App Engine Studio or custom web experiences by using Next Experience Components and custom web components.


**Parent Topic:**[ServiceNow AI Platform user interface release notes](now-platform-ui-rn-landing.md)

