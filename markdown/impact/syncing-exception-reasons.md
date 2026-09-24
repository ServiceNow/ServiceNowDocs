---
title: Sync exception reasons
description: Configure the Exception reason integration to automatically synchronize exception reasons between your non-production and production instances.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/impact/syncing-exception-reasons.html
release: brazil
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Exception reason integration, Configure Scan Engine integrations, Activate Scan Engine and review settings, Impact Guided Setup, Configuring Impact, Impact]
---

# Sync exception reasons

Configure the Exception reason integration to automatically synchronize exception reasons between your non-production and production instances.

## Before you begin

My SN Instances registration and authentication must be complete before configuring this integration. Instance names must match the exact instance subdomain. For example, use `testservicesdev` not `DEV`. See [Register your instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/register-your-instance.md).

**Important:** Verify that instance names in the My SN Instances table match the exact instance subdomain before proceeding.

Role required: sn\_se.scan\_engine\_admin

## Procedure

1.  Navigate to **ALL** &gt; **Impact** &gt; **Configuration** &gt; **Scan Engine Properties**.

2.  Select the **Exception reason** properties tab.

3.  Configure the integration settings.

    **Important:** Before enabling approvals, ensure your instances are registered in My SN Instances with the exact instance name matching your instance subdomain. For example, use `testservicesdev` not `DEV`. If the instance name is incorrect, the **Enable approvals in production** checkbox will remain greyed out. See [Register your instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/register-your-instance.md) for details.

    To require production approval before exception reasons take effect, select **Enable approvals in production** and specify one or more Approval Groups. Exception reasons will sync in a `Requested` state until approved or rejected.


## Result

Exception reasons created or updated on non-production instances are automatically synchronized to production. If approvals are enabled, the status syncs back to the developer instance after a decision is made.

**Parent Topic:**[Exception reason integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/exception-reason-integration.md)

