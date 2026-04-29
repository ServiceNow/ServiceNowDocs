---
title: Connect Figma MCP server to Build Agent
description: Connect the Figma MCP server to the Build Agent to accelerate the conversion of Figma designs into enterprise-grade applications on the ServiceNow AI Platform.Create an OAuth application in Figma to enable the Figma MCP server to authenticate users via OAuth and grant the Build Agent access to Figma designs.Set up an OAuth application registry and credentials to enable the ServiceNow IDE to connect to your Figma.Connect the Figma MCP \(Model Context Protocol\) server to the Build Agent to make the Figma designs accessible for application creation.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-04-29"
reading_time_minutes: 8
breadcrumb: [Configure, Build Agent, Vibe coding and AI app development on the ServiceNow AI Platform, Building applications]
---

# Connect Figma MCP server to Build Agent

Connect the Figma MCP server to the Build Agent to accelerate the conversion of Figma designs into enterprise-grade applications on the ServiceNow AI Platform.

## Before you begin

Role required: admin

## About this task

Connecting the Figma MCP \(Model Context Protocol\) server to the Build Agent enables the Build Agent to access design data from Figma files. This connection helps the Build Agent understand the design and its intent, enabling it to create applications that match the design.

Visit the Figma Developer Portal to connect the Figma MCP server to the Build Agent. Create an OAuth app to obtain your Client ID and Client Secret. Then, configure the ServiceNow IDE to handle the OAuth process using the credentials.

For more information on Build Agent and the Figma MCP server, see [Application development with Figma MCP server](../concept/accelerate-design-to-development-with-figma-mcp-server.md).

## Procedure

