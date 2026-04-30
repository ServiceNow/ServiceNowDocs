---
title: DEX policies for macOS
description: Policies for macOS are guidelines and rules to promote that the application is used in a consistent, secure, and conforming manner. DEX policies your organization to reduce the risk of data breaches, improve data quality and accuracy, and optimize application performance and availability.
locale: en-US
release: xanadu
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [DEX Content Playbook reference, Reference, Digital End-User Experience, IT Service Management]
---

# DEX policies for macOS

Policies for macOS are guidelines and rules to promote that the application is used in a consistent, secure, and conforming manner. DEX policies your organization to reduce the risk of data breaches, improve data quality and accuracy, and optimize application performance and availability.

For macOS systems, to retrieve the entire data, include the subsequent content to /etc/sudoers.

For Agent version 3.4.0 or earlier:

```
_servicenow ALL=NOPASSWD: SETENV: /Library/Caches/servicenow/agent-client-collector/osquery/bin/osqueryi *, /usr/bin/mdls, /usr/bin/log, /usr/local/bin/jamf, /bin/kill, /bin/launchctl
Defaults:_servicenow !requiretty
```

For Agent version 3.4.1 or later:

```
_servicenow ALL=NOPASSWD: SETENV: /Library/Application\ Support/servicenow/agent-client-collector/cache/osquery/bin/osqueryi *, /usr/bin/mdls, /usr/bin/log, /usr/local/bin/jamf, /bin/kill, /bin/launchctl
Defaults:_servicenow !requiretty
```

**Note:** The historical data for an application or device is the information that is kept in the MetricBase database for the past 7 days, while the latest data pertains to the most recent information available.

## Policies for Mac — Application

DEX provides the following policies for applications.

|Policy name|Description|Check instances|Frequency|Historical or latest|Check instance parameters|
|-----------|-----------|---------------|---------|--------------------|-------------------------|
|DEX Mac Apps Metrics|Collects the application metrics in the Mac device and sends metric data to Metric Base.|os.mac.check-app-historical|5 mins|Historical|cpu\_usage, memory\_usage, uptime, io\_usage\_read, io\_usage\_write, is\_running, last\_access\_time, crashes|

## Policies for Mac — Device

DEX provides the following policies for devices.

<table id="table_mjt_kmd_hwb"><thead><tr><th>

Policy name

</th><th>

Description

</th><th>

Check instances

</th><th>

Frequency

</th><th>

Historical or latest

</th><th>

Check instance parameters

</th></tr></thead><tbody><tr><td>

DEX Mac Device Metrics

</td><td>

Collects macOS device metrics and sends the metric data to the ServiceNow instance.

</td><td>

os.mac.check-system-metrics-latest

</td><td>

24 hours

</td><td>

Latest

</td><td>

uptime, logged\_in, firewall\_enabled, session\_details, disk\_details, os\_details, cpu\_details, battery\_details, device\_details, network\_details, pending\_updates, device\_events, cpu\_usage, memory\_details, os\_setup\_details, last\_access\_time, reboot\_details

</td></tr><tr><td>

DEX Mac Device Metrics

</td><td>

Collects macOS device metrics and sends the metric data to MetricBase.

</td><td>

os.mac.check-system-metrics-historical

</td><td>

5 mins

</td><td>

Historical

</td><td>

disk\_usage, io\_usage\_write, io\_usage\_read, memory\_usage, cpu\_usage, memory\_details, uptime, crashes, battery\_charge\_percentage, wifi\_transmit\_rate, wifi\_rssi

</td></tr><tr><td>

DEX Mac Device Metrics

</td><td>

Collects data for running macOS processes and sends the data to the ServiceNow instance.

</td><td>

os.mac.check-process-data

</td><td>

24 hours

</td><td>

N/A

</td><td>

N/A

</td></tr><tr><td>

DEX Mac Device Metrics

</td><td>

Collects macOS device metrics and sends the metric data to the ServiceNow instance.

</td><td>

os.mac.check-sys-compliance-historical

</td><td>

5 minutes

</td><td>

Historical

</td><td>

N/A

</td></tr><tr><td>

DEX Mac Device Metrics

</td><td>

Collects macOS device metrics and sends the metric data to the ServiceNow instance.

</td><td>

os.mac.check-sys-compliance-latest

</td><td>

24 Hours

</td><td>

Latest

</td><td>

N/A

</td></tr><tr><td>

DEX Mac Device Metrics

</td><td>

Collects macOS device metrics and sends the metric data to the ServiceNow instance.

**Note:** If the previous check runs for more than five minutes, the current check gets skipped.

</td><td>

os.mac.check-energy-consum-historical

</td><td>

5 minutes

</td><td>

Historical

</td><td>

energy\_consumption

</td></tr><tr><td>

DEX Mac Device Metrics

</td><td>

Collects macOS device metrics and sends the metric data to the ServiceNow instance.

</td><td>

os.mac.check-system-metrics-historical

</td><td>

30 minutes

</td><td>

Historical

</td><td>

vpn\_details

</td></tr><tr><td>

DEX Get online macOS user on change

</td><td>

Gets a logged-in user's data on a macOS device whenever there’s a change.

</td><td>

os.mac.check-system-custom-query-on-chan

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
</table>**Note:** If you upgrade the Content Playbook plugin on an instance and encounter unexpected policy update issues, see the [Troubleshooting: Policy update issues post DEX plugin upgrade \[KB1586917\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB1586917) article in the Now Support knowledge base.

**Parent Topic:**[DEX Content Playbook reference](dex-content-playbook-reference.md)

