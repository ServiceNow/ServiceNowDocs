---
title: Example: Automate badge request management using AI Desktop Actions
description: Automate various tasks related to badge requests through desktop actions using AI Desktop Actions and AI agents.Automate various badge-related tasks through desktop actions in AI Desktop Actions.Create an AI agent in AI Agent Studio and add desktop action tools for automating badge-related requests.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-11-21"
reading_time_minutes: 9
breadcrumb: [Desktop action examples, AI Desktop Actions, Enable AI experiences]
---

# Example: Automate badge request management using AI Desktop Actions

Automate various tasks related to badge requests through desktop actions using AI Desktop Actions and AI agents.

Your HR representatives manage repetitive badge-related tasks. For example, issuing new badges, distributing temporary badges, replacing lost badges, and disabling badges during offboarding. To streamline and automate this work, you can create a desktop action for each task and assign these actions to an AI Agent in AI Agent Studio.

When new requests come in, HR representatives can trigger the AI agent from the Now Assist panel. The AI Agent automatically selects and runs the appropriate desktop action. This automation reduces manual effort and enables them to focus on higher-value work.

## Create badge desktop action in AI Desktop Actions

Automate various badge-related tasks through desktop actions in AI Desktop Actions.

### Before you begin

To access the AI Desktop Actions functionality, perform the following steps:

-   Enable AI Desktop Actions on your ServiceNow instance. For more information, see [Configure AI Desktop Actions](../task/configure-agentic-desktop.md).
-   Download the AI Desktop Actions installer to automate repetitive tasks across applications and systems. For more information, see [Download AI Desktop Actions installer](../task/download-agentic-desktop-installer.md).

Confirm that the following system requirements are met:

-   Windows 11 operating system is used.
-   A .NET 9.0 runtime v9.0.10 and .NET 9 Desktop Runtime v9.0.10 is installed.
-   No extended monitors are connected.
-   Theme must match between the systems used for recording and execution.

Familiarize yourself with the Design workspace and Action recorder. For more information, see [AI Desktop Actions Design workspace](agentic-desktop-overview.md) and [Action recorder in AI Desktop Actions](action-recorder-ad.md).

Role required: sn\_aia.admin

### Procedure

1.  From your Windows system, launch the AI Desktop Actions application.

2.  On the login page, in the **Add ServiceNow URL** field, enter the ServiceNow instance URL.

    For example, `https://<instance name>.service-now.com`.

    ![AI Desktop Actions login screen for entering ServiceNow instance URL.](../image/ad-login-screen.png)

3.  Select **Proceed**.

4.  Log in to your ServiceNow account by entering your user name and password.

    Your account must have the sn\_aia.admin role.

    ![Login window for entering your ServiceNow account username and password.](../image/ad-login-screen-cred.png)

5.  On the AI Desktop Actions home page, select **Create desktop action**.

    ![AI Desktop Actions home page displaying the Create desktop action UI action, search and select options, and cards of existing desktop actions.](../image/home-page-actions-ad.png)

6.  In the New desktop action dialog box, select **Auto-capture steps \(recommended\)**.

    ![New desktop action window with auto-capture option selected and fields to enter name and description for the desktop action.](../image/new-desktop-action-window-ad.png)

7.  In the **Name** field, enter `Create new badge`.

8.  In the **Description** field, enter `Desktop action for issuing a badge to a new employee.`

9.  Select **Start capturing**.

    The AI Desktop Actions window is minimized and the Action recorder panel is launched. You can freely drag and reposition the Action recorder panel anywhere on your desktop screen.

    ![Floating recorder panel that has Discard, Pause, and Start recording UI actions.](../image/recorder-auto-capture-ad.png)

10. Open the **Employee Badge Management** application on your desktop.

11. From the Action recorder panel, select **Start**.

    You see that a "Recording started" message on the Action recorder panel.

    -   Pause recording: You can skip recording steps by selecting **Pause**.
    -   Discard recording: You can discard the recording if it doesn’t meet your needs by selecting **Discard**.
