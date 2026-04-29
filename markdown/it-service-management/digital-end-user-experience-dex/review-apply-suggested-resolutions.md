---
title: Execute suggested resolutions from incident investigation with DEX
description: Review and execute suggested resolutions from the Investigation tab of incident records to resolve detected issues on DEX monitored devices.
locale: en-US
release: australia
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Suggested resolutions and remedial actions, Incident diagnostics and suggested resolutions, DEX for service desk agents, Digital End-User Experience, IT Service Management]
---

# Execute suggested resolutions from incident investigation with DEX

Review and execute suggested resolutions from the Investigation tab of incident records to resolve detected issues on DEX monitored devices.

## Before you begin

Role required: sn\_dex.service\_desk\_user, sn\_dex.engineer

## About this task

In addition to the suggested resolutions, you can run remedial actions from the Action library in incident investigation with DEX. For more information, see [Run remedial actions from the Action library](remedial-actions-action-library.md).

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace**.

2.  Select the List icon ![](../../../common/image/icon-list.png) from the navigation pane and open the incidents list from the Incidents section.

3.  Open the incident record for a DEX monitored device and select the **Investigation** tab.

4.  Execute resolutions from the **Suggested resolutions** tab to solve device and application issues.

    -   Self-help instruction: Select **View self-help instructions** to view and execute steps to resolve an issue. After completion, select the **Mark as completed** check box.
    -   Catalog request: Select **Create catalog request** to submit a catalog request automatically.
    -   Help resources: Select **View help resource** to navigate to documentation with steps to resolve the issue. After executing the steps, select the **Mark as completed** check box.
5.  If a suggested resolution is a remedial action, execute it.

    1.  Select **Run action** to execute the remedial action automatically.

        A progress bar shows the execution stages. If the action requires end-user approval, the progress bar pauses with the message `Awaiting user approval`.

    2.  If end-user approval is required, contact the end user of the device to obtain approval.

    3.  Once the approval is received, select the Playbook icon ![](../image/icon-playbook.png) from the contextual side panel.

    4.  Expand the device name accordion.

    5.  Select the card for the action that requires end-user approval.

    6.  In the User approval check card, select the check box to confirm that you have received user approval.

    7.  Select **Submit**.

6.  Run multiple remedial actions by selecting the check boxes near the action names and then selecting **Run selected actions**.

7.  Monitor the status of executed resolutions, including actions that failed to execute, by selecting the **Completed** tab.

8.  Cancel an ongoing remedial action.

    1.  Select the Playbook icon ![](../image/icon-playbook.png) from the contextual side panel.

    2.  Expand the device name accordion.

    3.  Choose the action and select **Cancel** on the action card.


