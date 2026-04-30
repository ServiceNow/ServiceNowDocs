---
title: Configure a communication plan in Major Incident Management
description: Configure a communication plan and tasks for effective communication with various stakeholders about the progress, milestones, and issues related to the different stages of a major incident record.
locale: en-US
release: yokohama
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Setting up communication templates and plans in Major Incident Management, Configuring Major Incident Management in Service Operations Workspace, Setting up Major Incident Management in Service Operations Workspace, Getting started with Service Operations Workspace for ITSM, Configure, Service Operations Workspace for ITSM, IT Service Management]
---

# Configure a communication plan in Major Incident Management

Configure a communication plan and tasks for effective communication with various stakeholders about the progress, milestones, and issues related to the different stages of a major incident record.

## Before you begin

The Major Incident Management plugin must be activated in Service Operations Workspace. For more information, see [Activate Major Incident Management in Service Operations Workspace](install-mim-sow.md).

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Service Operations Workspace** &gt; **Configurations**.

2.  On the Admin Center page, navigate to the configuration page for Major Incident Management through either the **Overview** tab or the **Configurations** tab.

    -   In the **Overview** tab, select **Configure** for Major Incident Management.
    -   In the **Configurations** tab, select **Major Incident Management**.
    The configuration page displays all configurable features in Major Incident Management. In the Communication Plan subsection of the Communications section, you can view the number of configured communication plans and active communication plans.

3.  In the Communication Plan section, select **Configure**.

    The Communications plan page displays a list of available communications plan definitions. You can select any available communications plan and then select any of the following actions:

    -   **Activate**: Activates the selected communications plans.
    -   **Delete**: Deletes the selected communications plan.
    -   **Deactivate**: Deactivates the selected active communications plan.
    -   **Copy**: Copies the communications plans along with the task information. This option helps when creating a communications plan using the data of an existing communication plan.
    In case if no communication plans exist, the **Create a communication plan** option is displayed.

4.  Select **New** to create a communication plan definition.

    For more information on creating a communication plan, see [Define a communication plan](https://www.servicenow.com/docs/access?context=create-comm-plan-definition&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

    After a communication plan definition is created, the following related lists appear in the communication plan definition record:

    -   Communication Task Definitions
    -   Communication Contact Definitions
5.  Select the Communication Task Definitions related list and then select **New** to create a communication task.

    For more information on creating a communication task, see [Define a communication task](https://www.servicenow.com/docs/access?context=create-comm-task-definition&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

6.  On the Communication task definition record, select the required communication channel related link to define the communication channel.

    The communication channel related list contains the communication channel related links such as Add channel - Email, Add channel - Sidebar discussion and Add channel - DEX Desktop Assistant. For more information on creating a communication channel, see [Define a communication channel](https://www.servicenow.com/docs/access?context=create-comm-channel-definition&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

7.  On the Communication plan definition record, select the Communication contact definition related list.

8.  Select **New** to create a communication contact definition.

    For more information on creating a communication contact definition, see [Define a communication contact](https://www.servicenow.com/docs/access?context=create-comm-contact-definition&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).


