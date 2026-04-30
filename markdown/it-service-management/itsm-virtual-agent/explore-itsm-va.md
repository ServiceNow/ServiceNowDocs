---
title: Exploring ITSM Virtual Agent
description: The ServiceNow ITSM Virtual Agent provides assistance through conversations within an intelligent messaging interface.
locale: en-US
release: yokohama
product: ITSM Virtual Agent
classification: itsm-virtual-agent
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [ITSM Virtual Agent, IT Service Management]
---

# Exploring ITSM Virtual Agent

The ServiceNow ITSM Virtual Agent provides assistance through conversations within an intelligent messaging interface.

## ITSM Virtual Agent overview

Empower your IT technicians to concentrate on more challenging, demanding user requests and incidents by deflecting the most common, simpler incidents to a virtual agent. ITSM Virtual Agent enhances both the IT technician experience and the employee experience by addressing IT-related queries immediately.

## Virtual Agent benefits

<table id="table_q3d_bf3_fwb"><tbody><tr><td>

![](../image/icon-user-satisfaction-va.png)User Satisfaction

</td><td>

-   **User satisfaction**

Provide better self-service by helping users and customers get what they need quickly with always-on, omni-channel experiences. Enable your users to get immediate help, day or night. Boost user and customer satisfaction by offering a personalized Virtual Agent experience, whereby user information is remembered and applied during the conversation.


</td></tr><tr><td>

![](../image/icon-productivity-va.png)

</td><td>

-   **Increased productivity**

Deliver great experiences for your users, as well as your agents and technicians, by deflecting tickets and reducing call volumes. Drive productivity by providing a virtual agent on familiar channels, such as Slack, Microsoft Teams, Facebook Messenger, and Workplace.


</td></tr><tr><td>

![](../image/icon-automation-support-va.png)

</td><td>

-   **Automation support**

Scale your support organizations and free your agents and technicians to focus on more complex user issues by automating common support tasks.


</td></tr><tr><td>

![](../image/icon-empowered-srvc-owner-va.png)

</td><td>

-   **Empowered service owners**

Enable service owners to deliver and refine AI capabilities quickly without data science expertise.


</td></tr></tbody>
</table>## Components

-   **Natural Language Understanding**

    You can use Natural Language Understanding \(NLU\) for all your ITSM Virtual Agent topic conversation flows. ITSM Virtual Agent uses NLU to comprehend word meanings, recognize word contexts, and infer user or system actions.

    You can decide whether you want ITSM Virtual Agent to use only keywords, which result in quicker time-to-value in the short term. Or you can choose to use NLU, which results in a better employee experience in the long term.

    ITSM Virtual Agent and the ITSM NLU Model for Virtual Agent Conversations are available from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

    The ITSM NLU Model for Virtual Agent Conversations provides pre-built NLU entities, intents, and utterances. Some of the provided intents and utterances include:

    -   Escalate Ticket topic:
        -   Raise incident INC0010023 ticket priority to higher level
        -   Raise the priority on my open ticket
    -   Check Outages and Service Degradations topics:
        -   Are there currently any reported company-wide issues?
        -   Is there an outage?
    -   Email Setup topic
        -   I want to set up email on my mobile device
        -   How do I set up company email on my phone?
    Enable NLU on the ITSM Virtual Agent application and republish your existing conversations to optimize user experience with the NLU feature.

-   **ITSM Virtual Agent automatic notifications**

    Virtual Agent proactively informs you about the status of your incidents and requests. Managers are alerted when they have approvals.

    -   **ITSM Virtual Agent notification defined on the Task \[task\] table**

        These notifications are used by fulfillers and employees. The **Task type** filter on the Task table enables automatic status notification when the value is **Incident** or **Requested item**. When the state of the incident or requested item task changes, a Virtual Agent message is sent to the user.

    -   **ITSM Virtual Agent notification defined on the Approval \[sysapproval\_approver\] table**

        These notifications are used by request management or knowledge management. When an approval is submitted, an automatic Virtual Agent message is sent to the approver alerting them of the approval request.


**Parent Topic:**[ITSM Virtual Agent](itsm-virtual-agent.md)

