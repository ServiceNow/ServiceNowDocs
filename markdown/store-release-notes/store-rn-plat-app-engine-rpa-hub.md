---
title: RPA Hub release notes
description: Version history for the RPA Hub application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-plat-app-engine-rpa-hub.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 18
breadcrumb: [ServiceNow Store - ServiceNow AI Platform App Engine release notes, ServiceNow Store release notes]
---

# RPA Hub release notes

Version history for the RPA Hub application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 18.0.2 - June 2026**

    Fixed: The issue where the TOTP record could not be deleted when the assigned bot process was in maintenance mode is now fixed.

-   **Version 17.0.0 - March 2026**

    Fixed: When migrating Bot Process from one environment to another environment, the existing skills in the bot process in the target environment were not being overridden, which resulted in creation of duplicate entries is now fixed.

-   **Version 13.2.1 - March 2026 \(Yokohama\)**

    Fixed: When migrating Bot Process from one environment to another environment, the existing skills in the bot process in the target environment were not being overridden, which resulted in creation of duplicate entries is now fixed.

-   **Version 13.2.0 - January 2026 \(Yokohama\)**

    New: Use Now LLM Long-Term Support \(LTS\) model as AI model provider for RPA bot generation skill in addition to Azure OpenAI, Google Gemini, Now LLM, and Anthropic Claude on AWS.

-   **Version 16.0.0 - December 2025**
    -   Changed: Role for Create, Update, and Delete ACLs in the Robot License Distribution table is changed from admin to sn\_rpa\_fdn.rpa\_admin.
    -   Fixed: The issue related to the migration of a bot process from one environment to another when the system language is other than English is now fixed.
-   **Version 15.1.0 - September 2025 \(Zurich\)**
    -   New:
        -   Use the Python connector to execute custom Python scripts or files as part of an automation workflow.
        -   Use a Smart Card authentication for improved security. Use a physical smart card instead of a username and password for logging into a Windows machine.
-   **Version 13.1.0 - September 2025 \(Yokohama\)**
    -   New:
        -   Use the Python connector to execute custom Python scripts or files as part of an automation workflow.
        -   Use a Smart Card authentication for improved security. Use a physical smart card instead of a username and password for logging into a Windows machine.
    -   Fixed:
        -   The issue related to multiple process jobs getting created when the automation is triggered and the robot machine is signed out is fixed now.
        -   The issue related to FormatText component when there is no format defined and left blank gives an error is now fixed.
-   **Version 10.2.0 - September 2025 \(Xanadu\)**
    -   New: Use a Smart Card authentication for improved security. Use a physical smart card instead of a username and password for logging into a Windows machine.
    -   Fixed: The issue with consuming too many robot user sessions is now fixed.
-   **Version 15.0.0 - August 2025 \(Zurich\)**
    -   Fixed:
        -   The issue where two process jobs were created for a single trigger has been fixed.
        -   The issue where the Import functionality could not import an existing activity from a different automation project has been fixed.
        -   The issue regarding the incorrect marking of the application scope for the migrated RPA assets has been resolved.
-   **Version 13.0.1 - June 2025 \(Yokohama\)**
    -   Fixed:
        -   The issue showing Invalid Queue Name after migrating from one environment to another environment is fixed now.
        -   The issue related to Flow Designer Start Process action is triggering the retired robot when a robot with the same name is assigned to the bot process is fixed.
-   **Version 10.0.4 - June 2025 \(Xanadu\)**

    New: Use generative AI to create and edit automations, activities, and extend automation logic flow through text prompts and preview options in the RPA Desktop Design Studio.

