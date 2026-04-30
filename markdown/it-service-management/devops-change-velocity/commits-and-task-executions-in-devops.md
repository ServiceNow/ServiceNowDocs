---
title: Commits and task executions in DevOps
description: Run commits in DevOps are associated to a task execution.
locale: en-US
release: xanadu
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Manage, DevOps Change Velocity, IT Service Management]
---

# Commits and task executions in DevOps

Run commits in DevOps are associated to a task execution.

For a commit to show up as a run commit, the commit record must exist in ServiceNow prior to the job/pipeline run.

In the event that jobs are rerun on the same commit, these conditions apply.

-   Azure DevOps doesn’t show any run commits.
-   GitLab displays only the last commit as a run commit.
-   Jenkins displays only the last commit as a run commit on which it was run. The difference of all commits isn’t shown.

Multiple commits in a single payload \(commit arrays\) have these limitations.

<table id="setting-up-dev-ops-conn_table_d3t_32l_wmb"><thead><tr><th id="setting-up-dev-ops-conn_table_d3t_32l_wmb_entry_1">

Tool

</th><th id="setting-up-dev-ops-conn_table_d3t_32l_wmb_entry_2">

Max commits per payload

</th></tr></thead><tbody><tr><td>

Azure DevOps

</td><td>

-   If the DevOps property **Enable whether Azure DevOps Run Commits must be determined from the last successful pipeline build** is enabled, DevOps Change will pick up the last commits, up to a maximum of 2000, created after the last successful pipeline build from Azure DevOps as part of Run Commits.
-   If disabled, only the last 200 commits will be considered for Run Commits.

</td></tr><tr><td>

GitHub

</td><td>

-   If the DevOps property **Enable whether GitHub Run Commits must be determined from the last successful workflow run** is enabled, DevOps Change will pick up the first 2000 commits after the last successful workflow run in GitHub as part of Run Commits.
-   If disabled, only the last commit will be picked up for Run Commits.

</td></tr><tr><td>

GitLab

</td><td>

20

</td></tr></tbody>
</table>**Parent Topic:**[Managing DevOps Change Velocity](using-devops-change-velocity.md)

