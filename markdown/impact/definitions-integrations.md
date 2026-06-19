---
title: Definitions integration
description: The Definitions integration synchronizes new, customized, and overridden definitions between non-production and production instances.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/impact/definitions-integrations.html
release: australia
product: Impact
classification: impact
topic_type: concept
last_updated: "2026-05-05"
reading_time_minutes: 1
breadcrumb: [Scan Engine integrations, Configure the Impact Store Application, Configuring Impact, Impact]
---

# Definitions integration

The Definitions integration synchronizes new, customized, and overridden definitions between non-production and production instances.

When you customize or override a definition on a development instance, the Definitions integration pushes those changes to your production instance so that scans run consistently across environments. You can sync individual definitions or multiple definitions in bulk.

## Prerequisites

-   My SN Instances registration is complete. See [Register your instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/register-your-instance.md).
-   Authentication is configured. See [Configure the Basic authentication method](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/configure-basic-auth-method.md) or [Configure the OAuth authentication method development instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/configure-oauth-auth-method.md).
-   Role required: `sn_se.scan_engine_admin`.

## What syncs

The following definition states can be synchronized:

-   New definitions created on the development instance.
-   Customized definitions where default behavior has been modified.
-   Overridden definitions where the default has been replaced entirely.

-   **[Sync definitions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/sync-new-customized-overridden-defs.md)**  
Enable definition synchronization and push new, customized, or overridden definitions from a development instance to production.

**Parent Topic:**[Scan Engine integrations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/instance-integration-scan-engine.md)

