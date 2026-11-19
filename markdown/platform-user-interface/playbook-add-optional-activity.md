---
title: Add an optional activity to a playbook
description: Add optional activities in Playbook Experience to a running playbook to handle work that the configured stages don't cover.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-user-interface/playbook-add-optional-activity.html
release: zurich
topic_type: task
last_updated: "2026-11-04"
reading_time_minutes: 1
breadcrumb: [About Playbook Experience, Responding to issues in an open record in Workspace, Use, Configurable Workspace UI, Configure UIs and portals, Configure user experiences]
---

# Add an optional activity to a playbook

Add optional activities in Playbook Experience to a running playbook to handle work that the configured stages don't cover.

## Before you begin

Role required: agent

Optional activities must be configured for the playbook.

## About this task

An administrator configures which optional activities are available, and whether an activity can be added to any stage or only to a single stage. If no optional activities are configured for a playbook, none are available to add. For more information, see .

You can't add an optional activity as the first activity in a stage or between two finished activities.

## Procedure

1.  Open a playbook in workspace.

2.  Select the Action menu icon \[Omitted image "playbook-ellipses.png"\] Alt text: Playbook action menu icon.

3.  Select **Add Activity**.

    \[Omitted image "playbook-add-activity-button.png"\] Alt text: Add Activity button to add optional activities.

    **Note:** **Add activity** appears only when optional activities are configured for the stage.

4.  Select **+ Add activity here** in the position where you want the activity.

    \[Omitted image "playbook-add-activity-here.png"\] Alt text: Add an activity to a playbook by selecting + Add activity here.

5.  Select the activity to add to the playbook.

    \[Omitted image "playbook-add-activity-select.png"\] Alt text: Add activity modal.

6.  Select **Done**.


## Result

The selected optional activity appears in your playbook.

\[Omitted image "playbook-add-activity-complete.png"\] Alt text: Optional activities appear in the location selected.

If the activity doesn't appear, the selected position might not accept an optional activity. Select a position that isn't the first activity in the stage or between two finished activities.

If the activity you need isn't listed, it might not be configured for this stage. Contact your administrator.

