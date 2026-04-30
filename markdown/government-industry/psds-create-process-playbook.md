---
title: Configure a custom playbook in Service Request Playbook
description: Custom playbooks and service definitions enable you to customize the default Service Request Playbook user experience to interact with your desired agency workflows. After creating a service definition, you can associate a playbook with the definition.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Service Request Playbook, Playbooks, Configure Agent Workspaces, Configuring Public Sector Digital Services, Public Sector Digital Services \(PSDS\)]
---

# Configure a custom playbook in Service Request Playbook

Custom playbooks and service definitions enable you to customize the default Service Request Playbook user experience to interact with your desired agency workflows. After creating a service definition, you can associate a playbook with the definition.

## Before you begin

Role required: admin

## About this task

Before starting this procedure, you must create a service definition to associate your playbook with. For more information on how to create a service definition, see [Configure a service definition for Playbooks in Public Sector Digital Services](psds-create-new-service-definition.md).

When the agent selects **Create Case** on the case type selector screen, the system displays the new case record and launches the playbook associated with the service in a tab on the record page.

**Note:** This is an optional task.

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  Select **Create a New Process**, fill in the details of the playbook, and select **Select a trigger**.

3.  Select a trigger type from the dropdown menu.

    Your trigger type is the service definition you recently created.

4.  Select **Go to Designer**.

    Workflow Studio is now opened.

5.  Select **Activate** after creating the process to your specifications.

    The playbook is now published to run when triggered.

6.  Navigate to **All** &gt; **System UI** &gt; **UI Policies**.

    You are taken to edit the UI of the Playbook Record Generator, which is the initial form an agent sees when they are creating a case.

7.  Select **New**.

8.  Select **Service Request** in the **Table** dropdown menu, and enter a short description describing your new UI policy.

9.  Add the necessary conditions under the **When to Apply** and **Script**tabs,and select **Submit**.

    Your UI policy and playbook are now created.


