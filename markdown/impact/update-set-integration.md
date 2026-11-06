---
title: Configure update set integration
description: Synchronize update set scan results from the instance where you run the scan to production and the other instances in the integration.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/impact/update-set-integration.html
release: australia
topic_type: task
last_updated: "2026-10-27"
reading_time_minutes: 1
breadcrumb: [Deployment and synchronization integrations, Scan Engine integrations, Activate Scan Engine and review settings, Configuring Impact, Impact]
---

# Configure update set integration

Synchronize update set scan results from the instance where you run the scan to production and the other instances in the integration.

## Before you begin

My SN Instances registration and authentication must be complete. See [Register your instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/impact/register-your-instance.md).

Roles required: `sn_se.scan_engine_user` for the scanning user, or `sn_se.scan_engine_admin` if that user also manages definitions. The account that receives the summary sync requires `sn_se.internal_rest_integration`.

## Procedure

1.  Navigate to **All** &gt; **Impact** &gt; **Configuration** &gt; **Scan Engine Properties**.

2.  Select the **Update Set Scanning** properties tab.

3.  Select **Enable update set summary scan synchronization** on each instance whose update set scan data you want to share.

    The setting is read-only on production.


## Result

Update set scan results from each enabled instance sync to the Production instance and to all other instances in the integration, so you can check results from any instance.

**Parent Topic:**[Deployment and synchronization integrations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/impact/deployment-sync-integrations.md)

**Related topics**  


[Configure AES/AEMC integration properties]()

