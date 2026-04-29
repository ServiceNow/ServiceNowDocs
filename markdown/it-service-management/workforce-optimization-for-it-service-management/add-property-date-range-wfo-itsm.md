---
title: Add a system property to set default date range in Workforce Optimization for ITSM
description: Add a system property to set the default date range in the configurable Workforce Optimization for ITSM application.
locale: en-US
release: australia
product: Workforce Optimization for IT Service Management
classification: workforce-optimization-for-it-service-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Setting up, Teams, Workforce Optimization for ITSM, IT Service Management]
---

# Add a system property to set default date range in Workforce Optimization for ITSM

Add a system property to set the default date range in the configurable Workforce Optimization for ITSM application.

## Before you begin

Role required: admin

## About this task

The Teams application uses the sn\_optimize.default\_date\_range property in the configurable Workforce Optimization for ITSM application to set the default date range in the date range picker to view your team's performance for that time period.

## Procedure

1.  Select **All** and in the application navigator, enter enter `sys_properties.list`.

2.  Select **New**.

3.  Enter the following field values.

    |Field|Value|
    |-----|-----|
    |Name|sn\_optimize.default\_date\_range|
    |Type|Integer|
    |Value|The preferred number of days based on which the start and end dates are set in the date range picker in the Teams module.|
    |Read roles|sn\_team\_perf.team\_performance\_user|
    |Write roles|sn\_team\_perf.team\_performance\_admin|


**Parent Topic:**[Setting up Teams in Workforce Optimization for ITSM](../concept/setup-teams-configurable-workforce-optimization-itsm.md)

