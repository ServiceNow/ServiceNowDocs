---
title: ITSM Virtual Agent
description: You can use ITSM Virtual Agent to support and scale your IT organization. With ITSM Virtual Agent, your technicians can address more challenging IT-related user requests and incidents.
locale: en-US
release: australia
product: ITSM Virtual Agent
classification: itsm-virtual-agent
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [IT Service Management]
---

# ITSM Virtual Agent

You can use ITSM Virtual Agent to support and scale your IT organization. With ITSM Virtual Agent, your technicians can address more challenging IT-related user requests and incidents.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## About ITSM Virtual Agent

ITSM Virtual Agent helps you automate employee workflows by addressing common IT-related queries immediately. At any time during a virtual conversation, a user can request to interact with a live IT technician.

ITSM Virtual Agent includes pre-built topic conversations that cover common IT interactions. These conversations run in the web chat client and are also available in supported ITSM Virtual Agent messaging integrations.

![Overview of ITSM Virtual Agent components.](../image/itsm-va-overview.png)

Conversations between Virtual Agent and the user accomplish an IT goal. The information exchanged during the conversation flow, such as user inputs and Virtual Agent responses, enables Virtual Agent to fulfill a request or help complete a task.

ITSM Virtual Agent integrates with ServiceNow® [Integration Hub](https://www.servicenow.com/docs/access?context=integrationhub&version=australia&pubname=australia-integrate-applications&ft:locale=en-US) and [Flow Designer](https://www.servicenow.com/docs/access?context=flow-designer&version=australia&pubname=australia-application-development&ft:locale=en-US). Some topics may require specific spokes to be installed.

For more information about Virtual Agent features, see [Virtual Agent](https://www.servicenow.com/docs/access?context=virtual-agent-landing-page&version=australia&pubname=australia-conversational-interfaces&ft:locale=en-US).

## Languages supported for NLU services on the ITSM Virtual Agent

In addition to English, ITSM Virtual Agent supports the following languages for NLU:

-   German
-   French
-   French \(Canadian\)
-   Korean
-   Spanish
-   Brazilian Portuguese
-   Japanese
-   Italian
-   Dutch
-   Chinese \(Simplified\)

For details about NLU, see [Natural Language Understanding in Virtual Agent](https://www.servicenow.com/docs/access?context=va-NLU&version=australia&pubname=australia-conversational-interfaces&ft:locale=en-US).

The ITSM Virtual Agent topics re-factored with gs.getMessageLang\(\) provide you the improved operations on the ITSM Virtual Agent by utilizing and displaying all the messages in the bot conversations in your preferred language. The gs.getMessageLang method checks the UI Message table \[sys\_ui\_message\] for the translated version of the text in the language provided using the *vaContext.getRequesterLang\(\)* variable.

## Edge Encryption for ITSM Virtual Agent

Edge encryption provides you with direct control over your data security. Encryption and key management are performed on your intranet between your browser and your ServiceNow® instance. For details about edge encryption, see [Edge Encryption for ITSM Virtual Agent within ITSM](../../it-service-management/reference/r_ITServiceManagement.md#section_ppf_jdm_ykb).

-   **[Exploring ITSM Virtual Agent](explore-itsm-va.md)**  
The ServiceNow ITSM Virtual Agent provides assistance through conversations within an intelligent messaging interface.
-   **[Setting up ITSM Virtual Agent](setting-up-itsm-va.md)**  
Set up the ITSM Virtual Agent features and components that you need to provide support to your employees, IT teams, and customers.
-   **[Using ITSM Virtual Agent pre-built topics](using-itsm-va.md)**  
ITSM Virtual Agent includes several pre-built topic conversations designed to help your users complete common IT-related tasks, such as resetting a password and creating an incident.
-   **[ITSM Virtual Agent pre-built actionable notifications](itsm-actionable-notifications.md)**  
Send interactive messages to an employee through Virtual Agent, based on pending tasks or alerts. Deflect some of the most common ITSM incidents to ITSM Virtual Agent, reduce incident volume to Service Desk, and help employees discover ITSM Virtual Agent as a resolution channel.

**Parent Topic:**[IT Service Management](../../it-service-management/reference/r_ITServiceManagement.md)

