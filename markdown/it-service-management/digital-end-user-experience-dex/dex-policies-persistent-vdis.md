---
title: DEX policies for persistent VDIs
description: Policy reference for DEX monitoring on Windows persistent Virtual Desktop Infrastructures \(VDI\). Use this reference to understand available check instances, frequencies, and parameters for application, network, and device monitoring.
locale: en-US
release: australia
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: reference
last_updated: "2026-04-02"
reading_time_minutes: 2
breadcrumb: [DEX Content Playbook reference, Reference, Digital End-User Experience, IT Service Management]
---

# DEX policies for persistent VDIs

Policy reference for DEX monitoring on Windows persistent Virtual Desktop Infrastructures \(VDI\). Use this reference to understand available check instances, frequencies, and parameters for application, network, and device monitoring.

## Policies for Windows persistent VDIs — Application

DEX provides the following policies for persistent VDI applications.

<table id="table_hxg_t1b_bxb"><thead><tr><th>

Check instance

</th><th>

Description

</th><th>

Frequency

</th><th>

Historical or latest

</th><th>

Check instance parameters\*

</th></tr></thead><tbody><tr><td>

os.win.check-app-historical

</td><td>

Collects the application metrics in the persistent VDI Windows device and sends the metric data to Metric Base.

</td><td>

5 mins

</td><td>

Historical

</td><td>

cpu\_usage, memory\_usage, uptime, last\_access\_time, crashes, io\_usage\_read, io\_usage\_write, is\_running, freezes, zscaler\_service\_status

</td></tr><tr><td>

os.win.check-app-sccm-latest

</td><td>

Collect application-specific metrics for the Microsoft System Center Configuration Manager app on the persistent VDI Windows device.

</td><td>

24 hours

</td><td>

Latest

</td><td>

Not applicable

</td></tr><tr><td colspan="5">

**Important:** \* DEX Windows Apps Metrics with the uptime check instance parameter only runs with the Local System account.

</td></tr></tbody>
</table>## Policies for Windows persistent VDIs — Application Network Experience

**Note:** These policies have the following limitations:

-   A tracert command is used to get the network path.
-   ANE doesn't work for path in the domain URL. Example: &lt;domain&gt;/&lt;path&gt;

DEX provides the following policies for persistent VDIs applications.

|Check instance|Description|Frequency|Historical or latest|Check instance parameters|
|--------------|-----------|---------|--------------------|-------------------------|
|os.win.check-app-dom-network-historical|Collects Windows installed apps network monitoring metrics like latency, packet loss, and jitter and sends monitoring data to Metric Base and the ServiceNow® instance.|10 mins|Historical|domain\_network\_details|
|os.win.check-web-app-dom-net-historical|Collects Windows Web apps network monitoring metrics like latency, packet loss, and jitter and sends monitoring data to Metric Base and the ServiceNow instance.|10 mins|Historical|domain\_network\_details|

## Policies for Windows persistent VDIs — Device

DEX provides the following policies for persistent VDI devices.

<table id="table_cj5_4yd_1fc"><thead><tr><th>

Check instance

</th><th>

Description

</th><th>

Frequency

</th><th>

Historical or latest

</th><th>

Check instance parameters\*

</th></tr></thead><tbody><tr><td>

os.win.check-system-metrics-latest

</td><td>

Collects Windows device metrics and sends the metric data to the ServiceNow instance.

</td><td>

24 hours

</td><td>

Latest

</td><td>

uptime, logged\_in, antivirus\_enabled, firewall\_enabled, disk\_details, device\_details, battery\_details, bsod\_details, cpu\_details, os\_details, power\_plan, stability\_index, pending\_updates, network\_details, bitlocker\_details, user\_profiles, antimalware\_details, hard\_drive\_status, peripheral\_devices\_details, device\_events, last\_access\_time, os\_setup\_details, cpu\_usage, memory\_details, bios\_details, network\_connection\_profiles, network\_adapter\_details, boot\_details, reboot\_details

</td></tr><tr><td colspan="5">

**Important:** \* DEX Windows Device Metrics with the following check instance parameters runs only with a Local System account: bitlocker\_details, last\_access\_time, pending\_updates, user\_profiles.

</td></tr><tr><td>

os.win.check-system-metrics-historical

</td><td>

Collects Windows device metrics and sends the metric data to MetricBase.

</td><td>

30 mins

</td><td>

Historical

</td><td>

network\_connection\_profiles

</td></tr><tr><td>

os.win.check-system-metrics-historical

</td><td>

Collects Windows device metrics and sends the metric data to MetricBase.

</td><td>

5 mins

</td><td>

Historical

</td><td>

disk\_usage, disk\_available, io\_usage\_write, io\_usage\_read, memory\_details, cpu\_usage, battery\_charge\_percentage, energy\_consumption, wifi\_transmit\_rate, wifi\_receive\_rate, wifi\_signal\_strength, uptime, disk\_details, cpu\_performance\_details, crashes, power\_consumption, gpu\_usage, gpu\_vram\_usage

</td></tr><tr><td>

os.win.check-process-data

</td><td>

Collects data for running Windows processes and sends the data to the ServiceNow instance.

</td><td>

24 hours

</td><td>

Not applicable

</td><td>

Not applicable

</td></tr><tr><td>

os.win.check-sys-compliance-historical

</td><td>

Collects Windows device metrics and sends the metric data to the ServiceNow instance.

</td><td>

5 mins

</td><td>

Historical

</td><td>

Not applicable

</td></tr><tr><td>

os.win.check-sys-compliance-latest

</td><td>

Collects Windows device metrics and sends the metric data to the ServiceNow instance.

</td><td>

24 hours

</td><td>

Latest

</td><td>

Not applicable

</td></tr><tr><td>

os.win.check-system-executables-latest

</td><td>

Collects all the executables present on all volumes of a Windows device.

</td><td>

24 hours

</td><td>

Latest

</td><td>

config\_file\_read

</td></tr><tr><td>

os.win.check-system-registry-latest

</td><td>

Gets registry data on Windows device.

</td><td>

24 hours

</td><td>

Latest

</td><td>

config\_file\_read

</td></tr></tbody>
</table>**Parent Topic:**[DEX Content Playbook reference](dex-content-playbook-reference.md)

