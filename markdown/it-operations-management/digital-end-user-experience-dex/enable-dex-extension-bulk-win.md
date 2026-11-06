---
title: Enable the DEX browser extension on multiple Windows devices
description: Deploy the DEX browser extension to all your organization's employees using Microsoft Intune.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-operations-management/digital-end-user-experience-dex/enable-dex-extension-bulk-win.html
release: australia
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: task
last_updated: "2026-10-23"
reading_time_minutes: 1
keywords: [deploy browser extension windows, microsoft intune extension, bulk extension windows, force installed extension, settings catalog]
breadcrumb: [Deploying DEX to employees, Configure, Digital End-User Experience, IT Operations Management]
---

# Enable the DEX browser extension on multiple Windows devices

Deploy the DEX browser extension to all your organization's employees using Microsoft Intune.

## Before you begin

The DEX browser extension ID must be available.

Role required: admin

## About this task

Your organization might have a different method to accomplish this task.

## Procedure

1.  From Microsoft Intune, navigate to **Windows** &gt; **Manage devices** &gt; **Configuration**.

2.  Select **Create**.

3.  Select the appropriate platform, then select **Settings catalog** under **Profile type**, and then select **Create**.

4.  On the **Basics** tab, enter a profile name, then select **Next**.

5.  On the **Configuration settings** tab, select **Add settings**.

6.  In the Settings picker form, select the following:

    1.  Select **Google Google Chrome Extensions**, then select **Configure the list of force-installed apps and extensions**.

    2.  Select **Microsoft Edge\\Extensions**, then select **Configure the list of force-installed apps and extensions**.

    3.  Close the Settings picker form.

7.  Enable the setting for both Google Chrome and Microsoft Edge browsers.

8.  For each browser, enter the extension ID and the update URL.

    For example, for the Google browser extension it’s `egjklpkeefoaknigleepliepdbonpbehchttp://clients2.google.com/service/update2/crx%22`.

9.  Select **Next**.

10. On the **Assignments** tab, select an appropriate option under **Groups** and select **Next**.

11. Review the profile and select **Create**.


