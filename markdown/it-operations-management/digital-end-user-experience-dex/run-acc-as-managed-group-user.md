---
title: Run ACC as a managed group user
description: Run Agent Client Collector \(ACC\) from a managed group account to meet your organization's security, manageability, and auditability requirements.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-operations-management/digital-end-user-experience-dex/run-acc-as-managed-group-user.html
release: australia
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: task
last_updated: "2026-10-22"
reading_time_minutes: 1
keywords: [run acc managed group user, acc service account, managed group, run agent client collector as user, service log on account]
breadcrumb: [Installing DEX on your local machine, Configure, Digital End-User Experience, IT Operations Management]
---

# Run ACC as a managed group user

Run Agent Client Collector \(ACC\) from a managed group account to meet your organization's security, manageability, and auditability requirements.

## Before you begin

A user must be created and added to the following groups:

-   Remote Desktop users: Required to fetch the logged-in user details.
-   Performance Monitor users: Required to fetch all performance-related metrics at the application and device level.
-   ServiceNow users: Granted privileges for Performance Monitor, Log on as a service, and Debug program.
-   Administrator users: Equivalent to a local system user, provides access to fetch information about BitLocker, energy consumption, and so on.

Role required: none

## Procedure

1.  On the Windows host, navigate to **Services**.

2.  Select and hold \(or right-click\) **Agent Client Collector**.

3.  Select **Properties**.

4.  Select the **Log On** tab.

5.  Select the user that you created.

6.  Select **OK**.


