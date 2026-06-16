---
title: RPA Plugin Bundle release notes
description: Version history for the RPA Plugin Bundle application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-plat-app-rpa-plugin-bundle.html
release: store
topic_type: reference
last_updated: "2025-03-12"
reading_time_minutes: 14
breadcrumb: [ServiceNow Store - ServiceNow AI Platform App Engine release notes, ServiceNow Store release notes]
---

# RPA Plugin Bundle release notes

Version history for the RPA Plugin Bundle application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 9.1.1 - March 2025**
    -   Fixed:
        -   The issue with PickWorkItem component failing when the the Request content has array of JSON objects is now fixed.
        -   The issue with DownloadAttachment component replacing filename with "\_" when the attachment name is having non English text is now fixed.
-   **Version 10.0.4 - September 2024**
    -   Fixed:
        -   The issue where the Break component is not functioning correctly when the Break is used in loop with in Skill automation is now fixed.
        -   The issue where the SendKeys component is taking long time to enter the text during runtime for Portuguese is now fixed.
        -   The issue where the error message "There was an error generating the XML document." exception while saving the automation is now fixed.
        -   The issue where the ReadFromRange, WriteToRange, and GetCellcolor Excel methods are missing/not working for automations with lesser than 8.0 plugins, when used in latest studio/runtime is now fixed.
        -   The issue where the Log Component showing an error when the message passed is empty or null is now fixed.
-   **Version 9.0.3 - September 2024**
    -   Fixed:
        -   The issue where the Break component is not functioning correctly when the Break is used in loop with in Skill automation is now fixed.
        -   The issue where the SendKeys component is taking longer time to enter the text during runtime for Portuguese is now fixed.
        -   The issue where the error message "There was an error generating the XML document." while saving the automation is now fixed.
        -   The issue where the ReadFromRange, WriteToRange, and GetCellcolor Excel methods are missing/not working for automations with lesser than 8.0 plugins, when used in latest Studio/Runtime applications is now fixed.
        -   The issue where the Log Component showing an error when the message passed is empty or null is now fixed.
-   **Version 9.0.1 - June 2024**
    -   New:
        -   First Mile Journey
            -   New RPA developers can begin their guided tour journey to build their first automation. This experience provides interactive call-out cards and instructional video designed to acquaint them with the Studio environment.
            -   Revamped homepage of the RPA Desktop Design Studio. Seamlessly access existing projects, explore sample automations, and revisit recently opened projects. The homepage showcases a new card layout for quick navigation and a comprehensive list view for individual project pages, enhancing accessibility, and usability.
        -   Templates
            -   A template in the RPA Desktop Design Studio provides a framework to execute automations that cater to specific use cases. For example, opening emails and downloading invoices, and copying the invoice details to Microsoft Excel spreadsheets. Create automation projects from templates and execute the workflow. The RPA Desktop Design Studio provides default templates for specific use cases, enables you to create custom templates and add multiple versions to those templates.
        -   Run This
            -   Run This functionality enables you to isolate a component in an automation from other components, test it and debug one or more issues. It stops output and executes that component only.
        -   Skip This
            -   Skip This functionality enables an automation on the RPA Desktop Design Studio to complete execution after skipping one or more components that are the parts of the automation.
    -   Changed:
        -   Terminal Connector for BlueZone Emulator
            -   The Terminal \(Mainframe\) connector automates tasks on the IBM Personal Communications and the Rocket BlueZone emulator screens so you can interact with the Mainframe server.
    -   Fixed:
        -   The issue with the Break component not being able to terminate the loops \(While, For Loop, For Each\) when it is placed in nested activity, is now fixed.
        -   The issue with the Windows legacy form button click that opened a dialog and the control execution hanged for more than 60 seconds, is now fixed.