-   **Version 13.0.0 - May 2025 \(Yokohama\)**
    -   New:
        -   Support for Active Accessibility when adding elements in the Universal App Connector, using the AA mode.
        -   Support for Windows 11 Operating System for RPA Desktop Design Studio/Unattended Robot/Attended Robot/Login Agent.
    -   Changed:
        -   OCR Text component now uses latest Tesseract engine 5.0. When updating older automations that include the OCR text component, you may notice slight differences in the output. Therefore, it's important to validate your automations after the update.
        -   Enhanced RPA bot generation by adding more components information. For more information about the list of supported components, see Supported components and connectors for Now Assist for RPA Hub in Yokohama release
    -   Fixed:
        -   The "Attachments" parameter in SendMail, Reply, and SentAs methods in Microsoft Outlook connector is modified to address the issue when the file names contain "comma\(,\)" or "semicolon\(;\)" that splits the file using these delimiters and fails. Now, we can separate multiple file paths using "vertical bar or pipe\(\|\)" only. Old automations that use "," or ";" must be updated with "\|", when multiple file paths are passed. This change is required when old automations are upgraded to Plugins above 13.0.
        -   The issue with Try catch not reporting errors from a nested activity is now fixed. The issue was, in a nested activity, if an exception occurred, the try-catch block in the parent activity was not catching it. Try-catch now shows errors that occurred inside an activity within its scope. However, you must test existing automations for expected outcomes.
        -   The issue related to Desktop in Desktop mode on Windows 10 or Windows 11 systems related to administrative access is now fixed.
        -   The issue with PickWorkItem is now fixed, when Robot pool is enabled with Allocation type as SLA Based.
-   **Version 12.0.1 - March 2025 \(Yokohama\)**
    -   Fixed:
        -   The issues related to RPA Hub licensing checks are now fixed.
        -   The issue with the PickWorkItem component failing when the the Request content had array of JSON objects is now fixed.
        -   The issue with the DownloadAttachment component replacing filename with "\_" when the attachment name is having non English text is now fixed.
        -   The issue with the Log component failing intermittently when used in Attended automations is now fixed.
-   **Version 10.0.3 - March 2025 \(Xanadu\)**
    -   Fixed:
        -   The issues related to RPA Hub licensing checks are now fixed.
        -   The issue with the PickWorkItem component failing when the the Request content had array of JSON objects is now fixed.
        -   The issue with the DownloadAttachment component replacing filename with "\_" when the attachment name is having non English text is now fixed.
-   **Version 9.0.2 - March 2025 \(Washington DC\)**
    -   Fixed:
        -   The issues related to RPA Hub licensing checks are now fixed.
        -   The issue with the PickWorkItem component failing when the the Request content had array of JSON objects is now fixed.
        -   The issue with the DownloadAttachment component replacing filename with "\_" when the attachment name is having non English text is now fixed.
-   **Version 12.0.0 - February 2025**
    -   New:
        -   Use generative AI to create and edit automations, activities, and extend automation logic flow through text prompts and preview options in the RPA Desktop Design Studio.
        -   Run multiple unattended robots on different user sessions at the same time on the same Windows Server machine using the high-density robots feature.
        -   Use new sample automations that were added in the RPA Desktop Design Studio that cater to different use cases.
        -   Leverage the communication capabilities of the SSH protocol in the automation processes with the new Secure Shell \(SSH\) connector in the RPA Desktop Design Studio.
        -   Use the SAP connector to identify the screens and elements and to automate workflows on the SAP Graphical user interfaces \(GUI\).
    -   Changed: Support for bypassing Legal notice in Login Agent. This ensures that a legal notice is not displayed during the robot's login process.
-   **Version 10.0.1 - September 2024**
    -   Fixed:
        -   The issue with the Break component not functioning correctly when Break is used in a loop within Skill automation is now fixed.
        -   The issue with the SendKeys component taking long time to enter the text during runtime for Portuguese is now fixed.
        -   The issue with the "There was an error generating the XML document." exception while saving the automation is now fixed.
        -   The issue with the ReadFromRange, WriteToRange, and GetCellcolor Excel methods missing/not working for automations with lesser than 8.0 plugins, when used in latest studio/runtime is now fixed.
        -   The issue with Log Component showing an error when the message passed is empty or null is now fixed.
        -   The issue with Assign bot process giving error when the Bot process doesn't have package/package version is now fixed.
