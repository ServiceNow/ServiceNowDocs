---
title: Use the IsLeapYear component
description: Specify a year to find out whether it's a leap year by using the IsLeapYear component in RPA Desktop Design Studio.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/integrate-applications/rpa-hub/use-datetime-isleapyear.html
release: zurich
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [DateTime, Utilities, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# Use the IsLeapYear component

Specify a year to find out whether it's a leap year by using the IsLeapYear component in RPA Desktop Design Studio.

## Before you begin

Role required: none

## About this task

You can configure the properties for the IsLeapYear component. For more information about these properties, see [Properties of the DateTime components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/util-datetime-prop.md).

## Procedure

1.  In the Toolbox pane, navigate to **Utilities** &gt; **DateTime**.

2.  Drag the IsLeapYear component to the Design surface.

3.  Drag the Now component to the Design surface.

4.  Drag the GetPart component to the Design surface.

5.  To configure the input field, see [Configure port properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/configure-input-port-properties.md).

6.  Connect the data and control ports of the IsLeapYear component to the corresponding ports of the other components as described in the following table and image.

    |Port Name|Port type|Data type|Purpose of connection|
    |---------|---------|---------|---------------------|
    |Year|Data In| |Passes the year that you specify from a previously executed component.|
    |Return|Data Out| |Returns **True** if the specified year is a leap year. Otherwise, it returns **False**.|

7.  To test the component, under the **DESIGN** tab, click **Run**.

    GetPart component extracts a date part from the Now component, and IsLeapYear determines if the year is a leap year.


## IsLeapYear component with GetPart and Now component

\[Omitted image "isleapyear-datetime-utlities-rpa.png"\] Alt text: GetPart component extracts a date part from the Now component, and IsLeapYear determines if the year is a leap year.

**Parent Topic:**[DateTime](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/datetime-utility.md)

