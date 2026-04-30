---
title: DEX system tables for remedial actions
description: Definitions for any remedial action are predetermined based on the rules and criteria that store configuration settings for remedial actions. Each execution of the remedial action is maintained in the DEX tables to track the progress of remedial action executions.
locale: en-US
release: yokohama
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [DEX remedial actions, Configure, Digital End-User Experience, IT Service Management]
---

# DEX system tables for remedial actions

Definitions for any remedial action are predetermined based on the rules and criteria that store configuration settings for remedial actions. Each execution of the remedial action is maintained in the DEX tables to track the progress of remedial action executions.

## Remedial action configuration

Stores the configuration settings for remedial actions.

|Field|Description|
|-----|-----------|
|OS|Operating system compatibility \(macOS, Windows, all\)|
|source|Origin of the remedial action \(alert, configuration\_item\)|
|playbook\_type|Type of playbook \(generic, tailored\)|
|check\_definition|Reference to associated check definitions|
|is\_bulk\_action|Flag for bulk action capability|
|active|Status of the configuration|

## Remedial action execution

Tracks the progress of remedial action executions.

|Field|Description|
|-----|-----------|
|state|UI progress state|
|device\_list|List of target devices|
|source\_record\_table|Source table reference|
|source\_record\_id|Source record identifier|

## M2M remedial action execution

Maps the relationship between tracking and actual execution.

| | |
|---|---|
|dex\_remedial\_action\_execution|Links to UI execution record|
|remedial\_action\_execution|Links to actual execution record|

**Note:** For more information on the base system remedial actions, see [Digital End-User Experience Remedial Actions](dex-diff-ra.md).

