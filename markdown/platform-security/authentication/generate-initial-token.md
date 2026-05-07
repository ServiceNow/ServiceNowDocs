---
title: Generate Personal Auth Initiator URL
description: Generate the initial token for a user who doesn’t have access to the credentials page to configure personal authentication.
locale: en-US
release: australia
product: Authentication
classification: authentication
topic_type: task
last_updated: "2026-05-06"
reading_time_minutes: 1
breadcrumb: [Personal authentication, Authentication, Access Management]
---

# Generate Personal Auth Initiator URL

Generate the initial token for a user who doesn’t have access to the credentials page to configure personal authentication.

## Before you begin

Role required: connection\_admin, oauth\_admin

## About this task

Users without the **connection\_admin** role can’t access the Credentials page to generate OAuth tokens. These users must generate a personal token using the `oauth_initiator` URL with additional parameter indicating that the token is personal and requested for session user.

You can also use the scoped `PersonalAuthAPI` with the `sn_personal_auth` plugin to generate the initiator URL. For more information, see [PersonalAuthAPI - getInitiatorURL\(String aliasId\)](https://www.servicenow.com/docs/bundle/yokohama-api-reference/page/app-store/dev_portal/API_reference/PersonalAuthAPI/concept/PersonalAuthAPIScoped.html#title_PerAuth-getInitiatorURL_S)

**Note:** If the personal authentication plugin \(`com.snc.sn_ihub_personal_auth`\) is activated, use the scoped API to generate the initiator URL. This. API is available only if the plugin is installed.

## Procedure

1.  Use the following format to construct the token generation URL for Password Grant Type:

    ```
    https://<instance-name>.service-now.com/oauth_password_input.do?
    sysparm_oauth_requestor_context=oauth_2_0_credential&sysparm_oauth_requestor=
    <credential sys_id>&sysparm_oauth_provider_profile=<OAUTH profile sys_id>&sysparm_oauth_personal=true 
    ```

2.  Use the following format to construct the token generation URL for Authorization Code Grant Type:

    ```
    https:// ://<instance-name>.service-now.com /oauth_initiator.do?
    oauth_requestor_context=oauth_2_0_credentials&oauth_requestor=
    <credential sys_id>&oauth_provider_profile=<OAUTH profile sys_id>&response_type=code&personal=true
    ```


