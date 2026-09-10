---
title: Configure potential relationship table limits
description: Configure the maximum potential relationship records that automated correlation can create. By default, each potential relationship table has a limit of 1,000,000 records for each domain.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/threat-intelligence-security-center/tisc-update-potential-relationship-record-limit.html
release: australia
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2026-08-12"
reading_time_minutes: 1
keywords: [threat intelligence, correlation, potential relationships, performance]
breadcrumb: [Automated correlation, Threat Intel Library, Use, Threat Intelligence Security Center, Security Operations]
---

# Configure potential relationship table limits

Configure the maximum potential relationship records that automated correlation can create. By default, each potential relationship table has a limit of 1,000,000 records for each domain.

## Before you begin

Role required: sn\_sec\_tisc.admin

## About this task

Automated correlation stops creating potential relationships when a potential relationship table reaches its record limit. Review the system logs for further information.

## Procedure

1.  Select **All**.

2.  In the navigation filter, enter `sn_sec_tisc_table_threshold_config.list` and press Enter.

    The Table Threshold Configuration list opens.

3.  Open the record for the potential relationship table you want to update.

    The base system provides a record for each of these tables:

    -   sn\_sec\_tisc\_m2m\_observable\_potential
    -   sn\_sec\_tisc\_m2m\_indicator\_potential
    -   sn\_sec\_tisc\_m2m\_object\_potential
    -   sn\_sec\_tisc\_m2m\_object\_indicator\_potential
4.  Review the **Current Record Count** field.

    The record count updates every 10 minutes.

5.  In the **Record Limit** field, enter the maximum number of records for the table.

    **Warning:** Retain a value close to the default of 1,000,000. Higher limits let the table grow well beyond the volume that the correlation engine is tuned for, which can cause performance issues as your threat intelligence data grows.

6.  Verify that the **Enable Record Limit** check box is selected.

    **Warning:** If this check box is cleared, no limit is enforced and the table can grow without restriction, which can degrade instance performance.

7.  Verify that the **Active** check box is selected.

8.  Select **Update**.


## Result

Automated correlation creates potential relationships in the table until the record count reaches the limit you set.

**Parent Topic:**[Automated correlation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/threat-intelligence-security-center/automated-correlation-rules.md)

