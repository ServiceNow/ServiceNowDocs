---
title: Run ACC as a local system account user
description: To fetch the complete playbook content data for a Windows device, the Agent Client Collector \(ACC\) must run as a local system account.
locale: en-US
release: xanadu
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Install ACC on Windows, Getting started, Configuring Digital End-User Experience, Digital End-User Experience, IT Service Management]
---

# Run ACC as a local system account user

To fetch the complete playbook content data for a Windows device, the Agent Client Collector \(ACC\) must run as a local system account.

## Before you begin

Role required: sn\_dex.admin

## Procedure

1.  From the Windows task bar, navigate to **Services** &gt; **Run as administrator**.

2.  Open the Agent Client Collector service and select the **Log On** tab.

3.  Select **Local System account** and select **OK**.

    ![The Agent Client Collector Properties window from which you can select the local system account to log on.](../image/playbook-local-sys-account.png "Agent Client Collector Properties window")


