---
title: Release states
description: A release might be in one of several different states during the release process.
locale: en-US
release: australia
product: ReleaseOps
classification: releaseops
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Reference, ReleaseOps, Deploying applications, Building applications]
---

# Release states

A release might be in one of several different states during the release process.

<table id="table_d2v_hmj_1gc"><thead><tr><th>

State

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Draft

</td><td>

The initial state of a release. ReleaseOps doesn't act on any release in this state, regardless of the release schedule set. Draft releases don't appear in a deployment request as a target. This enables the creation of schedules into the future, but they must be manually moved into the Active state before deployment requests can be added and deployed.

</td></tr><tr><td>

Active

</td><td>

The release is open in this state, and waiting for the freeze time to arrive. While in this state, attached deployment requests are actively in the Assessing or Reconciling state.

 Deployment requests can still be added at this point, or removed \(by the developer or release admin\).

</td></tr><tr><td>

Preparing

</td><td>

The deployment is frozen. All deployment requests attached to the release are validated to be Ready for Deployment, or else they’re deferred. The release ordering has been generated. A release administrator can remove a deployment request.

 This change of state is derived from the scheduler based on the freeze time.

**Note:** If the release is associated with a change management record, the release time is determined by that change management record.

</td></tr><tr><td>

Ready for Release

</td><td>

All deployment requests are finalized. No deployment requests can be added to or removed from the release, and the release has passed all checks and is eligible for deployment. Any manual steps within the pipeline playbook have been completed.

</td></tr><tr><td>

Deploying

</td><td>

The act of finalizing the move of all build artifacts to the destination instance. This change of state is derived from the scheduler, based on the release time.

 **Note:** If the release is associated with a change management record, the release time is determined by that change management record.

</td></tr><tr><td>

Reconciling

</td><td>

There was a problem with at least one deployment request in the release that requires manual intervention. From the playbook, a deployment task will be created for a preview conflict.

</td></tr><tr><td>

Complete

</td><td>

The release completed without issue.

</td></tr><tr><td>

Cancelled

</td><td>

The deployment of the release was manually canceled before commencement.

</td></tr><tr><td>

Failed

</td><td>

The deployment was either unable to be completed or completed with issues.

 Common reasons for deployment failure include:

 -   An update set is unable to be retrieved.
-   An update set that was planned to be retrieved was already retrieved and committed. The commitment is deemed a failure as the defined order of update set deployments has been broken \(unless this update set was the first in the ordering\).
-   An update set was committed unexpectedly after retrieval.

</td></tr></tbody>
</table>**Parent Topic:**[ReleaseOps reference](releaseops-reference.md)