-   **Version 7.0.1 - December 2023**
    -   New:
        -   Use the GracefulStop component in RPA automations to avoid abruptly stopping an automation. Use the Return data port to automate housekeeping activities such as closing the application in use, perform clean-up operations, and so on.
        -   Convert local variables to global variables to if you have created a variable as local by mistake. If you have a local variable that needs to be used in two activities, you can convert the local variable to a global variable using the Convert to global option for a local variable.
        -   Locate Web UI elements and use this located element to design the automation using the XPath locator. You can select the XPath locator while configuring the screens and elements of a web page by using the Universal App Connector.
        -   Select Shadow Dom elements while configuring the screens and elements of a web page by using the Universal App Connector.
        -   The ability to drag and drop automation items such as components, variables, and activities are now updated for easier modification of automations.
    -   Changed:
        -   Previously, you were able to select an Unattended bot process and view all the robots assigned to it. Due to this, you were able to access sensitive information from other robots. Starting from Vancouver, an RPA developer or administrator can view and select only the assigned robots for Unattended process.
        -   Log component of RPA Desktop Design Studio is moved from the General section of Toolbox to RPA Hub.
        -   The Log component now sends messages to a new table Automation Logs in RPA Hub instead of updating the messages to the log files in your local machine. RPA business users and RPA developers can gain insights into the progress of automation execution. View the message logs at a single, unified space.
        -   Starting from Vancouver, Connection Manager is launched when you start RPA Desktop Design Studio. RPA Desktop Design Studio is launched only after you authenticate your connection using Connection Manager.
-   **Version 5.0.2 - May 2023**
    -   New:
        -   Use the new PDF connector that provides a single, unified space to perform all your PDF operations. Use this connector to accelerate PDF processing in your automation. Use the new PDF methods to load, split, merge, and close PDF files. The connector is available as a plugin by default.
        -   Execute a custom javascript on an application screen open in Microsoft Edge and Google browsers by using the ExecuteJavascript method of Universal App Connector.
        -   Use the javascript locator as a match rule by using Universal App Connector to identify web elements in an automation.
        -   Use actions available in Flow Designer as part of your automation by using the InvokeAction component.
        -   Search and select the list of available flow, subflow, and actions for Flow designer components.
    -   Changed: The PDF connector replaces the existing PDF methods in RPA Desktop Design Studio.
-   **Version 3.0.3 - April 2023**
    -   Fixed:
        -   The issue where the UploadAttachment component was throwing an error with mTLS is now resolved.
        -   The issue where you select Templates while configuring the XmlTemplate using the XmlTemplate Connector is now resolved.
        -   The issue where you are unable to launch Google Chrome and Microsoft Edge browsers in Attended Robot - Desktop in Desktop session when the operating system language is set as Portuguese \(Brazil\) is now resolved.
        -   The issue where the error 'Node was not in a document' is displayed when you select the Table in the XML VIEWER pane of the XmlTemplate connector is now resolved.
        -   The issue where an error is displayed when you delete an attribute from the Configure window of Windows connector is now resolved.
        -   The issue where the SendKeys component was not working when the Clear Existing Value parameter is set as true is now resolved.
        -   The issue where the POST method of the HTTP component is a returning a null response when you run method in RPA Desktop Design Studio is now resolved.
        -   The issue where an unhandled exception is displayed when you double-click a web application in Global Objects, and when the operating system language is set as Portuguese \(Brazil\) is now resolved.
-   **Version 4.1.10 - March 2023**
    -   Fixed:
        -   The issue where the UploadAttachment component is displaying an error when you connect therobot with an mTLS instance is now fixed.
        -   The issue where Windows connector is unable to capture field in Open file or Save as windows in Google Chrome browser is now fixed.
        -   The issue where the GetScreenShot method of Windows connector is failing when RPA Desktop Design Studio is pointed to the latest version and the essential connectors are pointed to the previous versions is now fixed.
        -   The issue where the Save component of Image Utilities is failing when the Overwrite property is set as true is now fixed.
        -   The issue where the IsNullOrEmpty component failed to run when a DB Null value is used from the GetCellValue method is now fixed.
        -   The issue when you try to recapture an element in Universal App Connector for a Windows application and the child element is created in the current element instead of replacing it with recaptured element is now fixed.
