---
title: HTTP device discovery
description: Discovery can find devices that use the HTTP protocol.
locale: en-US
release: zurich
product: ITOM Visibility
classification: itom-visibility
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Network device discovery, Data collected by ITOM Visibility, ITOM Visibility reference, ITOM Visibility, IT Operations Management]
---

# HTTP device discovery

Discovery can find devices that use the HTTP protocol.

**Note:** For information on Probe to Pattern migration see the knowledge article [KB0694477](https://support.servicenow.com/kb_view.do?sysparm_article=KB0694477).

## Classifier, probes, and patterns

HTTP discovery relies on a the **HTTP** port probe, which Discovery runs after trying to run SSH and SNMP port probes. This port probe launches the **HTTP - Classify** probe which runs an HTTP GET request for every entry in the HTTP classification table. You should configure your own classifications that the **HTTP - Classify** probe can access.

The HTTP port probe uses mappings between a protocol and port number in the IP Service \[cmdb\_ip\_service\] table. You can add additional port-to-protocol definitions in this table, or you can override the protocol used for a specific HTTP classifier.

|Classifier|Probes|Pattern|
|----------|------|-------|
| |HTTP \(port probe\): this probe launches the HTTP - Classify probe, which runs an HTTP GET request for every entry in the HTTP classification table.| |

-   **[Run discovery through an HTTP or HTTPS REST call](../task/run-http-discovery.md)**  
Discovery can classify devices using the HTTP\(S\) protocol. You can create your own HTTP classifier to find devices and access them with Basic Auth credentials, rather than using SNMP or SSH credentials.

**Parent Topic:**[Network device discovery](c_NetworkDevices.md)

