---
title: Agent Workspace for HR Case Management release notes
description: Version history for the Agent Workspace for HR Case Management application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-hr-agent-workspace-hr-case-mgmt.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 12
breadcrumb: [ServiceNow Store - HR Service Delivery release notes, ServiceNow Store - Employee Service Management release notes, ServiceNow Store release notes]
---

# Agent Workspace for HR Case Management release notes

Version history for the Agent Workspace for HR Case Management application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 4.6.0 - June 2026**
    -   Fixed:
        1.  Security &amp; data protection: Closed an ACL bypass vulnerability in the email utility script include and ensured the At a Glance view honors ACLs, so protected HR data is no longer exposed.
        2.  Stability &amp; runtime errors: Eliminated server-side errors across HR case flows—including sentiment analysis on multiple HR tables, case creation from interactions, and PDF document-template tasks.
        3.  Knowledge management: Fixed Knowledge blocks failing to load, custom-template articles opening in the wrong view, form values resetting with multiple forms open, and made the enhanced content editor available to non-GenAI customers.
        4.  Case creation &amp; handling: Enforced custom mandatory-field validation, preserved Short Description/Description edits on Close Incomplete, fixed the Close Complete button after activity-stream comments, and corrected fields hidden by non-workspace view preferences.
        5.  Agent Workspace usability: Resolved stuck reference-field previews, interceptor subtab loading, interaction close, worker config updates, UX List fixed queries, and Move Attachments behavior.
        6.  Localization &amp; catalog: Fixed playbook string translation caching and restored missing fields on the Travel Reimbursement catalog item.
-   **Version 4.5.1 - April 2026**

    New: Workspace UI components for AI Execution and AI Configurations \(for specific AI features not all\)

-   **Version 4.4.1 - March 2026**
    -   New:
        -   HR Profile View in Case Creation Step 2 - HR Profiles of both "Opened For" and "Subject Person" are now available.
        -   Advanced Knowledge Editor
            -   Advanced knowledge editor with new tools, within workspace, to help create, enhance, and manage knowledge content faster and efficiently.
            -   Now Assist can be used to create or enhance knowledge article from within the Advanced knowledge editor. Article Optimization scans knowledge articles to get instant, actionable feedback.
-   **Version 4.3.1 - December 2025**
    -   New:
        1.  Genesys Integration - Seamless integration with Genesys via Native Voice Control for inbound and outbound calling
        2.  Interaction Wrap-up - Enables HR Agents to enter closing details and wrap up the conversation after closing voice interactions . New list view for viewing the Wrap ups
        3.  Added Close notes field by default in HR Case record page
    -   Fixed: Minor bug and accessibility fixes
-   **Version 4.2.0 - August 2025**
    -   New:
        1.  HR Agent Workspace - Performance Enhancements \(At A Glance, Playbook, Life Cycle Events and minor UI Elements\)
        2.  HR Agent Workspace now supports coral theme
        3.  Case Summarisation can now be shortened or elaborated using a single click in the Case summarisation section
    -   Fixed:
        1.  For HR service: Verification of Employment, Document template category and Document template fields are now visible in HR Agent Workspace
        2.  Creating a new case from the 'Child Cases' related list on HR Agent Workspace will now always skip step 1 \(employee selection\)
        3.  The Data Policy Exception error message 'The following fields are mandatory: Close notes' will not be visible when the Close notes are already available
        4.  Fixed the Contextual Sidebar availability issues in HR tasks
        5.  Fixed the Preview document error in HR Agent Workspace
-   **Version 4.0.2 - June 2025**
    -   Fixed:
        -   The New Evidence Creation button is now working as expected.
        -   When creating an HR case from an interaction, the HR case opens in the same sub tab within the parent interaction tab.
        -   The card footer is now auto refreshing on adding approvers and rejecting the approval in the playbook.
        -   All HR criteria is now visible to agents on Agent Workspace when creating a segment group for bulk case.
-   **Version 3.3.4 - June 2025**
    -   Fixed:
        -   The email client template that is created in the HR Agent Workspace application scope will now be visible in the HR Agent Workspace.
        -   Agents can now change the state of an interaction from the State drop-down.
        -   If case fields are added in case creation configuration and not available in the default view of the table, an error will be shown when creating a case from HR Agent Workspace.
        -   The Case Tab title can now be configured from the system page properties.
        -   The HR Case short description will not be overriden using the value from the HR Template; the manually entered value will persist.
        -   When creating an HR case from an interaction, the HR case opens in the same sub tab within the parent interaction tab.
        -   All actions are now supported when creating an adhoc task of type 'Flow'.
-   **Version 2.1.8 - May 2025**
    -   New:
        -   Support creation of firmware records in firmware table.
        -   Prevent import of empty rack slots into CMDB.
        -   Introduce new table to store class mappings for Claroty CTD SGC
        -   Update the SGC to support the new ire\_criterion\_attribute on the OT entity table.
        -   Supports Claroty CTD 5.1 APIs as well.
