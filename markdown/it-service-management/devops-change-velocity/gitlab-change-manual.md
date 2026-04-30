---
title: Change acceleration for manual jobs
description: Enable change tracking for the pipeline in the tool record page in DevOps Change Velocity.
locale: en-US
release: yokohama
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Change acceleration in GitLab, GitLab, Integrate, DevOps Change Velocity, IT Service Management]
---

# Change acceleration for manual jobs

Enable change tracking for the pipeline in the tool record page in DevOps Change Velocity.

The GitLab job under change control must have these instructions for the pipeline execution to be resumed or canceled via the change request:

-   **when:** `manual`
-   **allow\_failure:** `false`

For example:

```

deploy:
  stage: deploy
  tags:
    - local-runner1
  when: manual
  allow_failure: false
  script:
    - echo 'Deploy'
```

**Note:** For **when:manual** based changes, for a change request to get created at a certain stage, all the previous stages must complete successfully. If any of the previous stages is not invoked or not successful, even though there is no dependency of the current stage on its immediate previous stage, a change request will not get created in ServiceNow.

GitLab pipeline parallel stages is supported with GitLab Docker Image. For more details, see [GitLab pipelines with parallel jobs](gitlab-parallel-stages.md) and [Implement custom actions for pipelines using a generic Docker container image](servicenow-custom-actions-for-gitlab.md).

Refer to the [CI/CD pipeline configuration reference](https://docs.gitlab.com/) for more information on how to configure a GitLab job.

Additional considerations:

-   If **allow\_failure** is set to `true`, the pipeline continues even when the change is rejected.
-   A user with the appropriate role access in GitLab can unblock and continue a pipeline regardless of the change request state.

<table id="table_exk_tmb_gmb"><thead><tr><th>

Manual execution

</th><th>

Change acceleration in step

</th><th>

Change request approved

</th><th>

Result

</th></tr></thead><tbody><tr><td rowspan="4">

Yes

</td><td rowspan="3">

Yes

</td><td>

N/A

</td><td>

If the manual job is under change control, the change is automatically created.

</td></tr><tr><td>

Yes

</td><td>

The manual job is automatically executed.

</td></tr><tr><td>

No

</td><td>

The manual job is automatically rejected/failed.

</td></tr><tr><td>

No

</td><td>

N/A

</td><td>

The manual job waits for manual intervention from the pipeline owner via the GitLab UI \(default behavior\).

</td></tr><tr><td>

No

</td><td>

Yes

</td><td>

N/A

</td><td>

The change request is not created.

</td></tr></tbody>
</table>**Note:** Parallel jobs are displayed sequentially, based on the order in which the jobs are queued for execution.

**Parent Topic:**[GitLab integration with DevOps Change Velocity](gitlab-integration-dev-ops.md)

