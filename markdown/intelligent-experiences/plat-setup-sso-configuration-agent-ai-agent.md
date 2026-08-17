---
title: SSO configuration AI agent
description: This ServiceNow Otto for Setup AI agent guides administrators through secure Single Sign-On \(SSO\) setup for ServiceNow using SAML or OpenID Connect \(OIDC\). The agent collects and validates identity provider details, creates authentication configurations, and guides users through review, testing, and activation.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/plat-setup-sso-configuration-agent-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-08-14"
reading_time_minutes: 2
breadcrumb: [Setup Hub AI agents, ServiceNow AI Platform, Available AI agents on the ServiceNow AI Platform, AI assets, Enable AI experiences]
---

# SSO configuration AI agent

This ServiceNow Otto for Setup AI agent guides administrators through secure Single Sign-On \(SSO\) setup for ServiceNow using SAML or OpenID Connect \(OIDC\). The agent collects and validates identity provider details, creates authentication configurations, and guides users through review, testing, and activation.

## Workflow

1.  Check whether the SSO plugin is installed and whether an active SSO configuration already exists. If the plugin isn't installed, offer to install it and monitor progress before continuing.
2.  Identify whether the user wants SAML, OIDC, or generic SSO help; if unclear, ask them to choose. If an active configuration already exists, offer to deactivate it instead.
3.  For SAML: request the metadata URL. For OIDC: collect the configuration name, client ID, and well-known configuration URL \(client secret is handled separately, outside the conversation\).
4.  Create the SAML or OIDC Identity Provider record based on the provided information. Confirm success or display any errors for correction.
5.  Present a link to the newly created record and ask the user to review and correct any fields before continuing.
6.  Guide the user through testing the connection and confirm the test passed.
7.  Ask whether this should be the default login method and apply that setting if so.
8.  Explain ACR as a safety fallback and confirm whether it's been set up before proceeding.
9.  Ask for confirmation, then activate the configuration.
10. Depending on earlier default/active selections, mark the configuration as primary automatically or ask for confirmation.
11. Ask the user to test login redirection in a private browser.

<table><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Allow third party to access this AI agent

</td><td>

When enabled, third-party AI agents can use this agent. This value is off \(false\) by default. This setting is defined in the AI Agent configs \[sn\_aia\_agent\_config\] table on the External discoverable field.

</td></tr><tr><td>

Allow AI specialists to access this AI agent

</td><td>

When enabled, AI specialists can use this agent. This value is off \(false\) by default. When set to true, more configuration options for tools become available so that an AI specialist can map inputs and response templates to tool outputs. This setting is defined in the AI Agent configs \[sn\_aia\_agent\_config\] table on the Specialist enabled field.

</td></tr><tr><td>

Manage long-term memory

</td><td>

When enabled, all previous user interactions are used as context for the LLM. This value is off \(false\) by default. This setting is defined by the **sn\_aia.ltm.enable\_long\_term\_memory** system property. For more information, see [ServiceNow Otto AI agents reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/na-aia-reference.md).

</td></tr><tr><td>

Tools

</td><td>

-   **Scripts**

Activate SSO Configuration

Create Login Link For OIDC

Creation of OIDC using URL

Creation of SAML record using the metadata URL

Creation of SAML record using the metadata XML

Deactivate SSO Configuration

get activation status

Get Active SSO Configurations

Get SSO Setting Link

Install sso plugin

Set SSO identity provider as default

Update SSO Config To Primary

Update SSO Label

-   **Generative AI skills**

get knowledge

Plugin installation and existing configuration check

-   **Conversational topic**

IADynamicChoicePickerGenerator


</td></tr><tr><td>

Agent roles \(ACLs\)

</td><td>

sn\_ia\_config.ia\_user

</td></tr><tr><td>

Data access roles

</td><td>

Not defined.

</td></tr><tr><td>

Triggers

</td><td>

Optional. None defined by default. An admin can specify triggers if desired. For more information, see [Add a trigger to an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/add-trigger-aia.md).

</td></tr><tr><td>

Channels

</td><td>

Configure an assistant for Virtual Agent or ServiceNow Otto panel using [Assistant Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/configure-now-assist-va.md).

</td></tr><tr><td>

Used in agentic workflows

</td><td>

Default VA Workflow

</td></tr></tbody>
</table>Learn more about ServiceNow Otto for Setup at [ServiceNow Otto for Setup](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ia-landing.md).

**Parent Topic:**[Setup Hub AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/platform-setup-ai-agents-overview.md)

