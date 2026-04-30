---
title: Page Inspector
description: Identify the HTML and JavaScript page components in your user interfaces that are available for custom UI testing. Enable automated testing by ensuring that your user interfaces only contain testable page components.
locale: en-US
release: xanadu
product: Automated Test Framework \(ATF\)
classification: automated-test-framework-atf
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Custom UI test steps, UI test steps, Building and running automated tests with the Automated Test Framework, Test your apps with the ATF, Testing and debugging applications, Building applications]
---

# Page Inspector

Identify the HTML and JavaScript page components in your user interfaces that are available for custom UI testing. Enable automated testing by ensuring that your user interfaces only contain testable page components.

The Page Inspector is a developer setting that opens a new pane beside any currently displayed ServiceNow AI Platform page.

![Core UI view of Knowledge Base article KB0011110 and Page Inspector pane](../image/atf-page-inspector-01.png "Page Inspector view of Knowledge Base article KB0011110")

The Page Inspector provides these features.

1.  A highlighted frame to identify the currently inspected page.
2.  A banner icon to display or hide the Inspector pane.
3.  A button to refresh the list of page components.
4.  A button to hide the Inspector pane.
5.  An inspector button to identify specific components on a page.
6.  A list of page components available for custom UI testing.
7.  A page component search filter.
8.  A row to click to see more information about a page component.
9.  A highlighted row and tooltip to preview information about the currently inspected component.
10. A highlighted page component to identify the currently inspected component on the page.
11. A component label and back button to return to the list of page components.
12. A list of actions to take on the current page component.
13. A list of attribute information for the current page component.
14. An attribute name and value pair for a page component.

    **Note:** You can use the Label Path field to show the hierarchical page context around an element while inspecting a component on a page. If there are many "ancestor" label paths of an element, it can display only three. Each label path element is separated by a &gt;. It can be used to differentiate between two similar looking components.


**Note:** UI buttons with icons are now visible in the page inspector.

![Core UI view of the Page Inspector pane showing details for the Create Favorite page component](../image/atf-page-inspector-02.png "Page Inspector view of component details")

## Page inspector launcher

The page inspector launcher helps you select and launch a specific page within the page inspector. See [Inspect different page types](../task/atf-inspect-page-types.md) for more information.

![Gif showing the different page types for inspection](../image/atf-page-inspector-launcher.gif)

## Testable page components

The Page Inspector retrieves the list of testable page components when you first load a page. Testable components consist of standard HTML and JavaScript that are accessible to the Automated Test Framework. Test designers can use these components as part of custom UI testing.

## Untestable page components

The Page Inspector identifies these types of untestable page components.

-   **Exclusion listed**

    Exclusion listed page components can't be tested using any **Custom UI** test steps. Exclusion listed page components typically include specialized ServiceNow AI Platform user interfaces and components already testable by other means. Test designers can't create custom UI tests for exclusion listed page components. To test these components, they must use another supported test category such as Forms or Service Catalog.

    In the Page Inspector, the exclusion listed interfaces are indicated by a grey background color when the inspect icon is dragged over them. A detailed message about the step category that needs to be used to test these components is displayed by dropping the inspect icon on an exclusion listed component.![Gif file showing the allowed part in the entire exclusion listed form.](../image/atf-page-inspector.gif)

    -   Lists can't be tested using custom UI test steps. Use [List and Related List](../reference/test-steps-list-related-list.md#) test step category to test lists.

        ![Warning message reading "List are exclusion listed"](../image/atf-list-message.png "Sample exclusion listed list message")

    -   Forms can't be tested using custom UI test steps. To test forms, use [Form category](../reference/test-steps-form-category.md#) test steps.

        ![Warning message reading "Forms are exclusion listed"](../image/atf-form-message.png "Sample exclusion listed form message")

        **Note:** The UI formatters within forms can be accessed and tested using custom UI test steps. See [Create a custom UI test](../task/create-custom-ui-test.md) for more information.

    -   Service Catalog items can't be tested using custom UI test steps. To test catalog items, use [Service Catalog category](../reference/test-steps-service-catalog-category.md#) test steps.

        ![Warning message reading "Service Catalog items are exclusion listed"](../image/atf-service-catalog-message.png "Sample exclusion listed catalog item message")

    -   Certain components are excluded from custom UI pages and are forbidden from being tested.

        ![Warning message reading "This component is exclusion listed"](../image/atf-component-blacklist.png "Sample exclusion listed component message")

    -   Workspaces can't be tested using custom UI test steps. To test forms in an available workspace, use [Form category](../reference/test-steps-form-category.md#) test steps.

        ![Warning message reading "Workspaces are exclusion listed"](../image/atf-workspace-message.png "Sample exclusion listed workspace message")

-   **Inaccessible**

    Inaccessible page components are elements that Automated Test Framework either cannot identify or does not have permission to test because of some configuration issue. Inaccessible page components typically include third-party JavaScript libraries or elements with a Shadow DOM. Test designers cannot create custom UI tests for inaccessible page components, but may be able to redesign the page to use components accessible to Automated Test Framework.

    -   Certain components are not accessible in the Automated Test Framework

        ![Warning message reading "This component is not accessible"](../image/atf-component-not-accessible.png "Sample inaccessible component message")

    -   Team development is not supported in the Automated Test Framework

        ![Warning message reading "Team Development is not supported in ATF"](../image/atf-team-dev-message.png "Sample unsupported component message")

    -   Testing external sites that are embedded in platform pages is not supported in the Automated Test Framework

        ![Warning message reading "The Automated Test Framework is unable to test external sites that are embedded in pages on this site"](../image/atf-page-inspector-external-site.png "Sample unsupported embedded external sites message")


-   **[Inspect different page types](../task/atf-inspect-page-types.md)**  
Inspect and troubleshoot the functionality of different page types like **UI Pages**, **Service Portal**, **Standard UI**, and **Custom URL** using the Page Inspector.

**Parent Topic:**[Custom UI test steps](custom-ui-test-steps.md)

