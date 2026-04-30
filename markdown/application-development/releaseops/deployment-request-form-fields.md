---
title: Deployment Request form
description: Create a deployment request for the update sets to be deployed to target instances.
locale: en-US
release: zurich
product: ReleaseOps
classification: releaseops
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Reference, ReleaseOps, Deploying applications, Building applications]
---

# Deployment Request form

Create a deployment request for the update sets to be deployed to target instances.

<table id="table_zhq_vvk_1gc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Release

</td><td>

The release that the deployment request is associated with. A deployment request can only be attached to one release. **Note:** Deployment requests are deferred if they aren't in the Ready for Deployment state at the freeze date. If the deployment request is deferred, a new release must be associated with the deployment request to reset its state back to Draft and successfully deploy.

</td></tr><tr><td>

State

</td><td>

The state of the deployment request, which is changed throughout the release process. See [Deployment request states](deployment-request-states.md).

</td></tr><tr><td>

Source environment

</td><td>

The instance that contains the deployment request and its associated update sets.

</td></tr><tr><td>

Assigned to

</td><td>

Indicates the person who should receive task notifications related to the deployment request. Either Assigned to or Assignment group is required.

</td></tr><tr><td>

Assignment group

</td><td>

Indicates the group who should receive task notifications related to the deployment request. Either Assignment group or Assigned to is required.

</td></tr><tr><td>

On demand

</td><td>

Indicates if the deployment request should be released on demand, instead of scheduled.When On demand is selected, ReleaseOps creates a dedicated release that can only have this one deployment request attached. As soon as the deployment request's state is Ready for Deployment, it will be deployed. No freeze or release dates are followed for an on-demand release.

</td></tr><tr><td>

Configuration item

</td><td>

An optional association with a configuration item can be selected. This association doesn’t impact the behavior of ReleaseOps.

</td></tr><tr><td>

Deferred

</td><td>

Checked if the deployment request was deferred due to not being in the Ready for Deployment state by its associated release's freeze date.

</td></tr></tbody>
</table>**Parent Topic:**[ReleaseOps reference](releaseops-reference.md)

