---
title: Create an automation project manually
description: Create an attended or unattended automation project manually in RPA Desktop Design Studio that enables you to automate tasks. You can create an automation project that is based on a prebuilt template and targeted at a use case, or you can create an automation project without using a template.
locale: en-US
release: zurich
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Build, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# Create an automation project manually

Create an attended or unattended automation project manually in RPA Desktop Design Studio that enables you to automate tasks. You can create an automation project that is based on a prebuilt template and targeted at a use case, or you can create an automation project without using a template.

## Before you begin

Set up the RPA Desktop Design Studio application and add the ServiceNow instance details. For more information, see [Set up RPA Desktop Design Studio](set-up-rpa-studio.md).

Role required: none

## About this task

An unattended automation doesn’t require human supervision and can be used for highly repetitive tasks. For example, in a Customer Relationship Management \(CRM\) system, an unattended robot can perform the copy and paste tasks to a Microsoft Excel file without any human inputs.

An attended automation requires human supervision. For example, in a contact center, robots are used as user assistants. They’re installed on an operator’s workstation and are triggered by human operators on demand.

To create automation projects, you can use the default templates that RPA Desktop Design Studio provides or the custom automation templates that you have created and published to the RPA Hub. An automation template caters to a use case and provides a framework of automation. For example, automate a manual employee onboarding process. The default templates that the RPA Desktop Design Studio provides are `Unattended Non-Transactional Workflow`, `Unattended Transactional Workflow`, and `Attended Workflow`. You can also create automations with no template.

To create an automation project using Now Assist, see [Create an automation with Now Assist](create-automation-now-assist.md).

## Procedure

1.  On the RPA Desktop Design Studio home page, select **Create Automation**.

2.  In the Build an automation window, select **Build manually**.

    ![Select Build manually tile](../image/build-automation-manually-rpa.png "Build an automation manually")

3.  Select **Next**.

4.  In the Create new automation window, select either **Unattended Automation** or **Attended Automation**.

5.  In the **Name** field, enter the name of the unattended or attended automation project.

6.  In the **Description** field, enter the description of the unattended or attended automation project.

7.  In the **Location** field, enter the location of the automation project or retain the default location.

8.  Select **Next**.

9.  In the Do you want to select a template dialog box, you can perform either of the tasks.

    -   To create an automation without a template, select **Use a blank canvas**.
    -   To create an automation based on a template, select **Select a template** and choose from the default templates.

        **Note:**

        By default, the RPA Desktop Design Studio provides the latest versions of certain plugins with the automation project that you create. You can add more plugins after you create the project. In the Create new automation window, view the default plugins by selecting **View**.

        You can choose from the default templates that the RPA Desktop Design Studio provides or the custom templates that you have created and published to the RPA Hub. This template is built on the loaded plugin versions.

10. Select **Create**.


**Parent Topic:**[Building automations](../concept/rpa-studio-build.md)

**Related topics**  


[Create a skill project in RPA Desktop Design Studio](create-skill-project.md)

