---
title: ServiceNow\(Glide\) configuration for IDP
description: This process involves setting up the necessary tables and mappings within your ServiceNow instance. This includes configuring ServiceNow, creating the MCP server, and connecting the MCP client.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/servicenow-configuration-for-idp.html
release: australia
topic_type: task
last_updated: "2026-06-19"
reading_time_minutes: 1
keywords: [Glide configuration for IDP]
breadcrumb: [Integrating MCP server with third-party identity providers, Connect, MCP Server Console, Enable AI experiences]
---

# ServiceNow\(Glide\) configuration for IDP

This process involves setting up the necessary tables and mappings within your ServiceNow instance. This includes configuring ServiceNow, creating the MCP server, and connecting the MCP client.

## Before you begin

Role required: admin

## Procedure

1.  Configure the OIDC provider

    **Note:** Okta is used as the use case to guide you through the steps.

    \[Omitted image "mcp-configure-oidc.png"\] Alt text: Configure OIDC provider

2.  Navigate to the **oidc\_provider\_configuration** table and select **New**.

3.  Enter a **Name** for the OIDC provider.

    For example, `Okta MCP Third Party`.

4.  Set the **Cache Configuration Lifespan**.

    The maximum value is 720 hours.

5.  Enter the IDP metadata URL into the **Metadata URL** field.

6.  In the **User Claim** section, enter `sub`, and in the **User Field**, select **email**.

    This maps the `sub` claim from the IDP token to the `email` field in the `sys_user` table.

7.  Select **Submit**.

8.  Create the MCP server
9.  Navigate to the MCP server console and select **Create Server**.

10. Enter a name for the server and add the required tools.

    For example, `MCP with Third Party IDP`.

    After you create the server, ServiceNow automatically generates an entry in the **oauth\_protected\_resource** table and populates it with the list of APIs allowed for that server.

11. Map the protected resource to the IDP

    \[Omitted image "mcp-oath-idp-mapping.png"\] Alt text: Map protected resource to the IDP

12. Navigate to the **oauth\_protected\_resource\_idp\_mapping** table and select **New**.

13. In the **Protected Resource** field, select the resource that was created for your MCP server.

    If your MCP server name is `sn_mcp_server_default`, the protected resource path is `/sncapps/mcp-server/mcp/sn_mcp_server_default`.

14. In the **OIDC Provider** field, select the OIDC provider configuration you created earlier.

15. Select **Submit**.


## Result

Your MCP server is now configured to authenticate users through the third-party IDP. Users who connect an MCP client to this server are redirected to the related IDP to authenticate.

## What to do next

1.  Configure and set up the third-party IDP. This part involves setting up the application and authorization server within the third-party IDP setup. See [https://support.servicenow.com/kb?id=kb\_article\_view&amp;sysparm\_article=KB3095516](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3095516) to read more. This document uses Okta as the use case, however, Microsoft Entra is also recommended.
2.  Integrate and test.

**Parent Topic:**[Integrating MCP server with third-party identity providers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/integrating-mcp-server-with-third-party-identity-providers.md)

