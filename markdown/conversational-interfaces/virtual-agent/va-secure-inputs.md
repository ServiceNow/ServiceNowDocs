---
title: Virtual Agent secure password inputs
description: The Include a password input toggle switch on the Action utility properties sheet lets you enter passwords securely for use in Virtual Agent conversations.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/conversational-interfaces/virtual-agent/va-secure-inputs.html
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [Virtual Agent, secure, password, inputs, Action utility, conversations]
breadcrumb: [Integrating Virtual Agent with Workflow Studio workflows, Exploring other Virtual Agent features, Build and deploy, Virtual Agent, Conversational Interfaces]
---

# Virtual Agent secure password inputs

The **Include a password input** toggle switch on the Action utility properties sheet lets you enter passwords securely for use in Virtual Agent conversations.

If the workflow discovers a password2 type as an input, the Action utility properties sheet displays the **Include a password input** toggle switch.

**Note:** In previous releases, inputs with a string data type would also display this toggle switch. Starting with the San Diego release, only password2 data types are supported. If you have existing actions that use password inputs, update them to use password2.

\[Omitted image "include-password-input-slider.png"\] Alt text: Include a password input toggle switch.

If you enable this toggle switch, you see messages about clients that are supported, along with fields that let you do the following:

-   Designate the field you want to make secure
-   Enter the text you want to use for the password-related prompt
-   Enter the text for a confirmation prompt
-   Enter the text to use for messages about channels that aren't secure

**Important:** To implement secure \(password2\) inputs in your Virtual Agent custom control, you must adhere to the scoped application requirements in Workflow Studio. For details, see [Workflow Studio scoped application requirements for secure inputs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/virtual-agent/va-fd-app-reqs-secure-inputs.md).

\[Omitted image "additional-password-prompts.png"\] Alt text: Action utility with Include a password input toggle activated, and password detail prompts exposed.

These password input type fields are dynamic in the sense that the fields you see map to the fields set for the action when it was created in Workflow Studio. Some of the password2 fields may also be read-only.

For password-related design considerations in Workflow Studio, see [Password \(2 Way Encrypted\) design considerations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/password-2-data.md) .

Note the following points about how password-related inputs are handled securely:

-   Only users can see the passwords. No one else can.
-   The passwords are held in memory on the server and are passed securely to the Workflow Studio Action or Subflow.
-   When users enter a password on a channel, users can toggle the Hide text icon \[Omitted image "hide-password-icon.png"\] Alt text: Hide text icon. to show or hide the password.
-   ServiceNow admins can mark a specific channel as secure. If topic authors attempt to include a channel that isn't marked as secure, a warning message appears.

    For more information about creating secure channels, see [Create a Virtual Agent conversational custom chat integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/virtual-agent/create-adapter-for-virtual-agent.md).

-   Passwords are masked \(not readable\) in queues, tables, and logs.

**Parent Topic:**[Integrating Virtual Agent with Workflow Studio workflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/virtual-agent/va-flow-designer-integration.md)

