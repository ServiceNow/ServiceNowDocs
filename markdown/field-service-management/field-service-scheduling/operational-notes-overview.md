---
title: Operational notes
description: Operational notes are day-specific notes that dispatchers add for a technician, crew, equipment, or work order task. Other dispatchers see the notes in Dispatcher Workspace, but technicians can't.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/field-service-management/field-service-scheduling/operational-notes-overview.html
release: australia
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: concept
last_updated: "2026-10-23"
reading_time_minutes: 1
breadcrumb: [Using Dispatcher Workspace, Assigning tasks from Dispatcher Workspace, Scheduling and dispatching, Use, Field Service Management]
---

# Operational notes

Operational notes are day-specific notes that dispatchers add for a technician, crew, equipment, or work order task. Other dispatchers see the notes in Dispatcher Workspace, but technicians can't.

Use operational notes to share scheduling context that other dispatchers need, such as a special requirement for a technician or a task that is waiting on a customer callback. Operational notes are temporary and actionable. They don't affect scheduling optimization or dynamic scheduling.

Operational notes are different from work notes and the activity stream. The activity stream is a permanent record of what happened on a task. Operational notes hold current context for scheduling decisions.

## Who can see and manage notes

Only dispatchers and administrators can see operational notes. Technicians can't see them. Any dispatcher who can see a note can edit or delete it, and a deleted note can't be recovered.

## How notes are stored

All operational notes are stored in the `app_cmn_operational_note` table. Dispatchers manage notes from Dispatcher Workspace, so they don't need to open this table. Administrators can open it to delete notes or change a note's description.

## Note rules

Each note has a plain-text description of up to 4,000 characters. A note is assigned to one record: a user, a crew, equipment, or a work order task. A note covers one or more calendar days. A record can have only one note on a given day, so you can't save a note whose dates overlap another note for the same record. You can create notes for past dates.

## Note indicators on the Gantt and calendar

A note icon appears on a resource or task row in the Gantt \[Omitted image "note-icon-panel.png"\] Alt text: when a note is active on the day you're viewing. Note icons appear only in day views. Week and multi-day views don't show note icons.

On task cards, the note icon \[Omitted image "note-icon-calendar.png"\] Alt text: appears only for notes that are active on today's date. On calendar events, the icon appears for notes that are active on the day you're viewing.

When operational notes are enabled, hovering over a note icon on a task card or calendar event shows the note's description. Resource cards don't show hover text.

## Turning operational notes on or off

Operational notes are controlled by the `sn_fsm_disp_wrkspc.dispatcher_workspace.operational_notes_enabled` system property, which is true by default. Dispatchers can't override this setting.

