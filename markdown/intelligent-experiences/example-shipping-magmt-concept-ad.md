---
title: Example: Automate shipping management tasks using AI Desktop Actions
description: Automate various tasks related to shipping management through desktop actions using AI Desktop Actions and AI agents.Automate various tasks related to shipping management through desktop actions in AI Desktop Actions.Create an AI agent in AI Agent Studio and add desktop action tools for Shipping Management task automation.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-11-20"
reading_time_minutes: 11
breadcrumb: [Desktop action examples, AI Desktop Actions, Enable AI experiences]
---

# Example: Automate shipping management tasks using AI Desktop Actions

Automate various tasks related to shipping management through desktop actions using AI Desktop Actions and AI agents.

Your shipping coordinators frequently handle repetitive data-entry tasks. For example, entering PO numbers, invoice details, customer information, shipping addresses, item dimensions, and weights from Excel into the Shipping Management application on their desktops. When there are dozens of rows to process, it becomes time-consuming, error-prone, and significantly slows down their daily workflow.

To streamline this process, you can create a dedicated desktop action that reads each row from the Excel file and automatically inputs the data into the Shipping Management application. You can then assign this action to an AI Agent. When new shipping batches arrive, shipping coordinators simply trigger the AI Agent from the Now Assist panel. The agent then automatically processes each line item by selecting and running the appropriate desktop action.

## Create Process shipping orders desktop action in AI Desktop Actions

Automate various tasks related to shipping management through desktop actions in AI Desktop Actions.

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

6.  In the New desktop action dialog box, select **Manual capture steps**.

    ![New desktop action window with manual capture option selected and fields to enter name and description for the desktop action.](../image/create-desktop-action-manual-ad.png)

7.  In the **Name** field, enter `Process shipping orders`.

8.  In the **Description** field, enter `Enter Shipping order details from Excel to Shipping Management tool.`

9.  Select **Start capturing**.

    The Design workspace is displayed.

    ![Design workspace in a state when no screenshot is captured.](../image/design-workspace-ad.png)

10. Capture screens.

    1.  In the Design tab, select the **Capture Options** icon ![](../image/capture-options-icon.png).

    2.  Select **Manual capture screens**.

        ![Design workspace displaying two options: Auto-capture steps and Manual capture screens.](../image/design-tab-manual-ad.png)

        The AI Desktop Actions window is minimized and the Capture panel is launched.

        ![Manual capture floating panel with Select and Cancel UI actions.](../image/manual-select-screen-ad.png)

    3.  Open the Shipping Management application from your desktop.

        ![Displaying user desktop with app for automating steps open and manual capture panel on the side.](../image/ex-ship-app.png)

    4.  Capture the area of the external application’s window by selecting the **Select** icon ![](../image/ad-select-icon.png) on the Capture panel or pressing the `Ctrl + Shift + C` on the keyboard.

        **Note:** If the `Ctrl + Shift + C` shortcut conflicts with another application on the your machine, such as Zoom, then you must use the **Select** button to initiate manual screen capture.

        For example, you can capture the area surrounding a button or a text field in a web browser. The cursor icon changes to the ![](../../../reuse/icons/product-icons/plus-outline-24.svg) icon.

    5.  Drag the ![](../../../reuse/icons/product-icons/plus-outline-24.svg) icon and select the required screen area.

        When you leave the ![](../../../reuse/icons/product-icons/plus-outline-24.svg) icon, the selected area is captured as a screenshot in the Design workspace.

        If you are not satisfied with the captured screen, you can recapture the screen area by selecting the **Capture image** icon ![](../image/ad-capture-image-icon.png).

11. Insert anchors.

    1.  Insert an anchor on the captured screen by selecting the **Add anchor** icon ![](../image/ad-add-anchor-icon.png).

        ![Screen capture of the Shipping Management app with anchor added on the Window title](../image/ex-ship-app-anchor-ad.png)

        An anchor is a reference point on the screen that helps the automation identify and interact with a nearby UI elements. During execution, the system uses computer vision to locate the anchor and then identifies the UI elements at a related distance from the anchor. Anchors improve the stability and accuracy of steps when the target element’s location may shift or when the UI layout varies across sessions.

        **Note:** Do not use dynamically changing UI elements as anchors. If an element changes its color, text, or state after an action \(for example, after a click\), select a different anchor that remains static on the screen.

    2.  Move the anchor to a part of the captured image that won’t change.

        For example, move the anchor to a title or field label.

        If the area under the anchor doesn’t exactly match the corresponding area of the captured image, the anchor isn't recognized, and the steps are not performed as intended. Choose a static area of the image for setting your anchor.

        You can add multiple anchors on each screen. Multiple anchors let you define the geographical relationship between anchor and target with greater accuracy when targeting different locations in the image.

12. Configure the steps.

    1.  From the Step control menu, select the **Add step** icon ![](../../../reuse/icons/product-icons/circle-plus-outline-24.svg).

    2.  Select the type of step for each field on the ORDER FORM from the contextual menu.

        ![Screen capture of the Shipping management app with anchor and steps added.](../image/ex-ship-app-anchor-actions.png)

        |Number|Field|Step|
        |------|-----|----|
        |1|PO\#|Set Text|
        |2|Invoice\#|Set Text|
        |3|Customer Name|Set Text|
        |4|Shipping Address|Set Text|
        |5|Item size|Set Text|
        |6|Weight limit|Set Text|
        |7|Phone|Set Text|
        |8|Express Delivery|Click|
        |9|SMS Alerts|Click|
        |10|Submit|Click|