1.  [Configure an OAuth app in Figma](connect-figma-mcp-server-to-build-agent.md#)

2.  [Configure OAuth provider in ServiceNow IDE](connect-figma-mcp-server-to-build-agent.md#)

3.  [Connect Figma MCP server to Build Agent](connect-figma-mcp-server-to-build-agent.md#)

    ![A process flow diagram showing the integration from Figma through OAuth authentication, connecting to the Figma MCP server, then the Build Agent, and finally resulting in application generation](../image/build-agent-process-flow.png "Application generation workflow using Figma and Build Agent")


**Parent Topic:**[Configure Build Agent](configure-build-agent.md)

## Configure an OAuth app in Figma

Create an OAuth application in Figma to enable the Figma MCP server to authenticate users via OAuth and grant the Build Agent access to Figma designs.

### Before you begin

You must have a Dev or Full seat on a Figma Pro, Org, or Enterprise plan.

Role required: admin

### About this task

The Figma MCP \(Model Context Protocol\) server uses OAuth for authentication and makes the Figma design data accessible to the Build Agent installed. To connect the Figma MCP server with the Build Agent, you must create an OAuth app in Figma. This process generates a Client ID and Client Secret. ServiceNow uses these credentials to initiate the OAuth process and authenticate users with their Figma accounts.

### Procedure

1.  Step 1: Create an OAuth application in Figma to obtain the Client ID and Client Secret.
2.  Go to the [Figma Developers Page](https://www.figma.com/login?cont=/developers/apps).

3.  Select **Create a new app**.

4.  Enter the following information in the form.

<table id="choicetable_pbb_nhf_dhc"><thead><tr><th align="left" id="d68784e254">

Field

</th><th align="left" id="d68784e257">

Description

</th></tr></thead><tbody><tr><td id="d68784e263">

**Name**

</td><td>

Name for your application; for example, ServiceNow Integration.

</td></tr><tr><td id="d68784e272">

**Choose an owner for your app**

</td><td>

Team or organization that must own the app.

 **Important:** The value that you enter can’t be modified.

</td></tr></tbody>
</table>5.  Select **Create app**.

    A Client ID and Client Secret are generated.

6.  Store the Client ID and Client Secret securely, as you’ll need them for the OAuth setup in the ServiceNow IDE.

    **Important:**

    You won't be able to see the Client Secret again after closing this window.

7.  Select **Done**.

8.  Step 2: Configure and publish the OAuth App in Figma.
9.  Open the application that you created.

10. In the **General** tab, upload a logo for your app and provide a brief description.

11. In the **OAuth credentials** tab, in the **Redirect URLs** field, add the following URL: `https://<instance name>.service-now.com/oauth_redirect.do`. and then replace *&lt;instance name&gt;* with actual ServiceNow instance name.

    The OAuth flow only works in ServiceNow instances that are included in the list of Redirect URLs. Make sure that you add all instances where you want the OAuth flow to function to this list.

    You can add a redirect URL at any time.

12. In the OAuth scopes tab, under the MCP section, select the **mcp:connect** check box.

    **Important:** If the MCP section isn't visible, reach out to your ServiceNow account manager or ServiceNow Support \([Contact ServiceNow Support](https://support.servicenow.com/now?draw=case)\) to enable the MCP connect scope. Make sure to share your Client ID with them so they can enable the MCP feature.

13. In the **Publish** tab, make sure the **Private** check box is selected, and then select **Publish**.


## Configure OAuth provider in ServiceNow IDE

Set up an OAuth application registry and credentials to enable the ServiceNow IDE to connect to your Figma.

### Before you begin

Role required: admin

### Procedure

1.  Step 1: Create an Application Registry record.
2.  In your ServiceNow instance, navigate to **System OAuth** &gt; **Application Registry**.

3.  Select **New**.

4.  On the interceptor page, select **Connect to a third-party OAuth Provider**.

5.  Fill out the form with the following details.

    |Field|Description|
    |-----|-----------|
    |**Name**|A unique name; for example, Figma OAuth Provider.|
    |**Client ID**|Client ID that you obtained from the Figma app.|
    |**Client Secret**|Client secret that you obtained from the Figma app.|
    |**Default Grant Type**|Select **Authorization Code** from the drop-down list.|
    |**Authorization URL**|`https://www.figma.com/oauth`.|
    |**Token URL**|`https://api.figma.com/v1/oauth/token`.|
    |**Redirect URL**|The redirect URL that you added in the Figma app.|
    |**Send Credentials**|Select **As Basic Authorization Header**.|

6.  Select **Submit**.

7.  Step 2: Define the OAuth scope.
8.  On the Application Registry record you saved, scroll down to the related lists.

9.  Select the **OAuth Entity Scopes** tab.

10. Double-click \(or use the keyboard shortcut\) **Insert a new row** to add a new row.

11. In the new row, enter the following values.

    |Field|Description|
    |-----|-----------|
    |**Name**|A name; for example, Figma MCP Connect.|
    |**OAuth scope**|Exact scope name that you defined in Figma \(mcp:connect\).|

12. Select **Update**.

    ![The configuration tab for OAuth entity scopes shows the "Name" and "OAuth Scope" fields, an example "Figma MCP Connect: mcp:connect," and options to add, update, or delete scopes.](../image/build-agent-mcp-oauth-entity-scope.png)

13. Step 3: Configure the OAuth entity profile.
14. On the same Application Registry record, select the **OAuth Entity Profiles** tab.

    ![In the OAuth Entity Profiles tab, existing profiles like the "Figma OAuth Provider" with the Authorization Code grant type are shown, along with options to update, delete, or add profiles.](../image/build-agent-mcp-oauth-entity-profiles.png)

    You see an automatically created default profile.

15. Select the profile name to open the record.

16. Rename the default profile to `figma_profile`.

17. On the OAuth Entity Profile record, under the **OAuth Entity Profile Scopes** related list, double-click \(or use the keyboard shortcut\) **Insert a new row**.

18. Search for **Figma MCP Connect** and select it.

    ![On the configuration page for the Figma OAuth Provider profile, the OAuth entity scope "Figma" connects with the "Figma OAuth Provider default_profile" through the Authorization Code grant type.](../image/build-agent-mcp-figma-mcp-connect.png)

19. Select **Save**.

    You’re redirected back to the profile record.

20. Select **Update** to save the profile.

    The default profile is connected to the MCP scope.


## Connect Figma MCP server to Build Agent

Connect the Figma MCP \(Model Context Protocol\) server to the Build Agent to make the Figma designs accessible for application creation.

### Before you begin

Role required: admin

### About this task

With the OAuth connection set up between your ServiceNow instance and Figma, you can now link Build Agent to your Figma account to begin using the Figma MCP Server. The Build Agent within the ServiceNow IDE enables you to automatically create and update ServiceNow applications.

### Procedure

1.  Make sure the OAuth app is configured on Figma and that you have created the application registry.

    **Tip:** On the ServiceNow IDE, go to **All** &gt; **System OAuth** &gt; **Application Registry** to verify if the OAuth app is created and configured on Figma.

    For configuration steps, see [Configure an OAuth app in Figma](connect-figma-mcp-server-to-build-agent.md#) and [Configure OAuth provider in ServiceNow IDE](connect-figma-mcp-server-to-build-agent.md#).

2.  Enable the Figma MCP server on ServiceNow IDE:

    1.  On ServiceNow IDE, select the gear icon ![Gear icon](../../../reuse/icons/product-icons/gear-outline-24.svg) at the bottom-left corner and then select **Settings**.

    2.  Search for Build Agent.

        All the Build Agent settings are listed.

    3.  Enable the Figma MCP server by selecting the **Build-agent: Enable Mcp Servers** check box.

3.  Open the Build Agent chat panel.

4.  Locate the MCP icon ![MCP icon](../image/build-agent-mcp-icon.png) at the top-right of the chat panel and select it to open the MCP server page.

5.  Select **Connect** to trigger the OAuth authentication flow that you configured.

    You’re prompted to log in to Figma and authorize your ServiceNow application.

6.  After you approve the ServiceNow connection request, go back to the Build Agent chat panel.

    The status of Figma MCP Server is green, indicating that it’s connected to Figma, and all available tools are listed. The generated token is saved in the Ide Git Credential table on the ServiceNow IDE.


### Result

You can now interact with the Figma MCP server using natural language through the Build Agent.

For example, you can use prompts such as: "Create a UI page and build &lt;figma link&gt;." The Build Agent retrieves the design context from Figma and creates an application that matches the design.

**Important:** The extent to which the application aligns with the original design is largely influenced by the complexity and the overall structure of the design. When the design is straightforward and uncomplicated, the application tends to closely mirror the intended design. Conversely, if the design is intricate or multifaceted, the application may diverge more significantly from the original design.

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

The MCP server may sometimes be inactive, and you might encounter an unauthorized access error. The issue occurs when Figma rejects the token created after completing the OAuth flow.

</td><td>

Perform the following the steps to fix the issue:

1.  Navigate to the **Ide Git Credential** table in the ServiceNow IDE and find the relevant token. In the Active column, switch the value from `true` to `false` for that token.
2.  Go back to the Build Agent chat panel.
3.  Locate the MCP icon ![MCP icon](../image/build-agent-mcp-icon.png) at the top-right of the chat panel and select it to open the MCP server page.
4.  Select **Connect** to trigger the OAuth authentication flow.

</td></tr></tbody>
</table>