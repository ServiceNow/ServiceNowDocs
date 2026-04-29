---
title: Data Discovery sources
description: Create, and select the data patterns to be used in Data Discovery, and what tables to scan.
locale: en-US
release: australia
product: Data Discovery
classification: data-discovery
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Data Discovery Store, Data Discovery, Platform Privacy]
---

# Data Discovery sources

Create, and select the data patterns to be used in Data Discovery, and what tables to scan.

The **Sources** tab of Data Discovery helps you review your all your data patterns, set which pattern to use for scans, and select the tables to scan.

## All Patterns

The **All Patterns** table lists all current patterns. Note that inactive patterns will show up in this list.See [Create new data pattern](../task/dds-create-new-data-pattern.md) to create a new data pattern.

**Note:** Patterns musts be active to be used in discovery jobs.

|Label|Description|
|-----|-----------|
|Name|Name of the data pattern.|
|Expression|Regular expression used to discover the data pattern.|
|Keyword|A specific word\(or words separated by comma\) to be searched for around a expression.|
|Keyword Proximity|How far from the expression to search for keywords.|
|Privacy Technique Configuration|Privacy technique used for the pattern|

## Active Patterns

The **Active Patterns** table lists all of the current active data patterns. See [Select active data patterns](../task/dds-active-data-patterns.md) to learn how set a pattern to active and used by discovery jobs.

|Label|Description|
|-----|-----------|
|Name|Name of the data pattern.|
|Expression|Regular expression used to discover the data pattern.|
|Keyword|A specific word\(or words separated by comma\) to be searched for around a expression.|
|Keyword Proximity|How far from the expression to search for keywords.|
|Privacy Technique Configuration|Privacy technique used for the pattern|

## Target Tables

The **Target Tables** table lists all tables currently selected for discovery jobs. See [Select target tables](../task/dds-select-target-tables.md) to select tables for use in discovery jobs.

|Label|Description|
|-----|-----------|
|Table Name|The name of the table|
|Display name|The display name of the table \(Used in reporting\)|
|Application|The application scope of the table.|

