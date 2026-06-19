---
title: Configure the JavaScript connector
description: Configure the JavaScript connector by writing custom script and validating custom classes and functions. Then you execute the script by providing values for the functions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/workflow-data-fabric/configure-javascript-connector.html
release: australia
product: Workflow Data Fabric
classification: workflow-data-fabric
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [JavaScript, Connectors, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# Configure the JavaScript connector

Configure the JavaScript connector by writing custom script and validating custom classes and functions. Then you execute the script by providing values for the functions.

## Before you begin

Ensure you have installed the Scripting plugin on the RPA Desktop Design Studio. To install, see [Manage plugins in RPA Desktop Design Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/install-plugins-rpa-studio.md).

Role required: Developer

## Procedure

1.  In the Toolbox pane, navigate to **Connectors** &gt; **JavaScript**.

2.  Drag the **JavaScript** connector to **Global Objects** in the Project Explorer pane.

3.  Right-click the **JavaScript** connector in **Global Objects** and select **Configure**.

    The Script Editor window is displayed.

4.  Enter the custom JavaScript in the Script pane.

    \[Omitted image "jscript-scripteditor.png"\] Alt text: Script pane in Script Editor

5.  Select **Validate**.

    If your custom script has any errors, it is displayed in the Errors pane. Resolve the errors and select **Validate** to check for errors again.

    \[Omitted image "jscript-error.png"\] Alt text: Error pane for Script Editor

6.  Click **OK**.

    If you want to save the changes, select **Yes**. An error validation is performed again and the changes are saved. If you want to discard the changes, select **No**.


## What to do next

The custom script you created by using the JavaScript connector is now ready to be used in your automation.

**Parent Topic:**[JavaScript](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/javascript.md)

