---
title: Release form
description: Create a release for the deployment requests to be deployed to target instances.
locale: en-US
release: zurich
product: ReleaseOps
classification: releaseops
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Reference, ReleaseOps, Deploying applications, Building applications]
---

# Release form

Create a release for the deployment requests to be deployed to target instances.

<table id="table_ejb_t5k_1gc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Release type

</td><td>

Indicates if the release is on-demand or scheduled.

</td></tr><tr><td>

Change request

</td><td>

If a change request is associated with the release, the date on the change request determines the Release date of the release.

</td></tr><tr><td>

State

</td><td>

The state of the release, which will be moved automatically after the release admin selects Activate Release and the release process begins. See [Release states](release-states.md).

</td></tr><tr><td>

Release window

</td><td>

Set automatically by the system and shouldn’t be changed.

</td></tr><tr><td>

Destination environment

</td><td>

Indicates the deployment instance to which the release will be deployed.

</td></tr><tr><td>

Assigned to

</td><td>

Indicates the person who should receive task notifications related to the deployment request. Either Assigned to or Assignment group is required.

</td></tr><tr><td>

Assignment group

</td><td>

Indicates the group who should receive task notifications related to the deployment request. Either Assignment group or Assigned to is required.

</td></tr><tr><td>

Configuration item

</td><td>

An optional association with a configuration item can be selected. This association doesn’t impact the behavior of ReleaseOps.

</td></tr><tr><td>

Pipeline

</td><td>

Indicates the pipeline that this release will run on.

</td></tr><tr><td>

Freeze date

</td><td>

The date on which all deployment requests associated with this release must be in the Ready for Deployment state. All deployment requests must be ready to release and deployed by this date, or else they’ll be deferred \(and removed from the release\).

 During the freeze window, the system orders the update sets be deployed in the order that they were deployed in the last instance.

</td></tr><tr><td>

Release date

</td><td>

The date on which the release will be pushed to the destination environment.

</td></tr></tbody>
</table>**Parent Topic:**[ReleaseOps reference](releaseops-reference.md)

