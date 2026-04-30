---
title: Configuring the ADM adapter for Service Graph Connectors
description: You can configure the Application Dependency Mapping \(ADM\) adapter to populate running processes, TCP connections, and applications into CMDB.
locale: en-US
release: yokohama
product: CMDB Integration Commons
classification: cmdb-integration-commons
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Integration Commons for CMDB, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Configuring the ADM adapter for Service Graph Connectors

You can configure the Application Dependency Mapping \(ADM\) adapter to populate running processes, TCP connections, and applications into CMDB.

As a user with the admin role, you can use the **ADMHelper** script include to configure the ADM adapter that populates running processes, TCP connections, and applications into CMDB. The **ADMHelper** script include is available within the Integration Commons for CMDB \(sn\_cmdb\_int\_util\) store app. The **ADMHelper** script include invokes the **ApplicationDependencyMapping** script include that is available within the Discovery and Service Mapping Patterns application \(sn\_itom\_pattern\).

The ADM adapter requires the inputs as discussed in the following table:

|Input|Input type|
|-----|----------|
|Running Process Details|Required|
|Computer Sys Id|Required|
|TCP connection details|Optional|
|ADM Properties|Optional|

For interpreting and populating the CIs, the ADM processor requires the input data in a specific format. Ensure that the keys are formed as shown in the following example:

<table id="table_qf5_5jq_5wb"><thead><tr><th>

TCP connections data

</th><th>

Running process

</th></tr></thead><tbody><tr><td>

```
[
{
"pid": "1068",
"local_ip": "127.0.0.1",
"local_port": "199",
"ip": "0.0.0.0",
"port": "199",
"state": "LISTEN",
"type": "on"
}
]
```

</td><td>

```
[
   {
"pid": "1",
"ppid": "0",
"command": "/usr/lib/systemd/systemd", "name": "systemd",
"parameters": "--switched-root --system --deserialize 21"
}
 
]
```

</td></tr></tbody>
</table>The **ApplicationDependencyMapping** script include processes TCP connections and running process data and populates the following tables:

-   TCP Connections \[cmdb\_tcp\]
-   Running Process \[cmdb\_running\_process\]
-   Application \[cmdb\_ci\_appl\]

**Note:** After the data is populated into the TCP Connections \[cmdb\_tcp\] and Running Process \[cmdb\_running\_process\] tables, the **ApplicationDependencyMapping** script include reconciles the TCP connections and running process data for populating the Application \[cmdb\_ci\_appl\] table based on the data in the Network Adapter \[cmdb\_ci\_network\_adapter\] and IP Address \[cmdb\_ci\_ip\_address\] tables. Classified processes are added to the corresponding child class in the Application \[cmdb\_ci\_appl\] table. The addition of unclassified processes to the Application \[cmdb\_ci\_appl\] table depends on the system property value.

