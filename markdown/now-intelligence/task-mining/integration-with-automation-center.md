---
title: Integration with Automation Center
description: Create automation requests for your tasks directly from Task Mining.
locale: en-US
release: zurich
product: Task Mining
classification: task-mining
topic_type: concept
last_updated: "2025-11-21"
reading_time_minutes: 1
breadcrumb: [Integrating Task Mining, Explore, Task Mining, Platform Analytics]
---

# Integration with Automation Center

Create automation requests for your tasks directly from Task Mining.

You must install and configure the Automation Center plugin before using the integration. See [Install Automation Center](https://www.servicenow.com/docs/access?context=install-automation-center&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US) for more information.

To use the Now Assist feature in the integration, you must install Now Assist for Platform and activate the User Task Step Summarization skill. For more information, see [Install Automation Center](https://www.servicenow.com/docs/access?context=install-automation-center&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US).

## Initiate an automation request from the Task timeline analysis

![Infographic showing how users use the Task Mining integration with Automation Center to submit automation requests. For details, refer to the following description.](../image/tm-integrate-ac.png "Automation request workflow")

1.  As a Task Mining analyst, you create a Task Mining project with a Task timeline analysis as a Mining analysis goal. For more information, see [Create a Task Mining project](../task/create-task-mining-projects.md). You group user actions as a task to provide data for the analysis. For more information, see [Define user actions for task logging](../task/mine-data.md).
2.  Run a mining job on the Task Mining project to generate the Task timeline analysis of your project data.
3.  Go to the project's Task timeline analysis, and select a task to see a detailed list of the steps of the task.
4.  Create a copy that you use for automation without affecting the original. In the duplicate task, edit any of these steps if you want to change task details.
5.  When you're ready, select Take action and select the Request automation improvement action.
6.  Fill out the Automation Center Create New Automation Request form. Use the Generate details option to populate the description and detailed sequence of steps fields.

    **Note:** The generate details option is available only if Now Assist for Platform is installed and the User Task Step Summarization skill is activated.


![Screenshot showing the completed New Automation Request form.](../image/tm-automation-request-done.png)

**Parent Topic:**[Integrating Task Mining](integrations-for-task-mining.md)

**Related topics**  


[Task Mining analyses](task-mining-dashboard.md)

[Identify task improvement actions](../task/identify-improvement-opportunities.md)

