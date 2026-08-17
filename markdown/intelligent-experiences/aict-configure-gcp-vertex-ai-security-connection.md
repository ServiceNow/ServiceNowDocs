---
title: Add a GCP Vertex AI connection
description: Connect Google Cloud \(GCP\) Vertex AI to AI Control Tower using a service account and OAuth 2.0 JWT Bearer authentication, so AI agent containment using kill switch protocol can reach and deactivate agents running on GCP Vertex AI.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/aict-configure-gcp-vertex-ai-security-connection.html
release: australia
topic_type: task
last_updated: "2026-07-29"
reading_time_minutes: 5
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Configuring security connections, Configuring integrations, Configure, AI Control Tower, Enable AI experiences]
---

# Add a GCP Vertex AI connection

Connect Google Cloud \(GCP\) Vertex AI to AI Control Tower using a service account and OAuth 2.0 JWT Bearer authentication, so AI agent containment using kill switch protocol can reach and deactivate agents running on GCP Vertex AI.

## Before you begin

Confirm the following:

-   A GCP project with the Vertex AI API enabled and IAM permissions to create a service account.
-   A GCP service account granted three IAM roles.

|Role|Scope|Purpose|
|----|-----|-------|
|`roles/iam.denyAdmin`|Organization or folder level only|Create and delete the Deny policy used to contain an agent.|
|`roles/aiplatform.viewer`|Project level|Read the agent's identity from Vertex AI.|
|`roles/resourcemanager.projectViewer`|Project level|Resolve the GCP project ID.|

