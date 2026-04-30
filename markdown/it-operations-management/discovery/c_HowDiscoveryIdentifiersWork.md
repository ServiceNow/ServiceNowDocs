---
title: How Discovery identifiers work
description: When Discovery has determined the device's class, it launches an identity probe that is configured to run one or more commands with a single authentication.
locale: en-US
release: zurich
product: Discovery
classification: discovery
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Discovery identifiers, Configuring Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# How Discovery identifiers work

When Discovery has determined the device's class, it launches an identity probe that is configured to run one or more commands with a single authentication.

The identity probe in the base Discovery system can be configured to ask the device for information such as its serial numbers, name, and network identification. The results of this scan are processed by an identity sensor, which then passes the results to the identifier. The identifier then attempts to find a matching device in the CMDB. If the identifier finds a matching CI, the identifier either updates that CI or does nothing. If the identifier cannot find a matching CI, it either creates a new CI or does nothing. If Discovery is configured to continue, the identifier launches the exploration probes configured in the classification record to gather additional information about the device. Exploration probes can be multiprobes or simple probes.

**Note:** When you use patterns for Discovery, the identity probe isn’t used. Discovery uses the appropriate identifier rules based on the CI type that you’re trying to discover as specified in the pattern operations. The operations in the pattern along with these identifier rules perform the identification and exploration phases of discovery.

This diagram shows the processing flow for classifying and probing devices with identifiers configured.

![Discovery identifiers](../image/DiscoveryIdentifiersDiagram.png "Discovery identifiers")

**Parent Topic:**[Discovery identifiers](c_DiscoveryIdentifiers.md)

