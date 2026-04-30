---
title: Configure domain separation for Metric Intelligence
description: Configure Metric Intelligence for domain separation to create logically defined domains that limit unauthorized access to data.
locale: en-US
release: yokohama
product: Metric Intelligence
classification: metric-intelligence
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuring Metric Intelligence, Metric Intelligence, IT Operations Management]
---

# Configure domain separation for Metric Intelligence

Configure Metric Intelligence for domain separation to create logically defined domains that limit unauthorized access to data.

## Before you begin

Role required: evt\_mgmt\_admin and evt\_mgmt\_integration

## Procedure

1.  Activate the Domain Support – Domain Extension Installer plug-in.

2.  Configure the MID Server for Operational Intelligence as a user that belongs to the desired domain with the role ‘mid\_server’ assigned to it.

3.  Configure a MID Server distributed cluster in the domain you desire and add Operational Intelligence MID Servers that belong to the same domain.

    For more information about setting up MID Servers for Metric Intelligence, see [MID Server and MID Server distributed cluster for Metric Intelligence](../concept/ops-intelligence-mid-server.md).

    **Note:** The Event Management’s binding events are configured using the domain of the logged-in MID Server user. Once the process has finished, the record’s domain is updated to use the domain from the CI so that any user within that domain can see the metric data.


