---
title: Air-gapped networks and OT Discovery installation
description: This section explains the options for air-gapped and non-air-gapped network, installation of Discovery for OT components, and accessing data from scans and queries.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/operational-technology/air-gapped-networks-installation.html
release: australia
product: Operational Technology
classification: operational-technology
topic_type: concept
last_updated: "2026-04-24"
reading_time_minutes: 1
breadcrumb: [Configure the Discovery Console for OT, Discovery Console for Operational Technology \(OT\), Operational Technology Native Discovery components, Operational Technology Discovery, Operational Technology]
---

# Air-gapped networks and OT Discovery installation

This section explains the options for air-gapped and non-air-gapped network, installation of Discovery for OT components, and accessing data from scans and queries.

## Non-air-gapped networks

During the installation of the Discovery Console for OT, you must have access to the internet to download and install dependent third-party packages such as MongoDB and RabbitMQ. The Console installation automatically installs these packages as long as there's an internet connection. After installation of the third-party packages, the internet connection is unnecessary.

When using the installation for a non-air-gapped network, the Discovery Console for OT not only needs access to dependent third-party packages, but it also needs to communicate with the Sensors, the Collectors, the MID Server, the Service Graph Connector for ServiceNow Operational Technology \(OT\) Discovery, and your ServiceNow instance.

For these specific steps see the documentation on configuring the individual OT Discovery components. Start with .

## Air-gapped networks

If you plan to install the Discovery Console for OT on an air-gapped network, additional steps are needed to move your queried data from your OT components and environment to your ServiceNow instance.

One way to work around this type of network is to first install the OT Discovery component packages on your network. The challenge is then how to get the data from your network to the Mid Server so that it is uploaded to the ServiceNow instance. To do this:

1.  Run queries within your closed network with the OT Discovery components to generate the desired data.
2.  Download the physical data files from the Console to a physical, portable storage device \(USB drive\).
3.  Then manually move these files to the MID Server.
4.  On the MID Server, create a folder for your files.
5.  Copy the physical files to this folder on the MID Server.
6.  The MID Server uploads your data to your ServiceNow instance.

## What to do next

To install the containerized packages, see [Install containerized OT Discovery packages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/operational-technology/install-containerized-ot-discovery-packages.md).

