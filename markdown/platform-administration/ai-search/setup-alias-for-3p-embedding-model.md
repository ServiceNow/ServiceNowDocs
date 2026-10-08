---
title: Set up connection and credential alias for third-party embedding model
description: Set up connection and credential record for your aliases to authenticate an integration between your ServiceNow instance and third-party embedding model.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/platform-administration/ai-search/setup-alias-for-3p-embedding-model.html
release: australia
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Configuring an external or custom embedding model, Semantic index configuration for indexed sources, Indexed sources, Configure, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Set up connection and credential alias for third-party embedding model

Set up connection and credential record for your aliases to authenticate an integration between your ServiceNow instance and third-party embedding model.

## Before you begin

Role required: admin

## About this task

The system provides the default connection and credential alias for Azure OpenAI Embedding model \(text-embedding-3-large\) and Gemini Text Embedding model \(text-embedding-004\). Set up these default aliases to manage the secure connection of your ServiceNow instance with either of the embedding model. A connection and credential alias includes the endpoint URL of the models and the login details, such as OAuth token or API keys to tell the system how to connect to these third-party models.

## Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Connection &amp; Credential Aliases**.

2.  Select an alias that you want to set up.

    -   To set up the embedding model alias for Azure OpenAI Embedding, select **Azure OpenAI**.
    -   To set up the embedding model alias for Google Gemini Text Embedding, select **Google Gemini API**.
3.  Create a connection record for your alias.

<table id="choicetable_hql_2zg_1gc"><thead><tr><th align="left" id="d309529e107">

Option

</th><th align="left" id="d309529e110">

Procedure

</th></tr></thead><tbody><tr><td id="d309529e116">

**Update the existing connection record**

</td><td>

1.  In the Connections related list, select a connection from the connection alias list.
    -   Select **Azure OpenAI Connection** for the Azure OpenAI alias.
    -   Select **Google gemini API connection** for the Google gemini API alias.
2.  Update the **Name** and **Connection URL** fields based on your requirement.
3.  Select **Update**.


</td></tr><tr><td id="d309529e163">

**Create a new connection record**

</td><td>

1.  In the Connections related list, click **New**.
2.  On the form, fill in the fields.

For a description of the field values, see [Create an HTTP\(s\) connection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/create-https-connection.md).

3.  Select **Submit**.


</td></tr></tbody>
</table>    The connection record is created.

4.  Create a credential record for your alias.

<table id="choicetable_xp4_ykh_1gc"><thead><tr><th align="left" id="d309529e208">

Option

</th><th align="left" id="d309529e211">

Procedure

</th></tr></thead><tbody><tr><td id="d309529e217">

**Update the existing credential record**

</td><td>

1.  In the Connections related list, select a connection record from the connection alias list.
    -   Select **Azure OpenAI Connection** for the Azure OpenAI alias.
    -   Select **Google gemini API connection** for the Google gemini API alias.
2.  In the Credentials field, select the Preview this record icon and then select **Open Record**.

The API Key Credentials record opens.

3.  Update the **API Key** field.
4.  Select **Update**.
5.  Select **Update**.


</td></tr><tr><td id="d309529e275">

**Create a new credential record**

</td><td>

1.  In the Connections related list, select a connection record from the connection alias list.
    -   Select **Azure OpenAI Connection** for the Azure OpenAI alias.
    -   Select **Google gemini API connection** for the Google gemini API alias.
2.  In the Credentials field, select the search icon and then select **New**.
3.  From the list of credentials, select a credential type.
    -   To create a credential record for Azure OpenAI alias, select **API Key Credentials**.
    -   To create a credential record for Google Gemini API alias, select **OAuth 2.0 Credentials**.
4.  On the form, fill in the fields.

For a description of the field values, see [API key credentials](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/API-key-credential-form.md) or [OAuth 2.0 credentials](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/oauth-2-credentials.md).

5.  Select **Submit**.
6.  Select **Update**.


</td></tr></tbody>
</table>    The credential record is created.


## What to do next

Activate the embedding model to start using it. For more information, see [Activate the third-party embedding model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-administration/ai-search/activate-3p-embedding-model.md).

