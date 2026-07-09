---
title: OT Discovery System Resources
description: You can review the OT Discovery component resources before setting up your OT network.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/operational-technology/ot-discovery-system-resources.html
release: australia
topic_type: concept
last_updated: "2026-06-30"
reading_time_minutes: 1
breadcrumb: [Deploy Operational Technology Discovery, Operational Technology Native Discovery components, Operational Technology Discovery, Operational Technology]
---

# OT Discovery System Resources

You can review the OT Discovery component resources before setting up your OT network.

## OT Discovery components required resources

The requirements in this section are a generalization. Consider factors such as segmentation level, communication pathways, network traffic, redundancy, and environmental conditions. Also account for physical constraints when determining network requirements. The following tables provide resource estimates for each OT Discovery component. Review your system requirements beyond these minimums.

<table id="table_i5f_kpx_vgc"><thead><tr><th>

Component

</th><th>

Minimum System Requirements

</th></tr></thead><tbody><tr><td>

Discovery Console for OT

</td><td>

-   16 GB RAM
-   100 GB Hard drive
-   2 CPUs

</td></tr></tbody>
</table>For additional requirements for the Console, see [Requirements for Discovery Console for OT installation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/operational-technology/reqs-ot-console-installation.md) and [Install the Discovery Console for Operational Technology \(OT\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/operational-technology/install-discovery-console-ot.md).

<table id="table_sensor_requirements"><thead><tr><th>

Component

</th><th>

Minimum System Requirements

</th></tr></thead><tbody><tr><td>

Discovery Sensor for OT

</td><td>

-   2 GB RAM\*
-   100 GB Hard drive
-   2 CPUs
-   2 virtual NIC cards

\*8 GB of RAM is recommended for all queries.

</td></tr></tbody>
</table>For additional requirements for the Sensor, see [Configure the Discovery Sensor for OT](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/operational-technology/configure-discovery-sensor-ot.md).

**Note:** The Collector can be installed and run on either a Windows OS or a Linux OS.

<table id="table_collector"><thead><tr><th>

Component Operating System

</th><th>

Minimum System Requirements

</th></tr></thead><tbody><tr><td>

Windows

</td><td>

The OT Discovery Collector installation is compatible with Windows 10 or Windows 11 systems.

 The required Windows \(10 or 11\) environment for the OT Discovery Collector is x86\_64. ARM or Apple Silicon devices aren't supported.

 See [Install the OT Discovery Collector on a Windows system](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/operational-technology/installing-collector-on-windows.md).

</td></tr><tr><td>

Linux

</td><td>

See [Install OT Discovery Collector on a Linux system](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/operational-technology/linux-install-ot-discovery-collector.md) for specific information.

</td></tr></tbody>
</table>