---
title: Associate existing slack channel with a group
description: Associate an existing slack channel to reach out to an assignment group from an incident. Assignment groups are a great way to contact all your stakeholders at once.
locale: en-US
release: australia
product: Collaboration Services
classification: collaboration-services
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Set up slack for a user or group, Slack integration - Incident Management, Collaboration services, IT Service Management]
---

# Associate existing slack channel with a group

Associate an existing slack channel to reach out to an assignment group from an incident. Assignment groups are a great way to contact all your stakeholders at once.

## Before you begin

Role required: sn\_slack\_ah\_v2.slack\_admin or admin

## Procedure

1.  Navigate to **All** &gt; **Slack** &gt; **Slack Channel Cache** and click **New**.

2.  On the form, fill in the fields.

<table id="table_mp4_grd_jnb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Channel Name

</td><td>

Name of the existing slack channel.

</td></tr><tr><td>

Channel ID

</td><td>

Unique ID given by slack for a channel.

</td></tr><tr><td>

Channel Topic

</td><td>

Description about the purpose of the channel.

</td></tr><tr><td>

Channel Link

</td><td>

URI scheme to deep link into native Slack client of user. Example: slack://channel?team=\{TEAM\_ID\}&amp;id=\{CHANNEL\_ID\}, where &lt;TEAM\_ID&gt; is slack workspace id and &lt;CHANNEL\_ID&gt; is the unique Id for the slack channel.**Note:** For more information, refer [Deep linking into Slack](https://api.slack.com/reference/deep-linking#client__supported-uris__open-a-channel).

</td></tr><tr><td>

Document ID

</td><td>

Group record for which channel is intended to be used.-   Table: Group \[sys\_user\_group\]
-   Document: &lt;Reference to a group&gt;


</td></tr><tr><td>

Is Archived

</td><td>

Option to indicate whether the slack channel is active or inactive.

</td></tr><tr><td>

Is Private

</td><td>

Option to indicate whether the slack channel is private or public.**Note:** It is strongly recommended to associate a public slack channel. In case of private channel, and you are not a member of it, the navigation link may break.

</td></tr><tr><td>

Creator

</td><td>

User who creates the slack channel cache record.

</td></tr></tbody>
</table>3.  Click **Submit**.