13. Configure the properties for added screens, anchors, and steps.

    For more information, see [Screen, anchor, and step properties in AI Desktop Actions](../reference/screen-anchor-and-action-properties-ad.md).

14. Provide names for all added screens, anchors, and steps.

    When you create these elements, you can edit the auto-generated name, but follow these naming guidelines.

    -   Name fields must not be empty.
    -   Name fields must contain only alphanumeric characters. Spaces and special characters are not permitted.
    -   Each name must be unique at its respective parent level.
        -   Each screen must have a unique name at the desktop-action level.
        -   Each anchor must have a unique name at the screen level.
        -   Each step must have a unique name at the anchor level.
15. Select the Details tab.

16. In the Applications list, add Shipping Management.

17. Select **Save**.

18. Test and activate the desktop action.

    For more information, see [Test and activate a desktop action in AI Desktop Actions](../task/test-activate-desktop-action-ad.md).

19. Similarly, create and activate the **Shipping Management login** desktop action.


## Create AI agents and add tools for shipping orders

Create an AI agent in AI Agent Studio and add desktop action tools for Shipping Management task automation.

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
        |AI agent name|Shipping Management Agent|
        |AI agent Description|The Shipping Management Agent automates end-to-end handling of shipping orders across multiple platforms. It retrieves order data from an Excel sheet and seamlessly uploads the information into the shipping management tool. This reduces manual effort, ensures data consistency, and accelerates the overall invoice life cycle.|

    2.  Define the role and necessary steps so that the AI agent can carry out its tasks.

        **Note:** The AI agent uses this information as guidance to tailor its responses and actions.

<table id="table_uj3_msj_zcc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

AI agent role

</td><td>

Automates the retrieval of shipping orders from Excel and performs seamless data entry into the shipping management application.

</td></tr><tr><td>

List of steps

</td><td>

**Note:** If your automation requires manual inputs, such as entering an OTP or CAPTCHA, you must provide instructions to the AI Agent to wait for the user input during execution. Otherwise, the automation can't proceed.

 1.  Launch and log in to the Shipping Management application.
2.  Open the Excel file from the user-specified folder.
3.  Navigate to the designated worksheet within the Excel file.
4.  Read the required columns for each order from the Excel sheet.
5.  Enter the extracted data into the corresponding fields in the shipping management application.
6.  Select **Submit** to register the order.
7.  Repeat steps 4–6 until all pending orders in the Excel sheet have been processed.


</td></tr></tbody>
</table>    3.  Select **Save and continue**.

        You’re directed to the Add tools and information page.

4.  On the Add tools and information page, add Desktop actions tools for AI agents to automate your desktop tasks.

    1.  In the Add tool drop-down list, select **Desktop action**.

    2.  In the **Select a type of desktop action** field, select **UI block**

    3.  In the **Select a desktop action** drop-down list, select **Shipping Management login** desktop action.

        This desktop action enables AI agents to log in to the Shipping Management application.

    4.  Provide a name and tool description for this desktop action configuration.

        Tool description of the desktop action helps with what it’s going to do to assist your AI agent.

        **Note:** This description is sent to the large language model \(LLM\).

    5.  In the **Execution mode** field, select **Autonomous**.

    6.  Select **Add**.

        The desktop action is added in the Desktop actions list on the Add tools and information page.

    7.  In the Add tool drop-down list, select **Desktop action**.

    8.  In the **Select a type of desktop action** field, select **UI block**

    9.  In the **Select a desktop action** drop-down list, select **Process shipping orders** desktop action.

        This desktop action enables AI agents to enter data extracted from the spreadsheet into the Shipping Management application.

    10. Provide a name and tool description for this desktop action configuration.

        Tool description of the desktop action helps with what it’s going to do to assist your AI agent.

        **Note:** This description is sent to the large language model \(LLM\).

    11. In the **Execution mode** field, select **Autonomous**.

    12. Select **Add**.

        The desktop action is added in the Desktop actions list on the Add tools and information page.

    13. In the Add tool drop-down list, select **Desktop action**.

    14. In the **Select a type of desktop action** field, select **Non UI block**

    15. In the **Select an application** drop-down list, select Microsoft Excel.

        The Microsoft Excel tool, non-UI block desktop action, enables AI agents to contextually extract information from the spreadsheet.

    16. Provide a name and tool description for this desktop action configuration.

        Tool description of the desktop action helps with what it’s going to do to assist your AI agent.

        **Note:** This description is sent to the large language model \(LLM\).

    17. In the **Execution mode** field, select **Autonomous**.

    18. Select **Add**.

        The desktop action is added in the Desktop actions list on the Add tools and information page.

5.  Select **Save and continue**.

6.  Complete the remaining steps that are necessary.

    For more information, see [Create an AI agent](../../../administer/now-assist-ai-agents/task/configure-next-best-action-agent.md).

7.  Select **Save and test** to complete the configuration steps or review a previous step by selecting **Back**.

    Selecting Save and test leads you to the AI agent testing page, where you can test the AI agent that you created. For more information, see [Manually test the execution of an AI agent](../../../administer/now-assist-ai-agents/task/test-ai-agent.md).

    To test the AI agent, you must have the sn\_aia.admin role and any roles the ACLs configured for the AI agent and its tools require, if applicable.


### What to do next

Enable shipping coordinators to trigger AI agents from the Now Assist panel to enter data automatically into the Shipping Management application.

For more information, see [Example: Use AI agents to automatically enter data into the shipping management app](../task/example-use-shipping-ai-agent-ad.md).

