---
title: Configuring RPA Desktop Design Studio
description: You can plan and configure an RPA Desktop Design Studio implementation in your organization.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [RPA Desktop Design Studio, Workflow Data Fabric]
---

# Configuring RPA Desktop Design Studio

You can plan and configure an RPA Desktop Design Studio implementation in your organization.

The ServiceNow® RPA Desktop Design Studio is a Windows native application that is used by RPA developers to design or configure automation workflows.

## Important information

Refer to the [List of components compatible with latest version](../reference/list-components-upgrade.md) topic, for a list of components that are executed in their latest versions in the RPA Desktop Design Studio and robots, irrespective of the version they were used during the automation design.

## Configuration overview

Perform the following tasks to download the installation package and configure the RPA Desktop Design Studio after installation.

1.  [Install RPA Desktop Design Studio](../task/install-rpa-studio.md)

    You can install the RPA Desktop Design Studio application in your Windows machine if you have the admin role.

2.  [Set up RPA Desktop Design Studio](../task/set-up-rpa-studio.md)

    Set up RPA Desktop Design Studio to add your ServiceNow® RPA Hub instance details in Connection Manager and to start using the application.

3.  [Connect to an RPA Hub instance from RPA Desktop Design Studio](../task/connect-studio-instance-rpa.md)

    Establish a connection between the RPA Desktop Design Studio and ServiceNow® RPA Hub instance to connect to an RPA Hub instance in three ways using Connection Manager.

4.  For the upgrade scenario, if your instance is installed with a hot fix and later upgraded to a newer release, verify to install the required hotfix for the respective plugins on the new plugin bundle. The system overrides it by default. Failing to do so, the hotfix will not be applied and you might encounter the same issue again. For more information, see [Post requisites after installing a hot fix](../task/post-req-hot-fix-rpa.md).

## Using Guided Setup to implement RPA Desktop Design Studio

Guided Setup provides a sequence of tasks that help you configure RPA Desktop Design Studio. With Guided Setup, keep track of what you have completed, so you can stop and start again where you left off. To open Guided Setup for RPA Hub, navigate to **All** &gt; **Robotic Process Automation** &gt; **Administration** &gt; **Guided Setup**.

For more information about using the guided setup interface, see [Using guided setup](https://www.servicenow.com/docs/access?context=guided-setup&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US).

