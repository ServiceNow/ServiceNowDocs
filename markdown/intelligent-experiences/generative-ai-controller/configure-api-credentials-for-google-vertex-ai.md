---
title: Create API credentials for Google Vertex AI
description: Configure your API credentials to use Google Vertex AI in custom workflows and Virtual Agent Designer topics.
locale: en-US
release: zurich
product: Generative AI Controller
classification: generative-ai-controller
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configuring API credentials for generative AI capabilities, Configuring Generative AI Controller, Generative AI Controller, Now Assist, Enable AI experiences]
---

# Create API credentials for Google Vertex AI

Configure your API credentials to use Google Vertex AI in custom workflows and Virtual Agent Designer topics.

## Before you begin

You must have a Google Cloud project and the permissions to generate new OAuth credentials.

Role required: admin

## About this task

In order to use Google Vertex AI as your LLM provider for Generative AI Controller capabilities, you must have an active connection configured.

## Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Connections &amp; Credentials Aliases**.

2.  Open the record for Google Bard Vertex AI.

3.  Select the **Create New Connection &amp; Credential** related link.

4.  Fill in the required fields.

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

To get the OAuth Client ID, create OAuth Client ID with the Google Cloud console with the following attributes: 1.  Application type: `Web application`
2.  Authorized redirect URI: URL in the OAuth Redirect URL field, usually `<instance>.service-now.com/oauth_redirect.do`
 For more information, see the [Google documentation for creating OAuth client IDs](https://support.google.com/cloud/answer/6158849). Once you have created the OAuth client, a pop-up window will have the Client ID and Client secret for you to copy into your clipboard.

</td></tr><tr><td>

OAuth Client Secret

</td><td>

Client secret from your OAuth Client ID found in the Google Cloud console

</td></tr></tbody>
</table>5.  In the pop-up window, log in to a Google Account with access to the project.

6.  When prompted for Google Cloud access for gsuite spokes, select **Allow**.


## Result

You can now use Completions – Vertex AI and Chat Completions – Vertex AI in Flow Designer, Virtual Agent Designer, and scripts to create custom experiences with generative AI.

