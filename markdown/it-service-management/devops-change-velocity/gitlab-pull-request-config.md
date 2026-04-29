---
title: GitLab pull request configurations
description: GitLab pull \(merge\) request pipeline executions, which goes through change acceleration before moving to production, can be tracked in DevOps Change Velocity. This integration also collects GitLab merge requests meta data to persist in DevOps Change Velocity. The data is linked with the change created in the merge request pipeline execution and can be used for applying change policies, review, and approval.
locale: en-US
release: australia
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [GitLab, Integrate, DevOps Change Velocity, IT Service Management]
---

# GitLab pull request configurations

GitLab pull \(merge\) request pipeline executions, which goes through change acceleration before moving to production, can be tracked in DevOps Change Velocity. This integration also collects GitLab merge requests meta data to persist in DevOps Change Velocity. The data is linked with the change created in the merge request pipeline execution and can be used for applying change policies, review, and approval.

-   Create, update, close, re-open, and merge of pull requests are supported.
-   Pull request pipeline execution for change acceleration in GitLab pipelines is supported. Pull request details will be available for use in the change approval policy.
-   Status of GitLab pipeline is updated with the pull request status automatically after the change creation. The pipeline is paused and resumed automatically.
-   Email ids are defaulted to the format `<user_name>@noreply.gitlab.com`.
-   Comments are supported as part of merge request support. Create and update to pull requests are supported, while delete and edit are not supported.
-   Maximum of 100 commits will be shown in DevOps Change Velocity. If you need to access more than 100, you must refer your GitLab instance. Only the latest comment is populated.

## Settings to enable pull \(merge\) requests for change approval

The DevOps property **Enable to track GitLab pull \(merge\) requests. If not enabled, then pull \(merge\) requests and related events will be ignored** enables the tracking of pull \(merge\) requests from GitLab in DevOps Change Velocity.

**Note:** The property is enabled by default. If you don't want the merge \(pull\) requests to be tracked, you must disable it.

When enabled, the pull \(merge\) request changes will be reflected in DevOps Change Velocity. When disabled, DevOps Change Velocity ignores the pull request events.

For pull request and orchestration pipeline linking and to enable change approval tracking, the following are required:

-   Use GitLab Docker for change tracking. For detailed information, see [Implement custom actions for pipelines using a generic Docker container image](servicenow-custom-actions-for-gitlab.md).
-   From your GitLab project,
    1.  Navigate to
        -   For GitLab cloud: **Settings** &gt; **Merge requests**.
        -   For On premises \(13.x\): **Settings** &gt; **General** &gt; **Merge requests**.
    2.  Select the **Pipelines must succeed** check box.

        With this selection, only if the change is approved, you can proceed with the merge request. That is, when the check box is selected, pull requests will be blocked until the change is approved.

        ![Settings for merge options.](../image/gitlab-merge-01.png)

    3.  Select **Save changes**.
-   Navigate to your project and open the `.yml` file.

    To the `.yml` file, add the following rule at the pipeline level or at specific job levels.

    ```
    rules:
     - if: $CI_PIPELINE_SOURCE == 'merge_request event'
     - if: $CI_PIPELINE_SOURCE != 'merge_request_event'
    ```

    Example for pipeline level:

    ```
    workflow:
      rules:
      - if: $CI_PIPELINE_SOURCE == 'merge_request_event'
      - if: $CI_PIPELINE_SOURCE != 'merge_request_event' 
    
    ```

    Example for job level:

    ```
    changeapproval:
       stage: changeapproval
       script:
         - sndevopscli create change -p '{"changeStepDetails":{"timeout":3600,"interval":100},"attributes":{"short_description":"Automated Software Deployment","description":"Automated Software Deployment.","assignment_group":"a715cd759f2002002920bde8132e7018","implementation_plan":"Software update is tested and results can be found in Test Summaries Tab.","backout_plan":"When software fails in production, the previous software release will be re-deployed.","test_plan":"Testing if the software was successfully deployed or not"}}'
       rules:
       - if: $CI_PIPELINE_SOURCE == 'merge_request_event'
       - if: $CI_PIPELINE_SOURCE != 'merge_request_event'
    
    ```


**Parent Topic:**[GitLab integration with DevOps Change Velocity](gitlab-integration-dev-ops.md)

