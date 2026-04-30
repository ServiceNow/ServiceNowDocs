---
title: Configure RWS TMS in the Localization Framework
description: Configure RWS TMS to use the RWS TMS service in the Localization Framework.
locale: en-US
release: yokohama
product: Localization Framework
classification: localization-framework
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Translation Management System configurations, Localization Framework settings, Configure the Localization Framework, Localization Framework, Translation and localization, Configure core features, Administer the ServiceNow AI Platform]
---

# Configure RWS TMS in the Localization Framework

Configure RWS TMS to use the RWS TMS service in the Localization Framework.

## Before you begin

Roles required: connection\_admin

## Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Connection &amp; Credential Aliases**.

    A credential record for RWS TMS is created when the RWS TMS spoke is installed with the Localization Framework Installer plugin \(com.glide.localization\_framework.installer\) activation.

2.  Open the RWS TMS credential record \(ID = sn\_sdl\_spoke.RWS\_TMS\).

3.  In the Connections related list, open the RWS connection record.

    A connection record for RWS is created when the RWS TMS spoke is installed with the Localization Framework Installer plugin \(com.glide.localization\_framework.installer\) activation.

    All the form fields are populated with the information that is fetched through the RWS spoke installation during the Localization Framework Installer plugin \(com.glide.localization\_framework.installer\) activation.

4.  In the Attributes section of the HTTP/HTTPS Connection form, provide the **project\_option\_id** connection attribute, and save the form.

    RWS provides an option to create automated or reviewed projects and provides the respective option IDs during RWS account creation.

5.  In the **Credential** field, click the information icon \(![Information icon.](../image/information-icon.png)\) and open the record.

    A record for OAuth 2.0 credentials is created when the RWS TMS spoke is installed with the Localization Framework Installer plugin \(com.glide.localization\_framework.installer\) activation.

6.  In the **OAuth Entity Profile** field, click the information icon \(![Information icon.](../image/information-icon.png)\) and open the record.

    An OAuth Entity profile is created when the RWS TMS spoke is installed with the Localization Framework Installer plugin \(com.glide.localization\_framework.installer\) activation.

7.  In the **OAuth provider** field, click the information icon \(![Information icon.](../image/information-icon.png)\) and open the record.

    An Application Registries record is created when the RWS TMS spoke is installed with the Localization Framework Installer plugin \(com.glide.localization\_framework.installer\) activation.

8.  Provide the Client ID and Client Secret provided by RWS at the time of account creation, and save the form.

9.  Open the OAuth 2.0 Credentials form again, and click the **Get OAuth Token** related link.

10. Provide the user name and password.

    RWS supports resource owner password credentials as the grant type. Provide these credentials to generate the token for the first time.

    **Note:** The user name and password do not persist in the ServiceNow instance.

11. Click **Get OAuth Token**.

    Once the OAuth token is created, the ServiceNow® platform regenerates the token until the refresh token expires.


**Parent Topic:**[Translation Management System configurations](../concept/tms-configuration.md)

