---
title: App Settings panel
description: The App Settings panel contains configuration for your profile, appearance, editor behavior, instance connection, integrations, and updates.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/application-development/app-settings.html
release: zurich
topic_type: reference
last_updated: "2026-09-30"
reading_time_minutes: 2
keywords: [App Settings panel, Ways to open the panel, Settings sections, Profile, Appearance, Editor, Context, Instance, Integrations, Updates, Advanced, Default settings]
breadcrumb: [Configuring Lux Lab, Lux Lab, Building pro-code applications, Developing your application, Building applications]
---

# App Settings panel

The App Settings panel contains configuration for your profile, appearance, editor behavior, instance connection, integrations, and updates.

## Ways to open the panel

You can open the App Settings panel in the ways shown in the following table.

|Method|Action|
|------|------|
|Keyboard shortcut|Cmd+, \(macOS\) or Ctrl+, \(Windows\)|
|Activity Bar|Select the gear icon at the bottom of the Activity Bar|

The Settings panel opens as a modal dialog and displays the Lux Lab version at the top left, for example v2.0.8.

## Settings sections

The panel's sidebar lists the sections in the following table.

|Section|Description|
|-------|-----------|
|Profile|Your name, email, and profile picture|
|Appearance|Theme, brand colors, and visual depth settings|
|Editor|Code editor preferences|
|Context|How the agent collects and uses project context|
|Instance|ServiceNow instance connection settings|
|Integrations|Figma integration and Now SDK version|
|Updates|Lux Lab update preferences|
|Advanced|Advanced configuration options|

## Profile

The Profile section shows your connected account. You can update the display information in the following table.

|Field|Description|
|-----|-----------|
|Name|Your display name|
|Email|Your account email address|
|Profile picture|Custom avatar that you upload, or a preset that you choose|

The Profile section also has the following controls:

-   **Presets** — Displays built-in avatar options to select from.
-   **Upload** — Uploads a custom profile image.
-   **Refresh** — Re-syncs your profile information from your account.

## Appearance

The Appearance section sets the theme, brand colors, and dark surface depth.

## Theme

The theme control switches between **Light** and **Dark** mode.

## Brand colors

Brand colors customize the app color palette, as described in the following table.

|Color|Description|
|-----|-----------|
|Primary|Main accent color used for active states and highlights|
|Accent|Secondary accent color|
|Neutral|Neutral or background color|

The brand colors have the following controls:

-   **Shuffle** — Randomly generates a new color combination.
-   **Reset** — Restores the default color set.

## Dark surface depth

When Dark mode is active, **Dark Surface Depth** controls how much surface elevation contrast Lux Lab applies. The options are **2**, **4**, **7**, and **10**. Higher values give more contrast between layered surfaces.

## Editor

The Editor section controls code editing preferences such as tab size, font settings, word wrap, and formatter behavior.

## Context

The Context section controls how the agent gathers and uses project context in the Agent Chat Harness. This includes how many files, how much history, and which parts of the project the agent includes automatically with each request.

## Instance

The Instance section holds the following ServiceNow instance connection settings:

-   Default instance on startup
-   Connection timeout settings
-   Auto-refresh behavior for the Instance Explorer

## Integrations

The Integrations section has the following settings:

-   **Figma** — Connects Lux Lab to Figma for design-to-code workflows directly from the app.
-   **Now SDK Version** — Sets the version of the Now SDK that your project uses. The default is **latest**.

## Updates

The Updates section controls how Lux Lab checks for and applies updates. You can choose stable releases or pre-release builds.

## Advanced

The Advanced section holds configuration options for power users and non-standard setups.

## Default settings

Selecting **Reset to Defaults** at the bottom of the Settings panel restores all settings to their original values. Your projects, work items, and connected instances are unaffected.

