---
title: Using ITSM Virtual Agent pre-built topics
description: ITSM Virtual Agent includes several pre-built topic conversations designed to help your users complete common IT-related tasks, such as resetting a password and creating an incident.
locale: en-US
release: yokohama
product: ITSM Virtual Agent
classification: itsm-virtual-agent
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [ITSM Virtual Agent, IT Service Management]
---

# Using ITSM Virtual Agent pre-built topics

ITSM Virtual Agent includes several pre-built topic conversations designed to help your users complete common IT-related tasks, such as resetting a password and creating an incident.

Once installed, ITSM Virtual Agent pre-built topics are read only and have **\(Template\)** after the name. To use them, duplicate the topic in the ITSM Virtual Agent conversation scope and rename it according to your company's naming conventions. Natural Language Understanding \(NLU\) models are used to identify and trigger the action that a user wants to perform.

The ITSM Virtual Agent pre-built topic conversations are organized in several topic categories. Use the following table to find the topics that fit your needs.

**Note:** Some pre-built topics require additional paid plugins.

<table id="table_ox5_nn4_tvb"><thead><tr><th>

I want to

</th><th>

Using this ITSM topic category

</th><th>

Available pre-built topics

</th></tr></thead><tbody><tr><td>

Resolve issues as an ITSM professional with the itil role

</td><td>

[ITSM Fulfiller](../reference/itsm-va-fulfiller-topics.md)

</td><td>

-   Create Change Request
-   Create Problem
-   Identify Available Change Windows
-   Identify Scheduled Changes
-   Resolve Incident
-   Update Assigned Task
-   Update Change Request

</td></tr><tr><td>

Automate common IT-related issues, such as email setup, VPN connectivity, and conference room problems

</td><td>

[ITSM IT Issues](../reference/itsm-va-it-issues-generic.md)

</td><td>

-   Collaboration Applications
-   Email Issues
-   Email Setup
-   Guest WiFi Access
-   Hardware Issues
-   Local Admin Access
-   Meeting Room Issues
-   Printer Issues
-   Repository Access
-   RSA Token
-   Troubleshoot Slow Computer
-   VPN Connectivity

</td></tr><tr><td>

Give users to access IT-related information, such as IT ticket management, verify assigned equipment, and service disruptions

</td><td>

[ITSM Self-Service](../reference/itsm-va-self-service-topics.md)

</td><td>

-   Book Conference Room EXO
-   Book Conference Room OnPrem
-   Check IT Ticket Status
-   Check Ticket and Support Status
-   Escalate IT Ticket
-   Get Password Reset Link
-   Get Zoom Meeting Recording
-   My Assigned Equipment
-   Open IT Ticket
-   Open IT Ticket 2.0
-   Process Approval
-   Report IT Issue
-   Service Disruptions
-   Set OOO reply Exchange Online
-   Set OOO reply Exchange Server
-   Submit a request
-   Walk-up Check-in
-   Windows 365 Cloud PC

</td></tr><tr><td>

Automate Citrix connections

</td><td>

[ITSM Self-Service \(with Citrix integration\)](../reference/manage-citrix-convo-flow.md)

</td><td>

-   Reset Citrix Sessions
-   Provision Citrix Desktop/Apps

</td></tr><tr><td>

Automate user password management

</td><td>

[Password Reset for Virtual Agent application](itsm-password-management.md)

</td><td>

-   Change Password
-   Reset Password
-   Unlock Account

</td></tr><tr><td>

Manage Microsoft Office 365 groups

</td><td>

[ITSM Self-Service \(with Microsoft Office 365 integration\)](../reference/manage-office-365-group-convo-flow-actions.md)

</td><td>

-   Add Owner to Office 365 Group
-   Add User to Office 365 Group
-   Create Office 365 Group
-   Get Office 365 Group Details
-   Remove Office 365 group Owner
-   Remove Office 365 group Users

</td></tr><tr><td>

Manage Microsoft Active Directory groups

</td><td>

[ITSM Self-Service \(with Microsoft Active Directory integration\)](../reference/manage-microsoft-active-directory-actions.md)

</td><td>

-   Add User to AD Group
-   Create AD Distribution Group
-   Remove User from AD Group
-   Show My AD Group Membership

</td></tr><tr><td>

Automate meeting invitations in Microsoft Exchange Online

</td><td>

