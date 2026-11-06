---
title: Definitions integration
description: The Definitions integration manually syncs new, customized, and overridden definitions from development to production and the other instances.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/impact/definitions-integrations.html
release: australia
topic_type: concept
last_updated: "2026-10-27"
reading_time_minutes: 2
breadcrumb: [Scan Engine integrations, Activate Scan Engine and review settings, Configuring Impact, Impact]
---

# Definitions integration

The Definitions integration manually syncs new, customized, and overridden definitions from development to production and the other instances.

When you customize or override a definition on a development instance, use the **Sync Definition** action to send the change to your production instance so that scans run consistently across environments. Definitions don't sync automatically. You can sync individual definitions or multiple definitions in bulk.

## Prerequisites

-   My SN Instances registration is complete. See [Register your instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/impact/register-your-instance.md).
-   Authentication is configured. See [Configure the Basic authentication method](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/impact/configure-basic-auth-method.md) or [Configure the OAuth authentication method development instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/impact/configure-oauth-auth-method.md).
-   Role required: `sn_se.scan_engine_admin`.

## Where to configure

Manual definition sync actions appear only on instances whose environment is Development. Set the environment on each development record as described in [Register your instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/impact/register-your-instance.md).

Selecting **Enable definition synchronization** on a development instance only makes the manual **Sync Definition** action available. It doesn't sync definitions on its own, and the setting is read-only on production. Definitions also don't sync after you clone an instance. To update definitions after a clone, sync them again from a development instance.

## Sync direction

Definitions sync from development to production first. From production, they sync to every other registered instance in the stack, except the development instance where the definition originated. Only development instances can start a manual definition sync.

Definitions don't sync directly between development instances. When you sync a definition from one development instance, production receives it and sends it to the other registered instances, including other development instances.

**Note:** Enable definition synchronization on only one development instance. That way, definition changes come from one instance, and your team has one place to work on definitions.

## What syncs

The following definition states can be synchronized:

-   New definitions created on the development instance.
-   Customized definitions where default behavior has been modified.
-   Overridden definitions where the default has been replaced entirely.

-   **[Sync definitions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/impact/sync-new-customized-overridden-defs.md)**  
Enable definition synchronization and push new, customized, or overridden definitions from a development instance to production.

**Parent Topic:**[Scan Engine integrations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/impact/instance-integration-scan-engine.md)

