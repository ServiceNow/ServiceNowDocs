---
title: Slack slash commands
description: Slash commands provides a quick way to invoke your app to perform specific actions from Slack.
locale: en-US
release: zurich
product: Collaboration Services
classification: collaboration-services
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Slack integration - Incident Management, Reference, Collaboration services, IT Service Management]
---

# Slack slash commands

Slash commands provides a quick way to invoke your app to perform specific actions from Slack.

You need to [configure slash commands](https://www.servicenow.com/docs/access?context=set-up-slack&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US) to execute the commands. Only a user with the sn\_incident\_write, itil or admin role can execute the commands.

<table id="table_eg5_4td_jnb"><thead><tr><th>

Commands

</th><th>

Description

</th></tr></thead><tbody><tr><td>

/now help

</td><td>

Provides list of available ServiceNow commands with description.

</td></tr><tr><td>

/now create incident

</td><td>

Creates an incident with the inputs provided by the user.

</td></tr><tr><td>

/now list incidents

</td><td>

Lists all active incidents assigned to the user.

</td></tr><tr><td>

/now oncall \[group name\]

</td><td>

Displays shifts and members who are currently on-call for a group.**Note:** Only a user with the itil or the admin role can execute this command.

</td></tr><tr><td class="sub-head" colspan="2">

Slash commands that can be run only from channels associated with ServiceNow

</td></tr><tr><td>

/now comment \[comment\]

</td><td>

Posts a comment in the **Additional comments** field of the associated incident.

</td></tr><tr><td>

/now note \[note\]

</td><td>

Posts a note in the **Work notes** field of the associated incident.

</td></tr><tr><td>

/now assigntome

</td><td>

Assigns associated incident to the slack user.

</td></tr><tr><td>

/now assign \[@slack\_user\]

</td><td>

Assigns associated incident to a specific user.

</td></tr></tbody>
</table>**Parent Topic:**[Slack integration - Incident Management](../concept/im-slack-collaboration.md)

