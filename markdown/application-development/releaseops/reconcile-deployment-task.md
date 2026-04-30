---
title: Reconcile a deployment task
description: Reconcile a deployment task to enable a deployment request to move to the next stage in deployment.
locale: en-US
release: zurich
product: ReleaseOps
classification: releaseops
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
keywords: [ReleaseOps, deploy changes, update sets, pipeline, ATF, schedule a release, deployment request, reconcile deployment task, deployment task]
breadcrumb: [Use, ReleaseOps, Deploying applications, Building applications]
---

# Reconcile a deployment task

Reconcile a deployment task to enable a deployment request to move to the next stage in deployment.

## Before you begin

Role required: developer or release\_admin

## Procedure

1.  Navigate to **All** &gt; **ReleaseOps** &gt; **Deployment tasks**.

2.  Select the deployment task that you want to reconcile from the list.

3.  On the deployment task record, review the record to see what type of issue the deployment request encountered.

4.  Reconcile the deployment task, depending on the type of issue.

    |Issue|Description|
    |-----|-----------|
    |**Needs code changes**|Additional coding effort is needed. The deployment request is returned to the Draft state for rework.|
    |**Rerun tests**|ATF re-assessment is needed as the result of insufficient code coverage or incomplete unit tests. The deployment request is returned to the Assessing state, which begins immediately.|
    |**Sign off**|The release manager, or someone with the appropriate permissions, must approve an exception for the deployment request to mark it as Ready for Deployment.|

5.  Once you've addressed the issues in the deployment task, select **Resolve** to enable the deployment request to be reassessed.


**Parent Topic:**[Using ReleaseOps to manage deployments](../concept/using-releaseops-to-manage-deployments.md)

