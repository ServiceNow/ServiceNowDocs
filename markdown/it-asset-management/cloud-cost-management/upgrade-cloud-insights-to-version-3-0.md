---
title: Upgrade Cloud Cost Management
description: You upgrade Cloud Cost Management on the System Applications page.
locale: en-US
release: xanadu
product: Cloud Cost Management
classification: cloud-cost-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring Cloud Cost Management, Cloud Cost Management, IT Asset Management]
---

# Upgrade Cloud Cost Management

You upgrade Cloud Cost Management on the System Applications page.

## Before you begin

Role required: sys\_admin

## Procedure

1.  Navigate to **System Applications** &gt; **All Available Applications** &gt; **Installed**.

2.  In the search box, enter `sn_clin`.

3.  Find the **Cloud Cost Management** app.

4.  In the selection list, select **Update** for version **8.0**.

    You can also update to the 8.0 version from 5.0.0 onwards.

5.  When the update is complete, clear the browser cache.

6.  Clear the server cache: `<instanceIP>/cache.do`

7.  Perform the Automatic Test Framework \(ATF\) tests to ensure data continuity after the upgrade.

    See [Run the Automatic Test Framework \(ATF\) tests](atf-tests-after-upgrade.md).


