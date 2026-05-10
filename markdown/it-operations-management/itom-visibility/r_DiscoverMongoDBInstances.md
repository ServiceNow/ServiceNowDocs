---
title: MongoDB discovery
description: Discovery creates or updates a CMDB record when it detects a running instance of MongoDB.
locale: en-US
release: australia
product: ITOM Visibility
classification: itom-visibility
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Database discovery, Data collected by ITOM Visibility, ITOM Visibility reference, ITOM Visibility, IT Operations Management]
---

# MongoDB discovery

Discovery creates or updates a CMDB record when it detects a running instance of MongoDB.

## Credentials

Configure [SSH credentials](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/connections-and-credentials/r_SSHCredentialsForm.md).

For a list of privileged commands that you need for Discovery and Service Mapping, see [Service Mapping commands requiring a privileged user](../../service-mapping/reference/r_CommandsnCredentials.md). This list includes commands that require elevated rights to discover and map Unix-based hosts in your organization.

**Note:** For information on Probe to Pattern migration see the knowledge article [KB0694477](https://support.servicenow.com/kb_view.do?sysparm_article=KB0694477).

The following data is collected:

|Label|Table Name|Field Name|Source|
|-----|----------|----------|------|
|Version|cmdb\_ci\_db\_mongodb\_instance|version|mongod \(UNIX\) or mongod.exe \(Windows\)|
|Mongo configuration|cmdb\_ci\_db\_mongodb\_instance|mongodb\_conf|mongod.conf|
|TCP port\(s\)|cmdb\_ci\_db\_mongodb\_instance|tcp\_port|Process Classification or mongod.conf|

**Parent Topic:**[Database discovery](../concept/database-discovery.md)

