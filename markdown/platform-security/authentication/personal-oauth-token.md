---
title: Get Personal OAuth Token \(using GlideOAuthClient\)
description: Check whether the user has a personal OAuth token. Use it to confirm valid access before running REST steps or integrations that require personal OAuth credentials.
locale: en-US
release: australia
product: Authentication
classification: authentication
topic_type: task
last_updated: "2026-05-08"
reading_time_minutes: 1
breadcrumb: [Personal authentication, Authentication, Access Management]
---

# Get Personal OAuth Token \(using GlideOAuthClient\)

Check whether the user has a personal OAuth token. Use it to confirm valid access before running REST steps or integrations that require personal OAuth credentials.

## Before you begin

Role required: oauth\_admin

## About this task

Use the `GlideOAuthClient` API to check if a personal OAuth token exists for the currently logged-in user. You can also use `ScopedPersonalAuthAPI` to get the personal OAuth token. For more information, see [PersonalAuthAPI - Scoped](https://www.servicenow.com/docs/bundle/yokohama-api-reference/page/app-store/dev_portal/API_reference/PersonalAuthAPI/concept/PersonalAuthAPIScoped.html).

## Procedure

1.  Use the following sample script to check for a personal access token associated with the current session user:

    ```
    function dumpToken(token) {
      if (token) {
        gs.info("Access token: " + token.getAccessToken());
        gs.info("Expires in: " + token.getExpiresIn());
        gs.info("Refresh token: " + token.getRefreshToken());
      }
    }
    
    var oAuthClient = new sn_auth.GlideOAuthClient();
    oAuthClient.setPersonal(true); // Returns the token for the logged-in user
    
    var token = oAuthClient.getToken('<credential_sys_id>', '<oauth_profile_sys_id>');
    dumpToken(token);
    ```

2.  Replace `<credential_sys_id>` and `<oauth_profile_sys_id>` with the appropriate record values.

    The `setPersonal(true)` method confirms that the token returned belongs to the currently logged-in user.

    **Note:** For more information on the methods for requesting and revoking OAuth refresh and access tokens, see: [Glide OAuth Client API Documentation](https://www.servicenow.com/docs/bundle/yokohama-api-reference/page/app-store/dev_portal/API_reference/GlideOAuthClient/concept/c_GlideOAuthClient.html).


