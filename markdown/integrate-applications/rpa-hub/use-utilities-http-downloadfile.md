---
title: Use the DownloadFile component
description: Download a file over the HTTP protocol using the DownloadFile component in RPA Desktop Design Studio.
locale: en-US
release: zurich
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [HTTP, Utilities, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# Use the DownloadFile component

Download a file over the HTTP protocol using the DownloadFile component in RPA Desktop Design Studio.

## Before you begin

Role required: none

## About this task

You can configure the properties for the DownloadFile component. For more information about these properties, see [Properties of the HTTP components](../reference/properties-http-components.md).

## Procedure

1.  In the Toolbox pane, navigate to **Utilities** &gt; **HTTP**.

2.  Drag the DownloadFile component to the Design surface.

3.  To configure the input fields, see [Configure port properties](configure-input-port-properties.md).

4.  Connect the data and control ports of the DownloadFile component to the corresponding ports of the other components as described in the following table:

    |Port name|Port type|Data type|Purpose of connection|Mandatory?|
    |---------|---------|---------|---------------------|----------|
    |URL|Data In|String|Takes the URL from a previously executed component.|Yes|
    |FilePath|Data In|String|Takes the path to the file the method downloads from a previously executed component.|Yes|
    |UserName|Data In|String|Takes the user name to log in to the server from a previously executed component.|Yes|
    |Password|Data In|String|Takes the password to log in to the server from a previously executed component.|Yes|
    |RequestTimeout|Data In|Integer|Time value in seconds to timeout the download request. If the download request does not happen after the timeout value that you set, the download request fails and a connection timeout exception is displayed. The default value of timeout is 100 seconds.|Optional|
    |NA|Control In|NA|Passes the control through the Control In port of the next component.|Optional|
    |NA|Control Out|NA|Passes the control through the Control In port of the next component.|Optional|

5.  To test the component, under the **DESIGN** tab, click **Run**.


**Parent Topic:**[HTTP](../concept/http.md)

