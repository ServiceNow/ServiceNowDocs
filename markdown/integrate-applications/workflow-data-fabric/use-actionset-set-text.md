---
title: Use the ActionSet SetText action
description: Set text to fields on the Windows applications or the Internet Explorer browser by using the Set Text action in RPA Desktop Design Studio.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/workflow-data-fabric/use-actionset-set-text.html
release: australia
product: Workflow Data Fabric
classification: workflow-data-fabric
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Use the ActionSet component, Actions \(UI\), Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# Use the ActionSet SetText action

Set text to fields on the Windows applications or the Internet Explorer browser by using the Set Text action in RPA Desktop Design Studio.

## Before you begin

Capture an image of the target application window and create an anchor. For information about how to do this, see [Use the ActionSet component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/use-actionsui-actionset.md).

Role required: none

## About this task

The ActionSet Set Text action enters text in a field that you specify in the ActionSet Settings window. You can use it to enter any text data such as a user name, an address, a survey response, or in any situation where text entry is accepted.

You can configure the properties for the GetText component. For more information about these properties, see [ActionSet-Get Text properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/actionset-actions-properties.md).

## Procedure

1.  Right-click the anchor.

    To learn about the anchor, see how to use the [Anchor](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/anchor.md).

2.  Click **Get Text**.

3.  Drag the green plus icon \(\[Omitted image "green-plus-icon.png"\] Alt text: Green plus icon.\) to the location where you want to enter text.

4.  In the Properties pane of the ActionSet Settings window, configure the properties of the Set Text action.

    For example, you can set a delay or change the name of the action.

5.  Close the ACTIONSET SETTINGS window.

6.  If you didn’t hide the port for the SetText parameter in Step 4, connect the port so the action can receive the text to send to the target application.

    The SetText parameter is described in the following table.

    |Port type|Port name|Data type|Purpose of connection|
    |---------|---------|---------|---------------------|
    |Data In|SetText|String|Receives text from another component.|

7.  To test the component, right-click the component bar and then click **Run From Here**.


**Parent Topic:**[Use the ActionSet component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/use-actionsui-actionset.md)

