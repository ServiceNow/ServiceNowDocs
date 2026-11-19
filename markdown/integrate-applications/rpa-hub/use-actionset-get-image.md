---
title: Use the ActionSet GetImage action
description: Capture images from the desktop, Windows applications, and web pages on the Internet Explorer browser by using the GetImage component in RPA Desktop Design Studio.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/integrate-applications/rpa-hub/use-actionset-get-image.html
release: zurich
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Use the ActionSet component, Actions \(UI\), Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# Use the ActionSet GetImage action

Capture images from the desktop, Windows applications, and web pages on the Internet Explorer browser by using the GetImage component in RPA Desktop Design Studio.

## Before you begin

Capture an image of the target application window and create an anchor. For information about how to do this, see [Use the ActionSet component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/use-actionsui-actionset.md).

Role required: none

## About this task

The ActionSet Get Image action captures an image from the area that you specify in the ActionSet Settings window. For example, you can use it to capture a product image or a user’s profile picture.

You can configure the properties for the GetImage component. For more information about these properties, see [ActionSet- Get Image properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/actionset-actions-properties.md).

## Procedure

1.  Right-click the anchor.

    To know about the anchor, see how to use the [Anchor](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/anchor.md).

2.  Click **Get Image**.

3.  Drag the green rectangle icon \(\[Omitted image "green-rectangle.png"\] Alt text: Green rectangle icon.\) over the location of the image that you want to capture.

    If necessary, adjust the size of the selection rectangle by dragging its edges.

4.  In the Properties pane of the ActionSet Settings window, configure the properties of the Get Image action.

    For example, you can set a delay or change the name of the action.

5.  To change the default area in the image covered by the green rectangle icon \(\[Omitted image "green-rectangle.png"\] Alt text: Green rectangle icon.\), do the following steps.

    1.  Place the mouse device along the edges of the green rectangle icon \(\[Omitted image "green-rectangle.png"\] Alt text: Green rectangle icon.\).

        The mouse device turns into a two-sided arrow \(\[Omitted image "bi-sided-arrow.png"\] Alt text: Two-sided arrow\).

    2.  Drag the edges of the green rectangle icon \(\[Omitted image "green-rectangle.png"\] Alt text: Green rectangle icon.\).

6.  Close the ACTIONSET SETTINGS window.

7.  If you didn’t hide the port for the GetImage parameter in Step 4, connect the port so the action can transmit the captured image for use.

    The GetImage parameter is described in the following table.

    |Port type|Port name|Data type|Purpose of connection|
    |---------|---------|---------|---------------------|
    |Data Out|Table|Bitmap|Sends the captured image to another component.|

8.  To test the component, right-click the component bar and click **Run From Here**.


**Parent Topic:**[Use the ActionSet component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/use-actionsui-actionset.md)

