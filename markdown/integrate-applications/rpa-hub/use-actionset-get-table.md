---
title: Use the ActionSet Get Table action
description: Capture a table from the Windows applications, and web pages on the Internet Explorer browser by using the Get Table component in RPA Desktop Design Studio.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/integrate-applications/rpa-hub/use-actionset-get-table.html
release: zurich
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Use the ActionSet component, Actions \(UI\), Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# Use the ActionSet Get Table action

Capture a table from the Windows applications, and web pages on the Internet Explorer browser by using the Get Table component in RPA Desktop Design Studio.

## Before you begin

Capture an image of the target application window and create an anchor. For information about how to do this, see [Use the ActionSet component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/use-actionsui-actionset.md).

Role required: none

## About this task

The ActionSet Get Table action captures an entire table from a location that you specify in the ActionSet Settings window. You can choose to ignore the table header by setting the Ignore Header property in Step 4 of the procedure.

**Important:**

For the action to successfully capture table data, the target data must already be in table form. The action cannot convert ordinary text to table data.

You can configure the properties for the Get Table action. For more information about these properties, see [ActionSet- Get Table properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/actionset-actions-properties.md).

## Procedure

1.  Right-click the anchor.

    To learn about the anchor, see how to use the [Anchor](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/anchor.md).

2.  Click **Get Table**.

3.  Drag the green plus icon \(\[Omitted image "green-plus-icon.png"\] Alt text: Green plus icon.\) to the area in the target window that contains a table that you want to capture.

4.  In the Properties pane of the ActionSet Settings window, configure the properties of the Get Table action.

5.  Close the ACTIONSET SETTINGS window.

6.  If you didn’t hide the port for the Table action in Step 4, connect the port so the Table parameter can pass on the extracted table data.

    The Table parameter is described in the following table.

    |Port type|Port name|Data type|Purpose of connection|Notes|
    |---------|---------|---------|---------------------|-----|
    |Data Out|Table|DataTable|Returns the extracted table data.|The Data Out port is enabled by default. You can disable it in the PROPERTIES pane.|

7.  To test the component, right-click the component bar and then click **Run From Here**.


**Parent Topic:**[Use the ActionSet component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/use-actionsui-actionset.md)

