---
title: Task Mining data model
description: Task Mining collects and processes workstation data to provide insights into workstation user activities and interactions.
locale: en-US
release: australia
product: Task Mining
classification: task-mining
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Explore, Task Mining, Platform Analytics]
---

# Task Mining data model

Task Mining collects and processes workstation data to provide insights into workstation user activities and interactions.

## Task Mining components and data flow

![Infographic showing a high-level overview of the Task Mining data flow. For details, refer to the following description.](../image/task-mining-data-flow.png)

The Task Mining agent is a service installed on a user's workstation that collects data from workstation users on their workstation. This data is sent as a data file to the data processing server. After processing, the data is forwarded to the Task Mining application where it’s stored in user data tables. The data is then used in projects and presented to authorized users through dashboards for analysis.

## Workstation users

A workstation user is an employee whose daily workstation activities are monitored and logged by the Task Mining agent. Workstation users generally interact with the Task Mining system passively, as the agent operates in the background to collect data on their interactions with various applications and tasks. Workstation users have access to certain features provided by the agent, such as pausing data collection. Their primary role is a source of task-related data and they’re a data subject, meaning their personal data is processed under applicable data protection regulations.

Appropriate safeguards must be in place to protect their privacy and promote compliance, as described in the "Data privacy" section.

**Important:** Workstation users must log in to their workstation using the same login credentials as they’re registered in their organization's ServiceNow instance.

## Multi-user support

Task Mining agents support multiple users working on the same workstation.

-   The Windows agent supports multiple users accessing the same workstation one at a time. The Windows agent also supports multiple users working simultaneously on the same workstation through remote desktop protocol \(RDP\), virtual desktop infrastructure \(VDI\), and virtual apps.
-   The macOS agent supports multiple users accessing the same workstation one at a time.

## Data collected by the Task Mining agent

The Task Mining agent collects various types of data. Review this list for personally identifiable information \(PII\) in the collected data.

-   Workstation user identifiers associate collected data with a specific workstation user while preserving the user’s privacy.
-   Application name, window titles, and web app URLs provide context and dashboard data by identifying the applications and web pages that workstation users interact with. Although these activities are essential for providing insights, the PII contained in window titles and URLs isn’t needed for analysis. Manage this data carefully to avoid the unintentional exposure of sensitive information such as session tokens, user names, or email addresses.
-   The Task Mining agent tracks user interactions with specific UI elements such as input fields, drop-down lists, and buttons. UI object attributes can contain PII, especially when they’re related to other data subjects such as customer names or personal details entered into forms.

In addition to the data collected by the Task Mining agent, Task Mining uses audit trail data that is collected from the Sys Audit \[sys\_audit\] table. This audit trail is used to identify and track activities that were performed during task execution, such as incident processing. This data provides a fuller view of the task, enabling a deeper view of the sequence and nature of activities. For more information, see [Data collected by Task Mining](../reference/data-management.md).

For a complete list of tables installed with Task Mining, see [Components installed with Task Mining](../reference/installed-with-task-mining.md).

## Data collection methods

Task Mining analysts initiate the collection of workstation user data in the following ways:

-   Adding a workstation user to a Task Mining project to collect data in the scope of a given project
-   Submitting a data log request for a specified time to create a data pool that you can pull from later for future projects

## Data privacy

These data privacy measures safeguard the data collected, reduce the risk of exposing sensitive information, and provide users with control over data collection.

-   Data encryption of all data during transmission and while stored.
-   A predefined list of applications to exclude from monitoring by the agent that is applied at the system level.
-   Event filters to exclude specific types of events from being captured, and to replace with replacement values.
-   Event masking to enable the system to protect sensitive information by masking specific attributes of an event rather than excluding the event entirely.
-   A private mode on the Task Mining agent controlled by workstation users that temporarily pauses data collection so users can perform personal or sensitive tasks without having their activities logged.
-   Required approval by the workstation user's manager \(or similar role\) for any data collection from workstation users. This role is responsible for reviewing and approving data collection on a case-by-case basis.
-   Required explicit consent from workstation users when data collection is enabled on their workstation.
-   Restricted workstation user data tables that conceal the identity of the workstation user from whom the data originated and are accessible only to system admins.
-   Automatic deletion of data that is not linked to an active project for analysis is deleted after a specified amount of time, so that unused data doesn’t remain in the system indefinitely.
-   Restricted access so only authorized users can create and modify Task Mining projects or view or manipulate project data.
-   The ability to mask specific activity details such as application names, window titles, and URLs.

**Related topics**  


[Data collected by Task Mining](../reference/data-management.md)

