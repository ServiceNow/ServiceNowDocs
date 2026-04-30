---
title: Connectors
description: The Connectors provide specialized abilities, such as automating tasks with Microsoft Excel spreadsheets and Microsoft Word documents. Connectors are different from components because they expose multiple methods and they are used differently.
locale: en-US
release: xanadu
product: RPA Hub
classification: rpa-hub
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 6
breadcrumb: [Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Creating integrations with applications]
---

# Connectors

The Connectors provide specialized abilities, such as automating tasks with Microsoft Excel spreadsheets and Microsoft Word documents. Connectors are different from components because they expose multiple methods and they are used differently.

Connectors reside in the ServiceNow® app store and become available to you when the RPA Desktop Design Studio connects to the appropriate RPA Hub instance.

Some connectors are available by default under the Toolbox pane while you must install the rest. To install, see [Manage plugins in RPA Desktop Design Studio](../task/install-plugins-rpa-studio.md).

When set up, Connector methods work just like the components. You connect methods with connectors and vice versa to create an automation.

An example of a connector is Google Chrome. The Chrome connector performs various tasks on the Chrome browser.

When you set up a connector, it exposes multiple methods that perform specific functions. For example, the Google Chrome connector exposes the following methods, and more:

-   Get the screenshot of a web page open on the Google Chrome.
-   Set a focus on a Google Chrome window that is inactive or running in the background.

The example shows the Microsoft Word connector and its methods.![Use Connectors.](../image/connectors-illustration.png)

To use a connector, see

-   [Manage plugins in RPA Desktop Design Studio](../task/install-plugins-rpa-studio.md)
-   [Use a connector in RPA Desktop Design Studio](../task/use-connector.md)
-   [Use connector method](../task/use-connector-method.md)

-   **[Chromium connector](chrome-connector.md)**  
The Chromium connector enables you to interact with various elements in web applications running on Google Chrome or Microsoft Edge Edge and build automations around them.
-   **[Counter](counter.md)**  
The Counter connector increments or decrements integers as part of an automation Workflow in RPA Desktop Design Studio.
-   **[C\#.Net](c.md)**  
The C\#.Net connector enables you to create and execute custom C\#.Net scripts by setting custom classes and methods and include them as part of an automation in the RPA Desktop Design Studio.
-   **[Email connector](email-connectors.md)**  
The Email connector lets an RPA Desktop Design Studio automation work with email. For example, an automation can send, retrieve, and reply to email messages, and can automatically download attachments.
-   **[Eventlog](eventlog.md)**  
The Eventlog connector listens from different sources and writes events and custom messages to the Microsoft Event Viewer.
-   **[FTP](ftp-connector.md)**  
The FTP connector enables you to perform various actions on FTP servers. For example, you can upload or download files from an FTP server. The connector provides multiple methods that perform these actions as part of an automation in the RPA Desktop Design Studio.
-   **[IdleTimer connector](idletimer-connector.md)**  
The IdleTimer connector sets, starts and ends an idle time within an attended automation.
-   **[IE connector](internet-explorer-connector.md)**  
The Internet Explorer \(IE\) connector enables you to perform various actions on the IE browser, applications, and their screen elements on the browser. For example, you can execute a method to open a website. You perform the actions through the methods.
-   **[Java](java-connector.md)**  
The Java connector enables you to perform various actions on Java applications as part of an automation in the RPA Desktop Design Studio
-   **[JavaScript](javascript.md)**  
The JavaScript connector enables you to execute custom JavaScript by writing custom classes and methods and include them as part of you automation in the RPA Desktop Design Studio.
-   **[Keyvalue pair](keyvaluepair.md)**  
The KeyValuePair connector enables you to do multiple actions on key value pairs as part of an automation in the RPA Desktop Design Studio. For example, you can create, search, count, or delete key value pairs.
-   **[List](../reference/list-connector.md)**  
The List connector enables you to create, view, search, and do many more actions on list items as part of an automation in the RPA Desktop Design Studio. List items can comprise key value pairs or any regular list item such as a list of employee names.
-   **[Microsoft Excel](microsoft-excel-connector.md)**  
The Microsoft Excel connector enables you to perform various actions on a Microsoft Excel document as part of a Robotic Process Automation. For example, open a Microsoft Excel file and export it to the PDF format.
-   **[Microsoft Outlook](microsoft-outlook-connector.md)**  
The Microsoft Outlook connector enables you to automate standard actions on the Microsoft Outlook application as part of an automation. For example, you can automate sending or replying to emails.
-   **[Microsoft Word](microsoft-word-connector.md)**  
The Microsoft Word connector enables you to perform various tasks on a Microsoft Word document through its methods. For example, you can add a footer to a document.
-   **[PDF connector](pdf-connector.md)**  
Use the PDF connector to perform all your PDF operations from a single, unified space in RPA Desktop Design Studio. Use this connector to accelerate PDF processing for your document automation.
-   **[Python connector](python-connector-rpa.md)**  
Execute custom Python scripts or files as part of an automation workflow in the RPA Desktop Design Studio.
-   **[StringBuilder](stringbuilder-connector.md)**  
The StringBuilder connector enables you to create, append, update, replace, or remove strings as part of your automation Workflow in RPA Desktop Design Studio.
-   **[System Events](system-events-connector.md)**  
Track various system events such as creation of files or loss of the network with the System Events connector as part of your automation Workflow. The connector also enables you to stop tracking events, whenever needed.
-   **[Table](table-connector.md)**  
The Table connector enables you to perform various actions on a table of any kind. For example, you can create or delete columns or rows or get the values from the cells in a table as part of a Workflow in RPA Desktop Design Studio.
-   **[Timer](timer.md)**  
The Timer connector sets a user-defined timer within a workflow and when the timer stops, it triggers an automation.
-   **[Terminal \(Mainframe\) connector](terminal-connector.md)**  
Automate various actions on the IBM Personal Communications and Rocket BlueZone emulators by using the Terminal connector that RPA Desktop Design Studio provides. For example, you can simulate a command on the emulator screen or get text from the screen.
-   **[Universal app connector](universal-app-connector.md)**  
Create automations for your Windows, Java, and web applications by using the Universal App Connector \(UAC\) of RPA Desktop Design Studio. Configure the application screens and their elements from a single, unified connector instead of using the individual connectors of these applications.
-   **[VB.Net](vb-net.md)**  
The VB.Net connector enables you to write and execute VB.Net scripts as part of a Workflow in RPA Desktop Design Studio.
-   **[Windows connector](windows-connector.md)**  
The Windows connector enables you to perform various actions on the Windows applications, and their user interface elements. These actions are performed through the methods provided by the Windows connector. You must configure the connector to expose its methods.
-   **[Application level method parameters](../reuse/application-level-method-parameters.md)**  
These parameters pass custom specifications to the various applications such as Java, Google Chrome, Windows, and Mainframe. Based on the specifications, the applications return an output. The process is a part of a Robotic Process Automation.
-   **[Element level method parameters](../reuse/element-level-method-parameters.md)**  
These parameters pass custom specifications to the elements in various applications such as Java, Google Chrome, Windows, and Mainframe. Based on the specifications, the applications return an output. The process is a part of a Robotic Process Automation.

**Parent Topic:**[Automation components](rpa-studio-automation-components.md)

