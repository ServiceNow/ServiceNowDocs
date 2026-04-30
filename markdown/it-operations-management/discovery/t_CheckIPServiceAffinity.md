---
title: Check IP service affinity for Discovery and Orchestration
description: You can check the IP Services table for a list of IP addresses that are associated with a protocol.
locale: en-US
release: xanadu
product: Discovery
classification: discovery
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Discovery classifiers, Configuring Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# Check IP service affinity for Discovery and Orchestration

You can check the IP Services table for a list of IP addresses that are associated with a protocol.

## Before you begin

Role required: admin

## About this task

The IP Services table maps a port to a protocol. Several mappings are provided by default for commonly used port-protocol combinations, such as port 80 for HTTP, port 22 for SSH, and port 161 for SNMP.

A system property called **glide.discovery.ip\_service\_affinity** allows Discovery to remember the last port of the IP address that was discovered.

**Important:** You should not modify IP services unless your organization uses custom ports.

## Procedure

1.  Navigate to **All** &gt; **Discovery Definition** &gt; **IP Services**.

2.  Filter the list to find the appropriate IP service.

3.  Click the name of the service to go to that IP service page.

4.  Click the **IP Service Affinities** tab for the list of IP addresses associated with that service.

    ![IP Service Affinities](../image/IPServiceAffinity.png "IP Service Affinities")


