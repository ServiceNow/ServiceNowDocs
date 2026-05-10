---
title: PostgreSQL discovery
description: Discovery can find running instances of PostgreSQL on Windows and Linux systems.
locale: en-US
release: australia
product: ITOM Visibility
classification: itom-visibility
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Database discovery, Data collected by ITOM Visibility, ITOM Visibility reference, ITOM Visibility, IT Operations Management]
---

# PostgreSQL discovery

Discovery can find running instances of PostgreSQL on Windows and Linux systems.

## Credentials and other prerequisites

These credentials are required:

-   [SSH credentials](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/connections-and-credentials/r_SSHCredentialsForm.md)
-   \[optional\] [Applicative credentials](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/connections-and-credentials/applicative-creds.md)


For a list of privileged commands that you need for Discovery and Service Mapping, see [Service Mapping commands requiring a privileged user](../../service-mapping/reference/r_CommandsnCredentials.md). This list includes commands that require elevated rights to discover and map Unix-based hosts in your organization.

The user must have root-level access to the database to access the `postgresql.conf` file.

**Note:** For information on Probe to Pattern migration see the knowledge article [KB0694477](https://support.servicenow.com/kb_view.do?sysparm_article=KB0694477).

## Classifiers, patterns, and probes

<table id="table_fzd_2yv_jz"><thead><tr><th>

Classifier

</th><th>

Trigger probes

</th><th>

Patterns

</th></tr></thead><tbody><tr><td>

PostgreSQL Instance

</td><td>

-   Horizontal Pattern: launches patterns
-   PostgreSQL - Configuration\* \(add the **must\_sudo** parameter to this probe\)
-   PostgreSQL - Version\*

</td><td>

PostgreSQL DB

</td></tr></tbody>
</table>\*For new instances, these probes are inactive on the classifier. Discovery uses patterns for discovery.

To use patterns, verify that the correct pattern is specified in the horizontal pattern probe on the classifier. See [Add the Horizontal Pattern probe to a classifier](../concept/c-UsingPatternsForHorizontalDiscovery.md#) for instructions.

## Data collected

The following gathers specified information from the target. If the source is not configured, it brings back default information. For instance, for PostgreSQL Instance@hostname \(default name\), the source needs to be modified. If not, all the "PostgreSQL Instance@hostname" will be added in the source for the \[cmdb\_ci\_db\_postgresql\_instance\] table.

|Label|Table Name|Field Name|Source|
|-----|----------|----------|------|
|Name|cmdb\_ci\_db\_postgresql\_instance|name|PostgreSQL Instance@*hostname*|
|Data Directory|cmdb\_ci\_db\_postgresql\_instance|data\_dir|running process|
|TCP port|cmdb\_ci\_db\_postgresql\_instance|tcp\_port|running process|
|SQL Configuration|cmdb\_ci\_db\_postgresql\_instance|postgres\_conf|*data\_directory*/postgresql.conf|
|Version|cmdb\_ci\_db\_postgresql\_instance|version|postmaster/postgres|

## Relationships

|Parent class|Relationship|Child class|
|------------|------------|-----------|
|cmdb\_ci\_db\_postgresql\_instance|Runs on:Runs|cmdb\_ci\_windows\_server or cmdb\_ci\_linux\_server|

**Parent Topic:**[Database discovery](../concept/database-discovery.md)

