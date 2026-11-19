---
title: PostgreSQL check
description: Credential and permission requirements for the PostgreSQL checks that monitor database size, statistics, connections, and locks.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/agent-client-collector/postgresql-check.html
release: zurich
product: Agent Client Collector
classification: agent-client-collector
topic_type: reference
last_updated: "2026-09-29"
reading_time_minutes: 1
breadcrumb: [Agent Client Collector checks – credential and permission requirements, Agent Client Collector Monitoring reference, Agent Client Collector, IT Operations Management]
---

# PostgreSQL check

Credential and permission requirements for the PostgreSQL checks that monitor database size, statistics, connections, and locks.

## PostgreSQL database account

The database user configured in the ServiceNow credential must meet the following requirements.

-   Required for every check in this group: the account must be allowed to authenticate and connect to the specific database named in `--database`. It needs `CONNECT` privilege on that database, and `pg_hba.conf` on the server must permit login from the agent host for that user and database combination.
-   Required only for `postgresql.check-connections` and `postgresql.metric-active-connections`: the `pg_monitor` role on `Postgres 10+`, or superuser. Both checks query `pg_stat_activity` across all databases and sessions.

Configuration Prerequisites:

The Postgres TCP endpoint must be reachable from the agent host.

-   `pg_hba.conf` must let the agent host's source IP to authenticate for this user and database.
-   The connection `sslmode=disable` is hard-coded. If the server enforces SSL/TLS only through `hostssl` entries, the check fails with an SSL-negotiation error that can look like an authentication failure.
-   Confirm `pg_monitor` is granted if you're using connection or stats metrics.

**Parent Topic:**[Agent Client Collector checks – credential and permission requirements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/agent-client-collector/acc-monitoring-checks-credential-and-permission-requirements.md)

