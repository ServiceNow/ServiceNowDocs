---
title: Enable the DEX browser extension on multiple macOS devices
description: Deploy the DEX browser extension to all your organization's employees using Jamf.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-operations-management/digital-end-user-experience-dex/enable-dex-extension-bulk-macos.html
release: australia
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: task
last_updated: "2026-10-23"
reading_time_minutes: 1
keywords: [deploy browser extension macos, jamf browser extension, bulk extension mac, configuration profile, force installed extension]
breadcrumb: [Deploying DEX to employees, Configure, Digital End-User Experience, IT Operations Management]
---

# Enable the DEX browser extension on multiple macOS devices

Deploy the DEX browser extension to all your organization's employees using Jamf.

## Before you begin

The DEX browser extension ID must be available.

Role required: admin

## About this task

Your organization might have a different method to accomplish this task.

## Procedure

1.  Create a configuration profile in Jamf.

    1.  Navigate to **Computers** &gt; **Configuration Profiles**.

    2.  Select **New**.

    3.  On the **General** tab of the new profile form, enter a meaningful name.

    4.  On the **Application &amp; Custom Settings** tab, select **Upload** &gt; **Add**.

    5.  Under **Preference Domain**, enter `com.google.chrome`.

    6.  Under **Property List**, copy and paste the following code block.

        ```
        <?xml version="1.0" encoding="UTF-8"?>
        <!DOCTYPE plist PUBLIC "-//Apple//DTD PLIST 1.0//EN" "http://www.apple.com/DTDs/PropertyList-1.0.dtd">
        <plist version="1.0">
          <dict>
            <key>ExtensionSettings</key>
            <dict>
              <key>egjklpkeefoaknigleepliepdbonpbehc</key>
              <dict>
              <key>installation_mode</key>
              <string>force_installed</string>
              <key>update_url</key>
              <string>http://clients2.google.com/service/update2/crx%22</string>
              <key>toolbar_pin</key>
              <string>force_pinned</string>
              </dict>
            </dict>
          </dict>
        </plist>
        ```

2.  Push the configuration profile to your end-user devices.

    1.  On the **Scope** tab of the configuration profile form, select **Add**.

    2.  Add your target computers or computer groups.

    3.  Select **Done**, then select **Save**.

3.  Validate the installation.

    -   Apple system: Navigate to **System Settings** &gt; **Privacy and Security** &gt; **Profiles**.
    -   Terminal: Enter the command `cd /Library/Managed\ Preferences` to navigate to the managed preferences folder and verify that the `com.google.Chrome.plist` file is present.
    -   End-user device: Open Google Chrome and navigate to the `chrome://extensions` page.

