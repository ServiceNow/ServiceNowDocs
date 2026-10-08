---
title: HAProxy check
description: Credential and permission requirements for the HAProxy checks check-haproxy and metrics-check-haproxy.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-operations-management/agent-client-collector/haproxy-check.html
release: australia
product: Agent Client Collector
classification: agent-client-collector
topic_type: reference
last_updated: "2026-09-29"
reading_time_minutes: 1
breadcrumb: [Agent Client Collector checks – credential and permission requirements, ACC-M reference, Agent Client Collector reference, Agent Client Collector, IT Operations Management]
---

# HAProxy check

Credential and permission requirements for the HAProxy checks `check-haproxy` and `metrics-check-haproxy`.

## HAProxy stats credential

The HAProxy stats credential are required only when the HAProxy stats page has authentication enabled.

## Agent Client Collector Agent OS account

When using an HTTP or HTTPS stats page an Agent Client Collector account is not required. OS-level access is only required if using the UNIX stats socket, with `--stats` pointed at a socket path instead of an HTTP hostname.

In that case, the ACC agent OS account needs read/write access to the socket, which is often owned by`haproxy:haproxy` with restrictive permissions.

Configuration prerequisites:

-   The HAProxy stats page or socket must be enabled in the HAProxy configuration through `stats socket` or `stats enable`.
-   If a `stats-page` credential is configured, it must match `stats auth user:pass` in the HAProxy configuration.

Troubleshooting:

A permission denied error when connecting to the stats socket is an OS-level group or ACL issue on the ACC agent account. It is not a credential problem.

**Parent Topic:**[Agent Client Collector checks – credential and permission requirements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/agent-client-collector/acc-monitoring-checks-credential-and-permission-requirements.md)

