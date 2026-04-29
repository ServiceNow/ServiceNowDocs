---
title: Set up an OAuth application
description: Set up an OAuth application on the Asana developer's console to generate the client ID and secret that you use to set up the Asana spoke connection record later.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Set up the Asana spoke, Asana Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Set up an OAuth application

Set up an OAuth application on the Asana developer's console to generate the client ID and secret that you use to set up the Asana spoke connection record later.

## Before you begin

Role required: admin

Access to the Asana developer's console.

## Procedure

1.  Log in to the Asana [developer's console](https://app.asana.com/0/my-apps).

2.  Under My apps, select **Create new app**.

    ![Create new app button.](../image/asana-spoke-create-oauth-app.png)

3.  Enter a name of the app.

    You can change the app name as many times as needed. To change the name, go to the Basic information tab on the left panel.![App name field.](../image/asana-spoke-name-ouath-app.png)

4.  From the Client ID and Client secret fields, copy the respective values and store them securely.

5.  Under the Redirect URLs heading, select **Add redirect URL**.

    ![Add Redirect URL button.](../image/asana-spoke-add-redirect-url.png)

6.  Enter the redirect URL in the format `https://<your instance name>.service-now.com/oauth_redirect.do`.

    You’ve created the OAuth app and generated the details required to create a connection record for the Asana spoke.


