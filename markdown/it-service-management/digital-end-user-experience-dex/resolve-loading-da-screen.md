---
title: Resolve Desktop Assistant screen loading issue
description: 
locale: en-US
release: australia
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: topic
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [DEX Desktop Assistant reference, Reference, Digital End-User Experience, IT Service Management]
---

# Resolve Desktop Assistant screen loading issue

## Symptom

The DEX Desktop Assistant screen is empty or in a continuously loading state. 

## Cause

The DEX Desktop Assistant is not loading because the user is not a valid DEX user or the settings.json file is corrupted.

## Resolution

## Procedure

1.  Refresh the application.

2.  Quit and relaunch the application.

3.  Clear the Electron settings file at the following location:

    -   macOS: `~/Library/Application\ Support/desktop_assistant_app/settings.json`
    -   Windows: `~\AppData\Roaming\desktop_assistant_app\settings.json`
4.  Verify you're logged in with the sn\_dex\_desktop.user role.

5.  Verify that the DEX Desktop Assistant application is installed on the instance to which you're connecting.


**Parent Topic:**[DEX Desktop Assistant reference](dex-desktop-experience-reference.md)

