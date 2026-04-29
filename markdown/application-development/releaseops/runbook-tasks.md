---
title: Runbook tasks in ReleaseOps
description: Learn about how runbook tasks enable flexibility in ReleaseOps deployments, without needing to customize playbooks each time.
locale: en-US
release: australia
product: ReleaseOps
classification: releaseops
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Explore, ReleaseOps, Deploying applications, Building applications]
---

# Runbook tasks in ReleaseOps

Learn about how runbook tasks enable flexibility in ReleaseOps deployments, without needing to customize playbooks each time.

Many organizations use spreadsheets to track all of the manual and automated activities that must be completed to finish a software deployment or release. ReleaseOps runbook tasks enable you to add those activities directly into your ReleaseOps playbooks, without having to restructure your playbooks as activities vary from one release to the next.

Runbook tasks are activities that pause the progression of a playbook until the specified task is resolved. Runbook tasks are added at the deployment request level, where you specify the playbook, playbook stage, and the point at which the runbook task should occur \(at either the beginning or end of the playbook stage\). Common types of runbook tasks might include:

-   Application install/update
-   Data import - XML
-   Manual action
-   Script - scheduled job
-   Update set commit

When the playbook executes and encounters a runbook task, the playbook pauses progression until the runbook task is resolved.

To add runbook tasks to your deployment requests, see [Create a runbook task](../task/create-runbook-task.md).

