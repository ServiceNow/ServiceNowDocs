---
title: Import based evidence collection
description: Reduce instance overhead by skipping step-level pipeline processing for accelerated change management and evidence collection for GitHub Actions, Azure DevOps \(ADO\), Jenkins and GitLab orchestration tools.
locale: en-US
release: yokohama
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Accelerate your DevOps change process, DevOps Change Velocity, IT Service Management]
---

# Import based evidence collection

Reduce instance overhead by skipping step-level pipeline processing for accelerated change management and evidence collection for GitHub Actions, Azure DevOps \(ADO\), Jenkins and GitLab orchestration tools.

All relevant evidence in the pipeline is attached to the change request using import request instead of webhook notifications.

## Enable import based evidence collection

You can enable this feature by switching on the **Import based evidence collection for orchestration capability** toggle in the Properties page. For more information, see [DevOps Change Velocity properties](dev-ops-administration.md).

Switching the toggle modifies how the pipeline events are processed. When switched on, the setting reduces instance overhead by skipping step-level processing in the pipeline. The skipped step-level events are ignored with the processing details, "IGNORED: This event is ignored because the 'Import based evidence collection for orchestration capability' property is enabled". Conversely, switching off reverts to the standard mode, where all inbound events undergo processing.

**Note:** Ensure that no pipeline is running before making changes to this setting. Switching the toggle during an active pipeline execution may cause the pipeline to hang and eventually time out, resulting in incomplete or incorrect data collection. If a change request has already been created, you must cancel it manually, as required evidence may not be attached. Select **Save** to continue, and initiate a new pipeline execution after switching the toggle.

## How is the evidence collected

When the change step in a pipeline is triggered, a callback record is created with the **state: created** and **change evidence status: pending**. An import request, with the corresponding import request pages are created to gather pipeline execution details and the required evidence. The change request is then created with all the evidence attached to it. In addition, the import based evidence collection feature is triggered again at the pipeline completion event to ensure all the associated evidence is accurately retrieved and associated with the change request. Post-creation of the change request, the auto-approval mechanisms, and subsequent behaviors remains the same as the existing behavior.

-   **For ADO**
    -   For build pipeline, when the property is enabled, the evidence collection happens based on the pipeline completion event only \(step level events aren’t processed to reduce the instance overhead\).
    -   For release pipeline, even if the property is enabled, the evidence collection happens based on processing step-level events.
-   **For GitHub Actions**
    -   When the property is enabled, the evidence collection happens based on the workflow completion event only \(step level events aren’t processed to reduce the instance overhead\).
    -   If you’re using GitHub Actions Deployment Gates in any of your steps, then you must configure the GitHub app, and the evidence collection happens based on the workflow completion event. For more information on deployment gates, see [GitHub Deployment Gates for ServiceNow DevOps Change](github-deployment-gate-for-servicenow-devops-change.md).
-   **Jenkins**

    When the property is enabled, the evidence collection happens based on the pipeline completion event only \(step level events aren’t processed to reduce the instance overhead\).

    **Note:** You must install the latest Jenkins from the Jenkins Marketplace. Navigate to **Manage Jenkins &gt; System configuration &gt; Plugins** in your Jenkins instance. Search for ServiceNow DevOps Plugin and select it, and then select **Install**.

-   **GitLab**

    When the property is enabled, the evidence collection happens based on the Pipeline events webhook event only \(step level events aren’t processed to reduce the instance overhead\).


## Key points

-   Import based evidence collection supports all existing pipeline styles \(reruns, parallel, sequential\) and configurations for GitHub Actions, Jenkins, and ADO.
-   All types of evidence collection supported for GitHub Actions, ADO, GitLab, and Jenkins in the base system are also supported when this property is enabled.
-   For GitHub Actions, environment-based change isn’t supported.
-   For GitLab, manual jobs \(when: manual\) are not supported.

    For example,

    ```
     run_tests:
      script: npm test
      when: manual
      allow_failure: true
    ```

-   For Jenkins, Freestyle pipelines are not supported.
-   Historical import and polling features works the same way regardless of the **Import based evidence collection for orchestration capability** property being enabled or turned off.
-   Restarting import in the import request record is also supported.
-   Troubleshooting and error handling frameworks remain unaffected.
-   If you’re upgrading, the **Import based evidence collection for orchestration capability** property is turned off by default.

**Parent Topic:**[Accelerating your DevOps change process](dev-ops-change-acceleration.md)

