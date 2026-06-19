---
title: Purge a waitlist
description: An auto flush rule on the Reservation Waiting List \(sn\_wsd\_rsv\_waitlist\) table purges expired waitlist records older than 30 days to maintain accurate waitlist management reporting.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/workplace-reservation-management/purge-waitlist.html
release: australia
product: Workplace Reservation Management
classification: workplace-reservation-management
topic_type: task
last_updated: "2026-05-22"
reading_time_minutes: 2
breadcrumb: [Manage and configure reservation waitlist, Manage employee reservations, Workplace Reservation Management, Workplace Service Delivery, Employee Service Management]
---

# Purge a waitlist

An auto flush rule on the Reservation Waiting List \(**sn\_wsd\_rsv\_waitlist**\) table purges expired waitlist records older than 30 days to maintain accurate waitlist management reporting.

## Before you begin

Role required: sn\_wsd\_core.admin

## About this task

Waitlist entries that are cancelled, expired, or fulfilled are purged automatically after 30 days \(one month\). The purge policy runs as a scheduled job. You can review the schedule and adjust settings to meet your organization's data retention requirements.

## Procedure

1.  Navigate to **All** and in the context filter menu, search for **sys\_auto\_flush.LIST**.

    The Auto Flushes page opens.

2.  In the Table name column, search for the waitlist.

3.  Select the **sn\_wsd\_rsv\_waitlist** table record.

4.  Review the **sn\_wsd\_rsv\_waitlist** record for purge configuration changes.

    **Note:** A purge policy on the waitlist table purges records older than 30 days. It purges only records whose status is **Confirmed**, **Failed**, **Expired**, or **Canceled**.

    |Field|Description|
    |-----|-----------|
    |Table name|Reservation Waiting List \[sn\_wsd\_rsv\_waitlist\]|
    |Match field|Start|
    |Age in seconds|2,592,000 \(equivalent to 30 days\)|
    |Active|True|
    |Conditions|**\[status\] \[is\] \[confirmed\] OR \[status\] \[is\] \[failed\] OR \[status\] \[is\] \[expired\] OR \[status\] \[is\] \[cancelled\]**|

5.  Adjust the retention period as needed for your organization's policy.

6.  The **Table Cleaner** scheduled job runs periodically and reads the Auto Flush configuration for reservation waitlist table **sn\_wsd\_rsv\_waitlist** table.

    For each record in the **sn\_wsd\_rsv\_waitlist** table, it verifies the following:

    -   Start time: Start time is 30 days or older from the current date.
    -   Status: Waitlist records with status **Confirmed**, **Failed**, **Expired**, or **Canceled** are purged from the system permanently.
7.  Select **Update** if you have made changes to this record.

    By default, the job purges entries in **Confirmed**, **Canceled**, **Expired**, or **Failed** states that are older than 30 days.

    Waitlist entries in terminal states older than the specified retention period are purged.


**Parent Topic:**[Manage and configure reservation waitlist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-reservation-management/subscribe-waitlist-overview.md)

**Previous topic:**[Create a schedule job for waitlist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-reservation-management/schedule-job-waitlist.md)

**Next topic:**[Manage Workplace Reservations for Microsoft Outlook Add-in](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-reservation-management/manage-outlook-addin-rsv.md)

