---
title: Exception reason integration
description: You can synchronize exception reasons from non-production to Production instances once a record is created or updated.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/impact/exception-reason-integration.html
release: australia
product: Impact
classification: impact
topic_type: concept
last_updated: "2026-05-05"
reading_time_minutes: 1
breadcrumb: [Scan Engine integrations, Configure the Impact Store Application, Configuring Impact, Impact]
---

# Exception reason integration

You can synchronize exception reasons from non-production to Production instances once a record is created or updated.

When a developer creates or updates an exception reason on a non-production instance, the integration automatically propagates that change to the production instance. If production approvals are enabled, the exception reason enters a Requested state and triggers an approval workflow before taking effect.

## Approval workflow

When **Enable approvals in production** is selected in Scan Engine Properties, the following workflow applies:

1.  A developer creates or updates an exception reason on the non-production instance.
2.  The exception reason is synced to production in a `Requested` state.
3.  An approval request is sent to the configured Approval Group\(s\).
4.  Once approved or rejected, the status syncs back to the developer instance.

## Prerequisites

-   My SN Instances registration is complete. See [Register your instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/register-your-instance.md).
-   Authentication is configured. See [Configure the Basic authentication method](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/configure-basic-auth-method.md) or [Configure the OAuth authentication method development instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/configure-oauth-auth-method.md).
-   Role required: `sn_se.scan_engine_admin`.

-   **[Sync exception reasons](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/syncing-exception-reasons.md)**  
Configure the Exception reason integration to automatically synchronize exception reasons between your non-production and production instances.

**Parent Topic:**[Scan Engine integrations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/instance-integration-scan-engine.md)

