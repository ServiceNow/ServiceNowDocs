---
title: Commits included in DevOps change request
description: The DevOps artifact package and its associated artifact versions are used to determine which commits are included in a DevOps change.
locale: en-US
release: yokohama
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 7
breadcrumb: [Artifacts and packages, Accelerate your DevOps change process, DevOps Change Velocity, IT Service Management]
---

# Commits included in DevOps change request

The DevOps artifact package and its associated artifact versions are used to determine which commits are included in a DevOps change.

Commits are included in a change based on the change type.

<table id="table_myb_wnq_zzb"><thead><tr><th>

Change type

</th><th>

Commits included

</th></tr></thead><tbody><tr><td>

Manual

</td><td>

Commits from the artifact versions of the package in the change. In addition, the commits from task executions of all the pipeline executions in the change reference record when the data\_type column is plan or pipeline execution are included.

</td></tr><tr><td>

Automated

</td><td>

-   Without package: All commits from the artifact versions are included. The artifact versions are the ones that are linked to the pipeline execution and the task executions for that pipeline execution.
-   With package: If any of the upstream task executions of the change has the prod deploy step, then commits from the last successful prod deploy pipeline execution are included. Commits that appear in multiple pipeline executions will be listed only once. If the prod deploy step is not present in the upstream task executions, the commits from all the artifact versions of the package are included.
-   Run commits: If there are no commits from either of the with or without package flow as specified previously, then the run commits from the upstream task executions of the change request are associated.

</td></tr></tbody>
</table>All commits for artifact versions in the package that were generated after the last deployment date \(up to the version currently being deployed\) are included in the change request. Previous major versions are not included.

**Note:** Patch and hot fix versions are excluded.

When provided, semantic version is used to determine commits for a change. Format is \(MAJOR.MINOR.PATCH\). For example, semantic version 2.0.1 is read as follows:

-   Major version 2
-   Minor version 0
-   Patch/hotfix version 1

Failed task executions between the previous and current artifact versions that did not build an artifact but have associated commits are also associated to the created artifact version.

## Types of commits

-   Normal commits: Commits on the tracked repository are associated to the change request.
-   Revert commits: Commits that have the revert field value as true. A revert commit results in a reverted commit and revert commit in the source tree. Both the commits are not associated to the change request.
-   Merge commits: Commits that have the merge field value as true.
    -   Merge commit: The source tree tracks the commit to a branch over time and allows for a special merge commit to be made. This merge commit combines the parent commits located directly after the most recent common commit on both the current branch and the branch to be merged. Merge commit adds a new commit on the main branch.
    -   Squash and merge: Squashing during a merge generates the working tree and index state to match a merge without creating a merge commit. Squash and merge keeps the changes but removes the individual commits from history. It has a single commit with the merge value as true.

## Example: Commits and packages

This example consists of:

-   Three build pipelines \(A, B, and C\)
-   A release pipeline \(ABC\) under change control, with four packages:
    1.  Build pipeline A \(major version 1\)
    2.  Build pipelines A and B \(major version 1\)
    3.  Build pipelines B and C \(major version 1\)
    4.  Build pipelines A, B, and C \(major version 1\)

<table id="table_fk1_33v_rkb"><thead><tr><th>

Commit

</th><th>

Build pipeline

</th><th>

Semantic version

</th><th>

Included in package

</th></tr></thead><tbody><tr><td>

1

</td><td>

A

</td><td>

1.0.0

</td><td>

X

</td></tr><tr><td>

2

</td><td>

A

</td><td>

1.0.1

</td><td>

--

</td></tr><tr><td>

3

</td><td>

A

</td><td>

1.1.0

</td><td>

X

</td></tr><tr><td colspan="4">

**Note:** Commit 2 \(build A, semantic version 1.0.1\) is not included in the package because the semantic version syntax indicates a patch or hot fix.

</td></tr></tbody>
</table><table id="table_in3_ljv_rkb"><thead><tr><th>

Commit

</th><th>

Build pipeline

</th><th>

Semantic version

</th><th>

Included in package

</th></tr></thead><tbody><tr><td>

4

</td><td>

A

</td><td>

1.1.1

</td><td>

--

</td></tr><tr><td>

5

</td><td>

A

</td><td>

1.2.0

</td><td>

X

</td></tr><tr><td>

6

</td><td>

A

</td><td>

1.2.0

</td><td>

X

</td></tr><tr><td>

7

</td><td>

B

</td><td>

1.0.0

</td><td>

X

</td></tr><tr><td>

8

</td><td>

B

</td><td>

1.0.0

</td><td>

X

</td></tr><tr><td>

9

</td><td>

B

</td><td>

1.1.0

</td><td>

X

</td></tr><tr><td>

10

</td><td>

B

</td><td>

1.1.0

</td><td>

X

</td></tr><tr><td colspan="4">

**Note:** Commit 4 \(build A, semantic version 1.1.1\) is not included because the semantic version syntax indicates a patch or hot fix.

</td></tr></tbody>
</table><table id="table_v5g_dnv_rkb"><thead><tr><th>

Commit

</th><th>

Build pipeline

</th><th>

Semantic version

</th><th>

Included in package

</th></tr></thead><tbody><tr><td>

11

