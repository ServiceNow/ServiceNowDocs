---
title: Connect Build Agent to a Figma MCP server
description: Connect the Figma Model Context Protocol Server Console \(MCP\) server to Build Agent to convert Figma designs into enterprise-grade applications on the ServiceNow AI Platform.Create an OAuth application in Figma to enable the Figma MCP server to authenticate users via OAuth and grant Build Agent access to Figma designs.Set up an OAuth application registry and credentials to enable Build Agent in ServiceNow Studio or the ServiceNow IDE to connect to your Figma MCP server.Connect the Figma Model Context Protocol \(MCP\) server to Build Agent in ServiceNow Studio to make Figma designs accessible for application creation.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/application-development/building-applications/connect-figma-mcp-server-to-build-agent.html
release: zurich
product: Building Applications
classification: building-applications
topic_type: task
last_updated: "2026-06-22"
reading_time_minutes: 8
keywords: [Now Assist, AI Agents, generative AI, agentic AI, Now Assist, AI Agents, generative AI, agentic AI, Now Assist, AI Agents, generative AI, agentic AI, Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Configure, Build Agent, Agentic development on the ServiceNow AI Platform, Developing your application, Building applications]
---

# Connect Build Agent to a Figma MCP server

Connect the Figma Model Context Protocol Server Console \(MCP\) server to Build Agent to convert Figma designs into enterprise-grade applications on the ServiceNow AI Platform.

## Before you begin

Role required: admin

## About this task

Connecting the Figma MCP server to Build Agent enables Build Agent to access design data from Figma files. The connection helps Build Agent interpret the design intent and create applications that match the design.

Visit the Figma Developer Portal to connect the Figma MCP server to Build Agent. Create an OAuth app to obtain your Client ID and Client Secret. Then, configure ServiceNow Studio or the ServiceNow IDE to handle the OAuth process using the credentials.

-   For more information on Build Agent and the Figma MCP server, see [MCP connections and Build Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/building-applications/accelerate-design-to-development-with-figma-mcp-server.md).
-   For details on connecting to other supported MCP servers, see [Connect Build Agent to a supported MCP server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/building-applications/ba-connct-mcp-server.md).

## Procedure

1.  [Configure an OAuth app in Figma](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/building-applications/connect-figma-mcp-server-to-build-agent.md)

2.  [Configure OAuth provider in ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/building-applications/connect-figma-mcp-server-to-build-agent.md)

3.  [Connect Figma MCP server to Build Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/building-applications/connect-figma-mcp-server-to-build-agent.md)

    \[Omitted image "build-agent-process-flow.png"\] Alt text: Flowchart showing the build agent process from Figma to application generation. For detailed process steps, refer to the surrounding text.


**Parent Topic:**[Configure Build Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/building-applications/configure-build-agent.md)

## Configure an OAuth app in Figma

Create an OAuth application in Figma to enable the Figma MCP server to authenticate users via OAuth and grant Build Agent access to Figma designs.

### Before you begin

You must have a Dev or Full seat on a Figma Pro, Org, or Enterprise plan.

Role required: admin

### About this task

The Figma MCP \(Model Context Protocol\) server uses OAuth for authentication and makes the Figma design data accessible to Build Agent after installation. To connect the Figma MCP server with Build Agent, you must create an OAuth app in Figma, which generates a Client ID and Client Secret. The ServiceNow AI Platform uses those credentials to initiate the OAuth process and authenticate users with their Figma accounts.

### Procedure

