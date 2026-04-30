---
title: REST API scope troubleshooting
description: Troubleshooting actions can help resolve common issues when setting up or running the REST API scope.
locale: en-US
release: xanadu
product: Authentication
classification: authentication
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [REST API Auth Scope, REST API access policies, API access policy, Authentication, Access Management]
---

# REST API scope troubleshooting

Troubleshooting actions can help resolve common issues when setting up or running the REST API scope.

<table id="table_upj_wjr_4tb"><thead><tr><th>

Issue

</th><th>

Action

</th></tr></thead><tbody><tr><td>

REST API is linked with auth scope, however in runtime there is no auth scope check even using Bearer token authentication.

</td><td>

-   Make sure the sys\_api\_access\_policy record is active. Runtime ignores inactive records.
-   Check if property **com.glide.rest.api.auth.scope.check.enable** is set to false.
-   Check if the OAuth token has `useraccount` auth scope.

</td></tr><tr><td>

REST API is linked with **auth\_scope1**, however the access token which has **auth\_scope2** is also able to access it.

</td><td>

-   Check if this record is active.
-   Check for this REST, check if any other records, which have the same APIs but different apply methods, versions, or resource.

</td></tr><tr><td>

REST API is linked with auth scope, however in runtime there is no auth scope check for **basicAuth** and **mutualAuth**.

</td><td>

It is expected since the REST API auth scope only applies to the OAuth access token or OIDC token. It doesn’t apply BasicAuth, Session Cookie and Certificate based authentication.

</td></tr><tr><td>

REST API call return 403 when using the OAuth access token.

</td><td>

Check for the error message "Missing required api access scope". If found then the auth scope check fails for this REST API

</td></tr><tr><td>

Pre-defined `useraccount` is deleted and not sure to restore.

</td><td>

Export `useraccount` as `xml` from the other instance and import it or create an `useraccount` and modify system property **glide.oauth.token.scope.useraccount** to the newly created sys\_id record.

</td></tr></tbody>
</table>## Frequently asked questions

Following are some of the frequently asked question when using the REST API Auth scope:

-   **Can one OAuth token be linked with several auth scopes?**

    Yes, one `oauth_entity` can be linked with multiple auth scopes, every OAuth token issued by this `oauth_entity` has the same auth scopes.

-   **Can different OAuth tokens with different auth scopes access the same REST API?**

    Yes, for the same REST API, it may be accessed by different auth scopes. As long as one auth scope is matched, the auth scope returns the results.

-   **Can OAuth access token with `useraccount` auth scope access any REST APIs?**

    Yes, the `useraccount` has full access to auth scope.

-   **Can OAuth access token OAuth scope be changed dynamically?**

    Yes, the auth scoped is not hard-coded with the access token in the `oauth_credential` table. Instead auth scope is getting from linked `oauth_entity` during runtime.

-   **Can OAuth token keep same auth scopes after refresh?**

    Yes, auth scope will not change after token refresh, unless `oauth_admin` modify auth scope linked with `oauth_entity`.

-   **Pre-defined `useraccount` auth scope record is deleted, can a new auth scope with name `useraccount` be created?**

    Creating a new auth scope with the same `useraccount` doesn't work. In the runtime, it uses the `sys_id` instead of name to do the auth scope check, modify the system property **glide.oauth.token.scope.useraccount** to the newly created `sys_id` record.

-   **If admin modify auth scoped linked with `oauth_entity`, are all the existing OAuth access token issued by this OAuth entity changed also?**

    Yes, the auth scope is not directly linked with the OAuth access token, it is getting from `oauth_entity` during runtime.

-   **Can different OAuth access tokens issued by the same `oauth_entity` have different auth scopes?**

    No, all access to the token is issued by the same `oauth_entity` and always have the same auth scopes.

-   **Can a user define different auth scopes for a particular endpoint?**

    No, there is a unique constrain check for a particular REST API endpoint. However for the same REST API endpoint, it may have more than one matched auth scopes.

-   **Is the auth scope check used for BasicAuth also?**

    No, auth scope check is only OAuth access token and OIDC token, it is not applied for **basicAuth** and **mutualAuth**