-   **Version 10.0.0 - August 2024 \(Xanadu\)**
    -   New:
        -   Migrate the bot process configuration and associated assets from one environment to another environment with a click of a button.
        -   Create the centralized credentials that you can reuse in multiple bot processes.
        -   View and manage the skill versions used in packages from a central location in RPA Hub. You can override an existing skill version that was used for each bot process.
        -   Use the 15 new sample automations that were added in RPA Desktop Design Studio that cater to different use cases.
        -   Manage sensitive and non-sensitive data in two separate fields of a work item.
        -   Use Guided Tours to get quick instructions on how to create queues and configure bot processes.
        -   Rearrange the recorded actions and screens according to your preference and generate the automation flow.
    -   Changed:
        -   In RPA Hub, the credential sets that were created for a bot process are now replaced with credential groups.
        -   In RPA Hub, when you select the Start Process button, you can't view the robots that are in the In Maintenance life-cycle stage status.
        -   Older MSIs that are related to Unattended Robot, Attended Robot, and RPA Desktop Design Studio from the RPA Hub store release versions 7.0.3 and 9.0.0 are compatible and can be used with this current store release version of RPA Hub.
    -   Fixed: An issue with the break components in the nested activities that failed to break their loops is now fixed.
    -   Removed:
        -   In RPA Hub, the credential set related list was removed from the bot process form.
        -   The RPA Sample templates store application is deprecated and is no longer supported or available for activation. RPA Desktop Design Studio provides the latest experience for this functionality.
        -   In RPA Hub, the Is Request Content Sensitive field in the Queues form is deprecated.
        -   In RPA Hub, the Credential Set field in the Process Robot Credentials form is deprecated.
-   **Version 9.0.0 - May 2024 \(Washington DC\)**
    -   New:
        -   Guided Tour for Queues:

            -   The RPA hub now includes a Guided Tour for Queues, providing a step-by-step walkthrough of queue creation. This auto-launch feature helps new users quickly learn and efficiently use the RPA hub, ensuring they are equipped to handle key functionalities without delay.
        -   Graceful Stop for Robot Pool
            -   The Graceful Stop feature is enhanced to support robot pools. You can now define secure termination points within an automation process, allowing for a smooth exit and proper clean-up of in-use applications. Stop or Graceful Stop of Bot Processes extends to both individual robots and those in a robot pool, with support for both UI actions and Stop Process Flow Designer actions.

            -   Provision to Stop or Gracefully Stop individual Robots from one Bot Process and able to use the released Robot in another Bot Process using Robot Pool.

    -   Changed:
        -   Verify Hashcode FD action:
            -   The new Verify Hashcode action ensures the integrity of automation zip files attached to package version records. This function validates the HashCode of the uploaded file and verifies its authenticity against the respective package version record.
-   **Version 7.0.3 - April 2024 \(Vancouver\)**
    -   Fixed:
        -   The issue where an error "Hashcode validation failed!" is encountered while trying to publish a bot process associated with a code-signed package is now fixed.
        -   The issue where the skill activity ports values are receiving Null, at the time of executing a skill activity, is now fixed.
        -   The issue where the system property "csdm.lifecycle.migration.activated" is enabled to true on platform upgrade or any update on bot process that does not change life cycle stage status, is now fixed.
        -   The issue with unattended robot, when the robot is connected, updates to Bot Process details are causing multiple jobs to be created is now fixed.
-   **Version 8.0.1 - February 2024**
    -   New:
        -   Embedded Task Automation feature enables to trigger attended bot processes \(attended automations\) fromServiceNowforms, playbooks, workspaces, and so on.
        -   Retrieve sensitive information securely, such as user names and passwords, from various external vaults by enabling the external credential vault feature inRPA Hub.
        -   Store the logs of a process execution in a readable format through flat files.
        -   New actions and subflow such asChange Life Cycle Stage Status of a Bot ProcessAction,Stop ProcessAction, andStop ProcessSubflow are available in theFlow Designerthat further refine RPA integration via flows, subflows, and APIs.
        -   New Chrome and Edge Extension 1.6 are released.
    -   Changed:
        -   Manage plugins from a single location
        -   New location for the Attachments andFlow Designercomponents in the Toolbox pane
        -   The name of the element appears in the Name field of the Capture element dialog
    -   Fixed: Intermittent issues with Start Process action are addressed.
-   **Version 7.0.1 - January 2024 \(Vancouver\)**
    -   Fixed:
        -   This patch addresses Empty ACLs related issues.
        -   Robot capacity calculation logic is syncronized for robot pool. At any given point in time, only one robot performs the capacity calculation.
