---
title: Create a schedule job for waitlist
description: A nightly scheduled job Waitlist Expirations handles expiration of past or stale waitlist records that are in Queued state. The nightly job runs daily and sets the status of any record with an expired or stale stale start time.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/workplace-reservation-management/schedule-job-waitlist.html
release: australia
product: Workplace Reservation Management
classification: workplace-reservation-management
topic_type: task
last_updated: "2026-05-22"
reading_time_minutes: 1
breadcrumb: [Manage and configure reservation waitlist, Manage employee reservations, Workplace Reservation Management, Workplace Service Delivery, Employee Service Management]
---

# Create a schedule job for waitlist

A nightly scheduled job Waitlist Expirations handles expiration of past or stale waitlist records that are in Queued state. The nightly job runs daily and sets the status of any record with an expired or stale stale start time.

## Before you begin

Stale or past entries are removed from the queue so that they don't remain active in the waitlist queue and affect space optimization and utilization insights.

**Note:** Expired entries are retained in the system until the purge job removes them based on the configured retention period \(30 days or more\). For more information, see [Purge a waitlist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-reservation-management/purge-waitlist.md).

Role required: sn\_wsd\_core.admin

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs.** and enter **sysauto\_script.LIST** in the search context menu filter.

    The Scheduled Script Executions page opens.

2.  In the Name column, search for `*Waitlist Expiration`.

3.  Open the job record and review the schedule and retention period.

4.  Set the scheduled job options as required.

5.  Adjust the schedule or retention period as needed for your organization's policy.

6.  Select **Execute Now** if you have updated the scheduled job record.

    The scheduled job runs and removes past waitlist entries with a stale start time. Expired waitlist records are removed from the reservation waitlist table. The records are not permanently removed from the system. A purge policy removes records that are 30 days or older. For more information, see [Purge a waitlist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-reservation-management/purge-waitlist.md).


**Parent Topic:**[Manage and configure reservation waitlist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-reservation-management/subscribe-waitlist-overview.md)

**Previous topic:**[Create a reservation waitlist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-reservation-management/create-rsv-waitlist.md)

**Next topic:**[Purge a waitlist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-reservation-management/purge-waitlist.md)