[ITSM Self-Service \(with Microsoft Exchange Online integration\)](../reference/manage-meeting-convo-flow.md)

</td><td>

-   Manage Meetings EXO v1.0
-   Manage Meetings EXO

</td></tr><tr><td>

Automate meeting invitations in Microsoft Exchange Server

</td><td>

[ITSM Self-Service \(with Microsoft Exchange Server integration\)](../reference/exchange-server-convo-flow.md)

</td><td>

Manage Meetings EXS

</td></tr><tr><td>

Manage virtual machines

</td><td>

[Cloud VMs](../reference/manage-virtual-machine.md)

</td><td>

-   Describe Virtual Machine
-   Manage Virtual Machine
-   Provision Virtual Machine
-   Start Virtual Machine
-   Start Virtual Machine CAI
-   Stop Virtual Machine
-   Stop Virtual Machine CAI

</td></tr><tr><td>

Create a standard welcome greeting and a conversation closing, as well as user feedback and surveys

</td><td>

[Setup Topics](../reference/itsm-va-setup-topics.md)

</td><td>

Dynamic Greeting Topic

</td></tr></tbody>
</table>-   **[IT Issues pre-built topics for ITSM Virtual Agent](../reference/itsm-va-it-issues-generic.md)**  
IT Issues topic conversations are designed to automate common IT-related issues, such as email setup, VPN connectivity, and conference room problems.
-   **[Self-Service pre-built topics for ITSM Virtual Agent](../reference/itsm-va-self-service-topics.md)**  
Self-Service topic conversations are designed to give users to access IT-related information, such as open or check IT ticket status, verify assigned equipment, and Knowledge Base search.
-   **[Citrix session pre-built topics for ITSM Virtual Agent](../reference/manage-citrix-convo-flow.md)**  
Users can reset any Citrix desktop or application session using Virtual Agent conversation flows. Users can also provision a Citrix desktop or application.
-   **[Password management topics for ITSM Virtual Agent](itsm-password-management.md)**  
End users can perform password reset, password change, and account unlock actions using Virtual Agent conversations.
-   **[Microsoft Office 365 Group pre-built topics for ITSM Virtual Agent](../reference/manage-office-365-group-convo-flow-actions.md)**  
ITSM Virtual Agent helps you manage Microsoft Office 365 Groups using actions in conversation flows.
-   **[Microsoft Active Directory pre-built topics for ITSM Virtual Agent](../reference/manage-microsoft-active-directory-actions.md)**  
ITSM Virtual Agent helps you manage Microsoft Active Directory distribution lists using actions in conversation flows.
-   **[Microsoft Exchange Online meeting management pre-built topic for ITSM Virtual Agent](../reference/manage-meeting-convo-flow.md)**  
ITSM Virtual Agent helps you manage meetings in Microsoft Exchange Online. Using the Manage Meetings EXO topic, you can schedule, reschedule, and cancel a meeting.
-   **[Microsoft Exchange Server meeting management pre-built topics for ITSM Virtual Agent](../reference/exchange-server-convo-flow.md)**  
ITSM Virtual Agent helps you manage meetings in Microsoft Exchange Server. Using the Manage Meetings EXS topic, you can schedule, reschedule, and cancel a meeting.
-   **[Virtual machine pre-built topics for ITSM Virtual Agent](../reference/manage-virtual-machine.md)**  
ITSM Virtual Agent helps you manage a virtual machine \(VM\) using conversation flows. With this conversation flow, you can start, stop, terminate, describe, and provision a virtual machine.
-   **[Pre-built setup topics for Virtual Agent](../reference/itsm-va-setup-topics.md)**  
Use pre-built setup topics to create a standard welcome greeting and a conversation closing. In addition, setup topics can provide user feedback and surveys, as well as error handling.
-   **[Fulfiller pre-built topics for ITSM Virtual Agent](../reference/itsm-va-fulfiller-topics.md)**  
Fulfiller topic conversations are designed specifically for ITSM professionals with the itil role. These pre-built topics include resolving an incident, creating a problem, and updating data in the system.
-   **[Reusable ITSM Virtual Agent pre-built topic blocks](../reference/itsm-va-topic-blocks.md)**  
Reuse topic blocks to perform common functions in ITSM Virtual Agent conversations, such as creating an incident or performing a search.

**Parent Topic:**[ITSM Virtual Agent](itsm-virtual-agent.md)

