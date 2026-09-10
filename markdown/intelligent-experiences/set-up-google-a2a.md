---
title: Setting up Google A2A authentication for ServiceNow AI agents
description: Configure ServiceNow AI agents as secondary agents over the Google Agent2Agent \(A2A\) protocol by setting up authentication and enabling external agent interoperability.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/set-up-google-a2a.html
release: australia
topic_type: task
last_updated: "2026-08-31"
reading_time_minutes: 4
breadcrumb: [Integrate external AI agents, AI Agent Studio, Enable AI experiences]
---

# Setting up Google A2A authentication for ServiceNow AI agents

Configure ServiceNow AI agents as secondary agents over the Google Agent2Agent \(A2A\) protocol by setting up authentication and enabling external agent interoperability.

## Before you begin

Before you begin, verify the following requirements:

-   Platform version: Yokohama Patch 11+ \(January 2026\) or Zurich Patch 4+ \(December 2025\)
-   Now Assist AI Agents 6.0.x or later \(December 2025 release or newer\)
-   Administrator access to configure system settings and API policies

Role required: sn\_aia.admin

## Procedure

1.  Enable external agent settings in AI Agent Studio.

    1.  Go to **All** &gt; **AI Agent Studio** &gt; **Settings**.

    2.  Under **External AI agents**, set the following properties to **Allow**:

        -   **Allow ServiceNow to access external AI agents**
        -   **Allow third party access to ServiceNow AI agents**
2.  Create and configure a service account with appropriate roles.

    1.  Create a user in the User \[Sys\_User\] table with the following settings:

        -   **Active**: **true**
        -   **Password needs reset**: **false**
        -   **Locked out**: **false**
    2.  Assign the following roles to the user:

        -   sn\_aia.integration \(recommended for basic runtime access\)
        -   sn\_aia.admin \(for testing only – full write/create access\)
        -   Any necessary application roles such as itil
        -   Integration roles: rest\_service and snc\_platform\_rest\_api\_access
3.  Select and configure the AI agent for external discovery.

    1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Agentic Solutions**.

    2.  Select the AI agent you want to configure.

        Note the Sys\_Id of the AI agent from the browser address bar or directly from the AI Agent \[sn\_aia\_agent\] table.

    3.  Enable **Allow third-party to access this AI agent**.

        This makes the agent externally discoverable and sets the `External discoverable` property to true in the AI Agent Config record.

    4.  Select a display channel where your external AI agent can be discovered.

        Under the Channel and display section of the external AI agent, select one or both the display options:

        -   **ServiceNow Otto panel**
        -   **ServiceNow Otto chat assistants**
4.  Configure the communication mode.

    1.  Decide on your communication mode:

        -   **Synchronous:** Use for testing with Postman or when you don't have a functional callback URL.
        -   **Asynchronous:** Recommended for production for better user experience and performance. Requires a callback URL configured in the External Agent Callback Registry table.
    2.  To set synchronous mode, go to **AI Agent Studio** &gt; **Settings** &gt; **External AI agents** &gt; **Discoverability** and set the **Communication mode** to **Synchronous**.

        Alternatively, navigate to **All** &gt; **Tables** &gt; **Messaging Channels** &gt; **AI Agent A2A Channel** and set **Synchronous** to **true**.

5.  Create an OAuth application registry for external clients.

    1.  Go to **System OAuth** &gt; **Application Registry**.

    2.  Select **New** and choose **Create an OAuth API endpoint for external clients**.

    3.  Fill in the following fields:

        -   **Name:** Enter a descriptive name \(example: A2A OAuth External Agents\)
        -   **Client ID:** Auto-populated
        -   **Client Secret:** Auto-generated upon saving
    4.  Under **Auth Scopes**, add the `a2aauthscope` record.

    5.  Save the Application Registry record.

6.  Configure authentication profiles for OAuth or API key access

    1.  Choose your authentication method: **OAuth 2.0** or **API Key**.

        -   To configure OAuth 2.0:
            -   Navigate to **System Web Services** &gt; **API Access Policies** &gt; **Inbound Authentication Profile** and select **New**.
            -   Set **Type** to **OAuth** and select the OAuth entity you created in the previous step.
        -   To configure API Key:
            -   Navigate to **System Web Services** &gt; **API Access Policies** &gt; **Inbound Authentication Profiles**, select **New**.
            -   Select **Create API Key authentication profiles** and set **Auth Parameter** to `x-sn-apikey`.
    2.  For API Key authentication, go to **System Web Services** &gt; **API Access Policies** &gt; **REST API Key**, select **New**, and configure:

        -   **User:** Select your service account
        -   **Auth Scope:** a2authscope
7.  Add authentication profiles to the API access policy.

    1.  Navigate to **System Web Services** &gt; **API Access Policies** &gt; **REST API Access Policies**.

    2.  Select **AI Agent A2A API Access Policy**.

    3.  Under **Inbound authentication profiles**, add your authentication profile \(OAuth or API Key\) to the list.

8.  Test the A2A API configuration using your chosen authentication method.

    1.  **API Key authentication**: Open Postman and create a GET request:

        -   **Method:** GET
        -   **URL:** `https://<your instance name>.service-now.com/api/sn_aia/a2a/id/<your AI Agent ID>/well_known/agent_json`
        -   **Headers:** Add `x-sn-apikey: <your API key>`
    2.  **OAuth 2.0 authentication**: In Postman, set **Auth Type** to **OAuth 2.0**, configure grant type and credentials, then select **Get New Access Token**.

    3.  Send the request and verify a 200 OK response with the Agent Card payload returned for your AI Agent sys\_id.

9.  Configure external instance connectivity \(for multi-instance setups\).

    1.  For API Key authentication on client instance, navigate to **IntegrationHub** &gt; **Connections &amp; Credential Aliases**.

        Create two connection aliases: one for Agent Card discovery and one for Agent Execution. For each, set the connection URL to the appropriate A2A endpoint on the server instance and configure a credential with header `x-sn-apikey`.

    2.  For OAuth 2.0 authentication on client instance, create an outbound Application Registry in **System OAuth** &gt; **Application Registry** using the same Client ID and Client Secret from the server instance.

        Create the appropriate connection aliases and OAuth 2.0 credentials in IntegrationHub.

    3.  In AI Agent Studio on the client instance, navigate to **Create and manage** &gt; **AI agents** and select **Add** &gt; **External**.

        Choose **Agent2Agent \(A2A\) Protocol** and select your connection alias as the external provider.

10. Debug and validate your A2A implementation.

    1.  Enable debug system properties to review logs during troubleshooting:

        -   **com.snc.platform.security.oauth.debug**: **true**
        -   **glide.auth.debug.enabled**: **true**
    2.  Navigate to **Flow Designer** &gt; **Flow Administration** &gt; **Settings**.

        Set **Reporting** to **Trace** and **Logging** to **Debug** for sub-production environments only.

    3.  Review the following tables to validate execution and connectivity:

        -   Execution Plan \[`sn_aia_execution_plan`\]
        -   External Agent Execution History \[`sn_aia_external_agent_exec_history`\]
    4.  Verify that service account credentials are in good standing: Active status, password does not need reset, and account is not locked out.


## Result

You have successfully configured ServiceNow AI agents as secondary agents over the Google A2A protocol. Your AI agents can now accept external requests from other systems using either OAuth 2.0 or API key authentication.

## What to do next

After completing this setup, you can:

-   Add your configured AI agents as external agents in other ServiceNow instances.
-   Integrate your AI agents with third-party systems using the A2A protocol.
-   Monitor agent execution and troubleshoot connectivity issues using the execution history tables.

