---
title: Disable event collection
description: For performance reasons, you might want to disable the collection of events from a data source from which metric data is also collected. You can disable event collection for data sources such as Nagios XI server, SolarWinds monitoring system, and Zabbix server.
locale: en-US
release: xanadu
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Get started with Metric Intelligence, Activating Metric Intelligence, Metric Intelligence, Agent Client Collector Monitoring, Agent Client Collector, IT Operations Management]
---

# Disable event collection

For performance reasons, you might want to disable the collection of events from a data source from which metric data is also collected. You can disable event collection for data sources such as Nagios XI server, SolarWinds monitoring system, and Zabbix server.

## Before you begin

Role required: evt\_mgmt\_admin

**Note:** To restart event collection after it has been disabled, you will need to restore the connector's original script.

## Procedure

1.  Navigate to **All** &gt; **Event Management** &gt; **Integrations** &gt; **Connector Instances**.

2.  Select a connector instance for the data source for which to disable event collection.

    For example, select a connector instance for Nagios, SolarWinds, or Zabbix.

3.  Set **Event collection schedule \(seconds\)** to a large value such as 20,000,000.

    Such setting avoids unnecessary communication with the MID Server, optimizing performance.

4.  Click **Update**.

5.  Navigate to **MID Server** &gt; **Script Includes** and extend the connector's script \(such as **NagiosMetrics\_JS**, **SolarWindsJS**, or **ZabbixJS**\) by overriding the **execute** method.

    Add a code snippet such as the following, and then click **Update**:


## Snippet for Nagios

```
var NagiosJSCustom = Class.create();
 
// Extending Nagios default script
NagiosJSCustom.prototype = Object.extendsObject(NagiosJS, {
 
// Override execute method
                    execute: function() {
        var retVal = {};                                            
        retVal['status'] = SUCCESS.toString();
       retVal['error_message'] = "Disabled by custom Class, 'Last event collection status' will be 'error' and this is normal. To achieve success status, enable event pull in custom class(NagiosJSCustom)";
                                               
        return retVal;
    });
```

For the SolarWinds connector use:

```
var SolarWindsJSCustom = Class.create();
 
// Extending solarwinds default script
SolarWindsJSCustom.prototype = Object.extendsObject(SolarWindsJS, {
```

For the Zabbix connector use:

```
var ZabbixJSCustom = Class.create();
 
// Extending zabbix default script
ZabbixJSCustom.prototype = Object.extendsObject(ZabbixJS, {
```