-   **Version 4.1.9 - February 2023**
    -   New:
        -   Build automations quickly and easily by capturing the actions that you perform on your desktop or web applications by using the RPA Desktop Design Studio recorder. You can create automation flows by interacting with the applications instead of using connectors or components.
        -   Use the Universal App Connector to provide a single, unified connector to capture elements for your desktop and browser-based applications.
        -   Use the GetProcessJobSysID component to retrieve the process job sys\_id of a process job record.
        -   Use the LockUIDialog component to provide additional authentication to any step of your attended automation.
        -   Validate certificates when you publish a package from RPA Desktop Design Studio and connect to an instance by using Unattended Robot.
        -   Use the new parameter that specifies the value in seconds to time out the request for the DownloadFile and Post components in HTTP methods.
        -   Generate the password during the automation by using the GetTOTP component in RPA Desktop Design Studio.
        -   Enable only the certificates that have the intended purpose as Code Signing for publishing a package in the RPA Desktop Design Studio application.
        -   Enable only certificates that are intended for Client Authentication while connecting to a Mutual Transport Layer Security \(mTLS\) instance in the Unattended Robot application.
        -   View the installed RPA Plugin Bundle version with the MSI version of the RPA Desktop Design Studio, Attended Robot, and Unattended Robot applications on their home pages.
        -   View the updated splash screen of RPA Desktop Design Studio that now includes the connected instance URL.
        -   Configure the elements of a recorded automation as Universal App Connector objects from Global Objects in the Project Explorer pane in RPA Desktop Design Studio.
        -   View Service Logs menu in the Unattended Robot that displays product error logs if there are any exceptions.
-   **Version 3.0.9 - February 2023**
    -   Fixed:
        -   We fixed issues with Open and Close methods for Microsoft Excel and Word connectors.
        -   Internet Explorer \(IE\) compatibility mode is now working in the Microsoft Edge browser.
        -   We fixed issues related to the ForEach component.
        -   We fixed the Unattended Robot unresponsive issue when the robot is idle.
        -   We fixed the "Unhandled Exception" issue while selecting the Match Attributes or Match rules for the configured pages or elements using Non-OS English language.
        -   We fixed the "Unhandled Exception" issue while selecting an element using Japanese language.
        -   We fixed the issue where RPA Desktop Design Studio is unable to load the relevant methods when you capture elements by using the windows connector in a Non-English OS language.
        -   We fixed the issue with backslash trimming in the SetText component \(Chromium connector\).
        -   We fixed the issue with the ReadFromSheet method in the Microsoft Excel connector taking a long time to execute.
        -   We fixed the issue where the skills package is not downloading to the packages folder when only Unattended Robot is installed in the machine.
        -   We fixed t&gt;he issue with file path parameter of the StartNew component \(Utilities and System Process\).
        -   We fixed the issue with saving an automation project due to an alert pop-up.
        -   We fixed the issue with copying an activity with local variables.
        -   We fixed the Try-catch component issue where an error was encountered for child activities.
        -   We fixed the issues with the Assign bot process in RPA Desktop Design Studio.
-   **Version 2.0.7 - February 2023**
    -   Fixed:
        -   The issue with copying an activity with local variables is now fixed.
        -   Intermittent RPC Server unavailability in the Open method of Microsoft connector" issue is now fixed.
        -   The issue with saving an automation project due to an alert pop-up is now fixed.
        -   The issue where the skills package not downloading to the packages folder when only Unattended Robot is installed in the machine is fixed.
        -   The issue with the ReadFromSheet method in the Microsoft Excel connector taking a long time to execute is now fixed.
        -   The issue with backslash trimming in the SetText component \(Chrome connector\) is now fixed.
        -   The issue related to the relevant methods not loading during the capture of the Windows connector elements using Non-OS English language is now fixed.
        -   The "Unhandled Exception" issue while selecting the Match Attributes or Match rules for the configured pages or elements using Non-OS English language is now fixed.
        -   The "Unhandled Exception" issue while selecting an element using Japanese language is now fixed.
        -   The Unattended Robot unresponsive issue when the robot is idle is now fixed.
        -   The issues related to ForEach component is now fixed.
        -   Internet Explorer \(IE\) compatibility mode is now working in the Microsoft Edge browser.
        -   The issue with file path parameter of the StartNew component \(Utilities and System Process\) is now fixed.
        -   The issues with Open and Close methods for Microsoft Excel and Word connectors are now fixed.