-   **Version 4.0.0 - February 2025**
    -   New:
        -   HR Walkup Experience - Employees can now request an appointment from HR agents, HR agents can now manage their walk-up appointments from the list view of their Agent Workspace.
        -   Delegation Management from HR Agent Workspace - HR agents can now establish delegation for their HR Cases and Tasks. HR agents can also view and manage their delegates, delegators and delegated tasks and cases in their Agent Workspace.
        -   Bulk Case Creation Configuration - Bulk case creation for a given service will now follow the same configuration as defined for the individual case creation.
        -   Preview PDF Document Template - HR Agents can now preview a PDF document template in their Agent Workspace itself, earlier this was possible only in UI 16.
        -   ER Reporting View - The data across 'ER cases', 'Allegation', 'Allegation Type', 'Interviews', 'Involved party', Evidence', and 'Corrective Action' tables have now been joined together to bring a unified view for ER reporting purposes.
        -   Contextual Side Panel configuration - New tabs can now be configured in the contextual side panel.
        -   Adding Child Cases from HR Agent Workspace - Child cases can now be directly added to a case from the Agent Workspace.
        -   Applying Response Template from HR Agent Workspace - HR Agents can now apply response template from their Agent Workspace.
        -   Copy HR Case - HR Agents can now create a copy of an HR Case from a single click in their Agent Workspace, the fields to be copied in the new case are configurable.
        -   Reminder to other HR Agents - HR Agents will now be able to add other HR Agents while adding a reminder.
        -   Download All Attachments - Multiple attachments in an HR Case can now be downloaded at once.
        -   Response Template Filtering - The response templates configurations have been updated to support language based filtering of the templates.
        -   Collect Employee Input - HR Agents can now access employee inputs directly on HR tasks.
        -   HRSD Triaging Dashboard - A customizable dashboard with a drag and drop like experience is now available for the HR Agents to get an overview of their cases, based on various filters like COE, Services etc.
        -   AWS Configuration Preview - A new Preview' button is now available in the configurations, with this preview option admins will now be able to view a screenshot/image of the workspace- that focuses on the area where the changes will occur.​
        -   HRSD Benchmarking - HR Data of various ServiceNow HRSD customers will be compiled together to bring a competitive overview of the HR Processes and Practices.The data is stored securely and appropriately aggregated and tokenized to avoid any data breach.
    -   Fixed:
        -   Issues around Create Knowledge action from workspace has been resolved.
        -   Issues around accessibility of 'Search button' has been improved.
        -   Resolution notes popup will come up in HR agent workspace when closed complete action is clicked.
        -   Sidebar tab Agent Assist will now not disappear after creating universal request.
        -   Case tab title can now be changed from the case tab title configuration of HR Agent Workspace.
-   **Version 3.3.1 - November 2024**
    -   Fixed:
        -   Few events are not displayed on the ER timeline
        -   HR Agent workspace card realignment issues on the landing page
        -   Response template not working
        -   Accessibility fixes
        -   Security fixes
-   **Version 3.1.5 - November 2024**
    -   Fixed:
        -   HR Agent Workspace At a Glance contact card fields appear in the wrong order
        -   The case form opened in Agent Workspace for the HR case COE is taking default view instead of workspace UIB view
        -   Few events are not displayed on the ER timeline
        -   Child case event icon is not displayed on the timeline
        -   Some message in "This case may already exist" popup in HR Agent Workspace is not translated in Japanese
        -   Scripted Template fields not working in Workspace on the Case Creation page
        -   \[GENAI\] Auto opening of knowledge creation record in Agent workspace for HR
        -   \[GENAI\] Auto opening of knowledge creation record and resolution notes modal on case creation
-   **Version 3.2.1 - August 2024**
    -   New:
        -   Landing Page Improvements - Performance improvements and a mult-tab structure to the Landing page
        -   Response templates for HR Tasks
        -   Guided Decision Trees for a better triaging process
        -   Uploaded attachments in Personal Notes
        -   Guided Tours for HR Agent workspace
    -   Changed:
        -   Ability to see the HR service description in the Step 1 of case creation
        -   Recently updated cases in the List view
        -   Ability to show the meeting details in Employee center for "Meeting" task type
-   **Version 3.1.3 - July 2024**

    Fixed at a glance contact card fields appearing in the wrong order.

-   **Version 3.1.2 - May 2024**
    -   New:
        -   Create bulk cases
        -   Report a Knowledge gap
        -   Added a Priority column in the List view
        -   Ability to have read only access in the workspace
-   **Version 2.3.0 - February 2024**

    New: Provide a summary during hand-off to help the agent taking over a task to ramp up faster.

