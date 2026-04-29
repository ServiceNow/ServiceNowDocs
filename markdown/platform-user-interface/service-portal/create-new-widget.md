---
title: Create a new widget
description: Create a new widget to build a custom widget from scratch.
locale: en-US
release: australia
product: Service Portal
classification: service-portal
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Developing custom widgets, Service Portal, Configure UIs and portals, Configure user experiences]
---

# Create a new widget

Create a new widget to build a custom widget from scratch.

## Before you begin

Role required: admin or sp\_admin

## Procedure

1.  Navigate to **All** &gt; **Service Portal** &gt; **Service Portal Configuration**.

2.  Select **Widget Editor**.

3.  Click **Create a new widget**.

4.  Enter a name for the new widget.

    The widget ID is created automatically based on the widget name. You can then select **Create test page** to automatically create a page containing the widget.

    ![Create a new widget](../image/add-widget.png)

    **Note:** After completing development of a widget with a test page, delete the test page. Maintaining test pages can create clutter when managing pages.

5.  Click **Submit**.

    The widget HTML template, client script, and server script display in the widget editor. Basic script templates are included as a guide.

    **Note:** For server-side scripts, you can turn on using the ECMAScript 2021 \(ES12\) JavaScript mode if your application uses ES5 Standards mode or Compatibility mode. Scripts in applications with the JavaScript mode set to ECMAScript 2021 \(ES12\) use ECMAScript 2021 \(ES12\) by default. For more information, see [Turn on ECMAScript 2021 \(ES12\) mode for a script](https://www.servicenow.com/docs/access?context=set-es12-mode-scripts&version=australia&pubname=australia-api-reference&ft:locale=en-US).

    ![Widget editor IDE](../image/basic-widget.png)


**Parent Topic:**[Developing custom widgets](../concept/widget-dev-guide.md)

