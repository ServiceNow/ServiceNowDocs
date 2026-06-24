---
title: Example: Automate badge request management using AI Desktop Actions
description: Automate various tasks related to badge requests through desktop actions using AI Desktop Actions and AI agents.Automate various badge-related tasks through desktop actions in AI Desktop Actions.Create an AI agent in AI Agent Studio and add desktop action tools for automating badge-related requests.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/example-badging-magmt-concept-ad.html
release: zurich
topic_type: concept
last_updated: "2026-05-25"
reading_time_minutes: 12
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

-   Enable AI Desktop Actions on your ServiceNow instance. For more information, see [Configure AI Desktop Actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/configure-agentic-desktop.md).
-   Download the AI Desktop Actions installer to automate repetitive tasks across applications and systems. For more information, see [Download AI Desktop Actions installer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/download-agentic-desktop-installer.md).

Confirm that the following system requirements are met:

-   Windows 11 operating system is used.
-   A .NET 9.0 runtime v9.0.10 and .NET 9 Desktop Runtime v9.0.10 is installed.
-   No extended monitors are connected.
-   Theme must match between the systems used for recording and execution.
-   For record with AI, the ServiceNow AI Lens skill must be active on your instance. Contact your ServiceNow administrator if you're unsure whether this condition is met.

Familiarize yourself with the Design workspace and Action recorder. For more information, see [AI Desktop Actions Design workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/agentic-desktop-overview.md) and [Action recorder in AI Desktop Actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/action-recorder-ad.md).

Role required: sn\_desktop\_core.desktop\_action\_user

### About this task

Record with AI generates more accurate anchor positions automatically, reducing the time you spend on manual anchor adjustments.

When you record with AI, after you finish recording, AI analyzes the recording, validates anchor positions, and corrects inaccuracies before you save or activate the desktop action. AI also generates a screen context for each captured screen and description for the desktop action. Screen context is a description of what the screen does and what it contains, which helps reviewers and AI agents understand the screen's intent.

**Note:** If your automation requires manual inputs, such as entering an OTP or CAPTCHA, you must provide instructions to the AI Agent to wait for the user input during execution. Otherwise, the automation can't proceed.

The **sn\_desktop\_core.record\_with\_ai** property is enabled by default, making **Record with AI** the default recording option. Turn off this property to set the manual recorder as the default recording option.

### Procedure

1.  From your Windows system, launch the AI Desktop Actions application.

2.  On the login page, in the **Add ServiceNow URL** field, enter the ServiceNow instance URL.

    For example, `https://<instance name>.service-now.com`.

    \[Omitted image "ad-login-screen.png"\] Alt text: AI Desktop Actions login screen for entering ServiceNow instance URL.

3.  Select **Proceed**.

4.  Log in to your ServiceNow account by entering your user name and password.

    Your must have the sn\_aia.admin role.

    \[Omitted image "ad-login-screen-cred.png"\] Alt text: Login window for entering your ServiceNow account username and password.

5.  On the onboarding journey modal, complete the onboarding and select **Get started**.

    \[Omitted image "onboarding-widget-ad.png"\] Alt text: Onboarding journey widget with five pages to show you the highlights of the application.

    If you launch the AI Desktop Actions for the first time, the onboarding journey widget appears. You can select **Don't show me again** to hide the widget the next time you launch AI Desktop Actions or **Skip intro** to skip the onboarding.

6.  On the AI Desktop Actions home page, select **Create desktop action**.

    \[Omitted image "home-page-actions-ad.png"\] Alt text: AI Desktop Actions home page displaying the Create desktop action UI action, search and select options, and cards of existing desktop actions.

7.  In the Create Desktop Action dialog, do one of the following.

    -   If you want to record with AI, keep the **Record with AI \(recommended\)** check box selected.

        \[Omitted image "create-desktop-action-with-ai.png"\] Alt text: Create desktop action modal with Record with AI option selected and a field to enter name for the desktop action.

        **Important:** If the **Record with AI \(recommended\)** check box is unavailable, the ServiceNow AI Lens is inactive on your instance. Contact your ServiceNow administrator to enable it. You can still create desktop actions using [auto-capture](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/auto-create-desktop-action-ad.md) mode.

    -   If you want to use manual recorder, clear the **Record with AI \(recommended\)** check box.

        \[Omitted image "ad-lens-skill-disabled.png"\] Alt text: Create desktop action modal with Record with AI option inactive and a fields to enter name and description for the desktop action.

8.  In the **Name** field, enter `Create new badge`.

9.  In the **Description** field, enter `Desktop action for issuing a badge to a new employee.`

    This field only appears when you clear the **Record with AI \(recommended\)** check box.

10. Select **Continue**.

11. In the modal, review the tips and select **Open recorder** to begin.

    \[Omitted image "open-recorder-ad.png"\] Alt text: Guided slow model for providing tips for effective recording.

    The AI Desktop Actions window is minimized and the Action recorder panel is launched. You can freely drag and reposition the Action recorder panel anywhere on your desktop screen.

    \[Omitted image "recorder-auto-capture-ad.png"\] Alt text: Floating recorder panel that has Discard, Pause, and Start recording UI actions.

