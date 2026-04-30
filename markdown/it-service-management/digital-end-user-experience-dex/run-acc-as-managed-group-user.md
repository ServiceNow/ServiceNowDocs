---
title: Run ACC as a managed group user
description: Run Agent Client Collector \(ACC\) from a managed group account to meet your organization's security, manageability, and auditability requirements.
locale: en-US
release: xanadu
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Install ACC on Windows, Getting started, Configuring Digital End-User Experience, Digital End-User Experience, IT Service Management]
---

# Run ACC as a managed group user

Run Agent Client Collector \(ACC\) from a managed group account to meet your organization's security, manageability, and auditability requirements.

## Before you begin

Create a user and add the user to the following groups:

-   Remote Desktop users: Required to fetch the logged-in user details.
-   Performance Monitor users: Required to fetch all performance-related metrics of application and device level.
-   ServiceNow users: Has privileges to Performance Monitor, Log on as a service, and Debug program.
-   Administrator users: Equivalent to a local system user, provides access to fetch information on Bit locker, energy consumption, and so on.

Role required: admin

## Procedure

1.  On the Windows host, navigate to **Services**.

2.  Select and hold \(or right-click\) **Agent Client Collector**.

3.  Select **Properties**.

4.  Select the **Log on** tab.

5.  Select the user that you created.

6.  Select **OK**.


