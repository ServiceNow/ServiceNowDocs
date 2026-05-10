---
title: Configure Personal Authentication
description: You can configure personal OAuth authentication with the REST step in Flow Designer.
locale: en-US
release: australia
product: Authentication
classification: authentication
topic_type: task
last_updated: "2026-05-09"
reading_time_minutes: 2
breadcrumb: [Personal authentication, Authentication, Access Management]
---

# Configure Personal Authentication

You can configure personal OAuth authentication with the REST step in Flow Designer.

## Before you begin

Role required: oauth\_admin

Ensure that you install the IntegrationHub Starter Pack Installer \(com.glide.hub.integrations\) or a higher version.

## About this task

This task guides you through configuring personal OAuth authentication for REST steps in ServiceNow® Flow Designer. It enables REST calls to run using the session user's credentials, ensuring secure and personalized API access.

For information on how to check if a personal OAuth token exists for a user, see [Get Personal OAuth Token \(using GlideOAuthClient\)](personal-oauth-token.md).

For information to generate the initial token for a user, who doesn’t have access to the credentials page, see [Generate Personal Auth Initiator URL](generate-initial-token.md).

## Procedure

1.  Navigate to **Application Registries**, and create an OAuth application registry to connect to an external endpoint.

2.  Navigate to **Connection &amp; Credentials Aliases**, and create a connection alias.

    This alias is used in the REST steps. For more information, see [Create a Connection &amp; Credential alias](../../../product/credentials/task/connection-alias.md).

3.  Navigate to **HTTP\(s\) Connection**, and update the external end-point details for the connection record created in the previous step.

4.  Create an **OAuth Credential**.

    1.  Navigate to **OAuth 2.0 Credentials**.

    2.  Create a new OAuth credential record and link it to the OAuth profile created in Step 1.

5.  Add the **IntegrationType** field to the credential form.

6.  Update the **IntegrationType** field of the credential created in Step 4 to **Personal**.

7.  Generate a personal access token.

    1.  As a logged-in user, open the credential record.

    2.  Select **Get OAuth Token** to create a personal token.

    3.  Select **Manage Tokens** to view and manage the tokens.

    **Note:** Add a UI action to your application so that the end users can generate tokens. Only administrators can open the credential form directly.

8.  Navigate to **Action** to create an action for your use case.

9.  Add a REST step to the action.

    Select the connection alias created in Step 2.

    **Note:** Test the action with the REST outbound call. The credential is marked to be used for personal integration. The REST step might display an error since the action runs with the System integration role.

10. Create a new subflow, and add the action created in Step 8.

    1.  In the **Subflow properties** window, select **User who initiates session** in the **Run As** text field.

        Don’t select **System User** instead from the **Run As** text field.

11. Test the subflow.

    The REST step uses the token created for the session user. The subflow can also be invoked using FlowAPIs.

    -   **Sample script to invoke a subflow:**

        ```
        try {
            // Execute synchronously in the foreground. Allows access to subflow outputs.
            var result = sn_fd.FlowAPI.getRunner()
                .subflow('global.getpersonalincidentssubflow')
                .inForeground()
                .run();
        
            var outputs = result.getOutputs();
        } catch (ex) {
            var message = ex.getMessage();
            gs.error(message);
        }
        ```

12. Manage missing or expired tokens.

    If the session user has no access token, the REST request returns a **HTTP 401 Unauthorized status code** response. Ensure that the token is created before you initiate the flow.

    If the access token is expired but a valid refresh token exists, the system automatically renews the access token.


