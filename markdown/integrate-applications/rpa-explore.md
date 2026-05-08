---
title: Learn about RPA suite of applications
description: Learn about the Robotic Process Automation \(RPA\) Hub applications, types of automations, benefits, high-level architecture, and workflow.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 7
keywords: [RPA overview, RPA Hub overview, Robotic Process Automation overview, Robotic Process Automation Hub overview, Learn about Robotic Process Automation Hub, Learn about RPA Hub, Robotic Process Automation RPA automation types, Robotic Process Automation RPA benefits]
breadcrumb: [Explore, RPA Hub, Workflow Data Fabric]
---

# Learn about RPA suite of applications

Learn about the Robotic Process Automation \(RPA\) Hub applications, types of automations, benefits, high-level architecture, and workflow.

## Robotic Process Automation \(RPA\) Hub overview

The following Robotic Process Automation \(RPA\) applications operate and interact with each other in an enterprise environment to automate tasks efficiently.

-   **[RPA Hub](../../rpa-hub/concept/rpa-hub-landing-page.md)**

    The ServiceNow® RPA Hub application provides a centralized orchestration to deploy, monitor, manage, measure, and verify compliance of all robots at an enterprise level.

-   **[Unattended Robot](../../rpa-runtime/concept/rpa-runtime-landing-page.md)**

    The ServiceNow® Unattended Robot is a software agent that you install on a Windows machine. Unattended Robot can execute unattended automations without requiring any human intervention.

    The ServiceNow® Unattended Robot Login Agent is a software agent that you install on a Windows machine with Unattended Robot. You can use this application to unlock or to perform a self-login to the robot machine when an unattended bot process is triggered.

-   **[Attended Robot](../../rda-runtime/concept/rda-runtime-landing-page.md)**

    The ServiceNow® Attended Robot is a software agent that you install on a Windows machine. Attended Robot can execute attended automations that require human intervention.

-   **[RPA Desktop Design Studio](../../rpa-studio/concept/rpa-studio-landing-page.md)**

    The ServiceNow® RPA Desktop Design Studio is a Windows native application that is used by RPA developers to design or configure automation workflows.


## Types of automations

You can create two types of automations with RPA Desktop Design Studio and run them with Unattended Robot or Attended Robot:

-   **Unattended automation**

    In this automation, tasks, processes, or workflows are carried out by the robots without the need for direct human intervention or supervision. You can use this type of automation to automate highly repetitive tasks.

    For example, Report generation. In this use case, the reports are automatically generated and distributed to relevant stakeholders.

    Unattended automation offer significant efficiency gains, reduced operational costs, and improved accuracy in organizations.

-   **Attended automation**

    Also known as human-assisted automation. In this automation, the robots work alongside human users to augment their tasks and activities. You can use this type of automation with human supervision.

    For example, Customer service. In this use case, robots can assist customer service representatives by providing relevant information, suggesting responses, and automating data entry. The robots are installed on operator’s workstations and are triggered by human operators on demand.

    Attended automation is often suited for scenarios where a combination of automation and human judgment is required to handle complex, dynamic, or non-standard tasks.


## Robotic Process Automation \(RPA\) Hub users

|User|Description|
|----|-----------|
|Release manager|Creates bot processes and robots in RPA Hub. Add developers to the Managed by group of the bot process so that they can customize the bot process. Configures and publishes the bot process.|
|Developer|Configures bot processes to assign business applications, robots, credentials, process parameters, schedules, and so on. Builds automation packages, tests the automation projects, and handles exceptions in RPA Desktop Design Studio. Publishes packages to RPA Hub. Creates and deploys automations in a low-code environment.|
|Robot user/Assisted user|Executes automations in the specified robot machine.|

## Robotic Process Automation \(RPA\) Hub workflow

The three main parts of a process workflow are RPA Hub, RPA Desktop Design Studio, and robot machines \(virtual machine or user desktop\).

The following diagram shows the process workflow of the Robotic Process Automation \(RPA\) Hub applications.

![Basic tasks related to configuring automations in RPA Hub. Infographic showing how release managers create bot process and how developers configure, test, and publish bot processes.](../../rpa-hub/image/rpa-workflow-diagram.png "Workflow of creating and executing automations using Robotic Process Automation (RPA) Hub applications")

1.  As a release manager, create a bot process, define robots, and assign a developer who would continue to configure the bot process.
2.  As a developer, configure the bot process to associate a package, business applications, robots, parameters, and credentials so that robots can use them to run automations.
3.  As a developer, build automation packages, tests the automation projects, and handles exceptions in RPA Desktop Design Studio.
4.  As a developer, publish the configured bot process to execute, manage, and monitor automations.
5.  As a robot user or assisted user, execute automations in the specified Windows machine where Attended Robot or Unattended Robot is installed.

## RPA Hub Benefits

-   Increases productivity and delivers higher operational efficiencies.
-   Enhances accuracy by eliminating processing errors.
-   Enhances customer service and meets highly varied customer demands.

## Integration with Workflow Studio

Robotic Process Automation \(RPA\) Hub provides an integration with the Workflow Studio application. This integration enables you to integrate ServiceNow workflows with Robotic Process Automation by using ServiceNow components for Workflow Studio. For more information about RPA Hub actions and subflow, see [Workflow Studio actions and subflow in RPA Hub](../../rpa-hub/reference/rpa-hub-actions.md).

## Key Management Framework

RPA Hub uses the ServiceNow® Key Management Framework for all the sensitive data that is stored on the application. For more information, see Understanding the Key Management Framework.

## Important information for upgrading RPA Hub to Australia

Ensure that you upgrade the current installed Microsoft Software Installers \(MSIs\) \(RPA Desktop Design Studio, Attended Robot, Unattended Robot, and Unattended Robot Login Agent\), by downloading the RPA applications. For more information, see [Download the RPA applications from RPA Hub](../../rpa-hub/task/download-installer-rpa.md).

**Important:** The following upgrade steps are applicable only when you’re upgrading from San Diego or Tokyo to Australia.

Based on the number of records in the application file table, you could experience a potential delay while upgrading the RPA Hub applications from Tokyo or before to Australia.

Before upgrading RPA Hub to Australia, you must set the value of the **glide.rollback.blacklist.TableParentChange.change** system property to **false**. If this property doesn't exist in the System Property \[sys\_properties\] table, add the property and set its value to false.

After you upgrade to the Australia, the bot process definitions change to the new structure, that is, the bot process configuration. Although the bot process configuration doesn't replace the bot process completely. Most fields are moved from bot process to bot process configuration.

If you upgrade to the Utah version without updating the system property value, the tables don’t extend the Application File table. Manually to update the table changes, see the [Restructuring RPA Hub tables to sys\_metadata in Utah](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1223629) article in the Now Support Knowledge Base.

## What to explore next

To learn more about configuring Robotic Process Automation, see:

-   [RPA Hub](../../rpa-hub/concept/rpa-hub-landing-page.md)
-   [Unattended Robot](../../rpa-runtime/concept/rpa-runtime-landing-page.md)
-   [Unattended Login Agent](../../rpa-runtime/task/install-rpa-runtime-login-agent.md)
-   [Attended Robot](../../rda-runtime/concept/rda-runtime-landing-page.md)
-   [Now Assist for RPA Hub](../../rpa-studio/concept/rpa-now-assist-studio.md)
-   [RPA Desktop Design Studio](../../rpa-studio/concept/rpa-studio-landing-page.md)

