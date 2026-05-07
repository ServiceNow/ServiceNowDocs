---
title: Wrap up email interactions
description: Close email interactions with a wrap-up code to categorize the interaction outcome. Wrap-up codes support both AWA-routed and CCaaS-routed email interactions.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Using Email Interaction for CSM, Customer communication, Use, Customer Service Management]
---

# Wrap up email interactions

Close email interactions with a wrap-up code to categorize the interaction outcome. Wrap-up codes support both AWA-routed and CCaaS-routed email interactions.

## Before you begin

An administrator must configure internal wrap-up codes. See [Wrap up email interactions](wrap-up-email-interactions-eaai.md).

Role required: sn\_customerservice\_agent

## About this task

In the following scenarios, the system assigns a wrap-up code automatically:

-   When a case is created from an interaction, the wrap-up code is auto-selected to Task Created and the interaction is closed complete.
-   When the wrap-up window times out, the default wrap-up code Issue resolved is auto-saved.
-   When the interaction automatically closes because the customer doesn’t respond, the wrap-up code is set to Closed due to customer inactivity.

For more information, see Automatic wrap-up code assignment in [Using Email Interaction for Customer Service Management](../concept/using-email-interaction-customer-service-management.md).

## Procedure

1.  Navigate to **Workspaces** &gt; **CSM/FSM Configurable Workspace**.

2.  Select the List icon \( ![List icon that displays the interactions.](../image/List_icon.jpg)\).

3.  In the Interactions section, select **My Interactions**.

4.  Open an email interaction.

5.  Select **Close**.

    The system auto-detects the routing source \(AWA or CCaaS\) and displays the wrap-up modal with internal wrap-up codes configured by the administrator. The interaction state iss updated to Wrap Up. Select the appropriate wrap-up code from the list.

6.  Select **Submit and Close**.


## Result

-   The email interaction is updated to Closed Complete state.
-   For AWA-routed interactions, the selected wrap-up code is saved in the wrap-up segment table.
-   For CCaaS-routed interactions, the selected wrap-up code is returned to CCaaS and synced back to the instance.

