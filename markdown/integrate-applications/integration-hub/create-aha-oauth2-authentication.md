---
title: Create an Aha! OAuth2 application
description: Create an OAuth2 application in the Aha! account so that the application can authenticate access requests to the Aha! server from your ServiceNow instance.
locale: en-US
release: yokohama
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Aha! Spoke, Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Data and Automation]
---

# Create an Aha! OAuth2 application

Create an OAuth2 application in the Aha! account so that the application can authenticate access requests to the Aha! server from your ServiceNow instance.

## Before you begin

Role required: admin

Ensure that you've signed up as an admin in the Aha! account.

Ensure that you've installed the Aha! spoke plugin.

## Procedure

1.  Go to [OAuth2 Authentication](https://www.aha.io/api/oauth2).

2.  Log in to the Aha! site using your admin credentials.

3.  On the Features board page, click the settings icon \(![Aha settings icon.](../image/aha-settings-icon.png)\).

4.  On the Personal settings page, click **Developer**.

5.  Click the **OAuth applications** tab.

6.  Click **Register OAuth application**.

7.  On the Register new OAuth application form, enter `https://*instance*/oauth_redirect.do` as the Redirect URI, where *instance* is the name of your ServiceNow instance.

8.  Click **Create**.

    The **OAuth applications** tab shows Client ID and Client Secret keys.

9.  Note down the values in the Client ID and Client Secret fields.


