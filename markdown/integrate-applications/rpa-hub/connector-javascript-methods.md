---
title: JavaScript connector methods
description: Execute custom JavaScript with the Execute method as part of an automation in the RPA Desktop Design Studio.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/integrate-applications/rpa-hub/connector-javascript-methods.html
release: zurich
product: RPA Hub
classification: rpa-hub
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [JavaScript, Connectors, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# JavaScript connector methods

Execute custom JavaScript with the Execute method as part of an automation in the RPA Desktop Design Studio.

## Execute

Executes the custom JavaScript you have written. Before executing,

-   Configure the JavaScript connector before executing the method. To configure, see [Configure the JavaScript connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/configure-javascript-connector.md).
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

**Parent Topic:**[JavaScript](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/javascript.md)

