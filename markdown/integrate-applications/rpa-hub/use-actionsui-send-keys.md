---
title: Use the Send Keys component
description: Send text to fields in web pages, Windows applications, or the Windows desktop using the Send Keys component in RPA Desktop Design Studio. Use the component to enter data to fields such as text boxes and lists and to send special keys such as Shift, Control, F1, and F2.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/integrate-applications/rpa-hub/use-actionsui-send-keys.html
release: zurich
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Actions \(UI\), Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# Use the Send Keys component

Send text to fields in web pages, Windows applications, or the Windows desktop using the Send Keys component in RPA Desktop Design Studio. Use the component to enter data to fields such as text boxes and lists and to send special keys such as Shift, Control, F1, and F2.

## Before you begin

Role required: none

## About this task

You can use the Send Keys component in situations where the Set Text component does not work or in any application where you need to send keyboard shortcuts or special functions via the keyboard.

You can use the Action Set Send Keys action to send keyboard shortcuts, regular text, or a combination of both. Enter key combinations in one set of square brackets per key combination as shown below. Any keys used in combination will be sent together as if simultaneously pressed. Keys outside brackets are sent in the order they appear in the input string. For example, the following sequence replaces text in a text box by selecting all the text \(CTRL + A\), sending the delete key, and then entering the regular text “ServiceNow”: `[ctrl+a][del]ServiceNow`

To see all the supported special keys and functions, click [Supported keys and functions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/supported-keys-and-functions.md).

Many properties of the Send Keys component are common with other Actions UI components, to configure these properties, see [Properties of Actions \(UI\) components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/properties-actions-ui-components.md).

The properties unique to the Send Keys component are given.

<table id="table_ay5_2vr_c5b"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Input Type

</td><td>

Type of keyboard input sent to the application. The default input is SendInput.-   **SendInput**: Simulates key strokes to the target application.
-   **SendKeys**: Simulates key strokes to the target application but has certain limitations. For example, it doesn't work with RDP sessions.

</td></tr></tbody>
</table>## Procedure

1.  In the Toolbox pane, navigate to **Actions \(UI\)** &gt; **Send Keys**.

2.  Drag the Send Keys component to the Design surface.

3.  Click the camera icon \(\[Omitted image "camera-icon.png"\] Alt text: Camera icon.\).

    The `Press "CTRL+SHIFT" for selection` message appears.

4.  Press the **Ctrl + Shift** keys.

    The mouse device turns into a crossover icon \(\[Omitted image "crossover-icon.png"\] Alt text: Crossover icon.\).

5.  Drag the mouse device over the application to capture the area where the component will perform an action and release.

    **Tip:** Include a part of the image that does not change in your selection. This can help the automation find the capture area when the unchanging part is used as an anchor. To designate an anchor, see Step 7.

    The selected area is captured as an image in the Send Keys component.

6.  Drag the green plus icon \(\[Omitted image "green-plus-icon.png"\] Alt text: Green plus icon.\) over the captured image and place at the location where the Send Keys component will perform an action.

7.  Add an anchor to the captured image by doing the following actions:

    An anchor is a unique identifier that enables the Send Keys component to identify the part where the component will perform an action. Although adding an anchor is a good approach, it's optional. If you don't add an anchor, the Send Keys component treats the whole captured image as an anchor. To view how to use the anchor, see the steps to use the [Anchor](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/anchor.md).

    1.  In the Send Keys component, right-click the image, and click **Add Anchor**.

        The anchor appears as a yellow rectangle with red borders.

    2.  To identify the part of the image for the Send Keys component, drag and place the anchor at the unique location on the image.

        **Tip:**

        To change the dimensions of the anchor, position the mouse device along the edge of the anchor until the mouse device turns into a diagonal two-sided arrow \(\[Omitted image "bi-sided-arrow.png"\] Alt text: Two-sided arrow.\) and then drag the anchor.

8.  Capture alternate images by doing the following actions:

    Alternate images prevent an execution failure when the Send Keys component doesn't find the image that was captured first. In that case, the Send Keys component searches for alternative images to execute. You can add as many alternate images as you need.

    1.  In the ALTERNATE IMAGES window, click the add image icon \(\[Omitted image "add-image-icon.png"\] Alt text: Add image icon.\)

    2.  Click the camera icon \(\[Omitted image "camera-icon.png"\] Alt text: Camera icon.\).

        The `Press "CTRL+SHIFT" for selection` message appears.

    3.  Press the **Ctrl + Shift** keys.

        The mouse device turns into a crossover icon \(\[Omitted image "crossover-icon.png"\] Alt text: Crossover icon.\).

    4.  Drag the mouse device over the part of the area where you want the component to execute and then release the mouse device.

        The selected area is captured as an image in the Send Keys component.

    5.  Drag the green plus icon \(\[Omitted image "green-plus-icon.png"\] Alt text: Green plus icon.\) over the captured image and place at the location where the Send Keys component will perform an action.

    6.  Click **OK**.

9.  On the Properties pane, under **General**, select **SendInput** or **SendKeys** from the Input Type list.

    The default action is **SendInput**.

10. To set the keys in the **Text Input** field, see [Configure port properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/configure-input-port-properties.md).

11. Connect the control ports of the Send Keys component to the control ports of the preceding and next components in the automation.

    Optionally, connect the Data In port of the Send Keys component to the Data Out port of a preceding component. The Text Input parameter of the Data In port is described in the following table.

    |Port type|Port name|Data type|Purpose of connection|
    |---------|---------|---------|---------------------|
    |Data In|Text Input|String|Receives key strokes to send from another component.|

12. To test the component, right-click the component bar and then click **Run From Here**.


## Submit employee name in a badging app

\[Omitted image "ActionSet\_SendKeys\_1.PNG"\] Alt text: Simulate keystrokes on the Send keys component.

The Send Keys component has captured the Badging app image. Now, the user sends the keys "Abel Tuter" to the component. The green plus icon \(\[Omitted image "green-plus-icon.png"\] Alt text: Green plus icon.\) is the location where the text will be entered. Now, run the component.

\[Omitted image "ActionSet\_SendKeys\_2.PNG"\] Alt text: The text "Abel Tuter" have been entered in the Badging app.

As the user runs the component, the text "Abel Tuter" are typed in the Name field.

\[Omitted image "ActionSet\_SendKeys.PNG"\] Alt text: The employee name is submitted.

Use the Send Keys component to click the **Print Badge** button and run the component. The employee name is submitted for badging.

**Parent Topic:**[Actions \(UI\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/actions-ui.md)