-   **Version 7.0.0 - December 2023**
    -   New:
        -   Access the Help Center that is now available in the RPA Hub instance. Help Center provides targeted help content to users in a UI page. It provides easy visibility to get Help or knowledge content on the same glide record that the user accesses.
        -   Ensure data privacy when you pass sensitive information through the queues by enabling the Is Work Item Content Sensitive field on the Queue form.
        -   View Automation Logs in RPA Hub, which is series of succession stages or a series of checkpoints that occur during the execution of a bot process. It enables monitoring and auditing the automation process. These logs are generated from the robot for unattended and attended bot processes.
        -   Stop the bot process gracefully by enabling the Graceful Stop toggle switch in Stop Process section of the RPA Hub. View the new Graceful Stop field on the Process Jobs form. This field indicates whether the graceful stop is executed or not.
    -   Changed:
        -   On Assigned Studio Users tab in RPA Hub, you can add users to utilize the robots fromRPA Desktop Design Studio, depending on the associated bot process access.

            When RPA Hub components are used in an automation in Studio, you define the unattended bot process and the robot in the Assign Bot Process section. This helps in impersonating as a robot.

            Enable the sn\_rpa\_fdn.restrict\_robots\_in\_assign\_bot\_process\_by\_machine\_name system property to filter the robots assigned to the bot process based on the machine name.

-   **Version 5.0.3 - August 2023**

    Fixed:

    -   The issue with the schedule not getting saved when the end time was given before the start time for future dates is now fixed in both classic environment and workspace.
    -   The issue with the license distribution appending '0' at the end of the added number is now fixed.
-   **Version 3.0.10 - August 2023**

    Fixed:

    -   The issue with the schedule not getting saved when the end time was given before the start time for future dates is now fixed in both classic environment and workspace.
    -   The issue with the license distribution appending '0' at the end of the added number is now fixed.
-   **Version 5.0.2 - May 2023**
    -   New:
        -   Import package version attachments automatically instead of manually uploading a package version attachment, by selecting the Import Attachment button on a package version.
        -   Optimize robots utilization better, since both the unattended bot process and robot are now agnostic of trigger mode - Schedule or API. After assigning a bot process, any unattended robot can now run the process through schedule or API. It eases in creating and maintaining bot processes, as well.
        -   Manage \(create, update, and delete\) schedules on robot calendar. Optionally, you can publish bot processes from the calendar.
        -   Identify any conflicts in the schedule by selecting the Preview button on the robot calendar. To resolve the conflicts, you can either edit or delete the schedule on the robot calendar. To view additional details of the event, you can right-click the schedule and select View event details.
        -   Help alleviate eye strain by switching to a dark theme or mode that is available in Workspace for Robot Calendar, RPA Hub landing page, Overview page, RPA Hub properties.
    -   Changed:
        -   View robot calendar for unattended robots with active, inactive, and no schedules, that are associated with unattended bot processes.
        -   View robots in Busy state along with the robots in Available state when you start an unattended bot process, to facilitate process job queuing.
        -   Business users can now view the Run Time Threshold \(mins\) and Order fields on the Bot Process form and Bot Process Configuration form.
        -   Business users can now view the events and schedules on the robot calendar along with timezone, filters, month, week, and day views.
        -   Business users can now view RPA Hub workspace landing page.
    -   Removed: Trigger Mode field is removed from the Bot Process form, Bot Process Configuration form, Start Process Action, and Start Process subflow, for an optimum utilization of robots. Run an unattended robot to execute the unattended automations that are triggered either by a schedule, API, or manually.
-   **Version 4.1.2 - March 2023**

    Fixed: The issue with RPA admins and RPA release managers unable to view the Upload Attachment button \(in classic environment\), Browse button \(in workspace\), and Verify Hash Code button on the package version page is now fixed.

-   **Version 4.1.1 - February 2023**
    -   New:
        -   Increase product adoption by enabling personal developer instance \(PDI\) users to access RPA Hub.
        -   Use update sets to move Robotic Process Automation \(RPA\) configurations seamlessly across instances.
        -   Use the new table Bot Process Configuration that extends sys\_metadata. A bot process configuration is a record that contains the bot process settings.
        -   Use the robot calendar to visually determine the availability of robots and to optimize the utilization of robots.
        -   Enable unattended robots to authenticate seamlessly against multi-factor authentication \(MFA\)-enabled applications by using the new Time-based OTP \(TOTP\) fields.
        -   Retry your failed work-queue items based on the Application exception type by using auto-retry.
        -   Use the new action Update Process Parameter in Flow Designer to update the Value field of the process parameter.
        -   Use the new field, Triggered By, on the Process job form to identify the bot process trigger source.
    -   Changed:
        -   You can now start a robot in busy state if the Trigger Mode of the associated bot process is API. You can perform this action only in the Classic environment.
        -   Business users now have access to the Start Process and Stop Process UI actions on the Bot Process form. However, they must be a part of the Managed By Group list to access this functionality.
