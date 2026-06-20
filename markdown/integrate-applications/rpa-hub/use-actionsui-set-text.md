---
title: Use the Set Text component
description: Set text in text boxes and drop-down lists within applications, check boxes, radio button controls, web pages on Internet Explorer browser or Windows applications by using the Set Text component in RPA Desktop Design Studio.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/integrate-applications/rpa-hub/use-actionsui-set-text.html
release: zurich
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Actions \(UI\), Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# Use the Set Text component

Set text in text boxes and drop-down lists within applications, check boxes, radio button controls, web pages on Internet Explorer browser or Windows applications by using the Set Text component in RPA Desktop Design Studio.

## Before you begin

Role required: none

## About this task

The Set Text component uses inter-process communication \(IPC\) to interact with application controls. You can use it to enter any text data, such as a user name, an address, or a survey response, in any situation where text entry is accepted.

You can configure the properties for the Set Text component. For more information about these properties, see [Properties of Actions \(UI\) components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/properties-actions-ui-components.md).

## Procedure

1.  In the Toolbox pane, navigate to **Actions \(UI\)** &gt; **Set Text**.

2.  Drag the Set Text component to the Design surface.

3.  In the Set Text component, click the camera icon \(\[Omitted image "camera-icon.png"\] Alt text: Camera icon.\).

    The `Press "CTRL+SHIFT" for selection` message appears.

4.  Press the **Ctrl + Shift** keys.

    The mouse device turns into a crossover icon \(\[Omitted image "crossover-icon.png"\] Alt text: Crossover icon.\).

5.  Drag the mouse device over the application to capture the area where the action will be performed and then release.

    **Tip:** Include a part of the image that does not change in your selection. This can help the automation find the capture area when the unchanging part is used as an anchor. To designate an anchor, see Step 7.

    The selected area is captured as an image in the Set Text component.

6.  Drag the green plus icon \(\[Omitted image "green-plus-icon.png"\] Alt text: Green plus icon.\) over the captured image and place on the location on the captured image where the component will perform an action.

7.  Add an anchor to the captured image by doing the following actions:

    An anchor is a unique identifier that enables the Set Text component to identify the location where the text is set. Although adding an anchor is a good approach, it's optional. If you don't add an anchor, the Set Text component treats the whole captured image as an anchor. For more information on anchor, see [Anchor](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/anchor.md).

    1.  In the Set Text component, right-click the image, and click **Add Anchor**.

        The anchor appears as a yellow rectangle with red borders.

    2.  To identify the location for the Set Text component, drag and place the anchor at the unique location on the image.

        **Tip:**

        To change the dimensions of the anchor, position the mouse device along the edge of the anchor until the mouse device turns into a diagonal two-sided arrow \(\[Omitted image "bi-sided-arrow.png"\] Alt text: Two-sided arrow.\) and then drag the anchor.

8.  Capture alternate images by doing the following actions:

    Alternate images prevent an execution failure when the Set Text component does not find the image that was captured first. In that case, the Set Text component then searches for alternate images to execute. You can add as many alternate images as you need.

    1.  In the Set Text component, click the component settings icon \(\[Omitted image "component-settings-icon.png"\] Alt text: Component settings icon.\).

    2.  In the ALTERNATE IMAGES window, click the add Image icon \(\[Omitted image "add-image-icon.png"\] Alt text: Add image icon.\).

    3.  Click the camera icon \(\[Omitted image "camera-icon.png"\] Alt text: Camera icon.\).

        The `Press "CTRL+SHIFT" for selection` message appears.

    4.  Press the **Ctrl + Shift** keys.

        The mouse device turns into a crossover icon \(\[Omitted image "crossover-icon.png"\] Alt text: Crossover icon.\).

    5.  Drag the mouse device over the part of the application where the Set Text component appends text.

        The selected area is captured as an alternate image in the Set Text component.

9.  To configure the text input, see [Configure port properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/configure-input-port-properties.md).

10. Connect the data and control ports of the Set Text component to the corresponding ports of the other components as described in the following table.

    To receive the text to send from another component in your automation, connect a Data Out port from the component that provides the text to the Data In port of the Set Text component. The Text Input parameter of the Data In port is described in the following table.

    |Port type|Port name|Data type|Purpose of connection|
    |---------|---------|---------|---------------------|
    |Data In|Text Input|String|Receives text from another component.|

11. To test the component, under the **DESIGN** tab, click **Run**.


## Enter a name in the Name field of a badging app

\[Omitted image "ActionSet\_SetText\_1.PNG"\] Alt text: Badging App.

In this example, the Set Text component will be used to enter a name in the Name field of the badging app.

\[Omitted image "ActionSet\_SetText.PNG"\] Alt text: Set Text in the component.

Set the name in the Text Input field, as shown in the image and run the component.

The name is set in the Name field, as shown in the image.

\[Omitted image "ActionSet\_SetText\_4.PNG"\] Alt text: Name set in the field.

**Parent Topic:**[Actions \(UI\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/actions-ui.md)

