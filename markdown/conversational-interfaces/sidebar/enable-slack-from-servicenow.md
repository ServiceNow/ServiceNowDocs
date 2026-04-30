---
title: Enable Slack from ServiceNow
description: Ensure the email field of system user records that will be mapped to Slack users are properly updated. This must be done before the scheduled job that syncs the users between Slack and ServiceNow runs.
locale: en-US
release: zurich
product: Sidebar
classification: sidebar
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Integrate Sidebar and Slack, Sidebar and Slack, Configuring Sidebar, Sidebar, Conversational Interfaces]
---

# Enable Slack from ServiceNow

Ensure the email field of system user records that will be mapped to Slack users are properly updated. This must be done before the scheduled job that syncs the users between Slack and ServiceNow runs.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Settings** &gt; **Sidebar**.

2.  In the Integrations section, select **Set up** for Slack.

3.  On the Slack integration setup page, fill in the Slack credential fields:

    -   Client ID - ID associated with the app you created.
    -   Client Secret - auto-assigned client secret located on the Slack App Credentials screen.
    -   Signing secret - auto-assigned signing secret located on the Slack App Credentials screen.
    -   Bot User OAuth Token - auto-assigned token located on the Slack OAuth &amp; Permissions screen. This field must begin with `xoxb`.
4.  Select **Save**.

5.  In the navigation filter, enter `sys_cs_collab_settings.list`.

6.  On the Collab Chat Settings page, check that Enable Slack is set to true and that Preference Channel is set to Slack.

    If Enable Slack is not set to true or the Preference Channel is not set to Slack, deactivate and then reactivate Slack.

7.  In the navigation filter, enter `oauth_credential.list`.

8.  On the OAuth Credentials page, check that a new record named Sidebar Slack Oauth Entity exists.

    This is the app level token that is required for the scheduled job to run successfully to sync the users.

9.  In the navigation filter, enter `sys_cs_collab_provider_user_profile.list`.

10. On the Collaboration Chat Profiles page, check that Slack users have been imported properly.

11. Select **Discuss** and add at least one external user \(a Slack user who does not have a ServiceNow account\).


