---
title: Set up a connection and credential alias for a third-party embedding model
description: Set up a connection and credential alias to authenticate an integration between your ServiceNow instance and a third-party embedding model.
locale: en-US
release: yokohama
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configuring an external or custom embedding model, AI Search Retrieval Augmented Generation \(RAG\), Semantic index configuration for indexed sources, Indexed sources, Configure, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Set up a connection and credential alias for a third-party embedding model

Set up a connection and credential alias to authenticate an integration between your ServiceNow instance and a third-party embedding model.

## Before you begin

Role required: admin

## About this task

The system provides the default connection and credential alias for the Azure OpenAI Embedding model \(text-embedding-3-large\) and Google Gemini Embedding model \(gemini-embedding-001\). You set up these default aliases to manage the secure connection of your ServiceNow instance with either embedding model. A connection and credential alias includes the endpoint URL of the models and the login details, such as the OAuth token or API key. A connection and credential alias tells the system how to connect to these third-party models.

## Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Connection &amp; Credential Aliases**.

2.  Select an alias that you want to set up.

    -   To set up the embedding model alias for Azure OpenAI Embedding, select **Azure OpenAI**.
    -   To set up the embedding model alias for Google Gemini Embedding, select **Google Gemini API**.
3.  Create a connection record for your alias.

    1.  In the Connections related list, select **New**.

    2.  On the form, fill in the fields.

        For a description of the field values, see [Create an HTTP\(s\) connection](https://www.servicenow.com/docs/access?context=create-https-connection&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US).

    3.  Select **Submit**.

    The connection record is created.

4.  Create a credential record for your alias.

    1.  In the Connections related list, select a connection record from the connection alias list.

        -   Select the connection record that you created in step 3 for the Azure OpenAI alias.
        -   Select the connection record that you created in step 3 for the Google Gemini API alias.
    2.  In the Credentials field, select the search icon \(![Lookup using list.](../../../common/image/Banner_GlobalTextSearchIcon.png)\) and then select **New**.

    3.  From the list of credentials, select a credential type.

        -   To create a credential record for the Azure OpenAI alias, select **API Key Credentials**.
        -   To create a credential record for the Google Gemini API alias, select **OAuth 2.0 Credentials**.
    4.  On the form, fill in the fields.

        For a description of the field values, see [API key credentials](https://www.servicenow.com/docs/access?context=API-key-credential-form&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US) for the Azure OpenAI alias or [OAuth 2.0 credentials](https://www.servicenow.com/docs/access?context=oauth-2-credentials&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US) for the Google Gemini API alias.

    5.  Select **Submit**.

    6.  Select **Update**.

    The credential record is created.


## What to do next

Activate the embedding model to start using it. For more information, see [Activate a third-party embedding model](activate-3p-embedding-model.md).

**Parent Topic:**[Configuring an external or custom embedding model](../concept/setting-up-3p-embedding-models.md)

