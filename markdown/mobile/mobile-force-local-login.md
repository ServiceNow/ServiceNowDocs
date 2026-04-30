---
title: Force local login in mobile apps
description: Configure the force local login option to provide local login experience on mobile apps even when the instance is configured with Single Sign On \(SSO\) configuration. You can configure this feature independently on any available ServiceNow app.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Mobile authentication, Configuring the Mobile Platform, Mobile Platform]
---

# Force local login in mobile apps

Configure the force local login option to provide local login experience on mobile apps even when the instance is configured with Single Sign On \(SSO\) configuration. You can configure this feature independently on any available ServiceNow® app.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Mobile** &gt; **Mobile Branding** &gt; **Mobile App Configs**.

2.  Open the record for the mobile app where you want to force local logins.

3.  Enable the **Force Local Login** field.

4.  Click **Update**.


## Result

The selected mobile app routes your users to the local login authentication page. The app will default to the authentication method defined on your instance if this field is disabled.​

**Parent Topic:**[Mobile authentication](../concept/mobile-authentication.md)

