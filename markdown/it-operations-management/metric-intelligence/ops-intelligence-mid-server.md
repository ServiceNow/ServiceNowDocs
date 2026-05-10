---
title: MID Server and MID Server distributed cluster for Metric Intelligence
description: Using Metric Intelligence requires at least one MID Server distributed cluster which contains a single MID Server that is configured for Metric Intelligence.
locale: en-US
release: australia
product: Metric Intelligence
classification: metric-intelligence
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Exploring Metric Intelligence, Metric Intelligence, IT Operations Management]
---

# MID Server and MID Server distributed cluster for Metric Intelligence

Using Metric Intelligence requires at least one MID Server distributed cluster which contains a single MID Server that is configured for Metric Intelligence.

When using a single Metric Intelligence MID Server, that server must be added to a MID Server distributed cluster.

To support the specified throughput, create a distributed cluster with a single MID Server that meets the Metric Intelligence MID Server requirements. When using a virtual machine \(VM\), only a single MID Server can run that supports Metric Intelligence. When working with Agent Client Collector, a MID Server can also be connected to multiple agents \(ACC-M and ACC-L\).

A MID Server supporting Discovery can also be used with other applications.

For details on setting up Metric Intelligence, see [Get started with Metric Intelligence](../task/get-started-metrics.md).

## MID Server distributed clusters

Activating Metric Intelligence \(com.snc.sa.metric\), automatically activates MID Server distributed cluster \(com.snc.agent.distributed.cluster\). A MID Server distributed cluster supports the Distributed MID Server cluster type which is used exclusively with Metric Intelligence.

If automatic creation of a MID Server distributed cluster fails, you can configure the cluster manually. For details, contact Customer Support.

## Metric Intelligence MID Server

The Metric Intelligence MID Server supports the Metric Intelligence feature by processing data and detecting anomalies. The MID Server transmits batches of processed data to the instance. If an anomaly is detected, then information about the anomaly along with the raw data is sent immediately to the instance.

Each Metric Intelligence MID Server must be configured with the following settings:

-   Metric Intelligence as a supported application
-   The Metrics capability
-   Running the Metric Intelligence Metrics extension

**Note:** The Metric Intelligence MID Server does not support IPv6.

The Metric Intelligence application that the Metric Intelligence MID Server is configured with enables you to add additional supported applications to the same MID Server. By default, Metric Intelligence is included in the definition of the MID Server ALL option. For information about modifying the behavior of the ALL option when selecting supported applications, see [Configure applications included in ALL Applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/t_SpecifyMIDServerApplications.md).

If Domain Support - Domain Extensions Installer is activated, then you can configure a MID Server with the Metrics capability, per domain. In this case, metrics for a business service are processed on the MID Server that is in the same domain as the business service. Otherwise, a MID Server from the global domain is used.

Ensure that the MID Server that you want to configure for Metric Intelligence:

-   Is validated. For more information, see [Validate a MID Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/t_ValidateAMIDServer.md)
-   Is in running state
-   Meets all software, hardware, and configuration requirements

<table id="table_i4b_bqf_q5"><thead><tr><th>

Requirement

</th><th>

 

</th></tr></thead><tbody><tr><td>

One MID Server with:-   Memory: 12 GB
-   Processor: 4 cores

</td><td>

Supports approximately up to a total of 1.2 million metrics \(12,000 CIs with 100 metrics per CI\).

</td></tr><tr><td>

One MID Server with:-   Memory: 24 GB
-   Processor: 8 cores

</td><td>

Supports approximately up to a total of 1.7 million metrics \(17,000 CIs with 100 metrics per CI\).

</td></tr></tbody>
</table><table id="table_s3h_qqf_q5"><thead><tr><th>

Software

</th><th>

Supported versions

</th><th>

Additional requirements

</th></tr></thead><tbody><tr><td>

Windows

</td><td>

32-bit and 64-bit versions:-   Windows 2008 R2
-   Windows Server 2012 R2
-   Windows Server 2019

</td><td>

32-bit or 64-bit version of the MID Server

</td></tr><tr><td>

Linux

</td><td>

-   Red Hat Enterprise Edition Linux 6.6 or later
-   CentOS Linux 6.6 or later

</td><td>

32-bit or 64-bit version of the MID Server

</td></tr></tbody>
</table><table id="table_plk_r2g_jx"><thead><tr><th>

Configuration

</th><th>

Requirement

</th></tr></thead><tbody><tr><td>

MID Server service logon user \(required only for pulling\)

</td><td>

Must be set to a user with read access to the SCOM database \(OperationsManagerDW\).1.  On the MID Server, open the MID Server **Properties** dialog box.
2.  Click the **Log On** tab.
3.  Select **This account**, and enter credentials for a user with the required access.
4.  Click **Apply**.

</td></tr></tbody>
</table>## MID Server throttling mechanism

The MID Server throttling mechanism protects against data bursts to the instance. Data burst protection prevents overloading the instance, while ensuring that you do not lose any data.

The MID Server throttling mechanism is enabled by default. You may want to disable this mechanism when troubleshooting, to ensure that the mechanism is not causing system malfunction.

-   To disable this feature for metrics, set the mid.oi.metric\_token\_bucket\_enabled parameter to **false**.
-   To disable this feature for anomalies, set the mid.oi.anomaly\_token\_bucket\_enabled parameter to **false**.

## Configuration Override

Update the `wrapper-override.conf` file in folder `../agent/conf`:

-   Add the following code at the bottom of the file:

    ```
     
    # GC
    wrapper.java.additional.5=-XX:+AlwaysPreTouch
    wrapper.java.additional.6=-XX:+UseG1GC
    wrapper.java.additional.7=-XX:+ScavengeBeforeFullGC
    wrapper.java.additional.8=-XX:+DisableExplicitGC
     
    # IP4
    wrapper.java.additional.9=-DpreferIPv4Stack=true
    ```

-   Ensure that `wrapper.java.initmemory=1024` \(or higher\) and `wrapper.java.maxmemory=4096` \(or higher\) for Metric Intelligence to run properly.
-   Optionally, if a server has additional RAM available, for example 16 GB RAM, you can replace 4096 with 8192 in: `wrapper.java.maxmemory=4096`.

