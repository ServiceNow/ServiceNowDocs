---
title: Enable domain separation on reports
description: Activate the domain separation plugin to enable reports to display content based on data, rules, and settings from the logged-on user domain.
locale: en-US
release: australia
product: Reporting
classification: reporting
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Domain separation and Reporting, Administering reports, Reporting, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Enable domain separation on reports

Activate the domain separation plugin to enable reports to display content based on data, rules, and settings from the logged-on user domain.

## Before you begin

Role required: security\_admin.

## About this task

By default, the Domain Support plugin separates data on certain tables by domain. It does not, however, separate reports by domain unless the MSP Extensions plugin is installed. The report displays data only from the user's domain, but the user is able to see all the reports.

Follow these steps to ensure domain separation on reports if the MSP Extensions plugin is not installed.

## Procedure

1.  Navigate to **All** &gt; **Reports** &gt; **Administration** and select a report to separate by domain.

2.  Right-click the header and select **Configure** &gt; **Dictionary**.

3.  Configure the dictionary on the `sys_domain` field and fill in the **Reference** field with the domain for this report.

    If left blank, the report is global.

    **Domain** fields appear on reports, and this field references a table. After a domain field exists on a form, all records within the table will have the domain field enabled. By default, all these records are global.


**Parent Topic:**[Domain separation and Reporting](../concept/domain-separation-in-reporting.md)

**Related topics**  


[Request domain separation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/t_ActivateDomainSeparation.md)

