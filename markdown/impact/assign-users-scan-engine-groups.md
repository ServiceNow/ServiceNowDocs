---
title: Assign users to Platform Health groups
description: In addition to assigning Impact users to groups, Platform Health users must also be part of a group for the Scan Engine feature.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure the Impact Store Application, Configuring Impact, Impact]
---

# Assign users to Platform Health groups

In addition to assigning Impact users to groups, Platform Health users must also be part of a group for the Scan Engine feature.

## Before you begin

Feature allocation and availability in the Platform Health Scan Engine is based on role and group assignment. See [Analytics Dashboards](../concept/scan-engine-diagnostic-dashboards.md) for additional information on role-based feature availability.

**Note:** You may return to the various steps in the configuration if you don't complete the entire setup at once. As you complete each step successfully, mark the step as complete. Subsequent tasks are locked until the previous step is completed.

Role required: impact app admin or admin

## Procedure

1.  [Use Guided Setup to onboard users to the Impact Store Application](onboard_users_impact_store_application.md).

2.  Navigate to **All** &gt; **Impact** &gt; **Guided Setup** &gt; **Assign Platform Health users**.

3.  Select a user group to assign users to a group.

4.  Create Development Teams.

    Development teams are necessary so each persona can access the relevant Platform Health dashboard. Each record indicates a team and a development team lead that Scan Engine findings will be reported on the Analytics Dashboard.

    1.  Navigate to **All** &gt; **Impact** &gt; **Configuration** &gt; **Scan Engine Properties**.

    2.  In the Team Leads related list, select **New**.

    3.  Create the relevant development teams assigned to the appropriate team lead.

        See [Configure scanning properties per persona](../concept/teamdev-scanning-properties.md#) for additional information on assigning team leads to development teams.

5.  Select **Mark as Complete** to enable the next configuration step.


## What to do next

[Activate Scan Engine and review settings](configure-initial-scan-engine-settings.md)

**Parent Topic:**[Configure the Impact Store Application](../concept/configuring-impact-platform.md)

**Previous topic:**[Use Guided Setup to onboard users to the Impact Store Application](onboard_users_impact_store_application.md)

**Next topic:**[Activate Scan Engine and review settings](configure-initial-scan-engine-settings.md)

