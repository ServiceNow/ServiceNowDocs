---
title: JavaScript connector methods
description: Execute custom JavaScript with the Execute method as part of an automation in the RPA Desktop Design Studio.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/workflow-data-fabric/connector-javascript-methods.html
release: australia
product: Workflow Data Fabric
classification: workflow-data-fabric
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [JavaScript, Connectors, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# JavaScript connector methods

Execute custom JavaScript with the Execute method as part of an automation in the RPA Desktop Design Studio.

## Execute

Executes the custom JavaScript you have written. Before executing,

-   Configure the JavaScript connector before executing the method. To configure, see [Configure the JavaScript connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/configure-javascript-connector.md).
-   Configure the Execute method.

## Configure the Execute method

1.  Click the method settings icon \(\[Omitted image "component-settings-icon.png"\] Alt text: Method settings icon\).
2.  Select the class from the **Classes** list as set in the custom JavaScript you had written.
3.  Select the method from the **Methods** list as set in the custom JavaScript you had written.
4.  Click **OK**.

    A Data In port is created to accept the value for the function you have created.


|Parameter|Description|Data port type|Data type|Default value|Mandatory?|
|---------|-----------|--------------|---------|-------------|----------|
|Function value|Accepts the value for the function you have created.|Data in|Object|None|Yes|
|Result|Returns the output of the custom JavaScript execution.|Data out|String|None|Not applicable|

**Parent Topic:**[JavaScript](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/javascript.md)

