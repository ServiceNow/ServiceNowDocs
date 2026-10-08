---
title: Oracle check
description: Learn about the credential and permission requirements for the Oracle checks app.oracle.check-oracle-alive, app.oracle.metrics-oracle, and util.metrics-oracle-query.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-operations-management/agent-client-collector/oracle-check.html
release: australia
product: Agent Client Collector
classification: agent-client-collector
topic_type: reference
last_updated: "2026-09-29"
reading_time_minutes: 1
breadcrumb: [Agent Client Collector checks – credential and permission requirements, ACC-M reference, Agent Client Collector reference, Agent Client Collector, IT Operations Management]
---

# Oracle check

Learn about the credential and permission requirements for the Oracle checks `app.oracle.check-oracle-alive`, `app.oracle.metrics-oracle`, and `util.metrics-oracle-query`.

Oracle checks require two separate accounts with different permissions.

## Oracle database account

The database user configured in ServiceNow® must have the following permissions:

-   CREATE SESSION or CONNECT
-   SELECT access to the Oracle views or tables queried by the specific check that is running

|Check|Queries|
|-----|-------|
|`check-oracle-alive`|`SELECT BANNER FROM v$version WHERE banner LIKE 'Oracle%'`|
|`metrics-oracle`|`SELECT TABLESPACE_NAME, sum(BYTES), sum(MAXBYTES) FROM sys.dba_data_files GROUP BY TABLESPACE_NAME`|
|`util.metrics-oracle-query`|Any custom query. The database account needs SELECT on the object targeted by that query.|

## Agent Client Collector agent OS account

All three checks run `sqlplus` locally on the target host where the OS account runs the Agent Client Collector agent. This is a separate identity from the Oracle database account.

Agent Client Collector agent OS account needs the following access:

-   Execute access to `$ORACLE_HOME/bin/sqlplus`
-   Access to Oracle client libraries under `$ORACLE_HOME/lib`
-   Access to Oracle configuration files if applicable, such as `tnsnames.ora` and `sqlnet.ora`

Depending on the Oracle installation, this means the Agent Client Collector agent OS account must be a member of `oinstall` or a database administrator.

Configuration Prerequisites:

-   `sqlplus` installed and reachable at `$ORACLE_HOME/bin/sqlplus`
-   Oracle listener reachable from the agent host through `--host`, `default localhost`, and `--port`, default 1521
-   Valid Oracle database credentials

|Error|Cause|
|-----|-----|
|Permission denied or command not found on `sqlplus`|The Agent Client Collector agent OS account lacks access to `$ORACLE_HOME` or `sqlplus`. This is not a database credential problem.|
|`ORA-xxxxx` errors|Oracle-side error that points to the database account or grants and not the OS account.|
|Custom query fails only on `util.metrics-oracle-query`|Re-check SELECT grants whenever `--query` is changed to target a new object.|

**Parent Topic:**[Agent Client Collector checks – credential and permission requirements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/agent-client-collector/acc-monitoring-checks-credential-and-permission-requirements.md)

