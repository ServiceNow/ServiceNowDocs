---
title: Associate steps from GitHub, GitLab, and Azure DevOps with JFrog
description: JFrog Artifactory support for GitHub Actions, Azure DevOps, and GitLab in DevOps Change Velocity enables you to import the artifact data published to JFrog Artifactory for the corresponding pipeline executions. This can then be linked with all the DevOps data collected in DevOps Change Velocity, like Work Items, Commits, Quality Summary, Test Runs, and so on, which helps to trace and identify the root causes.
locale: en-US
release: yokohama
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [JFrog, Integrate, DevOps Change Velocity, IT Service Management]
---

# Associate steps from GitHub, GitLab, and Azure DevOps with JFrog

JFrog Artifactory support for GitHub Actions, Azure DevOps, and GitLab in DevOps Change Velocity enables you to import the artifact data published to JFrog Artifactory for the corresponding pipeline executions. This can then be linked with all the DevOps data collected in DevOps Change Velocity, like Work Items, Commits, Quality Summary, Test Runs, and so on, which helps to trace and identify the root causes.

**Before you begin**

Role required: sn\_devops.admin or sn\_devops.tool\_owner

Azure DevOps release pipelines are not supported.

Associate steps from GitHub, GitLab, and Azure DevOps to your JFrog tool. Before you can associate steps, you must:

-   Connect and configure your GitHub, GitLab, or Azure DevOps tools in DevOps Change Velocity.
-   Run the pipelines in the respective GitHub, GitLab, or Azure DevOps instances.
-   Discover pipelines and steps in the respective tools in DevOps Change Velocity.
-   Connect the JFrog tool in DevOps Change Velocity. The tool must be in the connected state.

**Important:**

-   Build info must be published to JFrog along with the artifacts.
-   Build info must contain the URL and modules or dependencies information.

## Associate steps from pipelines

1.  Open the tool record page of your GitHub, GitLab, or Azure DevOps tool and select the **Pipelines** tab.
2.  Select the pipelines that you want to associate with your JFrog tool.
3.  Select **Associate artifact tool**.

    ![Associate pipelines to JFrog.](../image/jfrog-asso-artifact-01.png)

4.  Select the JFrog tool to which you want the association.

    **Note:** Only the connected JFrog tools are available for selection.

    ![Select JFrog tool.](../image/jfrog-asso-artifact-02.png)

5.  Select the pipeline steps that you want to associate with the selected JFrog tool and select **Associate**.

    **Note:** A step can only be associated with one tool.

    ![Select the steps to associate.](../image/jfrog-asso-artifact-03.png)


The steps are associated with the JFrog tool. You can view the associated steps in your JFrog tool record, under the **Associated steps** tab.

To disassociate a step, select it from the **Associated steps** tab in your JFrog tool record and select **Disassociate**.

![Associated steps in JFrog tool record.](../image/jfrog-asso-artifact-04.png)

## Associate steps from the Steps table

1.  Open the tool record page of your GitHub, GitLab, or Azure DevOps tool and select the pipeline whose steps you want to associate with your JFrog tool.
2.  From the pipeline record, select the **Steps with artifact association** tab and select **Associate**.

    ![Steps with artifact association.](../image/jfrog-asso-artifact-05.png)

3.  From the list of connected JFrog tools, select the tool that you want the steps to be associated with.

    **Note:** Only the connected JFrog tools are available for selection.

    ![Select the JFrog tool.](../image/jfrog-asso-artifact-06.png)

4.  From the list of steps in the pipeline, select the ones you want to associate with the selected JFrog tool and select **Associate**.

    **Note:** If you select a step, which is already associated with another JFrog tool, it is disassociated from that tool and then associated with the current JFrog tool.

    ![Select steps to associate.](../image/jfrog-asso-artifact-07.png)


The selected steps are associated with the JFrog tool. To disassociate a step, select it and then select **Disassociate**.

## Associate step from the step record

For individual steps, you can associate with a connected JFrog tool directly from the step record.

1.  Open the step record page of the step that you want to associate with your JFrog tool.
2.  Select the **Artifact tool** tab and select **Associate**.

    ![Associate a step.](../image/jfrog-asso-artifact-08.png)

3.  From the list of connected JFrog tools, select the tool that you want the step to be associated with and select **Associate**.

    **Note:** Only the connected JFrog tools are available for selection.

    ![Select the JFrog tool.](../image/jfrog-asso-artifact-09.png)


The step is associated with the selected JFrog tool. To disassociate the step, select it and then select **Disassociate**.

## Associate steps from the JFrog tool

You can associate steps directly from the JFrog tool.

1.  Navigate to the connected JFrog tool.
2.  Select the **Associated steps** tab and select **Associate**.

    ![Associate from JFrog tool record.](../image/jfrog-asso-artifact-10.png)

3.  Select the pipelines whose steps you want to associate with the JFrog tool and select **Next**.

    ![Select pipelines containing steps.](../image/jfrog-asso-artifact-11.png)

4.  Select the steps from the pipelines that you want to associate with the JFrog tool and select **Associate**.

    **Note:** If you select a step, which is already associated with another JFrog tool, it is disassociated from that tool and then associated with the current JFrog tool.

    ![Select steps for association.](../image/jfrog-asso-artifact-12.png)


The selected steps are associated with the JFrog tool. To disassociate a step, select it and then select **Disassociate**.

**Parent Topic:**[JFrog integration with DevOps Change Velocity](../concept/devops-jfrog-integration.md)

