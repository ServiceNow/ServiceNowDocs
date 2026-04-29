---
title: View unread email counters on interaction tabs
description: Unread email counters display on email interaction tabs in CSM Configurable Workspace to help agents track new email activity across multiple interactions.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Set up CSM Configurable Workspace, CSM Configurable Workspace, Organize agent workspaces, Configure, Customer Service Management]
---

# View unread email counters on interaction tabs

Unread email counters display on email interaction tabs in CSM Configurable Workspace to help agents track new email activity across multiple interactions.

## Before you begin

Role required: admin

## About this task

Unread email counters help agents manage multiple email interactions efficiently by providing visual notification of new activity without requiring agents to switch between tabs. This enables agents to prioritize responses and maintain context while working on the current interaction.

When new emails arrive for an email interaction in an inactive tab, a counter increments on the tab. The counter clears when you select the tab. Hover over the tab to preview the latest email without switching to that interaction.

Example: You have multiple email interactions open in tabs. A customer replies to an interaction in an inactive tab. The tab displays an unread counter, such as \(2\), indicating new activity without requiring you to switch tabs. Complete the following configuration steps to enable unread email counters on interaction tabs.

Complete the following configuration steps to enable unread email counters on interaction tabs.

## Procedure

1.  Verify email receiving is enabled.

    1.  Navigate to **All** &gt; **Email Properties**.

    2.  Confirm that the **Email receiving enabled** check box is selected.

        If the check box is not selected, select it and select **Save**.

2.  Verify email system status.

    1.  Navigate to **All** &gt; **System Mailboxes** &gt; **Administrators** &gt; **Email Diagnostics**.

    2.  Verify that email sending and receiving statistics show operational status.

    3.  Verify that the connection status displays a green check mark.

3.  Configure the email address for receiving emails.

    1.  Navigate to **All** &gt; **System Properties** &gt; **sys\_properties.LIST**.

    2.  In the **Search** field, enter `sn_eaai_csm.email_addresses`.

    3.  In the **Value** field, verify that an email address is specified.

        If the field is empty, enter the email address where you want to receive emails.

    4.  Select **Update**.

4.  Configure presence states for email channels.

    1.  Navigate to **All** &gt; **Advanced Work Assignment** &gt; **Presence States**.

    2.  Select **Available**.

    3.  In the **Available** block, select **Chat - Asynchronous** and **Email**.

    4.  Move the selected options to the **Selected** block.

    5.  Select **Update**.


## Result

Email interactions appear under the **Ongoing** icon in the left navigation pane below the **Inbox**.

When configured agents receive new emails for interactions open in inactive tabs, an unread counter displays on the tab. Selecting the tab clears the counter and displays the interaction with the new email messages.

**Related topics**  


[Email Interaction record page](../concept/csm-email-interaction-record-page.md)

