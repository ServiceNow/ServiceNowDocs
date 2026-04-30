---
title: Third party token workflow for service accounts
description: Create a service account in ServiceNow to represent the identity of a third-party application accessing APIs through a trusted identity provider \(IdP\). This account maps the token claims to a user record and manages access with roles and permissions.
locale: en-US
release: zurich
product: Authentication
classification: authentication
topic_type: task
last_updated: "2026-04-29"
reading_time_minutes: 1
breadcrumb: [Third Party Token Grant, Inbound integrations, OAuth inbound, OAuth authentication, Authentication, Access Management]
---

# Third party token workflow for service accounts

Create a service account in ServiceNow® to represent the identity of a third-party application accessing APIs through a trusted identity provider \(IdP\). This account maps the token claims to a user record and manages access with roles and permissions.

## Before you begin

Role required: `oauth_admin, mi_admin, admin`

## About this task

When a third-party application authenticates using a token from an external identity provider \(IdP\), ServiceNow needs a corresponding user record to map the identity and apply access controls.

Create a corresponding `sys_user` account in ServiceNow for your service account. The value of the claim configured during the initial setup in the token issued by your Idp is mapped to the user field specified. This account represents the service identity in ServiceNow. You can restrict this account to API access only, and assign the necessary permissions by adding the appropriate roles and groups.

![Service Account Workflow](../images/mic-third-party-token-service-account.png "Service Account Workflow")

## Procedure

1.  Follow the [Third party token workflow for user accounts](third-party-token-worflow-for-user-accounts.md) to create a user account.

2.  Create a `sys-user` account in ServiceNow to represent your service account identity.

    Ensure that the token claim value matches with that of the value in the mapped user field \(such as user\_name or email\) in the user record. Example: user\_name, email.

    1.  Select the Web service access only option to restrict the account to API access.

    2.  Assign the required roles and groups to grant the appropriate permission.

    The ServiceNow platform maps the configured claim to the specified user field in the `sys_user` record. It enforces access based on that user's assigned roles and groups.

3.  Make a GET request with the authorization header to the following endpoint:

    ```
    Method: GET
    Endpoint: https:// <servicenow_base_url> /api/now/incident
    Authorization: Bearer YOUR_THIRD-PARTY_TOKEN
    ```