12. On the **Employee Badge Management** application, perform the following steps for creating a badge.

    The recorder feature records the steps that you perform for creating a badge.

    1.  Select **CREATE BADGE** on the **New Badge** tile.

    2.  In the New Badge Creation page, search for the employee using the employee ID.

    3.  After the employee record is found, select **CREATE BADGE** for creating badge.

        You see the success message that the new badge is created.

13. After you’re done with all the steps, select **Stop** on the Action recorder panel.

    You see a "Drafting recorded action\(s\)" message on the Action recorder panel.

    The recorded steps are displayed as screenshots in the Design workspace with anchors and steps automatically assigned.

    ![Employee badge management login window.](../image/ex-employee-badge-1.png "Screen1")

    ![Employee badge management welcome window displaying cards for creating new badge, inactivating badge, reissuing badge, and viewing audit logs.](../image/ex-employee-badge-2.png "Screen2")

    ![Displaying option for searching employee ID in the Employee Badge Management app.](../image/ex-employee-badge-3.png "Screen3")

    ![Displaying preview of new badge.](../image/ex-employee-badge-4.png "Screen4")

    ![Success message indicating new badge is successfully created.](../image/ex-employee-badge-5.png "Screen5")

14. Configure the following properties for the captured steps.

    |Screen &gt; Step|Property|Value|
    |----------------|--------|-----|
    |Screen1 &gt; SetText1|Value|admin|
    |Screen1 &gt; SetText2|Value|Enter your password|
    |Screen1 &gt; Click1|Delay after|5|
    |Screen2 &gt; Click2|Delay after|5|
    |Screen3 &gt; Click2|Delay after|10|

    For more information, see [Screen, anchor, and step properties in AI Desktop Actions](../reference/screen-anchor-and-action-properties-ad.md).

15. Provide names for all added screens, anchors, and steps.

    When you create these elements, you can edit the auto-generated name, but follow these naming guidelines.

    -   Name fields must not be empty.
    -   Name fields must contain only alphanumeric characters. Spaces and special characters are not permitted.
    -   Each name must be unique at its respective parent level.
        -   Each screen must have a unique name at the desktop-action level.
        -   Each anchor must have a unique name at the screen level.
        -   Each step must have a unique name at the anchor level.
16. Select the Details tab.

17. In the Applications list, add Badge Management Application.

18. Select **Save**.

19. Test and activate the desktop action.

    For more information, see [Test and activate a desktop action in AI Desktop Actions](../task/test-activate-desktop-action-ad.md).

20. Similarly, create and activate the following desktop actions.

    -   Badge application login
    -   Badge application logout
    -   Reissue badge
    -   Deactivate badge
    -   Issue a temporary badge
    -   Read Request details

## Create AI agents and add tools for badge management

Create an AI agent in AI Agent Studio and add desktop action tools for automating badge-related requests.

### Before you begin

Role required: sn\_aia.admin

### Procedure

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage** &gt; **AI agents**.

2.  From the **Add** drop-down, select **Chat**.

3.  On the New AI Agent page, in the Define the specialty step, define your AI agent and provide the specialties that this agent contains so that the LLM can analyze the wording you use to understand the purpose of the AI agent.

    ![AI Agent Guided Setup showcasing the different stages of configuring an AI agent.](../../../administer/now-assist-ai-agents/image/create-ai-agent-latest.png)

    **Note:** The more details that you provide, the more accurately your AI agent can perform.

    1.  Describe your AI Agent by giving it a unique name and description.

        |Field|Description|
        |-----|-----------|
        |AI agent name|Badge Management Agent|
        |AI agent Description|This AI agent takes Requests details and launches the Employee Badge Management application and perform various tasks—create badges, deactivate badges, replace lost badges, and Reissue the badges. The agent executes the appropriate desktop actions automatically. This reduces manual effort, ensures process consistency, and speeds up the overall employee lifecycle experience.|

    2.  Define the role and necessary steps so that the AI agent can carry out its tasks.

        **Note:** The AI agent uses this information as guidance to tailor its responses and actions.

