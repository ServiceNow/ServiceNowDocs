---
title: Custom UI test steps
description: Test customized user interfaces such as UI pages and UI macros by retrieving their HTML and JavaScript page components and identifying the test actions they support.
locale: en-US
release: australia
product: Automated Test Framework \(ATF\)
classification: automated-test-framework-atf
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 9
breadcrumb: [UI test steps, Building and running automated tests with the Automated Test Framework, Automated Test Framework \(ATF\) test building and execution, Automated Test Framework \(ATF\), Testing and debugging applications, Building applications]
---

# Custom UI test steps

Test customized user interfaces such as UI pages and UI macros by retrieving their HTML and JavaScript page components and identifying the test actions they support.

Custom UI test steps require the Automated Test Framework to retrieve and identify the testable components from a target web page.

**Note:** Next UI Experience pages are not supported by the Custom UI test steps, including but not limited to Configurable Workspaces \(except for Form steps\) and UI Builder.

## Testable components

Testable page components consist of standard HTML and JavaScript with these characteristics.

-   **Are set or clicked by user interaction**

    Testable page components allow users to set a value or click them.

-   **Are accessible from the Document Object Model \(DOM\)**

    Testable page components are accessible from the DOM and support JavaScript manipulation of the DOM. Custom UI test steps cannot access page components in the shadow DOM.

-   **Are accessible to JavaScript**

    Testable page components are accessible to JavaScript. Custom UI test steps cannot access page components that interact directly with the operating system such as file fields or display non-HTML content such as Excel or PDF files.

    New browser tabs or windows are not supported by Custom UI test steps.

-   **Are not excluded from custom UI testing**

    Testable page components are not excluded from custom UI testing. Automated Test Framework excludes page components that are already testable by other test step categories and also excludes page components associated with ServiceNow AI Platform features.

-   **Are accessible to the Page Inspector**

    Testable page components must return results when viewed from the [Page Inspector](atf-page-inspector.md). Test designers can use the Page Inspector to identify the testable components of a page.


Examples of testable page components include these UI elements.

-   Buttons
-   Links
-   Page text
-   UI controls
-   UI macros
    -   ui\_date
    -   ui\_date\_time
    -   ui\_reference
-   UI pages
-   Wizards

Examples of untestable page components include these UI elements.

|Reason untestable|Untestable page components|
|-----------------|--------------------------|
|Are not settable or clickable|Hidden controls|
|HTML comments|
|HTML layout elements such as div, section, and span.|
|HTML script elements|
|Are inaccessible from DOM|Dashboards|
|Images|
|Lists|
|Reports|
|Shadow DOM|
|Are inaccessible to JavaScript|Excel files|
|File fields|
|PDF files|
|Are ServiceNow AI Platform features|Flow Designer|
|Studio|
|Upgrade Monitor|
|Are testable by other test step categories|Form field labels|
|Form field values|
|Service Catalog|
|Workspaces|

## Settable page components

A settable component is a UI element that has a dynamic value such as a text input field. Settable components support these test actions and test steps.

|Page Inspector actions|Custom UI test steps|
|----------------------|--------------------|
|Set Component Value|Set Component Values \(Custom UI\)|
|Get Component Value|Assert Text on Page \(Custom UI\)|
|Component Value Validation \(Custom UI\)|
|Is Component Disabled|Component State Validation \(Custom UI\)|

Settable components have a data type that determines what values a Custom UI test step can set. For example, a page component intended to display a reference to a particular record can have a reference data type to only display Sys ID values.

Automated Test Framework allows UI developers to specify a data type to use during custom UI testing. UI developers can assign page components a data type to ensure that a test step sets a valid value. These data types are supported.

-   Date
-   Date Time
-   Reference

See [Override component data type](../task/override-component-data-type.md) for more information.

## Clickable page components

A clickable component is a UI element that users can interact with by clicking, such as inputs of type check box or radio. Clickable components support these test actions.

|Page Inspector actions|Custom UI test steps|
|----------------------|--------------------|
|Click On Component|Click Component \(Custom UI\)|
|Get Component Value|Assert Text on Page \(Custom UI\)|
|Component Value Validation \(Custom UI\)|
|Is Component Disabled|Component State Validation \(Custom UI\)|

Clickable components do not have a data type since they do not have dynamic values.

## Retrieved page components

Automated Test Framework stores a list of the retrieved page components for each custom UI page you test. Custom UI test steps display the list of retrieved components from the **Component** and **Component values** fields.

By default, the list of page components is static and is only updated when Test designers manually click **Retrieve Components**. Administrators can enable the system property **sn\_atf.page\_data\_capture.enabled** to refresh the list of page components every time a Custom UI test step is run. Enabling this property during test design ensures that your test designers always have access to the most current list of page components. Disabling this property after test design is complete allows your tests to run faster because test steps can use the previously retrieved list of page components.

The ServiceNow AI Platform treats the list of retrieved page components as data and does not include them in update sets or applications files. When transferring tests from one instance to another, test designers must manually retrieve page components again.

## Design considerations

Follow these design considerations when testing custom UI pages and page components.

-   **Use the page inspector to identify testable page components**

    The page inspector determines which page components are available for custom UI testing. Page components that are unavailable to the page inspector are unavailable to custom UI testing.

-   **Navigate to the custom UI you want to test**

    Use existing test steps to navigate to the target custom UI. For example, to test a Knowledge Base article, use the existing test steps to navigate to a module or to open an existing record. Most custom UI testing requires using existing test step categories as part of the test.

