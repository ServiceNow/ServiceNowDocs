---
title: Attended Robot authentication journey and automation execution in Embedded Task Automation
description: Learn about the authentication process in the Attended Robot application and the automation execution, when the automation is triggered from ServiceNow forms.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Explore, Attended Robot, Workflow Data Fabric]
---

# Attended Robot authentication journey and automation execution in Embedded Task Automation

Learn about the authentication process in the Attended Robot application and the automation execution, when the automation is triggered from ServiceNow® forms.

## Embedded Task Automation feature

With the embedded task automation feature, you can trigger attended bot processes \(attended automations\) from the ServiceNow forms, apart from initiating them from the Attended Robot application. For more information, see [Embedded Task Automation \(ETA\) in RPA Hub](../../rpa-hub/concept/embedded-task-auto-rpa.md).

## Attended Robot authentication journey in Embedded Task Automation

After you install the Attended Robot application in a Windows machine, it registers a URL schema 'snrdaforms' with Attended Robot, starting from the Washington DC release. This URL schema is used whenever a redirect occurs from OAuth. For more information about OAuth, see [OAuth Inbound and Outbound authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/authentication/api-inbound-and-outbound.md).

RPA assisted user selects the form action and this action redirects the user to the OAuth authentication.

After successful authentication, it generates the Callback URL that includes the information required for the bot process to launch. For example, for a bot process that is associated with an attended configuration, this information is passed to the Callback URL.

The Callback URL initiates the Attended Robot. The Attended Robot receives all the information sent by the Callback URL. In the Connection Manager, a profile \(instance details like host name, instance URL\) is created locally, if it doesn't exist. It’s required for synchronizing the plugins and it establishes the user context for further authentication purposes.

There are three scenarios for the user context.

-   If the Attended Robot application is already launched with embedded task automation and the same user, for example, User A, is used to retrigger the automation. Then, the next automation runs without restarting the Attended Robot application. The Attended Robot application doesn’t close.
-   If the Attended Robot application is already launched with embedded task automation by User A. Then, the different user, User B, and same instance are used to retrigger the automation. Then, it continues to use the Attended Robot application, logs out User A and reconnects with the User B, without closing and relaunching the Attended Robot application.
-   If the Attended Robot application is already launched with embedded task automation from Instance1 and user tries to launch embedded task automation from Instance2. Then, the Attended Robot application is relaunched.

If a default profile saved in the Connection Manager window of Attended Robot application, the robot still uses the URL profile from where the automation is triggered.

If a new version exists to the existing automation, to reflect those changes the Attended Robot application must be closed. Until then, it continues to use the existing version, as the Attended Robot application is already launched.

If a new version of RPA Hub is installed on the instance, to reflect those changes the Attended Robot application must be closed. Until then, it continues to use the existing set of plugins, as the Attended Robot application has already launched.

Attended Robot is then ready to launch automations and doesn’t prompt with the Connection Manager of Attended Robot when automation invoked from the ServiceNow® form.

If the RPA assisted user directly launches Attended Robot, the Connection Manager is displayed to verify instance and login details.

In the Connection Manager, when the user tries to connect to an instance for the first time, then an alert is displayed, that the user hasn’t used that instance before.

![Attended Robot authentication journey.](../image/auth-journey-attended-auto.png "Attended Robot authentication journey")

## Automation execution in a local session and a bot session

After the authentication, the process configuration is retrieved from RPA Hub.

