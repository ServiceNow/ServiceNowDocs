---
title: Configure Docusign for external content indexing
description: Create an app and integration key in Docusign to allow the Docusign external content connector to access your source system.
locale: en-US
release: australia
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Docusign external content connector, Configure, External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Configure Docusign for external content indexing

Create an app and integration key in Docusign to allow the Docusign external content connector to access your source system.

## Before you begin

You need a Docusign account with the DS Admin permission profile. To learn more about permission profiles, see the [Permission Profiles﻿](https://support.docusign.com/s/document-item?bundleId=pik1583277475390&topicId=pof1583277362435.html) Docusign support resource.

**Important:** If you have multiple Docusign developer accounts \(such as a work account and a personal account\), you must set the account you want the external content connector to use as your default account. For details on setting a default Docusign account, see the [Set a Default Account](https://support.docusign.com/s/document-item?language=en_US&bundleId=jux1643235969954&topicId=fdo1578456463193.html&_LANG=enus) Docusign resource.

Role required: none

## About this task

The Docusign external content connector retrieves agreements from envelopes in your Docusign source system using the eSignature REST API.

To allow the connector to access your Docusign source system via the eSignature REST API, you must create an app with an integration key in Docusign and generate a secret key for it. Your connector admin can use this app's integration key and secret key to configure the Docusign external connector for proper connection to your source system.

## Procedure

1.  In Docusign, create a new app to allow access by the Docusign external content connector.

    1.  Navigate to [https://apps-d.docusign.com/admin](https://apps-d.docusign.com/admin) and log in with your DS Admin account credentials.

    2.  Navigate to **Integrations** &gt; **Apps and Keys**.

        The Apps and Keys screen appears.

    3.  Select **Add App and Integration Key**.

    4.  Enter a name for your integration, then select **Create App**.

2.  Record the integration key for your new Docusign app.

    1.  Navigate to the General Info section to find the integration key for your new Docusign app.

    2.  Copy the integration key GUID and record it in a secure location.

        **Important:** Your external content connector admin needs this integration key GUID when configuring the Docusign external content connector.

3.  Generate a secret key for your new Docusign app.

    1.  Navigate to the Authentication section and select **Add Secret Key**.

        Docusign generates a secret key for your new app.

    2.  Copy the secret key GUID and record it in a secure location.

        **Important:** Your external content connector admin needs this secret key GUID when configuring the Docusign external content connector.

4.  Specify the redirect URI for your new Docusign app.

    1.  Navigate to **Additional settings** and select **Add URI**.

    2.  Enter `https://<instance-name>.service-now.com/oauth_redirect.do` as the callback URI, replacing `<instance-name>` with your ServiceNow AI Platform instance name.

    3.  Save your new redirect URI by selecting outside the URI field.

    The new redirect URI appears.


## What to do next

Provide the following items to your connector admin:

-   The integration key for your Docusign app that you copied in step [2.b](configure-docusign-external-content-indexing.md#copy-integration-key-step).
-   The secret key for your Docusign app that you copied in step [3.b](configure-docusign-external-content-indexing.md#copy-secret-key-step).

Your connector admin needs these items to configure a Docusign external content connector to retrieve envelopes and security principals from your Docusign source system.

For details on creating and configuring a Docusign external content connector, see [Create a Docusign external content connector](create-ext-cont-connector-docusign.md).

**Parent Topic:**[Docusign external content connector](../concept/docusign-external-content-connector.md)

