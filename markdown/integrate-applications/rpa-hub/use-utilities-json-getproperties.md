---
title: Use the GetProperties component
description: Get the values of multiple properties from a JSON object by using the GetProperties component in RPA Desktop Design Studio.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/integrate-applications/rpa-hub/use-utilities-json-getproperties.html
release: xanadu
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [JSON, Utilities, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Creating integrations with applications]
---

# Use the GetProperties component

Get the values of multiple properties from a JSON object by using the GetProperties component in RPA Desktop Design Studio.

## Before you begin

Role required: none

## About this task

To configure the properties of the GetProperties component, see [Properties of the JSON utilities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/integrate-applications/rpa-hub/properties-utilities-json.md).

## Procedure

1.  In the Toolbox pane, navigate to **Utilities** &gt; **JSON**.

2.  Drag the GetProperties component to the Design surface.

3.  Click the component settings icon \(\[Omitted image "component-settings-icon.png"\] Alt text: Component settings icon.\).

4.  Click the Add property icon \(\[Omitted image "add-image-icon.png"\] Alt text: Add keys icon.\).

5.  Enter a property name.

6.  Repeat the steps to add multiple property names.

    A Data In port is added with each property that you add.

7.  Click **OK**.

8.  To configure the input fields, see [Configure port properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/integrate-applications/rpa-hub/configure-input-port-properties.md).

9.  Connect the data and control ports of the GetProperties component to the corresponding ports of the other components as described in the following table.

<table id="table_jnw_jn1_krb"><thead><tr><th>

Port type

</th><th>

Port name

</th><th>

Data type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Data In

</td><td>

JsonObject

</td><td>

Object

</td><td>

The JSON object from which to extract property values. JSON object to be passed from the previous component.

Serialize the JSON and pass it from the previous component to get properties.

Example of JSON object:

```
{
  "name": "Abel Tutor",
  "age": 30,
  "email": "abletutor@example.com",
  "address": {
    "street": "123 Main St",
    "city": "New York",
    "state": "NY",
    "zip": "10001"
  },
  "phoneNumbers": [
    {
      "type": "home",
      "number": "555-1234"
    },
    {
      "type": "work",
      "number": "555-5678"
    }
  ],
  "isActive": true
}

```

</td></tr><tr><td>

Data Out

</td><td>

Name of the port is the same as the name of the properties that you added.

</td><td>

Object

</td><td>

Returns the values of the properties.If no property value is found, the port return an error.

</td></tr></tbody>
</table>10. To test the component, right-click the component bar and click **Run From Here**.


**Parent Topic:**[JSON](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/integrate-applications/rpa-hub/json.md)

