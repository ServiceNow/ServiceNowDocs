---
title: Flows, subflows, and actions in Workflow Studio release notes
description: The ServiceNow Workflow Studio application enables process analysts to automate work without having to code and to build multi-step flows from reusable components. Workflow Studio was enhanced and updated in the Xanadu release.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 4
---

# Flows, subflows, and actions in Workflow Studio release notes

The ServiceNow® Workflow Studio application enables process analysts to automate work without having to code and to build multi-step flows from reusable components. Workflow Studio was enhanced and updated in the Xanadu release.

## Workflow Studio highlights for the Xanadu release

-   Protect sensitive data in execution details by using the operations read role.
-   Provide improved support of the variables data type for subflow and action inputs.
-   Show annotations of what text directions were used to generate actions, flow logic, and subflows during flow generation.
-   Sign and validate any flow, subflow, or action.

See [Workflow Studio](https://www.servicenow.com/docs/access?context=workflow-studio&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US) for more information.

**Important:** Workflow Studio is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Important information for upgrading Workflow Studio to Xanadu

After upgrading, users who previously had the fd\_read\_operations role will now see only basic execution details such as the run state and duration. This restriction prevents users with this role from seeing sensitive information in execution details. To provide read access to all execution details such as input configuration and runtime values, grant the user the new role fd\_read\_operations\_all.

## New in the Xanadu release

-   **[Generate data pill values during flow generation](https://www.servicenow.com/docs/access?context=flow-generation&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US)**

    Generate appropriate data pill values for supported flow triggers and action inputs.

-   **[Run an action from a conversation](https://www.servicenow.com/docs/access?context=conversational-actions&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US)**

    Run a Workflow Studio action from a Now Assist conversation. Create and configure the conversational action from Workflow Studio. View and edit conversational actions within Virtual Agent Designer.

-   **[Run a subflow from a conversation](https://www.servicenow.com/docs/access?context=conversational-subflows&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US)**

    Run a Workflow Studio subflow from a Now Assist conversation. Create and configure the conversational skill from Workflow Studio. View and edit conversational subflows within Virtual Agent Designer.

-   **[Reference specific tables with hash tags during flow generation](https://www.servicenow.com/docs/access?context=flow-generation&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US)**

    Enter a hash tag character in the flow directions to refer to a specific table by name. Use auto-complete to select a table name from the options that match your partial entry.


-   **[Show annotations of the text directions used by flow generation](https://www.servicenow.com/docs/access?context=create-flow-now-assist&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US)**

    Show annotations of the text directions used for each item added by flow generation. Receive feedback about how your directions map to specific actions, flow logic, and subflows.


-   **[Control what users with read access can see in execution details](https://www.servicenow.com/docs/access?context=user-access-flow-designer&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US)**

    Grant a user role to control what users with read access can see in execution details. To limit read access to basic execution details only, grant a user the existing fd\_read\_operations role. To allow read access to all execution details, grant a user the new fd\_read\_operations\_all role.

-   **[Sign flows, subflows, and actions](https://www.servicenow.com/docs/access?context=cs-fdih&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US)**

    Sign and validate any flow, subflow, or action.


## UI changes

-   **[User preferences for flows](https://www.servicenow.com/docs/access?context=flow-preferences&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US)**

    Flow preferences have been renamed User preferences.


## Changed in this release

-   **[Flow generation configures action and flow logic inputs](https://www.servicenow.com/docs/access?context=create-flow-now-assist&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US)**

    Use the Now Assist for Creator flow generation skill to create and configure a flow from text directions. Flow generation uses data pills to set input values for actions and flow logic.


## Removed in this release

-   Removed the system property com.snc.process\_flow.reporting.iteration.lastn that was used to specify the number of loop iterations that a flow would generate execution details for. To report on all iterations of a loop, create a flow execution settings record for the flow instead. For more information about flow execution settings, see [Flow execution settings](https://www.servicenow.com/docs/access?context=flow-execution-settings&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US).
-   The user preference for flow authors to include draft actions in the list of available actions has been removed. To see a custom action during flow design, publish the action. For more information, see [Create an action in Workflow Studio](https://www.servicenow.com/docs/access?context=create-action&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US).

## Activation information

Workflow Studio is a ServiceNow AI Platform feature that is active by default.

## Related ServiceNow applications and features

-   **[App Engine Studio](https://www.servicenow.com/docs/access?context=aes-overview&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US)**

    ServiceNow® App Engine Studio \(AES\) is a development tool for creators of varying skill levels to build applications that meet the immediate needs of your organization.

-   **[Integration Hub](https://www.servicenow.com/docs/access?context=integrationhub&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US)**

    Automate integration tasks using ServiceNow components for ServiceNow® Workflow Studio, or develop custom integrations. A separate subscription is required.

-   **[Integration Hub available spokes](https://www.servicenow.com/docs/access?context=spokes-list&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US)**

    Activate spokes to enhance your Workflow Studio experience with integration-specific content. Use prebuilt flows and actions to automate your integrations or create your own integration automation.

-   **[MID Server](https://www.servicenow.com/docs/access?context=mid-server-landing&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)**

    The Management, Instrumentation, and Discovery \(MID\) Server is a Java application that runs as a Windows service or UNIX daemon on a server in your local network. The ServiceNow® MID Server enables communication and the movement of data between a ServiceNow instance and external applications, data sources, and services.

-   **[Now Assist for Creator](https://www.servicenow.com/docs/access?context=now-assist-for-creator-landing&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US)**

    Use generative AI skills to make developing on the ServiceNow AI Platform more efficient.

-   **[Process Automation Designer](https://www.servicenow.com/docs/access?context=process-automation-designer&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US)**

    ServiceNow® Playbooks enables process owners to author cross-enterprise workflows and create a single, unified process. You can also use Playbooks to provide end users with a simplified, task-oriented view of your process.

-   **[Robotic Process Automation \(RPA\) Hub](https://www.servicenow.com/docs/access?context=rpa-main-landing-page&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US)**

    Use the ServiceNow® Robotic Process Automation \(RPA\) Hub to enable end-to-end automation for your organization. With a combination of UI interactions, element-based automations, and APIs that interact between the various business applications, you can emulate user actions and eliminate mundane and repetitive human activities.


**Parent Topic:**[Workflow Studio release notes](workflow-studio-rn.md)

