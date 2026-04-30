---
title: Get change request number in Jenkins pipeline
description: Retrieve the change request number in a Jenkins pipeline based on specific change details by running the snDevOpsGetChangeNumber script.
locale: en-US
release: xanadu
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Additional information - Jenkins, Jenkins, Integrate, DevOps Change Velocity, IT Service Management]
---

# Get change request number in Jenkins pipeline

Retrieve the change request number in a Jenkins pipeline based on specific change details by running the snDevOpsGetChangeNumber script.

## Before you begin

Role required: Jenkins admin

## Procedure

1.  In your Jenkins dashboard, open the pipeline for which you want to retrieve the change request number.

2.  Navigate to **Configure &gt; Pipeline**.

3.  In the Pipeline script section, update the `snDevOpsGetChangeNumber` script with the following input parameters:

    -   Pipeline Name

        **Note:** For a multi-branch pipeline, the pipeline name must be suffixed with the branch name.

    -   Build Number
    -   Stage Name

        **Note:** For a nested-stage, the stage name must be prefixed with the parent stage name.

    -   Branch Name \(only for multi-branch pipeline\)
    **Note:** If you do not provide the change request details as input parameters, the change request number associated with the current pipeline and stage will be retrieved.

    Example of a multi-branch pipeline:

    ```
    snDevOpsGetChangeNumber (changeDetails: """{ "pipeline_name": "github_multi_branch_pipeline/scratch/release", "build_number": "${env.BUILD_NUMBER}", "stage_name": "Prod/Deploy", "branch_name": "scratch/release" }""");
    ```

    Example of a Jenkins pipeline:

    ```
    snDevOpsGetChangeNumber (changeDetails: """{ "pipeline_name": "github_pipeline", "build_number": "${env.BUILD_NUMBER}", "stage_name": "Prod/Deploy" }""");
    ```

4.  Save the script.

5.  Navigate to **DevOps &gt; Orchestrate &gt; Pipeline Change Requests**.

6.  Select the change record associated with the pipeline.

7.  Approve the change request by selecting  **Approved**  in the  **State**  field.

8.  In Jenkins, open the pipeline for which you are retrieving the change request number.

9.  Select **Build Now**.

    The change request number associated with the pipeline will be displayed as an output in the pipeline.


