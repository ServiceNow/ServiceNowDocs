---
title: Create an AI connection for Veza access intelligence
description: Connect AI Control Tower to Veza using OAuth 2.0 so that agent risk scores and severity levels from Veza access intelligence appear in the agent map. Since Veza is an enrichment connector, it doesn't import new assets.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/aict-create-ai-connection-veza.html
release: brazil
topic_type: task
last_updated: "2026-09-08"
reading_time_minutes: 2
keywords: [ServiceNow Otto, AI Agents, generative AI, agentic AI]
breadcrumb: [Configuring connectors, Configuring integrations, Configure, AI Control Tower, Establishing AI governance, Enable AI Experiences]
---

# Create an AI connection for Veza access intelligence

Connect AI Control Tower to Veza using OAuth 2.0 so that agent risk scores and severity levels from Veza access intelligence appear in the agent map. Since Veza is an enrichment connector, it doesn't import new assets.

## Before you begin

Confirm the following are in place:

-   An OAuth 2.0 app or client configured in your Veza tenant. For more information, see [OAuth2 apps](https://docs.veza.com/4yItIzMvkpAvMVFAamTf/developers/api/authentication/oauth2-apps) and [OAuth2 clients](https://docs.veza.com/4yItIzMvkpAvMVFAamTf/developers/api/authentication/oauth2-clients) in Veza documentation.
-   An OAuth profile configured on the ServiceNow platform and linked to the pre-provided `SN AI Security Veza Connector` connection alias. For more information, see [Set up OAuth](https://www.servicenow.com/docs/r/platform-security/authentication/t_SettingUpOAuth.html).

Role required: sn\_ai\_governance.ai\_steward

## About this task

The Veza connector authenticates using OAuth 2.0 only. Create the AI connection after you complete OAuth setup on both the Veza tenant and the ServiceNow platform.

## Procedure

1.  Navigate to **Settings** &gt; **Integrations** &gt; **Connectors**.

2.  On the **Available connectors** tab, select the **Veza** tile from security connectors.

3.  On the **Configure connector** page, confirm that **Provider type** is set to **Security**.

    The **Connection alias** field is pre-populated with `SN AI Security Veza Connector` and can't be edited.

4.  Select the **I have configured the Veza user integration** check box.

    This confirms you completed the Veza-side OAuth setup. See [Configure OAuth in Veza](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/gov-sec-configure-veza-oauth.md).

5.  Select the **I have configured ServiceNow connectors/alias settings** check box.

    This confirms you completed the ServiceNow-side OAuth setup. See [Configure OAuth for Veza in ServiceNow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/gov-sec-configure-veza-servicenow.md).

    The **Validate Connection** button is disabled until both check boxes are selected.

6.  Select **Validate Connection**.

    If the connection already has a valid OAuth token, a `Connection Valid` message appears. If it doesn't, the button instead shows **Authenticate Connection**.

    -   If the button shows **Validate Connection**, continue to the next step.
    -   If the button shows **Authenticate Connection**, select it to log in to Veza. After you log in and allow access, the connection revalidates.
7.  Select **Save**.


## Result

The connection appears on the **Established connections** tab. Selecting **Re-Validate** from that tab updates the connection status.

**Parent Topic:**[Configuring connectors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/aict-configuring-connectors.md)

