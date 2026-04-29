---
title: Runtime Phase of the Embedded Task Automation \(ETA\)
description: Learn more about the triggering of an attended automation from a ServiceNow form.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Embedded Task Automation \(ETA\), Use, RPA Hub, Workflow Data Fabric]
---

# Runtime Phase of the Embedded Task Automation \(ETA\)

Learn more about the triggering of an attended automation from a ServiceNow form.

## Workflow of the Runtime Phase of an Embedded Task Automation

Familiarize yourself with Embedded Task Automation concepts. For more information, see [Embedded Task Automation \(ETA\) in RPA Hub](embedded-task-auto-rpa.md).

A user with RPA Assisted User role logs into the ServiceNow instance.

Navigates to the corresponding ServiceNow form from where the automation must be triggered.

The user selects the form action, that is created when you activate the attended configuration.

-   If any changes are made on the ServiceNow form, a confirmation message is displayed to save before triggering the UI Action. If the user selects **Proceed** or **OK**, the form is saved. The automation is triggered. If the user selects **Cancel**, the automation is not triggered and the ServiceNow form is not saved.
-   When the user selects the UI action, if it is successful, an attempt is made to start attended automation. Make sure that the Attended Robot is installed on the machine. If it is not successful, a connection to initiate the Attended Robot is not established. An information message is displayed to try again or contact system administrator.

A URL is generated that initiates the Attended Robot with details such as OAuth Entity ID, code challenge, ServiceNow form record SysID \(from where the automation is triggered\), Bot Process Sys ID, and Package SysID \(Automation SysID\).

Using these details, the Attended Robot makes a call to the OAuth to get the access and refresh token. Learn about the authentication journey in the Attended Robot application and the automation execution. For more information, see [Attended Robot authentication journey and automation execution in Embedded Task Automation](../../rda-runtime/concept/attended-auth-journey-rpa.md).

With these token details, the Attended Robot shares the session details with the ServiceNow form and starts executing the automation.

The **GetProcessFieldParameters** component makes a GraphQL API to the ServiceNow instance to read the form field values that are mapped to the dynamic process field parameters. For more information about the **GetProcessFieldParameters** component, see [Use the GetProcessFieldParameters component](../../rpa-studio/task/use-get-process-field-param-forms.md).

After the automation is executed, the data is passed to the downstream applications.

The **SetProcessFieldParameters** component makes a GraphQL API to the ServiceNow instance to set the form field values that are mapped to the dynamic process field parameters. For more information about the **SetProcessFieldParameters** component, see [Use the SetProcessFieldParameters component](../../rpa-studio/task/use-set-process-field-param-forms.md).

![Workflow of the Runtime Phase of an Embedded Task Automation.](../image/runtime-eta-rpa-trigger.png "Workflow of the Runtime Phase of an Embedded Task Automation")

## Launch attended automations from ServiceNow forms

Learn about the restrictions to launch an attended automation from ServiceNow forms and launching the attended automations. For more information, see [Attended Robot authentication journey and automation execution in Embedded Task Automation](../../rda-runtime/concept/attended-auth-journey-rpa.md).

**Parent Topic:**[Embedded Task Automation \(ETA\) in RPA Hub](embedded-task-auto-rpa.md)

**Related topics**  


[List of steps for configuring embedded task automation](../reference/list-steps-eta-rpa.md)

