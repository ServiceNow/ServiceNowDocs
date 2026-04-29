---
title: Find the elements on the application screen
description: Use the locators of the captured elements to find the elements on the application screen while using the Universal App Connector \(UAC\) in the RPA Desktop Design Studio.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Universal app connector, Connectors, Automation components, RPA Desktop Design Studio, Workflow Data Fabric]
---

# Find the elements on the application screen

Use the locators of the captured elements to find the elements on the application screen while using the Universal App Connector \(UAC\) in the RPA Desktop Design Studio.

## Before you begin

Familiarize yourself with UAC concepts. For more information, see [Universal app connector](../concept/universal-app-connector.md).

Configure the UAC. For more information, see [Use the Universal App Connector](configure-uac.md).

Verify that you have open or active Windows, Java, Google Chrome, or Edge applications.

Role required: None

## About this task

The UAC provides multiple locator types. For example, the XPath locator provides the XPath to the element.

![Element locators.](../image/uac-connector-element-attributes.png "Locator types")

## Procedure

1.  In the Toolbox pane, navigate to **Connectors**, and drag **Universal App Connector** to **Global Objects** in the Project Explorer pane.

    The connector is added as a **UniversalApplication** object under **Global Objects**.

2.  Configure Universal App Connector and add a screen.

    For more information, see [Use the Universal App Connector](configure-uac.md).

3.  Under the Screens and elements pane, select an element under a screen.

4.  From the **Locator** list, select one of the element locators.

<table id="table_d5c_1pn_rzb"><thead><tr><th>

Locator type

</th><th>

Application type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Id

</td><td>

Web, Java, and Windows

</td><td>

Unique identifier of the element if its defined in the target application.

</td></tr><tr><td>

Name

</td><td>

Web, Java, and Windows

</td><td>

Unique name of the element if its defined in the target application.

</td></tr><tr><td>

CssSelector

</td><td>

Web

</td><td>

The CSS selector that locates the captured web element. For example, `div#navbarNav > ul > li > a`. If a web application supports Shadow DOM, the CSS Selector shows the path with the shadow DOM elements. For example, `html > body > shop-app > /ShadowDom/ > app-header[id="header"] > app-toolbar > div:nth-of-type(3) > a > paper-icon-button > /ShadowDom/ > iron-icon[id="icon"]`

</td></tr><tr><td>

TagName

</td><td>

Web

</td><td>

Unique tag name of the web element.

</td></tr><tr><td>

JavaScript

</td><td>

Web

</td><td>

Allows the user to define a custom JavaScript code to locate an element.

</td></tr><tr><td>

XPath

</td><td>

Web

</td><td>

XPath to locate the web element. If a web application supports Shadow DOM, this locator shows the full XPath with the Shadow DOM elements. For example, `html > body > shop-app > /ShadowDom/ > iron-pages > shop-home > /ShadowDom/ > div > h2`.

</td></tr><tr><td>

Type

</td><td>

Java and Windows

</td><td>

Enables you to locate a screen element by its type. For example, button or text box.When you select the `Type` locator, the UAC connector populates the **Value** field with the type of the element.

</td></tr><tr><td>

Path

</td><td>

Java and Windows

</td><td>

Enables you to locate a screen element by specifying its position in the hierarchy of screen elements.When you select the `Path` locator, the UAC connector populates the **Value** field with the path of the element.

</td></tr><tr><td>

CustomPath

</td><td>

Windows

</td><td>

Enables you to fine-tune or trim the path to an element.

</td></tr></tbody>
</table>
**Parent Topic:**[Universal app connector](../concept/universal-app-connector.md)

