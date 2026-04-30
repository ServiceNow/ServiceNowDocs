---
title: Embedded Task Automation \(ETA\) in RPA Hub
description: With the embedded task automation feature, trigger attended bot processes \(attended automations\) from the ServiceNow forms, apart from initiating them from the Attended Robot application.
locale: en-US
release: zurich
product: RPA Hub
classification: rpa-hub
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 10
breadcrumb: [Explore, RPA Hub, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# Embedded Task Automation \(ETA\) in RPA Hub

With the embedded task automation feature, trigger attended bot processes \(attended automations\) from the ServiceNow forms, apart from initiating them from the Attended Robot application.

**Important:** The embedded task automation runs only for published attended bot processes.

## Invoke Embedded Task Automation via API

To trigger a bot process \(automation\) from a Workspace, a playbook, or any other service portal, you can create corresponding actions and call the RPAInstanceFormHooks Application Programming Interface \(API\). For more information about invoking an embedded task automation via an API, see [Invoke Embedded Task Automation via API in RPA Hub](create-button-att-config-rpa.md).

## Embedded Task Automation overview

Use the embedded task automation feature to initiate an automation seamlessly from ServiceNow screens in an attended mode. It provides users with a transparent view of the robot executing tasks directly on their machines. This feature provides a user-friendly experience by enabling individuals to observe and monitor the automation process in real-time.

## Why Embedded Task Automation

Since existing attended automations interact with forms that are built within the automation itself, form development is required. Use the Embedded Task Automation feature for attended automations that use the ServiceNow screens. The Embedded Task Automation feature enables the reuse of the existing ServiceNow screen without a need to develop forms with in automation.

## How Embedded Task Automation works

Let's consider an employee badge creation use case.

1.  In the Service Catalog, a request is created for an employee badge generation. Details such as **Requested for** and **Location** are included in this request form, for printing the badge on a third party application. After the badge is generated in the application, the badge ID is populated in the request form.
2.  In RPA Desktop Design Studio, build an automation using the new components and publish it to the ServiceNow instance. For more information about the new components, see [Forms](../../rpa-studio/concept/forms_sn_rpa_studio.md). Ensure to use the Terminate component for each UI action automation logic that helps in completing the automation execution for the respective UI action. For more information about the component, [Use the Terminate component](../../rpa-studio/task/use-general-terminate.md).
3.  In the RPA Hub, create an attended bot process \(for example, Employee Badge Generation\). For more information about creating an attended bot process, see [Configuring a bot process record in RPA Hub](create-botprocess.md).
4.  To trigger this bot process \(automation\) from the ServiceNow form, select the **Enable Embedded Task Automation** check box in the associated attended bot process form. On enabling this check box, two additional tabs, Process Field Parameters and Attended Configuration, are available on the bot process form. For more information about the bot process form, see [Bot Process form in RPA Hub](../reference/bot-process-form.md).
5.  On the Process Field Parameters tab, create dynamic parameters that are used in the automation. Process field parameters are used for setting the value or getting the value of a field on a particular form. Examples of process field parameters are the user's title, first name, last name, and location. These details are used in the automation workflow while generating a badge. For more information about creating process field parameters, see [Create a process field parameter in RPA Hub](../task/create-process-field-param-rpa.md).
6.  In the RPA Hub, create an attended configuration record. For more information about creating an attended configuration record, see [Create an attended configuration record in RPA Hub](../task/create-attended-config-rpa.md).
7.  In this attended configuration record, select the table associated with the required form from the **Table** field, from where this bot process must be triggered. Then, define the criteria in the **Conditions** field, to trigger the bot process. In this example, set the conditions for approved requests that are required for badge generation. For more information about the Attended Configuration form, see [Attended Configuration form in RPA Hub](../reference/attended-config-form-rpa.md).
8.  On the Field Parameter Mappings tab, map the form fields to the process field parameters that are used in the automations. This process enables an easy data flow during the execution of a bot process. For example, if "Full name" is the process field parameter used in the automation, then map it to the form's 'Name' field. For more information about mapping field parameters, see [Map a table field to a bot process field parameter in RPA Hub](../task/create-field-param-mapping-rpa.md).
9.  On the Attended Configuration tab, the form is activated by selecting the **Activate** button. In the background, a UI action \(button\) is created on the corresponding request form. For more information about activating an attended configuration, see [Activate an attended configuration record in RPA Hub](../task/activate-attend-config-rpa.md).
10. Publish the bot process with the corresponding package published from the RPA Desktop Design Studio. For more information, see [Publish a bot process in RPA Hub](../task/publish-bot-process.md).

    To publish the bot process, assign the user with RPA AU \(RPA assisted user\) in the **Assigned User** or **Assigned Group** field in the Attended Users/Groups tab of the attended bot process record. If the auto assignment system property **sn\_rpa\_fdn.allow\_rda\_robot\_auto\_assignment** is false, the attended robot record is available for the assigned RPA Assisted User. If the auto assignment system property is true, an attended robot license is available to auto create an attended robot at the time of triggering. For more information about this system property, see [Configure RPA Hub properties](../reference/rpahub-sys-properties.md).

11. Then, the assigned user can view the UI action \(button\) \(for example, Generate Badge\) on the corresponding ServiceNow form. Using this button, the user can trigger the attended bot process \(attended automation\). There are certain conditions to view this button \(UI action\). For more information, see [Conditions for the visibility of UI action \(button\)](../reference/visibility-cond-button-rpa.md).

![Configuration of Embedded Task Automation in RPA Hub.](../image/embedded-task-auto-config-rpa.png "Configuration of Embedded Task Automation in RPA Hub")

## Configuring Embedded Task Automation

To configure the embedded task automation, see [List of steps for configuring embedded task automation](../reference/list-steps-eta-rpa.md).

## New components for Embedded Task Automation in RPA Desktop Design Studio

The following four new components are added to the new **Forms** section in RPA Desktop Design Studio. These components are available under the new ServiceNow category in the Toolbox pane.

-   **AttendedConfigurations**: Segregate the execution of the automations in a single automation project and call the respective logic according to the action invoked. For more information, see [Use the AttendedConfigurations component](../../rpa-studio/task/use-attended-configurations-forms.md).
-   **GetProcessFieldParameters**: Fetch the values of the ServiceNow form fields associated in the Field Parameter Mapping of the corresponding attended configuration record in RPA Hub. For more information, see [Use the GetProcessFieldParameters component](../../rpa-studio/task/use-get-process-field-param-forms.md).
-   **GetRecordContextID**: Fetch the current record sys\_id of the ServiceNow form, from where the automation is triggered. For more information, see [Use the GetRecordContextID component](../../rpa-studio/task/use-get-record-context-id-forms.md).
-   **SetProcessFieldParameters**: Update the values of the ServiceNow form fields associated in the Field Parameter Mapping of the corresponding attended configuration record in RPA Hub. For more information, see [Use the SetProcessFieldParameters component](../../rpa-studio/task/use-set-process-field-param-forms.md).

## Terminate component in attended automations

Use the **Terminate** component in attended automations to complete the automation execution. For more information about the component, [Use the Terminate component](../../rpa-studio/task/use-general-terminate.md).

## Launch attended automations from ServiceNow forms

Learn about the restrictions to launch an attended automation from the ServiceNow forms and launching the attended automations. For more information, see [Attended Robot authentication journey and automation execution in Embedded Task Automation](../../rda-runtime/concept/attended-auth-journey-rpa.md).

## Attended Robot authentication journey and automation execution

Learn about the authentication process in the Attended Robot application and the automation execution. For more information, see [Attended Robot authentication journey and automation execution in Embedded Task Automation](../../rda-runtime/concept/attended-auth-journey-rpa.md).

**Important:**

If a new version exists to the existing automation, to reflect those changes the Attended Robot application must be closed. Until then, it continues to use the existing version, as the Attended Robot application is already launched and running.

If a new version of RPA Hub is installed on the instance, to reflect those changes the Attended Robot application must be closed. Until then, it continues to use the existing set of plugins, as the Attended Robot application is already launched and running.

## Runtime Phase of the Embedded Task Automation

Learn more about the triggering of an attended automation from a ServiceNow form. For more information, see [Runtime Phase of the Embedded Task Automation \(ETA\)](runtime-trigger-automation-forms.md).

**Related topics**  


[Deactivate an attended configuration record in RPA Hub](../task/deactivate-attend-config-rpa.md)

[Delete an attended configuration record in RPA Hub](../task/delete-attended-config-rpa.md)

[Edit an attended configuration record in RPA Hub](../task/edit-attended-config-rpa.md)