</td><td>

A

</td><td>

1.3.0

</td><td>

--

</td></tr><tr><td>

12

</td><td>

B

</td><td>

1.2.0

</td><td>

X

</td></tr><tr><td>

13

</td><td>

B

</td><td>

1.2.0

</td><td>

X

</td></tr><tr><td>

14

</td><td>

C

</td><td>

1.0.0

</td><td>

X

</td></tr><tr><td>

15

</td><td>

C

</td><td>

1.0.0

</td><td>

X

</td></tr><tr><td>

16

</td><td>

C

</td><td>

1.0.0

</td><td>

X

</td></tr><tr><td colspan="4">

**Note:** Commit 11 \(build A, semantic version 1.3.0\) is not included because the package does not specify build A.

</td></tr></tbody>
</table><table id="table_prg_xnv_rkb"><thead><tr><th>

Commit

</th><th>

Build pipeline

</th><th>

Semantic version

</th><th>

Included in package

</th></tr></thead><tbody><tr><td>

17

</td><td>

A

</td><td>

1.4.0

</td><td>

X

</td></tr><tr><td>

18

</td><td>

A

</td><td>

1.4.0

</td><td>

X

</td></tr><tr><td>

19

</td><td>

B

</td><td>

1.3.0

</td><td>

X

</td></tr><tr><td>

20

</td><td>

B

</td><td>

1.3.0

</td><td>

X

</td></tr><tr><td>

21

</td><td>

C

</td><td>

1.1.0

</td><td>

X

</td></tr><tr><td>

22

</td><td>

C

</td><td>

1.1.0

</td><td>

X

</td></tr><tr><td>

23

</td><td>

C

</td><td>

1.2.0

</td><td>

X

</td></tr><tr><td>

24

</td><td>

C

</td><td>

1.2.0

</td><td>

X

</td></tr><tr><td colspan="4">

**Note:** Commit 11 is also included in this package because it is part of the changes in major version 1 of build A since the last package \(including major version 1 of build A\), package \#2, was deployed to production.

</td></tr></tbody>
</table>## Example: Commit calculation logic

Use case with the logic for calculating commits that get associated to artifact versions. The branch information is included whenever the commits are defined.

For example, consider two pipelines, one on the main branch, one on the test branch. Run scenario:

-   Create a commit C0 on main, run CI build, but don’t create Artifact Version.
-   Create a commit C1 on test, run CI build, but don’t create Artifact Version.
-   Create a commit C2 on main, run CI build and the build fails.
-   Create 2 commits C3,C4 on main, run a CI build and create an Artifact Version \(v1.0\).

Expected result: Artifact Version \(v1.0\) is associated to C0, C2, C3, C4. Commit C1 is excluded as it's on a different branch.

Continuing with the use case:

-   Create 1 commit C5 on main, run CI build, but don’t create Artifact Version.
-   Create 1 commit C6 on main, run CI build and create an Artifact Version \(v2.0\).

Expected result: The new artifact version \(v2.0\) created is associated to C5, C6.

**Summary**:

-   All commits from pipeline executions \(success &amp; failed\) in the same branch, between last Artifact Version for a given Artifact and current Artifact Version, are associated.
-   If no previous Artifact Version for the given Artifact is found, then all commits from pipeline executions in the same branch are associated.

Continuing with the use case:

Create a release with Artifact Version from the previous step, have a CD pipeline with Step type = Prod Deploy.

Expected result:

-   Release is associated with the same Artifact Version \(v2.0\).
-   Change Request created shows Artifact Version \(v2.0\) and Commits C0, C2, C3, C4, C5, C6.

**Summary**:

-   Commits from both Artifact Versions \(v1.0, v2.0\) built on main branch \(no previous package was deployed to Prod\) are shown in the change request, but not the commit from execution on test branch.
-   The number of commits shown in the change request will be the same as the number in the tool.

Continuing with the use case:

-   Create 2 commits C7, C8 on test branch, run CI build and create an Artifact Version.

    Expected result: Artifact Version \(v3.0\) is associated to C1, C7, C8.

-   Create 2 commits C9, C10 on main branch, run CI build and create an Artifact Version.

    Expected result: Artifact Version \(v4.0\) is associated to C9, C10.

-   Create a release with Artifact Version from previous step \(v4.0\), have a CD pipeline with Step type = Prod Deploy.

    Expected result:

    -   Release is associated with Artifact Version \(v4.0\).
    -   Change Request created shows Artifact Version \(v4.0\) and commits C9, C10.

**Summary**:

-   The change request shows commits just from the latest Artifact Version built on main branch, as commits from previous Artifact Versions built on main had been deployed to Prod on the previous package.
-   The number of commits shown in the change request will be the same as the number in the tool.
-   To have other step types, like Test or Deploy, use the same commit logic as Prod Deploy, update the **Controls whether other Step types should follow the same logic as Prod Deploy to determine commits for a Change** \[**sn\_devops.commit\_rel\_change\_step\_type**\] property. Specify which step types \(such as Deploy and Test\) should use the same commit logic as Prod Deploy as the property value. If these are set up, the Prod Deploy commit process will also apply to their relationship scripts.

**Parent Topic:**[Artifacts and packages](using-dev-ops-release-change.md)

