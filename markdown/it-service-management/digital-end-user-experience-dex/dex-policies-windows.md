---
title: DEX policies for Windows
description: Use policies for Windows are guidelines and rules to confirm that the application is used consistently, securely, and in compliance. DEX policies help organizations to reduce the risk of data breaches, improve data quality and accuracy, and optimize application performance and availability.
locale: en-US
release: yokohama
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [DEX Content Playbook reference, Reference, Digital End-User Experience, IT Service Management]
---

# DEX policies for Windows

Use policies for Windows are guidelines and rules to confirm that the application is used consistently, securely, and in compliance. DEX policies help organizations to reduce the risk of data breaches, improve data quality and accuracy, and optimize application performance and availability.

To fetch the complete playbook data for a Windows device, the Agent Client Collector \(ACC\) must run as a local system account. For more details on how to set up the ACC service as a local system account, see [Run ACC as a local system account user](../task/run-acc-local-sys-account.md).

**Note:** The historical data for an application or device is the information that is kept in the MetricBase database for the past 7 days, while the latest data pertains to the most recent information available.

## Policies for Windows — Application

DEX provides the following policies for applications.

<table id="table_hxg_t1b_bxb"><thead><tr><th>

Policy name

</th><th>

Description

</th><th>

Check instance

</th><th>

Frequency

</th><th>

Historical or latest

</th><th>

Check instance parameters\*

</th></tr></thead><tbody><tr><td>

DEX Windows Apps Metrics

</td><td>

Collects the application metrics in the Windows device and sends the metric data to Metric Base.

</td><td>

os.win.check-app-historical

</td><td>

5 mins

</td><td>

Historical

</td><td>

cpu\_usage, memory\_usage, uptime, last\_access\_time, crashes, io\_usage\_read, io\_usage\_write, is\_running

</td></tr><tr><td colspan="6">

**Important:** \* DEX Windows Apps Metrics with the uptime check instance parameter only runs with the Local System account.

</td></tr></tbody>
</table>## Policies for Windows — Application Network Experience

Before configuring the following policies, make sure that the Agent Client Collector is version 4.2 or higher to display the network path for applications. Additionally, the DEX browser extension plugin must be installed and should be version 2.5.0 or higher to fetch network metrics for web applications.

**Note:** These policies have the following limitations:

-   A tracert command is used to get the network path.
-   ANE doesn't work for path in the domain URL. Example: &lt;domain&gt;/&lt;path&gt;

DEX provides the following policies for applications.

|Policy name|Description|Check instance|Frequency|Historical or latest|Check instance parameters|
|-----------|-----------|--------------|---------|--------------------|-------------------------|
|DEX Windows Apps Domain Network Monitoring Metrics|Collects Windows installed apps network monitoring metrics like latency, packet loss, and jitter and sends monitoring data to Metric Base and the ServiceNow® instance.|os.win.check-app-dom-network-historical|10 mins|Historical|domain\_network\_details|
|DEX Windows Apps Domain Network Monitoring Metrics|Collects Windows Web apps network monitoring metrics like latency, packet loss, and jitter and sends monitoring data to Metric Base and the ServiceNow instance.|os.win.check-web-app-dom-net-historical|10 mins|Historical|domain\_network\_details|
|DEX Windows Apps Domain Network Monitoring Metrics|Collects Windows Web apps network monitoring metrics like latency, packet loss, and jitter and sends monitoring data to Metric Base and the ServiceNow instance.|os.win.check-app-dom-network-latest|30 mins|Latest|source\_details, domain\_network\_route\_details|

## Policies for Windows — Device

DEX provides the following policies for devices.

<table id="table_cj5_4yd_1fc"><thead><tr><th>

Policy name

</th><th>

Description

</th><th>

Check instance

</th><th>

Frequency

</th><th>

Historical or latest

</th><th>

Check instance parameters\*

</th></tr></thead><tbody><tr><td>

DEX Windows Device Metrics

</td><td>

Collects Windows device metrics and sends the metric data to the ServiceNow instance.

</td><td>

os.win.check-system-metrics-latest

</td><td>

24 hours

</td><td>

Latest

</td><td>

uptime, logged\_in, antivirus\_enabled, firewall\_enabled, disk\_details, device\_details, battery\_details, bsod\_details, cpu\_details, os\_details, power\_plan, stability\_index, pending\_updates, network\_details, bitlocker\_details, user\_profiles, antimalware\_details, hard\_drive\_status, peripheral\_devices\_details, cpu\_usage, memory\_details, device\_events, last\_access\_time, os\_setup\_details, reboot\_details, energy\_consumption

</td></tr><tr><td class="sub-head" colspan="6">

**Important:** \* DEX Windows Device Metrics with the following check instance parameters runs only with a Local System account:

-   energy\_consumption
-   bitlocker\_details
-   last\_access\_time
-   pending\_updates
-   user\_profiles

</td></tr><tr><td>

DEX Windows Device Metrics

</td><td>

Collects Windows device metrics and sends the metric data to MetricBase.

</td><td>

os.win.check-system-metrics-historical

</td><td>

30 mins

</td><td>

Historical

</td><td>

network\_connection\_profiles

</td></tr><tr><td>

DEX Windows Device Metrics

</td><td>

Collects Windows device metrics and sends the metric data to MetricBase.

</td><td>

os.win.check-system-metrics-historical

</td><td>

5 mins

</td><td>

Historical

</td><td>

disk\_usage, io\_usage\_write, io\_usage\_read, memory\_usage, cpu\_usage, battery\_charge\_percentage, energy\_consumption, memory\_details, uptime, disk\_details, cpu\_performance\_details, crashes, power\_consumption, wifi\_transmit\_rate, wifi\_receive\_rate, wifi\_signal\_strength

</td></tr><tr><td>

DEX Windows Device Metrics

</td><td>

Collects data for running Windows processes and sends the data to the ServiceNow instance.

</td><td>

os.win.check-process-data

</td><td>

24 hours

</td><td>

N/A

</td><td>

N/A

</td></tr><tr><td>

DEX Windows Device Metrics

</td><td>

Collects Windows device metrics and sends the metric data to the ServiceNow instance.

</td><td>

os.win.check-sys-compliance-historical

</td><td>

5 mins

</td><td>

Historical

</td><td>

N/A

</td></tr><tr><td>

DEX Windows Device Metrics

</td><td>

Collects Windows device metrics and sends the metric data to the ServiceNow instance.

</td><td>

os.win.check-sys-compliance-latest

</td><td>

24 hours

</td><td>

Latest

</td><td>

N/A

</td></tr><tr><td>

DEX Get online Windows user on change

</td><td>

Gets a logged-in user's data on a Windows device whenever there’s a change.

</td><td>

os.win.check-system-custom-query-on-chan

</td><td>

60 secs

</td><td>

Latest

</td><td>

query,query\_sys\_id, query\_type

</td></tr><tr><td>

DEX Get device configuration on change

</td><td>

Gets a logged-in user's device configuration whenever there’s a change.

</td><td>

os.all.check.internal.get-device-configu

</td><td>

60 secs

</td><td>

Latest

</td><td>

N/A

</td></tr></tbody>
</table>**Note:** If you upgrade the DEX Content Playbook plugin on an instance and encounter unexpected policy update issues, see the [Troubleshooting: Policy update issues post DEX plugin upgrade \[KB1586917\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB1586917) article in the Now Support knowledge base.

**Parent Topic:**[DEX Content Playbook reference](dex-content-playbook-reference.md)

