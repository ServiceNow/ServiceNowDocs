---
title: Configure XTM TMS in the Localization Framework
description: Configure XTM TMS to use the XTM TMS service in the Localization Framework.
locale: en-US
release: australia
product: Localization Framework
classification: localization-framework
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Translation Management System configurations, Localization Framework settings, Configure the Localization Framework, Localization Framework, Translation and localization, Configure core features, Administer the ServiceNow AI Platform]
---

# Configure XTM TMS in the Localization Framework

Configure XTM TMS to use the XTM TMS service in the Localization Framework.

## Before you begin

Roles required: connection\_admin

## Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Connection &amp; Credential Aliases**.

    A credential record for XTM TMS is created when the XTM TMS spoke is installed with the Localization Framework Installer plugin \(com.glide.localization\_framework.installer\) activation.

2.  Open the **XTM TMS** \(ID = sn\_xtm\_spoke.XTM\_TMS\) credential record.

3.  In the Connection Attributes tab of the form, provide the **template\_id** and **customer\_id** attributes, and save the form.

4.  In the Connections tab, open the XTM connection record by selecting the information icon \(![Information icon.](../image/information-icon.png)\).

    A connection record for XTM is created when the XTM TMS spoke is installed with the Localization Framework Installer plugin \(com.glide.localization\_framework.installer\) activation. All the form fields are populated with the information fetched through the XTM spoke installation.

    **Note:** In the **Connection URL** field, enter the URL of the XTM connection.

5.  In the **Credential** column, select the value **XTM**to open the **OAuth 2.0 Credentials** \[oauth\_2\_0\_credentials\] record.

    A record for OAuth 2.0 credentials is created when the XTM TMS spoke is installed with the Localization Framework Installer plugin \(com.glide.localization\_framework.installer\) activation.

6.  In the **OAuth Entity Profile** field, select the information icon \(![Information icon.](../image/information-icon.png)\) to open the record.

    An OAuth Entity Profile is created when the XTM TMS spoke is installed with the Localization Framework Installer plugin \(com.glide.localization\_framework.installer\) activation.

7.  In the **OAuth provider** field, select the information icon \(![Information icon.](../image/information-icon.png)\) to open the **Application Registries** \[oauth\_entity\] record.

    An Application Registries record is created when the XTM TMS spoke is installed with the Localization Framework Installer plugin \(com.glide.localization\_framework.installer\) activation.

8.  Provide the Client ID and Client Secret provided by XTM at the time of account creation, and save the form.

9.  Open the OAuth 2.0 Credentials form again, and select the **Get OAuth Token** related link.

10. Provide the username and password.

    XTM supports resource owner password credentials as the grant type. Provide these credentials to generate the token for the first time.

    **Note:** The username and password do not persist in the ServiceNow instance.

11. Select **Get OAuth Token**.

    Once the OAuth token is created, the ServiceNow® platform regenerates the token until the refresh token expires.


**Parent Topic:**[Translation Management System configurations](../concept/tms-configuration.md)

