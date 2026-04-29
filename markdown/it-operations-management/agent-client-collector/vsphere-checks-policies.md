---
title: vSphere default checks and policies
description: Agent Client Collector provides the following default checks and policies for vSphere monitoring.
locale: en-US
release: australia
product: Agent Client Collector
classification: agent-client-collector
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Agent Client Collector Monitoring default checks and policies, ACC-M reference, Agent Client Collector reference, Agent Client Collector, IT Operations Management]
---

# vSphere default checks and policies

Agent Client Collector provides the following default checks and policies for vSphere monitoring.

<table id="table_kzz_mv4_f5b"><thead><tr><th>

Type

</th><th>

Check

</th><th>

Description

</th><th>

Usage

</th><th>

Output

</th></tr></thead><tbody><tr><td>

Metric

</td><td>

vsphere.metric-VirtualMachine

</td><td>

Retrieves metrics for a vSphere virtual machine. Must use a proxy agent.

</td><td>

`commonchecks metric-vsphere -H hostname -R VirtualMachine -v vm_id -r true -i 20` where:

-   -H = hostname Instance Hostname
-   -i = intervalId 20 for real time metrics; 300 for 5 minutes older aggregate metrics \(default 300\)
-   -r = resourceLevelMetric To enable resource level metrics \(default=false\)

</td><td>

`vsphere.VirtualMachine.disk.usage.average.total 8 1654755994`

</td></tr></tbody>
</table><table id="table_lfl_nv4_f5b"><thead><tr><th>

Type

</th><th>

Check

</th><th>

Description

</th><th>

Usage

</th><th>

Output

</th></tr></thead><tbody><tr><td>

Metric

</td><td>

vSphere.metric-Datastore

</td><td>

Retrieves Metrics for vSphere Datastore. Must use a proxy agent.

</td><td>

`commonchecks metric-vsphere -H hostname -R Datastore -v vm_id -r` where:

-   -H = hostname Instance Hostname
-   -r = resourceLevelMetric To enable resource level metrics \(default=false\)

</td><td>

`vsphere.Datastore.disk.capacity.latest.total 21474836480 1655182836`

</td></tr></tbody>
</table><table id="table_gcv_nv4_f5b"><thead><tr><th>

Type

</th><th>

Check

</th><th>

Description

</th><th>

Usage

</th><th>

Output

</th></tr></thead><tbody><tr><td>

Metric

</td><td>

vsphere.metric-Datacenter

</td><td>

Retrieves metrics for the vSphere datacenter.

</td><td>

`commonchecks metric-vsphere -H hostname -R Datacenter -v vm_id -r` where:

-   -H = hostname Instance Hostname
-   -r = resourceLevelMetric To enable resource level metrics \(default=false\)

</td><td>

```
vsphere.Datacenter.vmop.numChangeDS.latest.total 217 1655194924
vsphere.Datacenter.vmop.numChangeHost.latest.total 1373 1655194924
vsphere.Datacenter.vmop.numChangeHostDS.latest.total 9 1655194924
vsphere.Datacenter.vmop.numClone.latest.total 192 1655194924

```

</td></tr></tbody>
</table><table id="table_ztc_4v4_f5b"><thead><tr><th>

Type

</th><th>

Check

</th><th>

Description

</th><th>

Usage

</th><th>

Output

</th></tr></thead><tbody><tr><td>

Metric

</td><td>

vsphere.metric-ESX\_Server

</td><td>

Retrieves metrics for vSphere ESX server or HostSystem. Must use a proxy agent.

</td><td>

`commonchecks metric-vsphere -H hostname -R HostSystem -v vm_id -r` where:

-   -H = hostname Instance Hostname
-   -r = resourceLevelMetric To enable resource level metrics \(default=false\)

</td><td>

```
vsphere.HostSystem.net.broadcastRx.summation.total 63885 1655198166
vsphere.HostSystem.net.broadcastTx.summation.total 196 1655198166
vsphere.HostSystem.net.bytesRx.average.total 5924 1655198166
```

</td></tr></tbody>
</table>**Parent Topic:**[Agent Client Collector Monitoring default checks and policies](agent-policies-checks.md)

