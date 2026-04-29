---
title: Auto-dismiss alerts in CSM Configurable Workspace
description: In CSM Configurable Workspace, alerts automatically dismiss after a set time to reduce alert fatigue and help agents stay focused. By default, Info, Low, and Moderate alerts dismiss after 5 seconds, while Critical and High alerts remain persistent until manually dismissed. Admins can customize the auto-dismiss behavior and timer duration for each alert level.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Set up CSM Configurable Workspace, CSM Configurable Workspace, Organize agent workspaces, Configure, Customer Service Management]
---

# Auto-dismiss alerts in CSM Configurable Workspace

In CSM Configurable Workspace, alerts automatically dismiss after a set time to reduce alert fatigue and help agents stay focused. By default, Info, Low, and Moderate alerts dismiss after 5 seconds, while Critical and High alerts remain persistent until manually dismissed. Admins can customize the auto-dismiss behavior and timer duration for each alert level.

Admins can configure auto-dismiss alert behavior at the experience level either using UI Builder or UX Page Properties. This configuration provides control over timer duration and display options. Agents view alerts based on the configuration created by the admin.

Role required: admin

You can either configure this feature using UI Builder or UX Page Properties, depending on your preference.

**Configuring using UI Builder**:

1.  Navigate to **All** &gt; **Now Experience Framework ** &gt; **UI Builder**.
2.  Select the **CSM/FSM Configurable Workspace** experience.
3.  In the top-right corner, select **View experience settings**.
4.  Scroll to the Configurable alerts section.
5.  For each alert level, modify the **Auto-dismiss** check box as needed. Info, Low, and Moderate alerts are enabled by default.
6.  In the **Timeout \(seconds\)** column, enter the duration for which the alert should remain visible. The default is 5 seconds.
7.  Configure the following display options.
    -   **Show time label**: Shows a countdown timer on the alert. This option is enabled by default.
    -   **Expand alert content by default**: Automatically expands the alert content when it appears.
8.  Select **Save**.

**Configuring using UX Page Properties**:

1.  Navigate to the UX Page Properties list by entering `sys_ux_page_property.list` in the application navigator.
2.  In the Name column, search for the alert\_auto\_dismiss\_config property.
3.  Select the property name to open the UX page property form.
4.  In the **Value** field, define the alert levels you want to configure. For example, add the following information to configure an info alert.

<table id="table_qbz_fty_bgc"><thead><tr><th>

Option

</th><th>

Description

</th></tr></thead><tbody><tr><td>

info

</td><td>

Identifies the alert level as an informational alert. Other levels include:-   critical
-   high
-   moderate
-   warning
-   low


</td></tr><tr><td>

enabled

</td><td>

Turns on auto-dismiss for the alert level. Set to true.

</td></tr><tr><td>

timeout

</td><td>

The duration for which the alert remains visible. The default value is 5 seconds. Info, Low, and Moderate alerts are enabled by default.

</td></tr><tr><td>

showTimer

</td><td>

Shows a visible countdown before the alert disappears. Set to true.

</td></tr></tbody>
</table>5.  Select **Save**.