-   **Use the component area to identify page components**

    The component area describes the HTML layout element containing the component such as a `<div>` or `<section>` element. The area helps test designers distinguish between components by providing the location in the page layout.

-   **Test your custom UI rather than ServiceNow AI Platform UI**

    The Automated Test Framework prevents custom UI testing of ServiceNow AI Platform features. For example, you cannot test dashboards or graphical designers. Instead, build tests to validate your custom UI pages and elements since you have direct control over these user interfaces.

-   **Use HTML attributes to override page component testing properties**

    Change the testing properties of a particular page component using HTML attributes that are specific to Automated Test Framework. See [Override component test actions](../task/develop-testable-components.md#).

-   **Retrieve page components again when you move tests to another instance**

    Custom UI test steps do not store UI components as metadata. Testers must manually retrieve page components again when moving tests between instances.


## Example custom UI testing

You can use the list of retrieved components to design custom UI test steps. For example, suppose that you want to test reviewing and commenting on a Knowledge Base article. A Knowledge Base article contains several page components that require custom UI steps to test.

![Page displaying KB0011110 "ServiceNow Secure Coding guide for Instance developers"](../image/atf-example-custom-ui-kb-article.png "Example Knowledge article page")

For example, these page components require custom UI test steps.

1.  The number of article views.
2.  The buttons to mark the article as **Helpful**.
3.  The text area to **Leave a comment**.

These steps demonstrate custom UI testing on a Knowledge Base article. The example test consists of these existing and custom UI test steps.

1.  **Navigate to Module**. Navigate to the 'Published' module in the 'Knowledge' application.
2.  **Open an Existing Record**. Open the 'Knowledge' form with id 'Knowledge: KB0011110'.
3.  **Click a UI Action**. Click UI Action 'View Article' on 'Knowledge' form.
4.  **Assert Text on Page \(Custom UI\)**. Assert that the text 'developers' is on the page.
5.  **Set Component Values \(Custom UI\)**. Set the components on the page as follows: 'Textarea &lt;textarea&gt; \[article\_comments\]' = Update with actual article rather than URL to article elsewhere.
6.  **Click Component \(Custom UI\)**. Click the component: 'Button &lt;button&gt;: Comment'.
7.  **Assert Text on Page \(Custom UI\)**. Assert that the text 'Update with actual article rather than URL to article elsewhere.' is on the page.

![Screenshot displaying example test with seven test steps.](../image/atf-example-kb-test-steps-enlarged.png "Example test steps for a knowledge base article test")

## Custom UI component version and order

When you select a component in any of the custom UI test steps, the Custom UI version might show up. If there are multiple duplicate components, the order of the components show up.

![Image showing order for duplicate components](../image/atf-version-order.png)

**Note:**

-   The Custom UI version shows up only if there are at least two different components with different Custom UI versions.
-   The Order shows up only if there are duplicate components in the component drop-down menu. You can disambiguate them according to the displayed order.
-   Both Custom UI version and Order show up if there are multiple duplicate components from different versions.

## Identifying components

Implement an alternative way to identify your component by using the sn-atf-id attribute. This is useful if the name or id attribute of your component is dynamic and changes every time a test runs. Add the sn-atf-id attribute with a consistent value to allow ATF identify your component when running a test. It also allows you to identify your component when building a test. For example, in a button component

```
<button sn-atf-id="consistentValue">Test</button>
```

**Note:** Starting with the Rome release, if you have exactly one component on the page that has sn-atf-id attribute, ATF finds that component irrespective of any other attributes on that component.

## Improve ATF component identification

Identify your component using the label path included in the **Page area** column. Starting with the Rome release, the `sn_atf.element.use_label_path` property has been set to true by default.

If a component has the `sn-atf-area` attribute, the **Page area** column displays the `sn-atf-area` value. If the `sn-atf-area` attribute is not present, the label path for that component is shown in the Page area column.

![Image showing label path of the component](../image/atf-label-path.png)

**Note:** If you have multiple, identically named **Label** values, the label path helps you identify the correct component. If a component doesn't have an `sn-atf-area` attribute or a label path, the value is displayed as default.

![Image showing default value of components](../image/atf-default.png)

When you select the required component from the list and click **Submit**, the description of the test step also gets updated with more details.

![Image showing an updated description of a submitted test step](../image/atf-description.png)

-   **[Page Inspector](atf-page-inspector.md)**  
Identify the HTML and JavaScript page components in your user interfaces that are available for custom UI testing. Enable automated testing by ensuring that your user interfaces only contain testable page components.
-   **[Enable and use the page inspector](../task/enable-page-inspector.md)**  
Enable a developer setting to inspect UI pages that open within the platform. Use the Manual Page Inspector to inspect pages that open in a new tab, such as Service Portal pages.
-   **[Create a custom UI test](../task/create-custom-ui-test.md)**  
Test components in custom UI pages.
-   **[Override component test actions](../task/develop-testable-components.md#)**  
Change the testing properties of a particular page component using HTML attributes that are specific to Automated Test Framework.
-   **[Override component data type](../task/override-component-data-type.md)**  
Use the `sn-atf-data-type` and `sn-atf-data-type-params` attributes to override the type of field displayed in a Set Component Value test step.
-   **[Select2 functionalities in ATF](atf-select2.md)**  
Use the Select2 component to search and select your option from a drop-down menu easily.

**Parent Topic:**[UI test steps](ui-test-steps.md)

