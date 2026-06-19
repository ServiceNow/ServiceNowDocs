---
title: Sync exception reasons
description: Configure the Exception reason integration to automatically synchronize exception reasons between your non-production and production instances.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/impact/syncing-exception-reasons.html
release: australia
product: Impact
classification: impact
topic_type: task
last_updated: "2026-05-05"
reading_time_minutes: 1
breadcrumb: [Exception reason integration, Scan Engine integrations, Configure the Impact Store Application, Configuring Impact, Impact]
---

# Sync exception reasons

Configure the Exception reason integration to automatically synchronize exception reasons between your non-production and production instances.

## Before you begin

My SN Instances registration and authentication must be complete before configuring this integration. See [Register your instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/register-your-instance.md).

Role required: sn\_se.scan\_engine\_admin

## Procedure

1.  Navigate to **ALL** &gt; **Impact** &gt; **Configuration** &gt; **Scan Engine Properties**.

2.  Select the **Exception reason** properties tab.

3.  Configure the integration settings.

    To require production approval before exception reasons take effect, select **Enable approvals in production** and specify one or more Approval Groups. Exception reasons will sync in a `Requested` state until approved or rejected.


## Result

Exception reasons created or updated on non-production instances are automatically synchronized to production. If approvals are enabled, the status syncs back to the developer instance after a decision is made.

**Parent Topic:**[Exception reason integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/exception-reason-integration.md)

