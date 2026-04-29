---
title: Onboard a new tool using DevOps generic playbook
description: DevOps Change has a pre-build playbook setup for users to configure a new tool. Custom tool integrations can be created using the guided playbook experience in the DevOps Change Workspace.
locale: en-US
release: australia
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Manage, DevOps Change Velocity, IT Service Management]
---

# Onboard a new tool using DevOps generic playbook

DevOps Change has a pre-build playbook setup for users to configure a new tool. Custom tool integrations can be created using the guided playbook experience in the DevOps Change Workspace.

Playbooks provide end users with a visual, task-oriented guide with the steps to complete a process, ensuring a consistent experience for tool onboarding. For detailed information about playbooks, see [About Playbook Experience](https://www.servicenow.com/docs/access?context=playbook-ui&version=australia&pubname=australia-build-workflows&ft:locale=en-US).

Perform the following steps to onboard your custom tool using the DevOps generic playbook.

## 1. Identify tool capabilities

To configure a tool using the generic playbook, first you must identify the capabilities supported by the tool. A tool can have one or more capabilities like code, plan, and orchestration.

The Generic playbook consists of the following stages and each stage has its related activities:

1.  Connect to a tool
    1.  Connect to a tool
    2.  Specify tool access
    3.  Configure the tool
2.  Capability

    Capability can be of type plan, code, or orchestrate. If the tool has multiple capabilities, multiple stages exist with the capability name.

    1.  Select to track
    2.  Import data
    3.  Associate \(This activity is for the Orchestration tools to associate pipeline steps\)
3.  Summary

This is how a playbook with multiple capabilities looks like:![Playbook with multiple capabilities.](../image/generic-pb-onboard1.png)

## 2. Configure Activity Definitions

Each Activity in a playbook is associated to an activity definition. DevOps has the following activity definitions:

-   DevOps CreateTool AD
-   DevOps Configure &amp; Test AD
-   DevOps Select Associated Objects AD
-   DevOps Import Data AD
-   DevOps Associate Services AD
-   DevOps Summary AD

For more information, see [Exploring Playbook](https://www.servicenow.com/docs/access?context=process-automation-designer&version=australia&pubname=australia-build-workflows&ft:locale=en-US) and [About Playbook Experience](https://www.servicenow.com/docs/access?context=playbook-ui&version=australia&pubname=australia-build-workflows&ft:locale=en-US).

The DevOps table **sn\_devops\_capability\_activity\_mapping** has been created to maintain associations between Activity definitions and capabilities. This table configuration is used to dynamically render the stages and activities for a tool. You can update the conditions as needed to either enable or disable a particular activity for a tool.

![The Tool Capability Activity Mappings table.](../image/generic-pb-onboard2.png)

For example, tools like GitLab and JFrog don’t support data import. So you don't require the Data Import activity for such tools. In that case, you must add the logic in the condition column to return false for these types of tools. See the following image as a reference:![Example where data import logic is false.](../image/generic-pb-onboard3.png)

## 3. Configure Activity UI for the Activity Definition

Playbook Activity UIs define the experience type and UI template rendered to users while managing Playbooks. You can configure multiple Activity UIs for an Activity Definition and render any one dynamically based on the condition evaluation.

DevOps has the following AUIs for Create Tool activity. Except this, all other activity definitions have only one Activity UI.

![DevOps AUIs.](../image/generic-pb-onboard4.png)

You can configure any one of the Activity UI based on the requirement.

Identify the required activity UI and add your tool in the condition builder so that the UI gets effected in the playbook for the tool.![Override playbook activity.](../image/generic-pb-onboard5.png)

**Result**

After completing these steps, your tool can be onboarded using the DevOps generic playbook.

**Parent Topic:**[Managing DevOps Change Velocity](../concept/using-devops-change-velocity.md)

**Related topics**  


[Integrating DevOps Change Velocity with third party tools](../concept/integrating-devops-change-with-third-party-tools.md)

