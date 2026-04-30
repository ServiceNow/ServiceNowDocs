---
title: MySQL discovery
description: Discovery can identify an instance of MySQL that is running on UNIX or Windows operating systems.
locale: en-US
release: zurich
product: ITOM Visibility
classification: itom-visibility
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Database discovery, Data collected by ITOM Visibility, ITOM Visibility reference, ITOM Visibility, IT Operations Management]
---

# MySQL discovery

Discovery can identify an instance of MySQL that is running on UNIX or Windows operating systems.

## Requirements

Discovery searches for the MySQL configuration file location from the following areas:

-   UNIX: Discovery searches for the MySQL configuration file location from the mysqld process, or port 3306.
-   Windows: Discovery searches for the MySQL configuration file location from the mysqld.exe process, or port 3306.

For each process, the following process parameters are explored in the following order:

**--defaults-extra-file**

**--defaults-file**

If the MYSQL configuration file location is not found from that search, then the following occurs:

-   UNIX: The configuration file location defaults to `/etc/my.cnf`.
-   Windows: No default configuration file location exists, and the probe to read the configuration file location is skipped.

**Note:** For information on Probe to Pattern migration see the knowledge article [KB0694477](https://support.servicenow.com/kb_view.do?sysparm_article=KB0694477).

## Credentials

Configure these credentials:

-   [Windows credentials](https://www.servicenow.com/docs/access?context=r_WindowsCredentialsForm&version=zurich&pubname=zurich-platform-security&ft:locale=en-US)
-   [SSH credentials](https://www.servicenow.com/docs/access?context=r_SSHCredentialsForm&version=zurich&pubname=zurich-platform-security&ft:locale=en-US)
-   [Applicative credentials](https://www.servicenow.com/docs/access?context=applicative-creds&version=zurich&pubname=zurich-platform-security&ft:locale=en-US) \(When applications require credentials in addition to the credentials the that host machine requires.\)

    **Note:** There’s no need to configure applicative credentials unless your Discovery prerequisites mention them.


For a list of privileged commands that you need for Discovery and Service Mapping, see [Service Mapping commands requiring a privileged user](../../service-mapping/reference/r_CommandsnCredentials.md). This list includes commands that require elevated rights to discover and map Unix-based hosts in your organization.

## Classifiers, patterns, and probes

Discovery uses these classifiers, probes, and patterns for MySQL discovery:

<table id="table_fzd_2yv_jz"><thead><tr><th>

Classifier

</th><th>

Trigger probes

</th><th>

Pattern

</th></tr></thead><tbody><tr><td>

MySQL Server

</td><td>

-   Horizontal Pattern: launches patterns
-   Windows - MySQL Configuration\*
-   Windows - MySQL Version\*
-   MySQL - Configuration\*
-   MySQL - Version\*

</td><td>

My SQL server On Windows and Linux Pattern

</td></tr></tbody>
</table>\*For new instances, these probes are inactive on the classifier. Discovery uses patterns for discovery.

To use patterns, verify that the correct pattern is specified in the horizontal pattern probe on the classifier. See [Add the Horizontal Pattern probe to a classifier](c-UsingPatternsForHorizontalDiscovery.md#) for instructions.

## Data collected

Discovery populates these fields in the MySQL Instance \[cmdb\_ci\_db\_mysql\_instance\] table:

|Label|Field name|Source|
|-----|----------|------|
|MySQL configuration|myconf|my.cnf|
|TCP port\(s\)|tcp\_port|running\_process|
|Version|version|mysqld|

**Parent Topic:**[Database discovery](database-discovery.md)

**Related topics**  


[Database Administrator \(DBA\) report discovery](dba-report-discovery-pattern.md)

