---
title: Import messages from an incident
description: You can import messages from a slack channel for an incident and append them in the Comments to store all important messages in the ServiceNow instance.
locale: en-US
release: xanadu
product: Collaboration Services
classification: collaboration-services
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Collaboration services, IT Service Management]
---

# Import messages from an incident

You can import messages from a slack channel for an incident and append them in the **Comments** to store all important messages in the ServiceNow® instance.

## Before you begin

-   Role required: sn\_incident\_write, itil, or admin
-   You must be a member of the private slack channel to import messages from the private channel.
-   Your ServiceNow® email ID must be associated with your slack account.
-   This feature is compatible with:
    -   Collaboration Services store app - minimum version 3.04
    -   Slack store app - minimum version 1.4.x

## About this task

Importing messages helps agents to view the history of the incident, allow the requester to see all discussions about their incident in one place. This helps to capture the information required for post-ticket review and continuous improvement processes.

## Procedure

1.  Navigate to **All** &gt; **Incident** &gt; **Open**.

2.  Select the incident for which you want to import messages.

3.  Click the **View Slack Channels** related link.

    The View Slack Channels form appears. The form shows all the available slack channel for that incident.

4.  Click **Import messages** for the channel that you want to import the messages from.

    The Import messages from Slack form appears. The form shows all the messages on that channel sorted by date.

5.  On the form, fill in the fields.

<table id="table_ijp_mcv_znb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Search

</td><td>

Field to enter a keyword and search for a specific message.

</td></tr><tr><td>

Include reply threads in search

</td><td>

Option to include threads in search.

</td></tr><tr><td>

Filter by

</td><td>

-   **Shared by**: The messages will be filtered based on the selected users.
-   **Date**: The messages will be filtered based on the **Start** and **End**dates that you select.


</td></tr><tr><td>

Import messages as

</td><td>

-   **Additional comments**: The messages will be appended under Additional comments.
-   **Work notes**; The messages will be appended under Work notes.


</td></tr><tr><td>

Include attachments

</td><td>

Option to include attachments while importing messages.

</td></tr></tbody>
</table>6.  Click **Import messages**.


