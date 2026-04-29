---
title: Configuring an address for VPN communication
description: To prevent conflict or overlap with internal ServiceNow networks or with another customer's internal IP address schemes, the instance requires that all tunneled traffic in the encryption domain use non-RFC-1918 addresses on both sides of the tunnel.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Virtual Private Network \(VPN\)]
---

# Configuring an address for VPN communication

To prevent conflict or overlap with internal ServiceNow networks or with another customer's internal IP address schemes, the instance requires that all tunneled traffic in the encryption domain use non-RFC-1918 addresses on both sides of the tunnel.

## Before you begin

Role required: admin

## About this task

The instance provides a single IP address for the source of queries into your network.

## Procedure

-   Provide Network Address Translation \(NAT\), non-RFC-1918 addresses for each host that is integrating with the instance.


