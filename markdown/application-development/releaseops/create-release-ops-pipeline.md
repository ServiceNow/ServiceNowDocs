---
title: Create a custom pipeline
description: Create a custom pipeline to move changes from your development environment to production \(or your target instance\) by duplicating one of the ReleaseOps playbooks.Create a custom pipeline to move changes through your non-production environment by duplicating the Deployment Request Assessment playbook. Add the deployment analyzer to detect if there are code changes in the deployment and skip Automated Test Framework \(ATF\) tests during assessment.
locale: en-US
release: zurich
product: ReleaseOps
classification: releaseops
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
keywords: [ReleaseOps, deploy changes, update sets, pipeline, ATF, schedule a release, deployment request, deployment analyzer]
breadcrumb: [Configure, ReleaseOps, Deploying applications, Building applications]
---

# Create a custom pipeline

Create a custom pipeline to move changes from your development environment to production \(or your target instance\) by duplicating one of the ReleaseOps playbooks.

## Before you begin

Role required: releaseops.pipeline\_admin and playbook.admin or pd\_author

For more information about playbooks, see [Exploring Playbook](https://www.servicenow.com/docs/access?context=process-automation-designer&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US).

## Procedure

1.  Duplicate one of the ReleaseOps playbooks.

    1.  Navigate to **All** &gt; **Workflow Studio** and select the desired playbook.

    2.  Enter a name for your new playbook and update any other required details.

    For more information, see [Duplicate Playbooks](https://www.servicenow.com/docs/access?context=duplicate-process&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US).

2.  Add or update stages in the playbook as desired.

    **Note:** Certain stages make sense at certain parts of the flow. For example, the deployment analyzer runs before the deployment state Move To Test. Other stages might need to be run after Move to Test or after Run ATF Tests. Typically, you shouldn’t add anything after Ready for Deploy.

    For more information, see [Add and configure a stage in a playbook](https://www.servicenow.com/docs/access?context=add-configure-stage&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US).

3.  Add or update decisions in the playbook as needed.

    For more information, see [Decision activities](https://www.servicenow.com/docs/access?context=create-a-decision-activity&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US).

4.  Select **Activate** to finalize your updates and make your new playbook available for use.

5.  Create a pipeline that leverages your new playbook.

    1.  Navigate to **All** &gt; **ReleaseOps** &gt; **Pipelines** and select **New**.

    2.  Give your pipeline a name, and select playbooks for the **Assessment playbook** and **Release playbook** fields.

        You can use your own custom playbooks for both, or use a combination of custom and sample playbooks.

    3.  Right-click the header on the Pipeline form and select **Save**.

6.  On your newly created pipeline, locate the Pipeline instances related list and select **New**.

    1.  Select the label `Test.`

    2.  Select your deployment instance.

    3.  Select **Submit**.


## Example: Create an assessment playbook

Create a custom pipeline to move changes through your non-production environment by duplicating the Deployment Request Assessment playbook. Add the deployment analyzer to detect if there are code changes in the deployment and skip Automated Test Framework \(ATF\) tests during assessment.

### Before you begin

Role required: releaseops.pipeline\_admin and playbook.admin or pd\_author

### Procedure

1.  Duplicate the Deployment Request Assessment playbook.

    1.  Navigate to **All** &gt; **Workflow Studio** and select the **Deployment Request Assessment** playbook.

    2.  Select **Duplicate** from the More actions menu.

    3.  Enter a name for your new playbook and update any other required details.

2.  Add a new stage to the playbook by selecting the + icon after Start, and enter a label, for example `Analyze Deployment`.

    **Note:** Certain stages make sense at certain parts of the flow. For example, the deployment analyzer runs before the deployment state \(Move To Test\). Other stages might need to be run after Move to Test or after Run ATF Tests. Typically, you shouldn’t add anything after Ready for Deploy.

3.  Add the **Run Deployment Analyzer** activity.

4.  Select the newly added Run Deployment Analyzer activity to configure it.

    1.  Select the **Automation** tab on the additional options modal.

    2.  In the Inputs section of the modal, select the icon and then select **Parent Record - Deployment Request**.

    3.  Select **Save and close**.

5.  Locate the Run ATF Tests section of the playbook, and add a new decision after the Transition to Assessing activity by selecting the + icon, and then selecting **Add a decision \(if/then\)**.

    For more information, see [Decision activities](https://www.servicenow.com/docs/access?context=create-a-decision-activity&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US).

6.  Select the newly added decision to configure it.

    1.  Select the **Branches** tab, and enter a label, for example `Skip Tests`.

    2.  Select **Add Condition**.

    3.  From the Field dropdown menu, select **1.1 Deployment Analyzer** &gt; **Outputs** &gt; **Has Code Change**.

    4.  Select **is** from the Operator dropdown menu.

    5.  Select **false** from the True/False dropdown menu.

    6.  Select **Save and Close**.

7.  Hover over the Skip Tests branch, select **Drag new connector** icon, and drag the connector to the junction after the Create Test Failure Task.

    Confirm that the default branch is connected to Run ATF Tests for Deployment.

8.  Select **Activate** to finalize your updates and make your new playbook available for use.

9.  Create a pipeline that leverages your assessment playbook.

    1.  Navigate to **All** &gt; **ReleaseOps** &gt; **Pipelines** and select **New**.

    2.  Give your pipeline a name, and select your newly created playbook in the **Assessment playbook** field.

    3.  Select and hold \(or right-click\) the header on the Pipeline form and select **Save**.

10. On your newly created pipeline, locate the Pipeline instances related list and select **New**.

    1.  Select the label `Test.`

    2.  Select your deployment instance.

    3.  Select **Submit**.


### Result

Your custom pipeline, which leverages the custom playbook you created from the default Deployment Request Assessment playbook for its assessment stage, is now ready for use.

**Note:**

-   The pipeline instance label \(in the example above, the `Test` label entered for step 10a\) is used to map the instance definition with the instance as referenced in the playbook. Mapping the instance definition with the instance label enables a playbook to be used by multiple pipeline definitions with different topologies \(but the same process\). For example, you can create another pipeline record and associate it to the same playbooks, but define a different test instance mapping.
-   The source instance for the playbook is defined in the deployment request, so you can have multiple source or development environments for one release.
-   The destination instance is defined in the release, so you can reuse the same pipeline to release to multiple destination or production environments.
-   Only intermediate instances must be mapped.

