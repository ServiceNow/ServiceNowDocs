---
title: Fulfiller pre-built topics for ITSM Virtual Agent
description: Fulfiller topic conversations are designed specifically for ITSM professionals with the itil role. These pre-built topics include resolving an incident, creating a problem, and updating data in the system.
locale: en-US
release: australia
product: ITSM Virtual Agent
classification: itsm-virtual-agent
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Using ITSM Virtual Agent pre-built topics, ITSM Virtual Agent, IT Service Management]
---

# Fulfiller pre-built topics for ITSM Virtual Agent

Fulfiller topic conversations are designed specifically for ITSM professionals with the itil role. These pre-built topics include resolving an incident, creating a problem, and updating data in the system.

## Create Change Request

Users with the itil role can create change requests using their client of choice, such as Slack. Users indicate the type of change request \(**Normal**, **Standard**, or **Emergency**\). Change type definitions are provided by the virtual agent.

For normal and emergency change requests, Virtual Agent prompts the user to enter the following criteria:

-   Short description
-   Justification
-   Configuration item
-   Assignment group
-   Planned start date
-   Planned end date

For standard change requests, Virtual Agent sends a carousel link to a catalog of standard change items. After the user selects an item, Virtual Agent provides a link to open the associated category page to request the change.

![Create Change Request topic.](../image/CreateChangeRequest.png)

## Create Problem

Users with the itil role can create problem records. Users provide a description of the problem and specify the urgency and the impact of the problem. Users must know and enter the associated problematic configuration item as well.

## Identify Available Change Windows

Users with the itil role can check the next available change window for a configuration item. For example, you can determine the next available change window for a specific asset assigned to a user, regarding maintenance or black-out calendars. Users must enter the configuration item to check, such as `PROmonitor`, and then select a planned start and end date and time.

![Identify Available Change Windows topic.](../image/IdentifyAvailableChangeWindows.png)

## Identify Scheduled Changes

Users with the itil role can find upcoming change requests for a specific configuration item \(CI\). To see the change requests, users must type in the name of the configuration item that contains the changes.

## Resolve Incident

Users with the itil role can resolve an incident through support chat by providing a close code, for example, **Solved \(Permanently\)** or **Solved \(Workaround\)**, and resolution notes.

![Resolve Incident topic.](../image/ResolveIncident.png)

## Update Assigned Task

Users with the itil role can update comments or work notes in assigned tasks. When a user wants to update a task, the virtual agent returns a list of all assigned tasks and asks which task the user wants to update. Users can select a single listed task to update or select **All** to load and update all assigned tasks. The virtual agent then asks if the user wants to add a comment, a work note, or both. Optionally, users can cancel the update.

## Update Change Request

Users with the itil role can update the actual start and end time of a change, as well as move it to work in progress or closed states.

**Parent Topic:**[Using ITSM Virtual Agent pre-built topics](../concept/using-itsm-va.md)

