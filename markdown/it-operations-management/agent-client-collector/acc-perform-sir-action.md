---
title: Perform an action on a security incident
description: Run an Agent Client Collector Security Incident Response action to gather more information on a security incident. Actions are referred to in the system as capabilities, and are configured with the base system.
locale: en-US
release: yokohama
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Agent Client Collector Security Incident Response, Agent Client Collector, IT Operations Management]
---

# Perform an action on a security incident

Run an Agent Client Collector Security Incident Response action to gather more information on a security incident. Actions are referred to in the system as **capabilities**, and are configured with the base system.

## Before you begin

Add the following JSON script to your Agent Client Collector allow list, to enable running the actions that come with the base system.

```

{
  "args": [
    "--logger_min_status 1",
    "--json",
    "SELECT p.name, p.state, p.pid, p.parent as ppid, p.path, p.total_size, p.start_time, p.elapsed_time as run_time, p.cmdline, p.uid, p.username, u.type as owner_domain, u.uuid FROM processes as p LEFT JOIN users as u ON u.uid = p.uid",
    "select name, process_open_sockets.pid, parent as ppid, processes.path, process_open_sockets.state, total_size, process_open_sockets.protocol, local_address, local_port, remote_address, remote_port from process_open_sockets, processes where process_open_sockets.pid = processes.pid",
    "select * from services order by service_type",
    "select computer_name, hardware_serial, hostname, name as os, build, version, mac, address from system_info, os_version, interface_details, interface_addresses where address like '%:%' and interface_addresses.type='manual' or interface_addresses.type ='dhcp' limit 1",
    "select * from logged_in_users order by time"
  ],
  "exec": "osqueryi",
  "skip_arguments": false
}
```

Role required: sn\_si.admin or sn\_si.basic

## About this task

For details on the capabilities that come with the base system, see [Agent Client Collector Security Incident Response capabilities](../reference/acc-sir-capabilities.md).

## Procedure

1.  Navigate to **All** &gt; **Security Incident** &gt; **Incidents** &gt; **Show All Incidents**.

2.  Select an incident.

3.  In the Related Links section, select **Agent Client Collector Capabilities**.

    The **Agent Client Collector Capabilities** dialog box opens.

4.  Select the capability you want to run.

<table id="table_orq_wnm_h5b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

ACC Integration Capabilities

</td><td>

The ACC Integration Capabilities.If the selected the capability you want is “Run OSQuery on Agent” then the data will be tabular formatted within the work notes.

</td></tr><tr><td>

ACC Integration OSQuery

</td><td>

The ACC Integration OSQuery. For example, Selected system info columns.

</td></tr><tr><td>

Transpose Data check box

</td><td>

Transpose the data. When selected,the information is displayed with vertical columns.

 ![Transpose selected](../image/transposed-column.png)

 When clear, the information is displayed horizontally.

 ![Transpose cleared](../image/Transposed-row.png)

</td></tr></tbody>
</table>5.  Select **Submit**.

    The selected capability runs on the security incident's CI.


**Parent Topic:**[Agent Client Collector Security Incident Response](../concept/acc-security-incident-response.md)

**Related topics**  


[Generate an Agent Client Collector allow list](acc-generate-allow-list.md)

