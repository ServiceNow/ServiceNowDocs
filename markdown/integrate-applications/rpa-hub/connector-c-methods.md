---
title: C\# connector methods
description: The C\# connector method enables you to execute the custom C\# scripts you had written while configuring the C\#.Net connector.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/integrate-applications/rpa-hub/connector-c-methods.html
release: zurich
product: RPA Hub
classification: rpa-hub
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [C\#.Net, Connectors, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# C\# connector methods

The C\# connector method enables you to execute the custom C\# scripts you had written while configuring the C\#.Net connector.

## Execute

Executes C\# scripts set up in the configuration window. Before executing the method, you must configure the connector. See [Configure the C\#.Net connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/configure-C-net-connector.md).

To execute, do the following steps.

1.  Click the method settings icon \(\[Omitted image "component-settings-icon.png"\] Alt text: Method settings icon\).
2.  From the **Classes** list, select the class defined during the configuration of the C\#.NET connector.
3.  From the **Methods** list, select the method defined during the configuration of the C\#.NET connector.
4.  Click **OK**.

    A Data Out port is created to return the output.

5.  To test the method, under the **DESIGN** tab, click **Run**.

|Parameter|Description|Data port type|Data type|Default value|Mandatory|
|---------|-----------|--------------|---------|-------------|---------|
|Result|Returns the output of the script.|Data Out|String|Not applicable|Not applicable|

**Parent Topic:**[C\#.Net](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/c.md)

