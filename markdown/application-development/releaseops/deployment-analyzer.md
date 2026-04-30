---
title: Deployment analyzer in ReleaseOps
description: The deployment analyzer reviews the update set in your release against rules to verify compliance with customizable rules.
locale: en-US
release: zurich
product: ReleaseOps
classification: releaseops
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
keywords: [ReleaseOps, deploy changes, update sets, pipeline, ATF, schedule a release, deployment request, deployment analyzer]
breadcrumb: [Explore, ReleaseOps, Deploying applications, Building applications]
---

# Deployment analyzer in ReleaseOps

The deployment analyzer reviews the update set in your release against rules to verify compliance with customizable rules.

The deployment analyzer scans a given deployment request \(and the update sets it contains\). The deployment analyzer checks for changes as compared to the current state of the production instance \(or the target release environment\). The deployment analyzer operates as a playbook activity, the results of which can be consumed to decide different actions in the deployment process.

By default, the deployment analyzer has five rules. For more information, see [Deployment analyzer rules](../reference/deployment-analyzer-rules.md).

You can create rule types, definitions, and rules as needed. New rules appear in the playbook conditional setup automatically.

