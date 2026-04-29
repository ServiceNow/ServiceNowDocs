---
title: Deviations life cycle
description: The deviation life cycle is the list of states that a deviation can go through.
locale: en-US
release: australia
product: Digital Factory Workspace
classification: digital-factory-workspace
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Deviation Management, Industrial Workflows, Use, Digital Factory Workspace, Industrial Connected Workforce]
---

# Deviations life cycle

The deviation life cycle is the list of states that a deviation can go through.

The deviation life cycle has the following states:

-   Found
-   Open
-   Scheduled
-   Fixed
-   Closed
-   Canceled

Once the deviation is fixed, it can be closed or reopened by a deviation expert.

**Note:** Deviations in the Fixed state are automatically moved to Closed after the number of days defined by the system property **sn\_icw.deviation\_close\_after\_days**. The default value is seven days.

Only the resolution and resolution code are still editable. If it's in any other state, it can be canceled.

**Note:** The actions Close, Cancel and Reopen are restricted to users with the sn\_icw.deviation\_expert role, while other actions are supported for both the sn\_icw.deviation\_user and sn\_icw.deviation\_expert role.

You can manage deviations, such as bulk assign from the list view, which is only available in the Workspace.

**Parent Topic:**[Deviation Management](industrial-deviation-management.md)

