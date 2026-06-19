---
title: Use the Click component
description: Simulate the click actions of a mouse device by using the Click component in RPA Desktop Design Studio.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/workflow-data-fabric/use-actionsui-click.html
release: australia
product: Workflow Data Fabric
classification: workflow-data-fabric
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Actions \(UI\), Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# Use the Click component

Simulate the click actions of a mouse device by using the Click component in RPA Desktop Design Studio.

## Before you begin

Role required: none

## About this task

The Click component uses the Inter-Process Communication \(IPC\) to send the click events to an application. Use it to click buttons, controls, or anything that typically expects a mouse click.

The properties of the Click component are common with other Actions UI components, to configure these properties, see [Properties of Actions \(UI\) components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/properties-actions-ui-components.md).

## Procedure

1.  In the Toolbox pane, navigate to **Actions \(UI\)** &gt; **Click**.

2.  Drag the Click component to the Design surface.

3.  In the Click component, click the camera icon \(\[Omitted image "camera-icon.png"\] Alt text: Camera icon.\).

    The `Press "CTRL+SHIFT" for selection` message appears.

4.  Press the **Ctrl + Shift** keys.

    The mouse device turns into a crossover icon \(\[Omitted image "crossover-icon.png"\] Alt text: Crossover icon.\).

5.  Drag the mouse device over the application to capture the area where the action will be performed and then release.

    **Tip:** Include a part of the image that does not change in your selection. This can help the automation find the capture area when the unchanging part is used as an anchor. To designate an anchor, see Step 7.

    The selected area is captured as an image in the Click component.

6.  Drag the green plus icon \(\[Omitted image "green-plus-icon.png"\] Alt text: Green plus icon.\) over the captured image and place on the location where the component will perform an action.

7.  Add an anchor to the captured image by doing the following actions.

    An anchor is a unique identifier that enables the Click component to identify the content where the mouse device actions are simulated. Although adding an anchor is a good approach, it's optional. If you don't add an anchor, the Click component treats the whole captured image as an anchor. For more information on anchor, see the steps to use the [Anchor](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/anchor.md).

    1.  In the Click component, right-click the image, and click **Add Anchor**.

        The anchor appears as a yellow rectangle with red borders.

    2.  Drag and place the anchor at the unique location on the captured image.

        **Tip:** To change the dimensions of the anchor, position the mouse device along the edge of the anchor until the mouse device turns into a diagonal two-sided arrow \(\[Omitted image "bi-sided-arrow.png"\] Alt text: Two-sided arrow.\) and then drag the anchor.

8.  Capture alternate images by doing the following actions:

    Alternate images prevent an execution failure when the Click component doesn't find the image that was captured first. In that case, the Click component then searches for alternative images to execute. You can add as many alternate images as you need.

    1.  In the Click component, click the component settings icon \(\[Omitted image "component-settings-icon.png"\] Alt text: Component settings icon.\).

    2.  In the ALTERNATE IMAGES window, click the add image icon \(\[Omitted image "add-image-icon.png"\] Alt text: Add image icon.\).

    3.  Click the camera icon \(\[Omitted image "camera-icon.png"\] Alt text: Camera icon.\).

        The `Press "CTRL+SHIFT" for selection` message appears.

    4.  Press the **Ctrl + Shift** keys.

        The mouse device turns into a crossover icon \(\[Omitted image "crossover-icon.png"\] Alt text: Crossover icon.\).

    5.  Drag the mouse device over the application to capture the area where you want the component to perform an action and release.

        The selected area is captured as an image in the ALTERNATE IMAGES window.

    6.  Drag the green plus icon \(\[Omitted image "green-plus-icon.png"\] Alt text: Green plus icon.\) over the captured image and place on the location where you want the component to perform an action.

    7.  To close the ALTERNATE IMAGES window, click **OK**.

9.  To test the component, right-click the component bar and then click **Run From Here**.


## Automate the clicking of an HTML button

\[Omitted image "Actions\_Click.PNG"\] Alt text: Automate the clicking of an HTML button.

The Click component automates the clicking of the **Home** HTML button on the window. As a result, the user navigates to the home screen or window.

**Parent Topic:**[Actions \(UI\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/actions-ui.md)

