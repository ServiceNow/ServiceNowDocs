---
title: Configure API credentials for Google Vertex AI
description: Configure your API credentials to use Google Vertex AI as your LLM provider for Generative AI Controller capabilities.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/generative-ai-controller/configure-api-credentials-for-google-vertex-ai.html
release: australia
product: Generative AI Controller
classification: generative-ai-controller
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring API credentials for generative AI capabilities, Configuring Generative AI Controller, Generative AI Controller, AI Admin Hub, Enable AI experiences]
---

# Configure API credentials for Google Vertex AI

Configure your API credentials to use Google Vertex AI as your LLM provider for Generative AI Controller capabilities.

## Before you begin

You must have a Google Cloud project and the permissions to generate new OAuth credentials.

Role required: admin

## About this task

To use Google Vertex AI as your LLM provider for Generative AI Controller capabilities, configure an active connection.

## Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Connections &amp; Credentials Aliases**.

2.  Open the record for Google Bard Vertex AI.

3.  Select the **Create New Connection &amp; Credential** related link.

    \[Omitted image "gai-create-new-connection-vertex.png"\] Alt text: Create New Connection &amp; Credential related link highlighted on the screen.

4.  Complete the required fields.

<table><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Project ID

</td><td>

The Project ID found in the Google Cloud console

</td></tr><tr><td>

Credential Name

</td><td>

The name of your credential, such as `Google OAuth Credential`

</td></tr><tr><td>

OAuth Name

</td><td>

The name of your OAuth authentication, such as `Google Registry`

</td></tr><tr><td>

OAuth Client ID

</td><td>

To get the OAuth Client ID, create a new OAuth Client ID with the Google Cloud console with the following attributes: 1.  Application type: `Web application`
2.  Authorized redirect URI: URL in the OAuth Redirect URL field, usually `<instance>.service-now.com/oauth_redirect.do`
 For more information, see the [Google documentation for creating OAuth client IDs](https://support.google.com/cloud/answer/6158849). After you create the OAuth client, a dialog box displays the Client ID and Client secret for you to copy.

</td></tr><tr><td>

OAuth Client Secret

</td><td>

Client secret from your OAuth Client ID found in the Google Cloud console

</td></tr></tbody>
</table>5.  In the dialog box, log in to a Google Account with access to the project.

6.  When prompted for Google Cloud access for gsuite spokes, select **Allow**.


## Result

You can now use Completions – Vertex AI and Chat Completions – Vertex AI as your LLM provider for Generative AI Controller capabilities.

\[Omitted image "gai-created-connection-vertex.png"\] Alt text: Complete connection for Google Bard Vertex AI.

## What to do next

Activate generative AI skills in the AI Admin Hub console for your workflow. For more information, see [AI Admin Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/platform-now-assist-landing.md).

