---
title: Desktop actions in AI Desktop Actions
description: Desktop actions enable you to automate repetitive tasks on your desktop and web applications. This capability helps you streamline repetitive tasks, improve efficiency, and integrate desktop application workflows into your ServiceNow processes.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-11-01"
reading_time_minutes: 7
breadcrumb: [AI Desktop Actions, Enable AI experiences]
---

# Desktop actions in AI Desktop Actions

Desktop actions enable you to automate repetitive tasks on your desktop and web applications. This capability helps you streamline repetitive tasks, improve efficiency, and integrate desktop application workflows into your ServiceNow processes.

## Types of desktop actions

AI agents use these desktop actions to interact with desktop applications, perform UI-based tasks, and automate end-to-end workflows. There are two types of desktop actions that can be added as tools to AI agents:

-   **UI blocks**

    The UI block actions help you simulate humans interacting with UI elements on your thick client applications, legacy systems, or SaaS applications without APIs. These actions include clicking buttons, typing into text boxes, selecting from dropdown menus, and more. These desktop actions make it easier to automate repetitive tasks. They encapsulate repeatable UI interactions, such as screens, anchors, and steps. You can create, manage, and test your desktop actions using the no-code Design workspace.

    Example: Filling in fields on a payroll application, updating inventory in a point-of-sale system, or submitting a request through a desktop insurance claims app.

    You can access and view the existing desktop actions in the ServiceNow instance by navigating to **All** &gt; **Agentic Desktop** &gt; **Desktop Actions**. You can see the details of related desktop action applications, AI agents, and desktop action execution records for UI block, and AI agents and desktop action execution records for non-UI block desktop actions.

-   **Non-UI block**

    The non-UI block actions include pre-built connectors that enable your AI agents to interact with various applications and system components in the background. These connectors streamline automation by offering actions for common tasks, reducing the need for complex scripting. Each connector focuses on a specific application or system area, providing a collection of related methods. You can't create non-UI block actions.

    Example: Reading data from Microsoft Excel, extracting emails from Microsoft Outlook, generating a PDF, compressing files into a ZIP, fetching records from a database, or sending a system notification.

    Non-UI block actions are supported for the following applications:

    **Note:** For the AI agents to perform non-UI block automations, the following applications must already be installed on the end-user's system.

<table id="table_i2q_4lb_hhc"><thead><tr><th>

Application

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Microsoft Excel

</td><td>

Enables AI agents to perform standard actions on the Microsoft Excel documents. For example, data manipulation, content modification, and information retrieval from spreadsheets.The following methods are supported:

-   ReadData
-   WriteData
-   FindAndReplace
**Note:** CSV and password-protected files aren't supported.

</td></tr><tr><td>

Microsoft Outlook

</td><td>

Enables AI agents to perform standard actions on the Microsoft Outlook application. For example, you can automate sending or replying to emails.The following methods are supported:

-   DeleteMail
-   ForwardMail
-   GetMailsFromFolder
-   MoveMail
-   Reply
-   SaveAllAttachments
-   SendMail
-   GetMail
-   MarkAsRead
-   MarkAsUnread
**Note:** Only the classic view is supported. Shared inboxes aren’t supported.

</td></tr><tr><td>

Microsoft Word

</td><td>

Enables AI agents to perform standard actions on the Microsoft Word documents. For example, you can replace text in a document.The following methods are supported:

-   GetText
-   InsertText
-   ReplaceText
**Note:** Password-protected files aren't supported.

</td></tr><tr><td>

PDF

</td><td>

Enables AI agents to perform standard actions on the PDF documents. For example, extracting text, converting to Excel or Images, and merging and spiting files.The following methods are supported:

-   GetText
-   ConvertToExcel
-   ConvertToImages
-   Merge
-   Split
**Note:** Password-protected files aren't supported.

</td></tr><tr><td>

PowerShell

</td><td>

Enables AI agents to execute PowerShell commands and scripts and returns the results.The following methods are supported:

-   InvokeCommand
-   InvokeScript
**Note:** Each PowerShell step runs in a new session. Output from one step isn’t carried over to the next step.

</td></tr><tr><td>

