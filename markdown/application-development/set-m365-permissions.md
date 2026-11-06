---
title: Manage Microsoft 365 action permissions
description: For each Microsoft 365 action, such as reading Microsoft Teams messages or sending email, select whether Arc takes the action without asking, asks you every time, or never takes it.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/application-development/set-m365-permissions.html
release: australia
topic_type: task
last_updated: "2026-10-27"
reading_time_minutes: 1
keywords: [Microsoft 365 permissions, Microsoft 365 action permissions, Ask me first, needs approval, connector permissions, Set by your organization]
breadcrumb: [Connectors in ServiceNow Arc, Use, ServiceNow Arc, Extend, AI Workflow Factory Prime, Agentic app development, Building applications]
---

# Manage Microsoft 365 action permissions

For each Microsoft 365 action, such as reading Microsoft Teams messages or sending email, select whether Arc takes the action without asking, asks you every time, or never takes it.

## Before you begin

Arc is connected to Microsoft 365. For more information, see [Connect ServiceNow Arc to Microsoft 365](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/connect-cowork-microsoft.md).

Role required: sn\_app\_arc.user

## About this task

Each Microsoft 365 action has three choices. With **Allow**, Arc takes the action without asking. With **Ask me first**, Arc shows an approval card every time it takes the action, and continues only if you allow it. With **Deny**, Arc doesn't take the action.

Your administrator can limit any action. A limited action shows **Set by your organization**, and you can choose only within that limit. For example, if your administrator requires approval, you can choose **Ask me first** or **Deny**, but not **Allow**. Actions your administrator turned off also appear in the list, but you can't turn them on.

## Procedure

1.  In Arc, select your name at the bottom of the sidebar, and then select **Settings**.

2.  Select **Connectors**.

3.  Select the edit button for Microsoft 365.

4.  Scroll to **Permissions**.

    To narrow the list, select an option from the filter list, which shows **All** by default.

5.  For each action, select the icon for the choice you want.

    -   To let Arc take the action without asking, select the check icon \[Omitted image "arc-m365-permission-allow.png"\] Alt text: Allow.
    -   To have Arc ask you every time, select the hand icon \[Omitted image "arc-m365-permission-ask.png"\] Alt text: Ask me first.
    -   To stop Arc from taking the action, select the block icon \[Omitted image "arc-m365-permission-deny.png"\] Alt text: Deny.

**Parent Topic:**[Connectors in ServiceNow Arc](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/connectors-in-cowork.md)

