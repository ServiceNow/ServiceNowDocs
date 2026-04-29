---
title: Deployment request states
description: A deployment request might be in one of several different states during the release process.
locale: en-US
release: australia
product: ReleaseOps
classification: releaseops
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Reference, ReleaseOps, Deploying applications, Building applications]
---

# Deployment request states

A deployment request might be in one of several different states during the release process.

<table id="table_lv2_s4j_1gc"><thead><tr><th>

State

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Draft

</td><td>

The deployment request hasn’t yet been associated with a release. Draft is the only state in which an update set can be added to a deployment request.

 A developer keeps their deployment request in Draft state until they believe the work associated with it is complete. It shouldn’t be moved into the Ready for Assessment state until the developer is comfortable with it being deployed as-is.

</td></tr><tr><td>

Ready for Assessment

</td><td>

The developer creating the deployment request has determined that it’s a functional and complete unit and is ready to be deployed.

 This state is the triggering condition for the assessment playbook. Immediately after the developer selects Ready to Assess, assessment will begin, running the processes, tests, and checks defined in the release pipeline.

</td></tr><tr><td>

Assessing

</td><td>

Automated Test Framework \(ATF\) tests are running, instance scans are running, and any Playbooks \(PAD\) process that will determine the suitability of this deployment request to be deployed is executed. Update sets contained within the deployment request are being moved from the development instance to the test instance.

 The Assessment phase results in one of two conclusions:

 -   The deployment request is ready, with no findings requiring action \(by means of a deployment task\).
-   The assessment surfaced one or more findings that must be reconciled for the deployment request to be ready. Deployment tasks will be generated and assigned to the user/group nominated in the request. The outcomes of these tasks are recorded against the request, and the request will be reassessed. This loop continues until the request is ready or canceled.

</td></tr><tr><td>

Reconciling

</td><td>

Open deployment tasks have been generated for action. These tasks must have an outcome for the assessment to be completed and the deployment request to move into the next stage.

 The sample pipelines included in ReleaseOps will create deployment tasks for preview conflicts and ATF test failures. Some outcomes might involve code changes or additions, updates to test suites or configuration, or approvals or sign-offs. After all open deployment tasks have an outcome, the request is reassessed.

</td></tr><tr><td>

Ready for Deployment

</td><td>

All assessments have been performed, and all reconciliations are complete. No new update sets can be added in this state, and the deployment request is effectively locked. If changes must be made at this point, the deployment request must be canceled.

 At this point, if the deployment request is an on-demand deployment, it will continue immediately into deployment. Otherwise, it waits for the scheduled time of the release before continuing.

</td></tr><tr><td>

Deploying

</td><td>

A release is in the process of deploying the update sets associated with this deployment request.

</td></tr><tr><td>

Complete

</td><td>

The deployment request was successfully deployed as part of a release.

</td></tr><tr><td>

Failed

</td><td>

The deployment request had a problem that requires manual intervention or resolution to be resubmitted for a release.

</td></tr><tr><td>

Cancelled

</td><td>

The deployment request was manually canceled.

</td></tr></tbody>
</table>**Parent Topic:**[ReleaseOps reference](releaseops-reference.md)

