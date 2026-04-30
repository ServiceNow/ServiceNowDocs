---
title: PaCE policy version states
description: A PaCE policy version can be in one of four states: Draft, Current, Archived, and Now-Content. The policy version state also defines the version numbering.
locale: en-US
release: xanadu
product: Policy as Code Engine \(PaCE\)
classification: policy-as-code-engine-pace
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Manage PaCE policy versions, Administer PaCE policies, Policy as Code Engine \(PaCE\), Extend ServiceNow AI Platform capabilities]
---

# PaCE policy version states

A PaCE policy version can be in one of four states: Draft, Current, Archived, and Now-Content. The policy version state also defines the version numbering.

Only one policy version in each policy can be Current at any one time. There is no limit to the number of Draft or Archived policy versions.

<table id="table_jj1_bd4_w4b"><thead><tr><th>

State

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Draft

</td><td>

When a version is created, its initial state is Draft. The new Draft version can be saved as a Draft for later use, or published to become the Current version. The draft versions cannot be used until they are published.

</td></tr><tr><td>

Current

</td><td>

Draft versions can be published to Current, which means the former draft version becomes the default published version used for policy execution. **Note:** When publishing the version, if mapping exists, verification is performed to confirm that all required inputs for mapping inputs were provided. If you update the mapping inputs, you must update the inputs in the Mapping screen. If you updated caller inputs, you must update the PaCE API call to ensure that the policy is executed.

</td></tr><tr><td>

Archived

</td><td>

A published Current version becomes Archived when a different version is published. Only Current versions can be Archived. If necessary, you can also republish an Archived version.**Note:** When a version is published, it becomes the Current version irrespective of its previous states.

</td></tr><tr><td>

Ready

</td><td>

The Ready state is assigned to optional policies available when an application content pack is installed. These policies cannot be modified. If you want to modify a policy, create a copy and make the required changes.

</td></tr></tbody>
</table>## Policy version numbering

There are three identifiers for each version: Version name, Version, and Revision number. These identifiers are shown as three separate columns in the **Versions** tab.

<table id="table_phw_whp_gpb"><thead><tr><th>

Identifier

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Version name

</td><td>

For Draft versions, the version name uses Draft-V\{Revision number\}.

 For Current \(published\) or Archived versions, V\{Version\} is used for the name.

</td></tr><tr><td>

Version

</td><td>

The Version number is assigned only when you publish a version. The number is automatically created according to the existing version number. For the first Current \(published\) version, the number is 1.0 and for subsequent current versions, the number increases by +1.0. For example, 2.0, 3.0, 4.0, and so on. Current versions that have been Archived retain the original version number.

 Draft versions are not assigned a version number.

</td></tr><tr><td>

Revision number

</td><td>

The Revision number is derived from the version that it was created from. If an empty new policy is created, the initial draft version is assigned 0.1. Each subsequent draft version is assigned 0.2, 0.3, 0.4, and so on.If the version was created from a published \(Current or Archived\) version, it inherits the Version number. For example, you can create a draft version from the Current \(published\) version 2.0. The draft version is assigned the revision number 2.1.

</td></tr></tbody>
</table>The following image illustrates the different states and their version numbering.

![Policy version numbering.](../image/pace-version-numbering-1.jpg)

As shown in the preceding image, the first draft policy version created was automatically assigned the Revision number 0.1. Each subsequent draft is assigned V0.2, V0.3, and so on. Draft version 0.2 \(as indicated in the Revision number column\) was published and became the Current version, with the Version name of V1.0.

A draft version of this Current version was created, with the Revision number 1.1. That draft was published to become the Current version and was assigned the Revision number 1.1. The previously Current version is now Archived, but retains the Revision number 0.2.