-   **Version 2.0.5 - October 2022 \(compatible with San Diego\)**
    -   Changed: Unattended Robot stability is now improved
    -   Fixed:
        -   RPA Desktop Design Studio localisation issue regarding multiple non-English languages is now fixed.
        -   Unattended and Attended Robot skill related issues are now fixed.
    -   **Note:** Ensure to upgrade the current installed MSIs \(Unattended Robot\), if any, by downloading the latest MSIs from San Diego upgraded instance. Then, install those MSIs to ensure a seamless interaction between these and the RPA Hub application.

    -   For more information, see Download the RPA applications from RPA Hub.
-   **Version 3.0.0 - August 2022**
    -   New:
        -   In the RPA Desktop Design Studio, the Cut and Copy options are added in the context menu of all components and methods.
        -   In the RPA Desktop Design Studio, GetResolution component is added. This enables the user to get the resolution of the primary screen.
        -   The ImpersonateAsRobot component is removed from the Toolbox and is now available as Assign bot process under the Design tab in the header of the RPA Desktop Design Studio.
        -   Chrome connector is renamed to Chromium connector. It extends the support for Edge browser.
        -   You can now mark data as sensitive by right-clicking any Data port and selecting the Mark Data as Sensitive option.
        -   The RPA Desktop Design Studio, Attended and Unattended Robots are compatible with Windows Server 2016 and 2019.
    -   Changed:
        -   Changes in the RPA Desktop Design Studio header:
            -   Connection Manager is renamed to Connect to instance.
            -   RPA Hub is renamed to Publish.
            -   The Publish and Connect to Instance options are grouped under the RPA Hub section.
        -   In the RPA Desktop Design Studio, the Chrome, Windows, Java, and IE plugins are available by default under the Connectors category in the Toolbox.
        -   In the RPA Desktop Design Studio, the Random Password component now enables the user to configure the random password complexity by specifying the type of characters, length, and more.
        -   In the RPA Desktop Design Studio, using the new AddRow method of the Table connector, you can add a row in a table at the specified index.
        -   In the RPA Desktop Design Studio, the properties of the Terminate component are now added as data input parameters.
        -   Using the unattended robot login agent, the robot machine can be unlocked even if it is enabled with the Ctrl+Alt+Del screen.
    -   Fixed:
        -   In the RPA Desktop Design Studio, the Java connector is now working with 32-bit apps. \(It is recommended that you install both the 32-bit and 64-bit versions of the JRE. The 32-bit version only adds support for 32-bit assistive technology, and the 64-bit version only adds support for 64-bit assistive technology.\)
        -   In the RPA Desktop Design Studio, the DecryptString component is now working as expected.
        -   In the RPA Desktop Design Studio, the issue with cursor is now fixed and is visible in the Filter by Name field under the Project Explorer pane, the Toolbox pane, the Properties pane, and in component parameters where you input the data.
        -   In the RPA Desktop Design Studio, the issue about the data ports connection is now fixed.
    -   **Note:** Ensure to upgrade the current installed MSIs \(RPA Desktop Design Studio, Attended Robot, and Unattended Robot\), if any, by downloading the latest MSIs from Tokyo upgraded instance. Then, install those MSIs to ensure a seamless interaction between these and the RPA Hub application. For more information, see Download the RPA applications from RPA Hub

        .

-   **Version 2.0.4 - May 2022**
    -   Fixed:
        -   The UploadAttachment method in Attachments component does not require a forward slash \(/\) in the Connection Manager instance URL.
        -   The Boolean input is now supported in the InvokeSubFlow method of the Flow designer component.
        -   Unattended Robot Login Agent is fixed.
        -   Chrome connector is fixed for handling browser idle time.
-   **Version 2.0.3 - March 2022**

    The Robotic Process Automation \(RPA\) Plugin Bundle is the application responsible for building automations. The RPA Plugin Bundle contains Windows library files that are consumed by RPA Desktop Design Studio, RPA Runtime, and RDA Runtime applications. These plugins extend the capability of the RPA product. For instance, RPA Chrome Plugin enables RPA application to automate tasks on the Chrome browser. Similarly, the RPA Excel plugin enables the RPA applications to interact with Excel files and many more. Along with Integration Hub, RPA Plugins Bundle is part of Automation Engine for a complete integration and automation solution for ServiceNow.


**Parent Topic:**[ServiceNow Store - ServiceNow AI Platform App Engine release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-plat-app-engine.md)

