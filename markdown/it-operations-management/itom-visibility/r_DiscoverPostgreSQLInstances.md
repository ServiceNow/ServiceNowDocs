---
title: PostgreSQL discovery
description: Discovery can find running instances of PostgreSQL on Windows and Linux systems.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/itom-visibility/r\_DiscoverPostgreSQLInstances.html
release: zurich
product: ITOM Visibility
classification: itom-visibility
topic_type: reference
last_updated: "2026-08-24"
reading_time_minutes: 3
breadcrumb: [Database discovery, Data collected by ITOM Visibility, ITOM Visibility reference, ITOM Visibility, IT Operations Management]
---

# PostgreSQL discovery

Discovery can find running instances of PostgreSQL on Windows and Linux systems.

## Credentials and other prerequisites

-   **Create credentials for PostgreSQL discovery**
    -   [SSH credentials](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-security/r_SSHCredentialsForm.md)
    -   \[optional\] [Applicative credentials](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-security/applicative-creds.md)

-   **Verify root-level access to the database**

    The user must have root-level access to the database to access the `postgresql.conf` file.

-   **Verify privileged commands for for PostgreSQL discovery**

    For a list of privileged commands that you need for Discovery and Service Mapping, see [Service Mapping commands requiring a privileged user](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/service-mapping/r_CommandsnCredentials.md). This list includes commands that require elevated rights to discover and map Unix-based hosts in your organization.

-   **Differentiate multiple PostgreSQL instances on the same host by port number**

    Starting with Discovery and Service Mapping Patterns version 1.35.0, you can make multiple PostgreSQL instances on the same host distinguishable by port number by creating the **mid.discovery.postgresql.include\_port\_in\_name** MID Server property. For more information, see [Include the port number in PostgreSQL instance names](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/itom-visibility/enable-postgresql-port-in-name.md).


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

To use patterns, verify that the correct pattern is specified in the horizontal pattern probe on the classifier. See [Add the Horizontal Pattern probe to a classifier](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery/c-UsingPatternsForHorizontalDiscovery.md) for instructions.

## Data collected

Discovery populates the data in the CMDB when running the PostgreSQL DB pattern.

The following fields gather specified information from the target. If the source is not configured, it brings back default information. For instance, for PostgreSQL Instance@hostname \(default name\), the source needs to be modified. If not, all the "PostgreSQL Instance@hostname" will be added in the source for the PostgreSQL Instance \[cmdb\_ci\_db\_postgresql\_instance\] table.

|Field|Description|
|-----|-----------|
|Name \[name\]|The display name of the PostgreSQL instance.\*|
|Data Directory \[data\_dir\]|The data directory of the PostgreSQL instance, parsed from the process command line.|
|TCP port\(s\) \[tcp\_port\]|The port on which the PostgreSQL instance is listening, determined from the running process.|
|Config File \[postgres\_conf\]|The path to the `postgresql.conf` configuration file.|
|Version \[version\]|The PostgreSQL version, retrieved from the process executable.|

\* To populate the **Name** field in the format **instance-port-tcp\_port@hostname** instead of the default **instance@hostname**, create the **mid.discovery.postgresql.include\_port\_in\_name** MID Server property. For more information, see [Include the port number in PostgreSQL instance names](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/itom-visibility/enable-postgresql-port-in-name.md).

## Relationships

|CI|Relationship|CI|
|---|------------|---|
|PostgreSQL Instance \[cmdb\_ci\_db\_postgresql\_instance\]|Runs on::Runs|Windows Server \[cmdb\_ci\_windows\_server\] or Linux Server \[cmdb\_ci\_linux\_server\]|

-   **[Include the port number in PostgreSQL instance names](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/itom-visibility/enable-postgresql-port-in-name.md)**  
You can make multiple PostgreSQL instances on the same host distinguishable by port number by creating the **mid.discovery.postgresql.include\_port\_in\_name** MID Server property. This property is supported for UNIX hosts only.

**Parent Topic:**[Database discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/itom-visibility/database-discovery.md)