1.  Create an OAuth application in Figma to obtain the Client ID and Client Secret.

    1.  Go to the [Figma Developers Page](https://www.figma.com/login?cont=/developers/apps).

    2.  Select **Create a new app**.

    3.  Enter the following information in the form.

<table id="table_mmh_1l3_ljc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name for your application; for example, `ServiceNow Integration`.

</td></tr><tr><td>

Choose an owner for your app

</td><td>

Team or organization that owns the app.

 **Note:** The value that you enter is permanent, and can't be changed.

</td></tr></tbody>
</table>    4.  Select **Create app**.

        Figma generates a Client ID and Client Secret.

    5.  Store the Client ID and Client Secret securely, because you need them for the OAuth setup in the ServiceNow AI Platform.

        **Note:** The Client Secret is not displayed again after you close this window.

    6.  Select **Done**.

2.  Configure and publish the OAuth App in Figma.

    1.  Open the application that you created.

    2.  In the **General** tab, upload a logo for your app and provide a description.

    3.  Add the following URL to the **Redirect URLs** field in the **OAuth credentials** tab: `https://<instance name>.service-now.com/oauth_redirect.do`, replacing *&lt;instance name&gt;* with the actual ServiceNow instance name.

        The OAuth flow works only in ServiceNow instances that are included in the list of Redirect URLs. Add all instances where you want the OAuth flow to function to this list.

        You can add a redirect URL at any time.

    4.  Select the **mcp:connect** check box in the **OAuth scopes** tab, under the MCP section.

        **Note:** If the MCP section isn't visible, contact your ServiceNow account manager or ServiceNow Support \([Contact ServiceNow Support](https://support.servicenow.com/now?draw=case)\) to enable the MCP connect scope. Share your Client ID with them so they can enable the MCP feature.

    5.  Confirm that the **Private** check box is selected in the **Publish** tab.

    6.  Select **Publish**.


## Configure OAuth provider in ServiceNow Studio

Set up an OAuth application registry and credentials to enable Build Agent in ServiceNow Studio or the ServiceNow IDE to connect to your Figma MCP server.

### Before you begin

Role required: admin

### Procedure

1.  Create an Application Registry record.

    1.  Navigate to **System OAuth** &gt; **Application Registry**.

    2.  Select **New**.

    3.  Select **Connect to a third-party OAuth Provider** on the interceptor page.

    4.  On the form, fill in the following fields.

        |Field|Description|
        |-----|-----------|
        |Name|Unique name. For example, Figma OAuth Provider.|
        |Client ID|Client ID that you obtained from the Figma app.|
        |Client Secret|Client secret that you obtained from the Figma app.|
        |Default Grant Type|Grant type for the OAuth flow. Set to **Authorization Code**.|
        |Authorization URL|`https://www.figma.com/oauth`|
        |Token URL|`https://api.figma.com/v1/oauth/token`|
        |Redirect URL|Redirect URL that you added in the Figma app.|
        |Send Credentials|Method for sending credentials. Set to **As Basic Authorization Header**.|

    5.  Select **Submit**.

2.  Define the OAuth scope.

    1.  Navigate to the related lists on the Application Registry record.

    2.  Select the **OAuth Entity Scopes** tab.

    3.  Select **Insert a new row** to add a row to the OAuth Entity Scopes list.

    4.  Enter the following values in the new row.

        |Field|Description|
        |-----|-----------|
        |Name|A name; for example, Figma MCP Connect.|
        |OAuth scope|Exact scope name that you defined in Figma \(mcp:connect\).|

    5.  Select **Update**.

        \[Omitted image "build-agent-mcp-oauth-entity-scope.png"\] Alt text: Configuration tab for OAuth entity scopes shows the "Name" and "OAuth Scope" fields, an example "Figma MCP Connect: mcp:connect," and options to add, update, or delete scopes.

3.  Configure the OAuth entity profile.

    1.  Select the **OAuth Entity Profiles** tab on the same Application Registry record.

        \[Omitted image "build-agent-mcp-oauth-entity-profiles.png"\] Alt text: OAuth Entity Profiles tab showing a default profile entry with Authorization Code grant type, and options to update or delete.

    2.  Select the profile name to open the record.

    3.  Rename the default profile to `figma_profile`.

    4.  Select **Insert a new row** under the OAuth Entity Profile Scopes related list.

        The option appears under the OAuth Entity Profile Scopes related list.

    5.  Search for **Figma MCP Connect** and select it.

        \[Omitted image "build-agent-mcp-figma-mcp-connect.png"\] Alt text: OAuth Entity Profile form with the OAuth Entity Scope field showing a search for "Figma" and the result "Figma MCP Connect."

    6.  Select **Save**.

    7.  Save the profile by selecting **Update**.


### Result

The default profile is connected to the MCP scope.

## Connect Figma MCP server to Build Agent

Connect the Figma Model Context Protocol \(MCP\) server to Build Agent in ServiceNow Studio to make Figma designs accessible for application creation.

### Before you begin

Navigate to **All** &gt; **System OAuth** &gt; **Application Registry** to verify that the OAuth app is created and configured on Figma. For configuration steps, see [Configure an OAuth app in Figma](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/building-applications/connect-figma-mcp-server-to-build-agent.md) and [Configure OAuth provider in ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/building-applications/connect-figma-mcp-server-to-build-agent.md).

Role required: admin

### About this task

After the OAuth connection is set up between your ServiceNow instance and Figma, you can link Build Agent to your Figma account to begin using the Figma MCP Server.

### Procedure

1.  Enable the Figma MCP server on ServiceNow IDE.

    **Note:** This step is only for the ServiceNow IDE, not ServiceNow Studio.

    1.  Select the gear icon \[Omitted image "gear-outline-24.svg"\] Alt text: in ServiceNow IDE, and then select **Settings**.

    2.  Search for Build Agent.

    3.  Enable the Figma MCP server by selecting the **Build-agent: Enable MCP Servers** check box.

2.  Open the Build Agent chat panel in either ServiceNow Studio or the ServiceNow IDE.

3.  Select the MCP icon \[Omitted image "build-agent-mcp-icon.png"\] Alt text: in the chat panel.

4.  Trigger the OAuth authentication flow by selecting **Connect** for the Figma option.

5.  Authorize your ServiceNow application by logging in to Figma.

6.  Approve the ServiceNow connection request.

    The status of Figma MCP Server indicates that it's connected to Figma, and all available tools are listed. The generated token is saved in the IDE Git Credential table on the ServiceNow IDE.


### Result

You can interact with the Figma MCP server using natural language through Build Agent.

For example, enter a prompt like `Create a UI page and build <figma link>`. Build Agent retrieves the design context from Figma and creates an application that matches the design.

**Note:** The extent to which the application aligns with the original design is largely influenced by the complexity and the overall structure of the design. When the design is uncomplicated, the application is close to the intended design. Conversely, if the design is intricate, the application may diverge more significantly from the original design.

To better organize your Figma files, refer to [Structure your Figma file for better coding](https://developers.figma.com/docs/figma-mcp-server/structure-figma-file/) and [Write effective prompts to guide the AI](https://developers.figma.com/docs/figma-mcp-server/write-effective-prompts/).

<table id="table_bcg_rrm_dhc"><thead><tr><th>

Issue

</th><th>

Description

</th><th>

Solution

</th></tr></thead><tbody><tr><td>

Unauthorized access error

</td><td>

The MCP server can become inactive, resulting in an unauthorized access error when Figma rejects the token created after completing the OAuth flow.

</td><td>

1.  Navigate to the IDE Git Credential table in the ServiceNow IDE.
2.  Find the relevant token.
3.  Switch the value of the **Active** column from `true` to `false` for the token.
4.  Return to the Build Agent chat panel.
5.  Select the MCP icon \[Omitted image "build-agent-mcp-icon.png"\] Alt text: in the chat panel.
6.  Select **Connect** to trigger the OAuth authentication flow.

</td></tr></tbody>
</table>