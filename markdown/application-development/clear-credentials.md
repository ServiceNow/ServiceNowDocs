---
title: Clear instance credentials in Visual Studio Code
description: Clear the stored credentials of the current project from the system. User credentials \(instance URL, user name, password\) of a project are stored in the operating system credentials vault so that the user does not need to log in each time.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/application-development/clear-credentials.html
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [ServiceNow Extensions for Visual Studio Code, Building pro-code applications, Developing your application, Building applications]
---

# Clear instance credentials in Visual Studio Code

Clear the stored credentials of the current project from the system. User credentials \(instance URL, user name, password\) of a project are stored in the operating system credentials vault so that the user does not need to log in each time.

## Before you begin

Role required: none.

## About this task

Once you clear credentials from the current instance, the ServiceNow Extensions for Visual Studio Code extension prompts for authentication the next time you open VS Code. You can continue working in the current session.

**Note:** The password is not stored in the Visual Studio Code settings.

## Procedure

1.  Navigate to **All** &gt; **View** &gt; **Command Palette**.

    You can also use a keyboard shortcut, Control+Shift+P on Windows or Command+Shift+P on MacOS to open the command palette.

2.  Choose **Now: Clear Credentials** from the command palette.

    \[Omitted image "vscode-clear-credentials.png"\] Alt text: Clear Credentials command

    The credentials of the current project are cleared.

3.  Navigate to **Code** &gt; **Preferences** &gt; **Settings** &gt; **Workspace** &gt; **Extensions** &gt; **ServiceNow** to check whether the credentials and the instance URL have been deleted.

    \[Omitted image "vscode-clearcredentials.png"\] Alt text: Navigation to clear credentials

    **Note:** To re-enter your credentials, navigate to **Code** **Preferences** **Settings** **Workspace** **Extensions** **Now**. Enter your credentials in **Username** and **Password** fields.


**Parent Topic:**[ServiceNow Extensions for Visual Studio Code](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/vs-code.md)