If the **Enable Desktop In Desktop** check box isn’t selected on the bot process form, the automation execution starts in a local session. After the execution is complete, the Attended Robot application remains active on the machine and waits for the upcoming automation triggers. For more information, see the **Launch an attended automation from ServiceNow forms** section in the following sections. For more information about the **Enable Desktop In Desktop** and **End Desktop In Desktop On Complete** check boxes, see [Bot Process form in RPA Hub](../../rpa-hub/task/select-botprocess.md#).

If the **Enable Desktop in Desktop** check box is selected on the bot process form, the automation execution starts in a bot session. After the execution is complete, depending on the **End Desktop In Desktop On Complete** setting, either of the following occurs:

-   If the **End Desktop In Desktop On Complete** check box is selected, the Attended Robot application closes the bot session, and the Attended Robot application remains with all the UI buttons disabled.

    The Attended Robot application won't be closed after the execution is complete or when user selects the **Stop** button, or any error occurs during automation initiation.

    After the execution is completed, the robot moves from **Busy** to **Available** state.

-   If the **End Desktop In Desktop On Complete** check box isn’t selected, the user must close the session. Until the user closes the session, the Attended Robot application runs and the associated robot state shows as **Busy**. After the user closes the bot session, the Attended Robot application remains open.

    If the Attended Robot login user session expires, the Attended Robot instance is closed along with the bot session.


![Automation execution in a local session and a bot session.](../image/automation-execution-local-bot.png "Automation execution in a local session and a bot session")

## Launch an attended automation from ServiceNow forms

Attended Robot executes attended automation when triggered from ServiceNow forms. For more information, see [Runtime Phase of the Embedded Task Automation \(ETA\)](../../rpa-hub/concept/runtime-trigger-automation-forms.md). For more information about invoking an attended automation across other types of forms, see [Invoke Embedded Task Automation via API in RPA Hub](../../rpa-hub/concept/create-button-att-config-rpa.md).

If your organization is configured with proxy settings, the prerequisite for this task is to configure the proxy. In the Proxy Settings section of the Connection Manager, configure the proxy, when you launch Attended Robot from ServiceNow forms, for the first time. For more information about connection manager, see [Connect to an RPA Hub instance from Attended Robot](../task/connect-rda-instance-rpa.md). For more information about setting a proxy, see [Set up Attended Robot](../task/set-up-rda-runtime.md).

On successful authentication, the following scenarios occur:

1.  Moves the associated robot state to **Available**, if it is not in Available state already.
2.  Creates a **Running** state process job record.

    In the process job record, the **Triggered By** field is updated by **Embedded Task Automation** value.

3.  Moves the associated robot state to **Busy**, starts synchronizing, and downloads the package, if not available locally.
4.  Initiates the automation in a local session or bot session, based on the option selected in the **Enable Desktop in Desktop** check box.
5.  After the automation execution is complete, the robot status is then updated as **Available**.
6.  After the automation execution is initiated, if the user selects the **Stop** button on the Attended Robot, it terminates the automation, and the robot state is set to **Available**. The process job record is marked as **Canceled** state.
7.  After the automation execution is initiated, if the user selects the **Close** button on the Attended Robot, after performing few pre-validations, it halts the bot process, logs out the user session, and closes the Attended Robot. For more information about stop and close actions, see [Run an automation using Attended Robot](../task/run-rda-robot.md).

    ![Stop and Close actions in the Attended Robot.](../image/attended-robot-actions.png "Stop and Close actions in the Attended Robot")

8.  After the automation is executed, the process job record is marked as success or failure after the automation flow ends.

    ![Post automation execution screen in the Attended Robot.](../image/attend-robot-actions-greyed.png "Post automation execution screen in Attended Robot")

9.  Shuts down the Attended Robot, if the session is timed out.

If the authentication fails, an error is displayed: `Unable to execute the automation as authentication has failed. Contact your system administrator`.

Use the **Terminate** component in attended automations to complete the automation execution. For more information about the component, [Use the Terminate component](../../rpa-studio/task/use-general-terminate.md).

To view detailed product logs, refer to the product logs.

## Restrictions to launch an attended automation from ServiceNow forms

In the following scenarios, the execution of attended automations via ServiceNow forms are restricted when you select the UI action from the ServiceNow form:

-   When an automation is executing
-   When an active child session \(Desktop In Desktop\) exists.
-   If the automation is triggered by the same user and same bot process, local cache is used. If a change is made, close the Attended Robot application and relaunch it, so that the new change is reflected.

