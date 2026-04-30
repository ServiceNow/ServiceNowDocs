---
title: Service Graph Connector for Splunk add-on
description: Import more detailed asset data with the Service Graph Connector for Splunk with an add-on developed by ServiceNow engineering. The add-on permits you to import data about your Windows and Linux assets.
locale: en-US
release: xanadu
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: concept
last_updated: "2024-10-28"
reading_time_minutes: 1
breadcrumb: [Splunk, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Service Graph Connector for Splunk add-on

Import more detailed asset data with the Service Graph Connector for Splunk with an add-on developed by ServiceNow engineering. The add-on permits you to import data about your Windows and Linux assets.

## Service Graph Connector for Splunk

The Service Graph Connector for Splunk retrieves computer and software information from the Splunk product and imports it into the Configuration Management Database \(CMDB\) in your instance. By default, the following basic data is imported:

-   Forwarder's version \(agent\)
-   Forwarder's type \(agent\)
-   Forwarder's last check-in time \(agent\)
-   OS
-   Host
-   Host IP address

The service graph connector for Splunk is available on the ServiceNow® Store.

## The ServiceNow Add-on for Windows and Linux assets

With the Windows and Linux Assets add-on, you have the option to import more detailed asset data with the Service Graph Connector for Splunk that includes the following data:

-   MAC address
-   Operating system details
-   Asset name
-   Installed software details
-   File system
-   Last logon date
-   Open ports
-   Running processes
-   Running services

This add-on is available for download into your Splunk console from [splunkbase](https://splunkbase.splunk.com/app/3921).

## Downloading and installing the add-on

Prior to installing this add-on, you must verify you have installed and activated the following applications and add-ons:

-   Service Graph Connector Splunk
-   Splunk\_TA\_nix version 9.0.0 \(Linux\) or later
-   Splunk\_TA\_windows version 8.9.0 or later add-ons available from splunkbase.

These add-ons permit you to identify and import more specific data related to your Linux and Windows assets with your imports with the Splunk Service Graph Connector API.

For example, searches from these add-ons might provide you with data you want about Windows drivers, Windows Network Adaptors, Linux Hardware, and other OS Details.

## Target workloads

In the app.manifest, individual agents on a specific machine send information to a central hub \(server\) where data is collected, stored, and managed. This central machine is where the apps are installed.

To adjust workloads to specify resources for a search, indexing, or other workloads, in Splunk Web, select **Settings** &gt; **Workload Management** &gt; **Workload Rules**.

In the Status column, select the toggle to activate or deactivate individual workload rules.

## Supported deployments

This add-on supports the following types of deployments:

-   standalone
-   distributed
-   search head clustering

See Splunk documentation for more information about their supported workloads.