-   **Version 3.0.9 - February 2023**
    -   Fixed:
        -   We fixed an issue where the process jobs are not starting and changing to abandoned state when you upgrade the RPA Hub plugins to the Tokyo version is now resolved.
        -   We fixed an an issue where the machine name appearing twice in the Robot field of the Process Jobs form.
        -   We fixed an issue with monthly interval schedules. Previously, the interval frequency was triggered from the month of January and not the selected start date of the month.
        -   We fixed an issue with the scheduled job to purge work items.
        -   We fixed an issue with RPA release managers unable to view the process jobs and RPA business users unable to view the robots in the navigator menu.
        -   We fixed an issue with blank email being sent when the email has html tags.
        -   We fixed an issue where RPA developers and RPA support users can view the Edit button in the Bot process related list of the Shared parameters and Queues forms.
        -   We fixed an issue where RPA developers and RPA support users can view the associated bot processes in the related list of Shared parameters is now fixed.
        -   We fixed an issue with the validation for Start Date field on the Schedules form. 
        -   We fixed an issue where RPA developers can view the New button in the Shared parameters page.
        -   We fixed an issue with the expired schedules for a bot process.
        -   We fixed an issue with the process job not creating in the virtual machine. This issue occurred in RPA Hub when Start Process was selected.
-   **Version 2.0.10 - February 2023**
    -   Fixed:
        -   The issue with the process job not creating in the virtual machine is now fixed. This issue occurred in RPA Hub when Start Process was selected.
        -   The issue with the expired schedules for a bot process is now fixed.
        -   The issue with Shared Parameters access control rule \(ACL\) is now fixed.
        -   The issue where RPA developers and RPA support users can view the Edit button in the Bot process related list of the Shared parameters and Queues forms is now fixed.
        -   The validation for Start Date field on the Schedules form is now fixed.
        -   The issue with blank email being sent when the email has html tags is now fixed.
        -   The issue with RPA release managers unable to view the process jobs and RPA business users unable to view the robots in the navigator menu is now fixed.
        -   The issue with the scheduled job to purge work items is now fixed.
        -   The issue with monthly interval schedules is now fixed. Previously, the interval frequency was triggered from January month and not the selected start date of the month.
-   **Version 2.0.8 - October 2022 \(compatible with San Diego\)**
    -   Fixed:
        -   The trigger issue for schedules with weekdays for non-English languages for Unattended Robot is now fixed.
        -   The published attended bot processes that are previously not listed for non-English languages in Attended Robot is now fixed.
        -   The "Studio plugin not found" issue for date time format is now fixed.
-   **Version 3.0.7 - August 2022**

    New:

    -   A new Overview tab in RPA Hub give a unified experience of unattended and attended bot processes.
    -   Internationalization support for RPA Hub scoped application. RPA Hub supports all languages offered by the NOW platform.
    -   A new "Update Work Item" action in Flow Designer for updating work queue items is introduced.
    -   Unattended robots can now be referenced from CMDB CI to map robot machines.
    -   Two new fields \(Managed By Group and Owned By\) are introduced in the Bot process form for better process governance.
-   **Version 2.0.6 - May 2022**
    -   Changed:
        -   The labels RPA Desktop Studio, Attended Robot, Unattended Robot, and Unattended Robot Login Agent are updated on the RPA Downloads page.
        -   The name field is updated with Robotic Process Automation's Application Menu.
    -   Fixed:
        -   The action or subflow with the Start Process action or subflow can be saved while using the Flow Designer.
        -   The Queue summary section is fixed on the RPA Hub landing page.
-   **Version 2.0.4 - March 2022**

    The Robotic Process Automation \(RPA\) Hub provides the capability to integrate the ServiceNow platform with applications that do not support APIs. RPA Hub enables deployment, management and monitoring of attended and unattended automations. It allows developers to store automation packages, configure attended and unattended robots, manage queues, store application credentials, and monitor alerts. Along with Integration Hub, RPA Hub is part of Automation Engine for a complete integration and automation solution for ServiceNow.


**Parent Topic:**[ServiceNow Store - ServiceNow AI Platform App Engine release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-plat-app-engine.md)

