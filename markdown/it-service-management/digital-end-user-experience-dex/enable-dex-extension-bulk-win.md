---
title: Enable DEX browser extension on multiple Windows devices
description: Deploy the DEX browser extension to all your organization's employees using Microsoft Intune.
locale: en-US
release: australia
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Deploying DEX to employees, Configure, Digital End-User Experience, IT Service Management]
---

# Enable DEX browser extension on multiple Windows devices

Deploy the DEX browser extension to all your organization's employees using Microsoft Intune.

## Before you begin

Obtain the DEX browser extension ID.

Role required: admin

## About this task

The following procedure describes how to deploy the DEX browser extension on multiple devices using Microsoft Intune. Your organization might have a different method to accomplish this task.

## Procedure

1.  From Microsoft Intune, navigate to **Windows** &gt; **Manage devices** &gt; **Configuration**.

2.  Select **Create**.

3.  Select the appropriate platform, then select **Settings catalog** under **Profile type**, and then select **Create**.

4.  On the Basics tab, provide a meaningful profile name, then select **Next**.

5.  In the Configuration settings tab, select **Add settings**.

6.  In the Settings picker form, select the following:

    1.  Select **Google Google Chrome Extensions**, then select **Configure the list of force-installed apps and extensions**.

    2.  Select **Microsoft Edge\\Extensions**, then select **Configure the list of force-installed apps and extensions**.

    3.  Close the Settings picker form.

7.  Enable the setting for both Google Chrome and Microsoft Edge browsers.

8.  For each browser, provide the extension ID and the update URL.

    For example, for the Google browser extension it’s `egjklpkeefoaknigleepliepdbonpbehchttp://clients2.google.com/service/update2/crx%22`.

9.  Select **Next**.

10. In the Assignments tab, select an appropriate option under **Groups** and select **Next**.

11. Review the profile and select **Create**.


**Parent Topic:**[Deploying DEX to employees](../concept/deploying-dex-to-employees.md)

