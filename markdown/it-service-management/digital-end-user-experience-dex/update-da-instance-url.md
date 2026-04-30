---
title: Update instance URL in the Desktop Assistant configuration file
description: Update the instance URL in the Desktop Assistant configuration file to automatically populate the Desktop Assistant login page instance URL on devices on which it is installed.
locale: en-US
release: xanadu
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: task
last_updated: "2025-06-13"
reading_time_minutes: 1
breadcrumb: [Download and install Desktop Assistant, Setting up DEX Desktop Assistant, Configuring Digital End-User Experience, Digital End-User Experience, IT Service Management]
---

# Update instance URL in the Desktop Assistant configuration file

Update the instance URL in the Desktop Assistant configuration file to automatically populate the Desktop Assistant login page instance URL on devices on which it is installed.

## Before you begin

Role required: admin

**Note:** Only the system administrator must update the configuration file or make changes to it while deploying Desktop Assistant on devices.

Desktop Assistant users can update the instance URL when logging in to the application. For more information, see [Open Desktop Assistant](open-desktop-exp.md).

## Procedure

1.  On your computer, navigate to the folder that contains the `settings.json` file.

    -   On Windows devices: Navigate to the `C:\Users\user_name\AppData\Roaming\desktop_assistant_app` folder.
    -   On macOS devices: Navigate to the `Users/user_name/Library/Application Support/desktop_assistant_app` folder.

        **Note:** If you don’t see a folder, use Command+Shift+period \(.\) key to show hidden folders.

2.  Find and open the `settings.json` file.

3.  Enter the Desktop Assistant instance URL in the **instanceURL** field of the JSON file.

4.  Save and close the JSON file.


