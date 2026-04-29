---
title: Configure the OT Discovery Collector
description: The OT Discovery Collector is an application that you can install on a Windows or Linux system.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Operational Technology \(OT\) Discovery Collector, Operational Technology Native Discovery components, Operational Technology Discovery, Operational Technology]
---

# Configure the OT Discovery Collector

The OT Discovery Collector is an application that you can install on a Windows or Linux system.

## Collector Credentials

Depending on how you have deployed the Console, you may need to manually edit the hostname value in the `config.json` file to validate the Collector's credentials. If you install an offline Console or install into cloud environments, the `hostname` value may not be correct. For the Collector, the hostname needs to be set to the Console hosts external/network IP address. It is important to check this setting and adjust it as needed.

## What to explore next

To install the OT Discovery Collector, see:

-   [Install the OT Discovery Collector on a Windows system](installing-collector-on-windows.md)
-   [Install OT Discovery Collector on a Linux system](linux-install-ot-discovery-collector.md)