-   **Version 3.0.1 - February 2024**
    -   New:
        -   Document Security on HR Cases - Ability to add additional security on documents that are in the case
        -   New HR Task Type - Schedule a Meeting - Helps agent schedule an in-person meeting with the employee
        -   Dashboards in Analytics Center on Sidebar - The Analytics center sidebar in the configurable Agent Workspace will now have reports that were part of the Platform Analytics Workspace
        -   Configurations Settings Page - A dedicated configuration setting page which will have configurations related to Landing, Record, List and Case Creation Page
        -   New Case Creation Page - A new variant was created with a more modular approach so that the customers can duplicate the variant and customize it
    -   Changed:
        -   Checklists - Ability to create, edit, rename and reorder checklists
        -   ER List Enhancements - Separate section for Employee Relations cases
        -   Personal Notes - A Personal Notes section on HR Cases where agents can write notes that are accessible just to them
        -   Automatically associate the interaction creation with an HR Case
        -   Added popovers to the Record page
        -   Added reasons for Transfer case
        -   Ability to tie the Corrective Action directly with the Allegation/Subject of Allegation for Employee Relations cases
    -   Fixed:
        -   Performance improvements in the case page
        -   Improved logging of work notes in the Activity Stream
        -   Parity with the platform view of showing the same data points while creating HR cases for an inactive user
        -   "At a Glance" translation fixes in multiple languages
        -   User Criteria being applied to "Subject Person" and not to "Opened for" during HR Case Creation
        -   Open the HR Profile field decorator in the Case creation page
-   **Version 2.2.3 - September 2023**
    -   New
        -   Enable HR agents to generate the summary of a case through Now Assist for HRSD
        -   Enable HR agents to generate the resolution notes of a case through Now Assist for HRSD and append it in the Activity Stream
        -   Enable HR agents to get a conversation summary while the case gets handed over from a Virtual Agent through Now Assist for HRSD
        -   Enable HR agents to get a chat wrap up summary of the whole conversation through Now Assist for HRSD
-   **Version 2.0.2 - September 2023**
    -   Fixed:
        -   Special Handling Notes.
        -   Changing the ServiceNow profiles in the Create Case Page.
        -   The case creation message is displayed as a banner in case form even for closed and it is reappearing whenever Agent Workspace is refreshed.
        -   Creating an HR case from the interaction is not generating a Create operation interaction related record.
        -   Recent Cases within the At A Glance view display the current date instead of their original opened date.
        -   The View All cards on the landing page do not use the filters defined in the Card List Configuration records.
        -   The broken carousel on the Landing page.
        -   Selecting an HR Service refreshes the page and clears any text entered in the Work Notes when creating an HR Case.
-   **Version 2.1.1 - August 2023**
    -   New:
        -   Enable the Analytics sidebar icon in AWS Target
        -   Enable the agent assist, employee document and response template configurations for disabled COEs
        -   Enable the comments and compose section for disabled COEs inside of Workspace
        -   Push scope RCAs for HR Agent Workspace to HR plugins
        -   Updates to the template of standard record page and list template
    -   Fixed:
        -   User presence;component is straying away from the Activity Actions group
        -   Buttons for activity actions are not scaled to view when the chat window is open;
        -   HR Agent workspace data broker ACLs do not have the right roles assigned
        -   Compose section is not visible in activity stream for an interaction that is created;
        -   Cosmetic issues on add approvers modal in Workspace
        -   Typeahead component is validating fields even when null is being passed as value into the typeahead value in Vancouver
        -   Schedule Calendar invite button tooltip is not defined, tooltip shows 'Undefined'
        -   'SLA at risk' and 'All cases' carousel is broken, a blank card is displayed for agent\(case\_writer\)
        -   Activity Stream is not available in comments/Work notes modal in playbook on Configurable workspace
        -   HR UIB module navigation link
        -   Clicking the New related list action redirected to page not found
        -   SNow profiles changing in Create Case Page
        -   Case creation banner message is displayed whenever a case is reloaded
        -   Multiple cases are being created when the Create Case button is clicked multiple times
-   **Version 2.0.1 - June 2023**

    Fixed:

    -   Fulfilment instructions shows an error when a KB article created from template is attached to it.
    -   Creating a case from an HR profile when opened for/subject person is pre-filled.
    -   Deep links on workspace.
    -   Few case fields are clearing out when creating a case.
    -   Reply button in activity stream does not work as expected.
    -   Category picker does not work in knowledge form.
    -   Internal server error when searching for users in the Create case page.
-   **Version 2.0.0 - February 2023**

    Changed: Uptake of the new standard record page and make use of the controllers/presets work developed by UXF and UIB teams. This doesn't include any changes in the feature.

-   **Version 1.1.1 - August 2022**
    -   Changed:
        -   Allow agents to add an ad hoc approval for HR cases
        -   Customize tab labels on HR cases
        -   View approval history in activity stream
        -   Improving search functionality during case creation
        -   Transferring attachments from an interaction to a case
        -   Adding e-sign functionality for old and new document templates
        -   Adding preview functionality for HTML attachments on HR cases for new document templates
        -   Adding Save feature in e-sign functionality for HR case
        -   Adding send email functionality for old and new document templates
        -   Updating at a glance data based on subject person changes
-   **Version 1.0.7 - April 2022**

    New: This is a minor release which includes localization upgrades, fixes and performance improvements.

-   **Version 1.0.5 - March 2022**

    The Agent Workspace for HR Case Management app is a new re-factored workspace for HR agents. The new UI Builder-based workspace is more configurable. Admins can use the HR Configurable Workspace Guided Setup to configure the workspace for their agents needs.


**Parent Topic:**[ServiceNow Store - HR Service Delivery release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-hr.md)

