---
title: Enable and use the page inspector
description: Enable a developer setting to inspect UI pages that open within the platform. Use the Manual Page Inspector to inspect pages that open in a new tab, such as Service Portal pages.
locale: en-US
release: yokohama
product: Automated Test Framework \(ATF\)
classification: automated-test-framework-atf
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Custom UI test steps, UI test steps, Building and running automated tests with the Automated Test Framework, Automated Test Framework \(ATF\) test building and execution, Automated Test Framework \(ATF\), Testing and debugging applications, Building applications]
---

# Enable and use the page inspector

Enable a developer setting to inspect UI pages that open within the platform. Use the Manual Page Inspector to inspect pages that open in a new tab, such as Service Portal pages.

## Before you begin

Role required: admin

## About this task

Identify the HTML and JavaScript page components in your user interfaces that are available for custom UI testing. Enable automated testing by ensuring that your user interfaces only contain testable page components.

## Procedure

1.  Enable the Page Inspector depending on the type of custom UI page you need to inspect.

    Note that some custom UI pages open in a new tab and can be inspected only manually.

<table id="choicetable_vxj_kgv_5fb"><thead><tr><th align="left" id="d127254e61">

Option

</th><th align="left" id="d127254e64">

Procedure

</th></tr></thead><tbody><tr><td id="d127254e70">

**Inspect page opening in the ServiceNow AI Platform.**

</td><td>

1.  Navigate to the record or URL for the page you would like to inspect.
2.  Open System Settings and select the Developer tab.
3.  Enable **Automated Test Framework Page Inspector**.
 The page opens in the Page Inspector and the inspect icon appears in the banner frame.

</td></tr><tr><td id="d127254e101">

**Inspect page opening in a new tab, such as a Service Portal page.**

</td><td>

1.  Navigate to **Automated Test Framework** &gt; **Manual Page Inspector**.
2.  Set the **Page Type** and select the page. If the page type is Service Portal, select the portal in which the page opens.
3.  Click **Inspect**.
 The page opens in the page inspector.

</td></tr></tbody>
</table>2.  Select a component to inspect.

    -   Drag the inspect icon \(![inspect icon](../image/inspect-icon.png)\) from the Page Inspector pane to a component on the page.
    -   Select an available component from the Page Inspector pane.
    The Page Inspector retrieves the list of testable page components when you first load a page. Testable components consist of standard HTML and JavaScript that are accessible to the Automated Test Framework. Test designers can use these components as part of custom UI testing.

3.  View component information and perform actions available in the **Action** field.

    Performing available actions helps you manually confirm which test steps are available to a component. For example, when you select **Click On Component**, the Page Inspector selects the component and displays the resulting page.


## What to do next

[Create a custom UI test](create-custom-ui-test.md)

**Parent Topic:**[Custom UI test steps](../concept/custom-ui-test-steps.md)

