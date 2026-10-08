---
title: MySQL check
description: Learn about the credential and permission requirements for the MySQL checks app.mysql.check-mysql-alive, util.metrics-mysql-query, app.mysql.check-mysql-threads, app.mysql.metrics-mysql, app.mysql.metrics-mysql-processes, and util.check-mysql-query
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/agent-client-collector/mysql-check.html
release: brazil
product: Agent Client Collector
classification: agent-client-collector
topic_type: reference
last_updated: "2026-09-29"
reading_time_minutes: 1
breadcrumb: [Agent Client Collector checks – credential and permission requirements, ACC-M reference, Agent Client Collector reference, Agent Client Collector, IT Operations Management]
---

# MySQL check

Learn about the credential and permission requirements for the MySQL checks `app.mysql.check-mysql-alive`, `util.metrics-mysql-query`, `app.mysql.check-mysql-threads`, `app.mysql.metrics-mysql`, `app.mysql.metrics-mysql-processes`, and `util.check-mysql-query`

MySQL checks require two separate accounts with different permissions:

## MySQL database account

The database user configured in the ServiceNow® credential must have the following permissions:

-   Basic login privilege on the target host and port, or socket
-   SELECT access to whatever schema or table is targeted by a custom query
-   PROCESS privilege for checks that read server-wide thread or connection state

|Check|Additional requirement|
|-----|----------------------|
|`check-mysql-alive`|Login privilege only|
|`check-mysql-query-result-count, metrics-mysql-query-result-count`|SELECT access on the object targeted by the configured `--query`|
|`check-mysql-threads, metrics-mysql-processes`|PROCESS privilege. Without it, the account only sees its own connection or thread, not the server-wide count, and the check silently under-reports instead of erroring.|
|`metrics-mysql-graphite`|Login privilege only|

## Agent Client Collector Agent OS account

There is no special OS permission required. The Agent Client Collector agent OS account only needs additional access if:

-   A UNIX socket is used instead of TCP through `--socket`. The agent needs read and execute access to the socket file and its parent directory.
-   An `ini` file is used to source connection settings through `--ini` or `--ini_section`, `my.cnf-style`. The agent needs read access to this `ini` file.

Depending on the deployment, this typically means group membership on the socket's owning group, or read ACLs on the `my.cnf` file. It doesn't usually require root or DBA-level access.

Configuration Prerequisites:

-   MySQL or MariaDB TCP endpoint that is reachable from the agent host through `--hostname` and `--port`, or through `--socket`
-   Database credentials are valid and not blocked by host-based grant restrictions, such as `user@'agent-host'` compared to `user@'%'`
-   For thread or process metrics, confirm PROCESS is granted by running `SHOW GRANTS FOR 'user'@'host';`

**Parent Topic:**[Agent Client Collector checks – credential and permission requirements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/agent-client-collector/acc-monitoring-checks-credential-and-permission-requirements.md)