12. Open the **Employee Badge Management** application on your desktop.

13. From the Action recorder panel, select **Start recording**.

    **Important:** Before you start recording, review the tips for accurate capturing of anchors and steps. For more information, see [Tips for accurate recording](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/action-recorder-ad.md).

    You will see a "Recording started" message on the Action recorder panel. You can select any of the following options when needed from the **More options** menu:

    -   **Pause**: Skip recording steps
    -   **Restart**: Restart recording the steps

        You will lose the recorded screens and steps.

    -   **Discard**: Discard the recording if it doesn't meet your needs
14. On the **Employee Badge Management** application, perform the following steps for creating a badge.

    The recorder feature records the steps that you perform for creating a badge.

    1.  Select **CREATE BADGE** on the **New Badge** tile.

    2.  In the New Badge Creation page, search for the employee using the employee ID.

    3.  After the employee record is found, select **CREATE BADGE** for creating badge.

        You see the success message that the new badge is created.

15. After you’re done with all the steps, select **End recording** on the Action recorder panel.

    You see a "Draft workflow saved" message on the Action recorder panel.

    For Record with AI option, AI processes the recording in three stages:

    1.  Analyzing your recording with AI
    2.  Inserting anchors
    3.  Generating screen contexts
    You must not close the application during processing.

    The recorded steps are displayed as screenshots in the Design workspace with anchors and steps automatically assigned.

    \[Omitted image "ex-employee-badge-1.png"\] Alt text: Employee badge management login window.

    \[Omitted image "ex-employee-badge-2.png"\] Alt text: Employee badge management welcome window displaying cards for creating new badge, inactivating badge, reissuing badge, and viewing audit logs.

    \[Omitted image "ex-employee-badge-3.png"\] Alt text: Displaying option for searching employee ID in the Employee Badge Management app.

    \[Omitted image "ex-employee-badge-4.png"\] Alt text: Displaying preview of new badge.

    \[Omitted image "ex-employee-badge-5.png"\] Alt text: Success message indicating new badge is successfully created.

16. Configure the following properties for the captured steps.

    |Screen &gt; Step|Property|Value|
    |----------------|--------|-----|
    |Screen1 &gt; SetText1|Value|admin|
    |Screen1 &gt; SetText2|Value|Enter your password|
    |Screen1 &gt; Click1|Delay after|5|
    |Screen2 &gt; Click2|Delay after|5|
    |Screen3 &gt; Click2|Delay after|10|

    For more information, see [Screen, anchor, and step properties in AI Desktop Actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/screen-anchor-and-action-properties-ad.md).

17. Modify the auto-generated names for all added screens, anchors, and steps.

    You can modify the auto-generated names following these naming guidelines.

    -   Name fields must not be empty.
    -   Name fields must contain only alphanumeric characters. Spaces and special characters are not permitted.
    -   Each name must be unique at its respective parent level.
        -   Each screen must have a unique name at the desktop-action level.
        -   Each anchor must have a unique name at the screen level.
        -   Each step must have a unique name at the anchor level.
18. Select the Details tab.

19. In the Applications list, add Badge Management Application.

20. Select **Save**.

21. Test and activate the desktop action.

    For more information, see [Test and activate a desktop action in AI Desktop Actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/test-activate-desktop-action-ad.md).

22. Similarly, create and activate the following desktop actions.

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

    \[Omitted image "create-ai-agent-latest.png"\] Alt text: AI Agent Guided Setup showcasing the different stages of configuring an AI agent.

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

    2.  In the **Select a desktop action** drop-down list, select **Create new badge** desktop action.

        This desktop action enables AI agents to create a badge in the Employee Badge Management application.

    3.  Provide a name and tool description for this desktop action configuration.

        Tool description of the desktop action helps with what it’s going to do to assist your AI agent.

        **Note:** This description is sent to the large language model \(LLM\).

    4.  In the **Execution mode** field, select **Autonomous**.

    5.  Select **Add**.

        The desktop action is added in the Desktop actions list on the Add tools and information page.

    6.  Similarly, add the following desktop actions related to the badge management to this AI agent.

        -   Badge application login
        -   Badge application logout
        -   Reissue badge
        -   Deactivate badge
        -   Issue a temporary badge
        -   Read Request details
5.  Select **Save and continue**.

6.  Complete the remaining steps that are necessary.

    For more information, see [Create an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/configure-next-best-action-agent.md).

7.  Select **Save and test** to complete the configuration steps or review a previous step by selecting **Back**.

    Selecting Save and test leads you to the AI agent testing page, where you can test the AI agent that you created. For more information, see [Manually test the execution of an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/test-ai-agent.md).

    To test the AI agent, you must have the sn\_aia.admin role and any roles the ACLs configured for the AI agent and its tools require, if applicable.


### What to do next

Enable your HR representatives to trigger AI agents from the Now Assist panel to address badge-related requests.

For more information, see [Example: Use AI agents to process badge-related requests automatically](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/example-use-badging-ai-agent-ad.md).

