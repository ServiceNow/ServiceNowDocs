---
title: Search files on your instance in VS Code
description: Search and download any script files on your instance using the ServiceNow Extensions for VS Code extension.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [ServiceNow Extensions for Visual Studio Code, Building pro-code applications, Developing your application, Building applications]
---

# Search files on your instance in VS Code

Search and download any script files on your instance using the ServiceNow Extensions for VS Code extension.

## Before you begin

Role required: none

## Procedure

1.  Open a project in VS Code containing your application.

2.  Click the **File Search** on the status bar on the bottom of the VSCode IDE.

    You can also use a keyboard shortcut, Control+Shift+P in Windows or Command+Shift+P on MacOS, to open the command palette and choose **Now: Global Search** from the list.

    ![Global Search File command](../image/vscode-globalsearch.png "Global File Search command")

3.  Select the file group from the **Select File Group** list in the command palette on the top of the screen.

    ![List of file groups](../image/vscode-filegroup.png "Select File Group list")

4.  Select the file type from the Select a File Type list in the command palette on the top of the screen.

    ![Select a file type list](../image/vscode-filetype.png "Select a file type list")

5.  Select files from the **Select files to download** list.

    ![Select files to download list](../image/vscode-listoffiles.png "Select files to download list")

    You can select and download multiple files at a time.

    The selected files are downloaded to the `scratch` folder of your application. You can edit the selected files.

6.  View more than 10,000 results from your search:

    1.  Open settings by selecting Control+, in Windows or Command+, on MacOS.

    2.  Enter `now` into the search bar.

    3.  Enter the number of records you want to see in the Fetch Records Max Limit settings.

        ![Fetch Records Max Limit settings](../image/vs-code-file-search.png "Fetch Records Max Limit settings")


**Parent Topic:**[ServiceNow Extensions for Visual Studio Code](../concept/vs-code.md)

**Related topics**  


[Create a file in VS Code](vscode-create-file.md)

