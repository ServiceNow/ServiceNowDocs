---
title: Analytics and reporting using the DevOps Config Insights dashboard
description: Use the DevOps Config Insights dashboard with Performance Analytics to quickly identify configuration errors and take action. View snapshot validation trend, open changesets, and failed snaphots for all applications and deployables.
locale: en-US
release: australia
product: DevOps \(Family\)
classification: devops-family
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [DevOps Config, IT Service Management]
---

# Analytics and reporting using the DevOps Config Insights dashboard

Use the DevOps Config Insights dashboard with Performance Analytics to quickly identify configuration errors and take action. View snapshot validation trend, open changesets, and failed snaphots for all applications and deployables.

**Important:** DevOps Config is now deprecated and no longer supported or available for new activation.

Error thresholds are configurable and widgets are customizable \(you can rearrange or hide them\).

You can filter results on applications, deployables, and by date.![DevOps Config Insights home](../image/devops-config-insights-home.png)

<table id="table_jcx_kdg_wpb"><thead><tr><th>

Report

</th><th>

Description and use case

</th></tr></thead><tbody><tr><td>

Open changesets

</td><td>

Open changeset details.

 Use case:

 As a DevOps engineer or App Engineer, I want to review my open changesets so that I can take action on them right away and not let them get stale.

 Accidentally committing changesets later could add risk to my data model and, by consequence, the fleet.

</td></tr><tr><td>

Failed snapshots

</td><td>

Non-compliant snapshots for changes committed.

 Use case:

 As a DevOps engineer or App Engineer, I want to review non-compliant snapshots for changes I committed so that I ensure my changes are in line with company policies before pushing the data out to my production environment.

</td></tr><tr><td>

Policy exception and recommended actions

</td><td>

Recommended actions for policies that have exceptions.

 Use case:

 As a DevOps Config and GRC customer, I want to be able to see the list of active exceptions and, for ones that are expiring soon, what the recommended action is.

</td></tr></tbody>
</table>## DevOps Config Insights Open changesets

![DevOps Config Insights Changesets](../image/devops-config-insights-changeset.png)

Review the changeset details and either make changes to the config data and commit the changeset, or discard the changeset altogether. You generally want this number to be 0 on the dashboard.

## DevOps Config Insights Failed snapshots

![DevOps Config Insights snapshot](../image/devops-config-insights-snapshot.png)

Investigate the snapshots and fix misconfigurations, or identify changes that need to be made to a policy. You generally want this number to be 0 on the dashboard.

## DevOps Config Policy exceptions

<table id="table_c5w_y1x_f5b"><tbody><tr><td>

Nothing

</td><td>

If the issue is already resolved and the latest snapshot status passed; or withdraw the exception if it is no longer needed.

</td></tr><tr><td>

Fix the issue

</td><td>

If the latest snapshot validation status is passed with exception and there's time to fix the issue before the exception expires.

</td></tr><tr><td>

Extend the exception

</td><td>

If the latest snapshot validation status is passed with exception and there isn't enough time to fix the issue.

</td></tr></tbody>
</table>