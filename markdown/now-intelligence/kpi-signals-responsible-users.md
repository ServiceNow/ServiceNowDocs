---
title: Configure responsibility for KPI Signals
description: Besides security access, a user needs a level of responsibility to act on a signal. Responsibility is granted for individual indicator/breakdown element combinations \(KPIs\) that the KPI Signals application monitors.You can assign responsibility for KPI Signals for a KPI to yourself or someone else. You can also unassign responsibility.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/now-intelligence/kpi-signals-responsible-users.html
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, KPI Signals, Platform Analytics experience, Platform Analytics]
---

# Configure responsibility for KPI Signals

Besides security access, a user needs a level of responsibility to act on a signal. Responsibility is granted for individual indicator/breakdown element combinations \(KPIs\) that the KPI Signals application monitors.

A KPI can have multiple responsible users.

Users with the admin, pa\_admin, or pa\_kpi\_signal\_admin role can reset a baseline or dismiss a signal without explicitly being a responsible user. Users with other roles must become responsible users to take such actions. These users also need a role that gives them access to a relevant workspace.

Responsible users get email notifications about the following:

-   New signals
-   Unresolved signals
-   Actions to resolve signals
-   "Anti-signals," which indicate that a KPI is long-term stable

Even responsible users without workspace access get these email notifications.

**Related topics**  


[Configure signal notifications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/configure-signal-notifications.md)

## Assign responsibility for signals

You can assign responsibility for KPI Signals for a KPI to yourself or someone else. You can also unassign responsibility.

### Before you begin

Role required: Any role if a responsible user, or pa\_admin or admin

### Procedure

1.  Open KPI Signals for an indicator, as described in [View KPI Signals](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/view-kpi-signals.md).

2.  Click the cogwheel \[Omitted image "kpi-signals-config-cogwheel.png"\] Alt text: Cogwheel button for KPI Signals configuration to open the KPI Signals configuration.

    \[Omitted image "kpi-signals-open-settings.png"\] Alt text: KPI Signals panel showing the cogwheel button for opening configuration settings

3.  In the KPI Signal Configuration screen, open the **Responsibility** tab.

4.  Select the KPI that you want to assign responsibility for.

    \[Omitted image "kpi-signals-select-kpi-responsibility.png"\] Alt text: KPI Signals configuration panel showing Responsibility tab with a KPI selected

    The user needs relevant workspace roles to view or act on signals. However, a responsible user without these roles still gets email notifications about unresolved signals or actions on signals.

5.  In the **Editing configuration items** panel, open a list of users and select whom to assign responsibility to.

6.  To unassign responsibility, click the x next to a user's name.

7.  Click **Save**.


