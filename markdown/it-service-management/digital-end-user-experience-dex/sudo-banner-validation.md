---
title: Sudo banner validation
description: Sudo banner validation flags missing sudo permissions on managed devices so you know when the DEX agent's capabilities are limited.
locale: en-US
release: australia
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: concept
last_updated: "2026-03-30"
reading_time_minutes: 1
breadcrumb: [Advanced configuration, Configure, Digital End-User Experience, IT Service Management]
---

# Sudo banner validation

Sudo banner validation flags missing sudo permissions on managed devices so you know when the DEX agent's capabilities are limited.

The DEX agent requires specific sudo permissions to perform actions such as restarting services \(`restart_service`\) or removing files \(`rm`\). The agent flags missing required permissions.

As a DEX administrator, you can control the sudo banner configuration for macOS. For example, if your organization does not use Jamf you can add that permission to the exclusion list so that the system does not show the banner on the device page for excluded commands.

**Note:** Updating exclusion list doesn't change configured sudo permissions on the end-user device.

-   **[Configure sudo banner exclusion list](configure-sudo-banner-exclusion-list.md)**  
Add the appropriate commands to the sudo banner exclusion list so the system doesn't flag it.

**Parent Topic:**[Advanced configuration](dex-advanced-configuration.md)

