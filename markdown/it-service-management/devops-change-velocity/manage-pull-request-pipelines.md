---
title: Manage Pull Requests \(PR\) or Merge Requests in DevOps Change Velocity
description: Manage Jenkins, GitHub Actions, and Azure DevOps \(ADO\) pipeline’s pull requests for GitHub, Bitbucket, and ADO coding sources from ServiceNow DevOps. You can enable the change approval process on your pull request to control pull request merge approvals from ServiceNow DevOps and monitor pull request details associated with the change request.
locale: en-US
release: yokohama
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Accelerate your DevOps change process, DevOps Change Velocity, IT Service Management]
---

# Manage Pull Requests \(PR\) or Merge Requests in DevOps Change Velocity

Manage Jenkins, GitHub Actions, and Azure DevOps \(ADO\) pipeline’s pull requests for GitHub, Bitbucket, and ADO coding sources from ServiceNow DevOps. You can enable the change approval process on your pull request to control pull request merge approvals from ServiceNow DevOps and monitor pull request details associated with the change request.

## Before you begin

Ensure that the following prerequisites are met before approving pull requests:

-   Your admin has created a pull request branch in GitHub or Bitbucket using a Multi-branch project pipeline. For more information, see [GitHub branch source](https://plugins.jenkins.io/github-branch-source/) and [Bitbucket branch source](https://plugins.jenkins.io/cloudbees-bitbucket-branch-source/).
-   Your admin has enabled pull request creation in the ADO repository. For more information, see [https://marketplace.visualstudio.com/items?itemName=ShaykiAbramczyk.CreatePullRequest](https://marketplace.visualstudio.com/items?itemName=ShaykiAbramczyk.CreatePullRequest).
-   Your admin has configured Jenkins integration with DevOps. For more information, see [Jenkins integration with DevOps](../concept/jenkins-integration-dev-ops.md).
-   Your admin has configured GitHub integration with DevOps. For more information, see [GitHub integration with DevOps](../concept/github-integration-dev-ops.md).
-   Your admin has configured Bitbucket integration with DevOps. For more information, see [Bitbucket integration with DevOps](../concept/bitbucket-integration-dev-ops.md).
-   Your admin has configured ADO integration with DevOps. For more information, see [Azure DevOps integration with DevOps Change Velocity](../concept/azure-devops-integration-dev-ops.md).
-   Your admin has enabled the Change Acceleration feature of DevOps for automatic change request creation in your pipeline. For more information, see [Accelerating DevOps change](../concept/dev-ops-change-acceleration.md).

Role required: sn\_devops.admin

## About this task

For Jenkins pipelines, pull requests can be managed for GitHub and Bitbucket coding sources.

For GitHub Actions pipelines, pull requests can be managed for GitHub coding source.

For ADO pipelines, pull requests can be managed for ADO coding source.

## Procedure

1.  Create a pull request in GitHub or Bitbucket or ADO.

    For more information, see [Creating a pull request](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/creating-a-pull-request) or [Create a pull request to merge your change](https://support.atlassian.com/bitbucket-cloud/docs/create-a-pull-request-to-merge-your-change/).

2.  Perform the following steps based on your orchestration tool.

<table id="choicetable_khj_xzd_vyb"><thead><tr><th align="left" id="d382010e221">

Orchestration tool

</th><th align="left" id="d382010e224">

Steps

</th></tr></thead><tbody><tr><td id="d382010e230">

**Jenkins**

</td><td>

1.  In the Jenkins dashboard, navigate to **Manage Jenkins &gt; Configure System &gt; ServiceNow DevOps Configuration**.
2.  Select the **Pull Request Pipeline Tracking Check** option.


</td></tr><tr><td id="d382010e257">

**GitHub Actions**

</td><td>

1.  In your GitHub repository, navigate to **Actions &gt; General &gt; Workflow permissions**.
2.  Select the **Allow GitHub Actions to create and approve pull requests** option.
3.  Select **Save**.


</td></tr><tr><td id="d382010e290">

**ADO**

</td><td>

1.  In ServiceNow, navigate to **All &gt; DevOps &gt; Properties.**
2.  Set the **Enable to track Azure DevOps Code Pull-Requests** to **Yes**.

Pull request tracking will be enabled for all the existing configured projects. For any project that is not configured, you must configure them for pull requests to be tracked.

</td></tr></tbody>
</table>3.  Run the pull request pipeline in Jenkins, GitHub Actions, or ADO.

    A build is initiated and a change request notification is sent to the approver associated with the pipeline.

4.  Navigate to **DevOps &gt; Orchestrate &gt; Pipeline Change Requests**.

5.  Select the change record associated with the pull request.

6.  Approve the change request associated with the pull request by selecting **Approved** in the **State** field.

    Merge is enabled in GitHub or Bitbucket or ADO for the pull request. Merge the pull request in the corresponding tool.

7.  Select the Pull Requests related list associated with the change record.

8.  View the pull request details by clicking the pull request number corresponding to the **Number** field.

    ![Pull request details associated with a change record for a Jenkins pipeline](../image/pull-request-change-record.png)

    All the pull request details \(including the details after the request is merged\) associated with the change record are displayed. Details such as Pull request ID, Commits, Origin branch, Destination branch, Raised by, Approver, Comments, PR raised time, PR approved time, PR merged/closed time are displayed. Commits from pull requests are shown in the **Commits** related list.

    -   **Limitation**

        Details of pull requests that are created in a BitBucket coding source and associated with a Jenkins pipeline are not displayed for a change request.


**Parent Topic:**[Accelerating your DevOps change process](../concept/dev-ops-change-acceleration.md)