-   Download a JSON key for the service account. In the Google Cloud console, go to **IAM &amp; Admin** &gt; **Service accounts**, select the service account, then select **Add key** &gt; **Create new key** and choose **JSON** as the key type. You'll need the `private_key`, `private_key_id`, `client_email`, and `token_uri` values from this file in the steps below.
-   For each ADK-based AI agent you want containment to cover, enable Agent Identity. Create an `.agent_engine_config.json` file with `{ "identity_type": "AGENT_IDENTITY" }` and follow [Create and deploy an agent with Agent CLI and Agent Identity](https://docs.cloud.google.com/iam/docs/create-and-deploy-agent) to deploy the agent with a unique identity.

    **Important:** AI agent containment is supported only for GCP agents that have a unique agent identity configured this way.


Role required: creating the OAuth, JWT, and certificate records in steps 1–8 below typically requires an instance admin or integration admin role. Creating the security connector in steps 9–11 requires sn\_ai\_governance.ai\_steward.

## About this task

Google Cloud \(GCP\) Vertex AI authenticates using OAuth 2.0 with a JWT Bearer grant, which requires more setup than an access-key based connection: you convert the service account key into a Java Key Store, build a chain of OAuth and JWT records from it, and then attach the resulting Connection &amp; Credential Alias to the security connector.

## Procedure

1.  Create the X.509 certificate.

    Convert the service account's private key into a Java Key Store \(`.jks`\) file and import it as an X.509 Certificate. See the ServiceNow documentation on converting a private key to a Java Key Store. If your team already has a pre-generated `.jks` bundle, you can upload it directly instead.

    |Field|Description|
    |-----|-----------|
    |**Name**|Descriptive name, such as the service account's email address.|
    |**Type**|Select **Java Key Store**.|
    |**Key store password**|Password used when the `.jks` file was created.|
    |**Active**|Select this option.|

2.  Create the JWT Keys record.

    Navigate to **JWT Keys** and create a new record.

    |Field|Description|
    |-----|-----------|
    |**Name**|Descriptive name.|
    |**Signing Keystore**|The certificate record from the previous step.|
    |**Key Id**|The `private_key_id` value from the service account JSON key. Copy it directly.|
    |**Signing Algorithm**|Select **RSA 256**.|
    |**Signing Key**|The password used to create the certificate in the previous step.|
    |**Active**|Select this option.|

3.  Create the JWT Provider record.

    Navigate to **JWT Provider** and create a new record with the following:

    -   **Name**: descriptive name.
    -   **Signing Configuration**: the JWT Keys record from the previous step.
    -   **Expiry Interval \(sec\)**: `3600`.
    Add these Standard Claims:

    -   `aud`: The `token_uri` value from the service account key \(typically `https://oauth2.googleapis.com/token`\).
    -   `iss`: The `client_email` value from the service account token.
    -   `sub`: The `client_email` value from the service account token.
    Add this Custom Claim:

    `scope : https://www.googleapis.com/auth/cloud-platform`

4.  Create the Application Registry record.

    Navigate to **Application Registries** and create a new **OAuth Provider** record.

    |Field|Description|
    |-----|-----------|
    |**Name**|Descriptive name.|
    |**Provider Type**|Select **Connect to a third-party OAuth Provider – Outbound** \(or the equivalent option on your instance\).|
    |**Default Grant Type**|Select **JWT Bearer**.|
    |**Client ID**|The `client_id` value from the service account JSON key you generated earlier.|
    |**Client Secret**|The `private_key` value from the service account JSON key, with `\n` sequences converted to actual newlines.|
    |**Authorization URL**|`https://accounts.google.com/o/oauth2/auth`|
    |**Token URL**|`https://oauth2.googleapis.com/token`|
    |**Refresh Token Lifespan**|`8640000`|
    |**Active**|Select this option.|

    Under **OAuth Entity Scopes**, add a scope named **Vertex AI Scope** with the value `https://www.googleapis.com/auth/cloud-platform`.

5.  Update the default OAuth Entity Profile.

    Open the default profile that was automatically created for the OAuth Provider in the previous step, and set:

    -   **Grant type**: **JWT Bearer**.
    -   **JWT Provider**: the JWT Provider record from the earlier step.
    -   **Is default**: select this option.
    Add **Vertex AI Scope** under **OAuth Entity Profile Scopes**.

6.  Create the OAuth 2.0 Credentials record.

    Navigate to **OAuth 2.0 Credentials** and create a new record with the following:

    -   **Name**: descriptive name.
    -   **OAuth Entity Profile**: the profile from the previous step.
    -   **Applies to**: **All MID servers** \(or as appropriate for your instance\).
    -   **Active**: select this option.
    Use the **Get OAuth Token** related link to confirm the credential retrieves a token successfully.

7.  Create the Connection &amp; Credential Alias.

    Navigate to **Connection &amp; Credential Aliases** and create a new record with the following:

    -   **Name**: descriptive name.
    -   **ID**: a unique identifier for the alias.
    -   **Type**: **Connection and Credential**.
    -   **Connection type**: **HTTP**.
    -   **Default Retry Policy**: **Default HTTP Retry Policy**.
8.  Create the HTTP\(S\) connection.

    From the **Connections** related list on the alias you just created, select **New** and fill in:

    -   **Name**: descriptive name.
    -   **Credential**: the OAuth 2.0 Credentials record from the earlier step.
    -   **Connection alias**: the alias from the previous step.
    -   **Protocol**: **https**.
    -   **Host**: `iam.googleapis.com`.
    -   **Connection URL**: `https://iam.googleapis.com`
    -   **Active**: select this option.
9.  Navigate to **AI Control Tower** &gt; **Settings** &gt; **Integrations** &gt; **Security**.

10. On the **Available connectors** sub-tab, select **GCP Vertex AI**.

11. Fill in the fields and select **Submit**.

    |Field|Description|
    |-----|-----------|
    |**Name**|Unique, descriptive name for this connection.|
    |**Connection Alias**|The Connection &amp; Credential Alias you created in the previous steps.|
    |**Active**|Select this option.|


## Result

The connector appears on the **Established connections** sub-tab. AI Control Tower can now use this connection to apply AI agent containment using kill switch protocol to Vertex AI agents that have a unique agent identity configured.

To verify the setup:

-   Confirm the HTTP connection appears in the **Connections** related list on the Connection &amp; Credential Alias.
-   Confirm the OAuth 2.0 Credentials record can retrieve a token using **Get OAuth Token**.
-   Confirm the connector appears under **Established connections** on the Security tab.

To deploy the AI agent, see [Create and deploy an agent with Agent CLI and Agent Identity](https://docs.cloud.google.com/iam/docs/create-and-deploy-agent) in Google documentation.

**Parent Topic:**[Configuring security connections](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/aict-configuring-security-connections.md)