SQL

</td><td>

Enables AI agents to execute custom SQL queries against supported databases \(MSSQL, ORACLE, MYSQL, OLEDB, ODBC\) and returns results as JSON.The following method is supported:

ExecuteQuery

</td></tr><tr><td>

Secure Shell \(SSH\)

</td><td>

Enables AI agents to securely connect to remote servers to run SSH commands and scripts; and returns the execution results. This connector supports non-interactive commands.The following method is supported:

RunCommand

**Note:** Each SSH step runs in a new session. Output from one step isn’t carried over to the next step.

</td></tr><tr><td>

System Actions

</td><td>

Enables AI agents to perform standard Windows system operations. For example, starting an app, creating a ZIP file, or deleting any file or folder.The following methods are supported:

-   StartApp
-   Terminate
-   DateTimeNow
-   SetEnvironmentVariable
-   GetEnvironmentVariable
-   CopyFileOrFolder
-   DeleteFileOrFolder
-   WriteToFile
-   ReadFromFile
-   GetFilesFromFolder
-   ExtractFile
-   CreateZip


</td></tr></tbody>
</table>
## Ways to create desktop actions

**Note:** If your automation requires manual inputs, such as entering an OTP or CAPTCHA, you must provide instructions to the AI Agent to wait for user input during execution. Otherwise, the automation can't proceed.

You can create desktop actions of type UI block in the following ways:

-   **[Auto-capture screens and steps](../task/auto-create-desktop-action-ad.md)**

    With Action recorder, you can record your interactions with desktop applications to create automated workflows. It records every step you take, including clicks, keystrokes, and data entry, along with visual and contextual information. By recording steps, you can automate tasks that replicate your interactions. You can save the recorded screens and steps as a reusable desktop action. For more information, see [Action recorder in AI Desktop Actions](action-recorder-ad.md).

-   **[Manually capture screens and steps](../task/manual-create-desktop-action-ad.md)**

    You can manually take a screen capture, add anchors and steps to automate a series of steps you perform on your computer, such as clicking buttons, typing text, or interacting with different applications, and then save this sequence as a reusable desktop action.


## Benefits of desktop actions

-   Eliminate manual effort by automating repetitive tasks for frequent desktop activities.
-   Execute complex sequences of steps quickly and consistently.
-   Connect desktop application processes with your broader ServiceNow automations.
-   Standardize task execution to minimize human error.
-   You can record steps directly on your desktop applications.
-   Automate tasks that span across multiple desktop applications.
-   Save recorded sequences as desktop actions to use them in various automations.
-   Review, rearrange, edit, or delete individual steps within a recorded action.

## How the Design workspace works

-   **Record steps**

    Capture your interactions with desktop applications, including clicks, text input, and screen navigation.

-   **Define steps**

    Specify individual steps like Click, Set Text, or Get Text to interact with elements on your screen.

-   **Application details**

    Select and store the desktop applications involved in your automations in the **Details** tab.

-   **Organize screens**

    Structure your recorded steps by application screens, making it easy to review and edit.

-   **Save and publish**

    Store your desktop actions in your ServiceNow instance for reuse and deployment.


## What you can automate

Desktop actions support a wide range of desktop application interactions, including:

-   Entering data into forms.
-   Extracting information from applications.
-   Navigating through application menus and screens.
-   Performing steps like saving files or generating reports.
-   Transferring data between different desktop applications.

**Related topics**  


[AI Desktop Actions Design workspace](agentic-desktop-overview.md)

[Action recorder in AI Desktop Actions](action-recorder-ad.md)

[Automate repetitive tasks by auto-capturing steps in AI Desktop Actions](../task/auto-create-desktop-action-ad.md)

[Automate repetitive tasks by manually capturing steps in AI Desktop Actions](../task/manual-create-desktop-action-ad.md)

[Add details to desktop actions in AI Desktop Actions](../task/add-details-desktop-action-ad.md)

[Test and activate a desktop action in AI Desktop Actions](../task/test-activate-desktop-action-ad.md)

[Add a desktop action to an AI agent](../../../administer/now-assist-ai-agents/task/add-desktop-action-ai-agent.md)