<table id="table_uj3_msj_zcc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

AI agent role

</td><td>

Automates the intake of badge-related requests and performs accurate, end-to-end execution of badge actions—such as issuance, replacement, temporary provisioning, and deactivation—across the HR and security systems.

</td></tr><tr><td>

List of steps

</td><td>

**Note:** If your automation requires manual inputs, such as entering an OTP or CAPTCHA, you must provide instructions to the AI Agent to wait for the user input during execution. Otherwise, the automation can't proceed.

 Read the comma-separated Request numbers from the input by invoking the **Read Request details** desktop action.

 Launch and log in to the Employee Badge Management application by invoking the **Badge application login** desktop action.

 Based on the details of each Request, perform one of the following actions that is applicable.

-   Create a badge
    1.  Create a badge in Employee Badge Management application by invoking **Create new badge** desktop action.
    2.  If badge creation failed, create an incident with the issue details. Otherwise, continue with other steps.
-   Deactivate a badge
    1.  Deactivate a badge in Employee Badge Management application by invoking **Deactivate badge** desktop action.
    2.  If badge deactivation failed, create an incident with the issue details. Otherwise, continue with other steps.
-   Reissue Badge
    1.  Reissue a badge in Employee Badge Management application by invoking **Reissue badge** desktop action.
    2.  If badge deactivation failed, create an incident with the issue details. Otherwise, continue with other steps.
-   Issue a temporary badge
    1.  Issue a temporary badge in Employee Badge Management application by invoking **Issue temporary badge** desktop action.
    2.  If badge reissue failed, create an incident with the issue details. Otherwise, continue with other steps.
 Log out of the Employee Badge Management application by invoking the **Badge application logout** desktop action.

</td></tr></tbody>
</table>    3.  Select **Save and continue**.

        You’re directed to the Add tools and information page.

4.  On the Add tools and information page, add Desktop actions tools for AI agents to automate your desktop tasks.

    1.  In the Add tool drop-down list, select **Desktop action**.

    2.  In the **Select a type of desktop action** field, select **UI block**

    3.  In the **Select a desktop action** drop-down list, select **Create new badge** desktop action.

        This desktop action enables AI agents to create a badge in the Employee Badge Management application.

    4.  Provide a name and tool description for this desktop action configuration.

        Tool description of the desktop action helps with what it’s going to do to assist your AI agent.

        **Note:** This description is sent to the large language model \(LLM\).

    5.  In the **Execution mode** field, select **Autonomous**.

    6.  Select **Add**.

        The desktop action is added in the Desktop actions list on the Add tools and information page.

    7.  Similarly, add the following desktop actions related to the badge management to this AI agent.

        -   Badge application login
        -   Badge application logout
        -   Reissue badge
        -   Deactivate badge
        -   Issue a temporary badge
        -   Read Request details
5.  Select **Save and continue**.

6.  Complete the remaining steps that are necessary.

    For more information, see [Create an AI agent](../../../administer/now-assist-ai-agents/task/configure-next-best-action-agent.md).

7.  Select **Save and test** to complete the configuration steps or review a previous step by selecting **Back**.

    Selecting Save and test leads you to the AI agent testing page, where you can test the AI agent that you created. For more information, see [Manually test the execution of an AI agent](../../../administer/now-assist-ai-agents/task/test-ai-agent.md).

    To test the AI agent, you must have the sn\_aia.admin role and any roles the ACLs configured for the AI agent and its tools require, if applicable.


### What to do next

Enable your HR representatives to trigger AI agents from the Now Assist panel to address badge-related requests.

For more information, see [Example: Use AI agents to process badge-related requests automatically](../task/example-use-badging-ai-agent-ad.md).

