---
title: Configure the OT Discovery Collector
description: The OT Discovery Collector is an application that you can install on a Windows or Linux system.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/operational-technology/configuring-the-collector.html
release: australia
product: Operational Technology
classification: operational-technology
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Operational Technology Discovery Collector, Operational Technology Native Discovery components, Operational Technology Discovery, Operational Technology]
---

# Configure the OT Discovery Collector

The OT Discovery Collector is an application that you can install on a Windows or Linux system.

## Collector Credentials

Depending on how you have deployed the Console, you may have to manually edit the hostname value in the `config.json` file to validate the Collector's credentials. If you install an offline Console or install into cloud environments, the `hostname` value may not be correct. For the OT Discovery Collector, the hostname needs to be set to the Console hosts external/network IP address. It is important to check this setting and adjust it as needed.

**Note:** If you want to download and install the Console and Collector containerized packages, see [Air-gapped networks and OT Discovery installation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/operational-technology/air-gapped-networks-installation.md) for more information.

**Collector minimum system requirements**

The OT Discovery Collector can be installed and run on either a Windows OS or a Linux OS.

<table id="table_collector"><thead><tr><th>

Component Operating System

</th><th>

Minimum System Requirements

</th></tr></thead><tbody><tr><td>

Windows

</td><td>

The OT Discovery Collector installation is compatible with Windows 10 or Windows 11 systems.

 The required Windows \(10 or 11\) environment for the OT Discovery Collector is x86\_64. ARM or Apple Silicon devices are not supported.

 See [Install the OT Discovery Collector on a Windows system](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/operational-technology/installing-collector-on-windows.md).

</td></tr><tr><td>

Linux

</td><td>

See [Install OT Discovery Collector on a Linux system](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/operational-technology/linux-install-ot-discovery-collector.md) for specific information.

</td></tr></tbody>
</table>## What to explore next

To install the OT Discovery Collector, see the installation steps compatible with your OS:

-   [Install the OT Discovery Collector on a Windows system](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/operational-technology/installing-collector-on-windows.md)
-   [Install OT Discovery Collector on a Linux system](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/operational-technology/linux-install-ot-discovery-collector.md)

