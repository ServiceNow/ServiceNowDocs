---
title: Integrate Password Reset with a Service Portal widget
description: You can enable a Password Reset process in a Service Portal page by adding a widget that opens the password reset pages inside the portal.
locale: en-US
release: zurich
product: Password Reset
classification: password-reset
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure, Password Reset, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Integrate Password Reset with a Service Portal widget

You can enable a Password Reset process in a Service Portal page by adding a widget that opens the password reset pages inside the portal.

## Before you begin

Role required: password\_reset\_admin or sp\_admin

## Procedure

1.  On the Service Portal Designer for the portal, create a new page — the page where the user will perform the password reset process.

2.  On the **Widget** tab, under Layouts, select the 12-column layout and drop it onto the page.

3.  Drop the **Pwd reset** widget into the 12-column layout and then save the page.

    The three tabs of the password reset process appear in the layout.

4.  In the **Reset my password** link on the login page for the portal, specify the URL of the new password reset page.

    The URL must include one required parameter and may contain one optional parameter:

    -   Required: `sysparm_show_custom_header_footer=false`. This parameter disables the native header and footer feature of the password reset page.
    -   `sysparm_redirect_url=<portalName>?id=<pageName>`. This parameter specifies the page to go to after a successful reset — typically the login page for the portal.
    For example, `https://server.acme.com/acme_community?id=password_reset_page& sysparm_show_custom_header_footer=false&sysparm_redirect_url=acme_community?id=communities_login`


**Parent Topic:**[Configuring Password Reset](../concept/password-reset-admin-guide.md)

