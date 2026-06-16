---
title: Process Automation Designer release notes
description: Version history for the Process Automation Designer application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-platcap-rn-process-automation-designer.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 12
breadcrumb: [ServiceNow Store - Other ServiceNow AI Platform Capabilities applications, ServiceNow Store - ServiceNow AI Platform Capabilities release notes, ServiceNow Store release notes]
---

# Process Automation Designer release notes

Version history for the Process Automation Designer application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 29.3.2 - June 2026 \(Australia\)**
    -   New:
        -   Playbook authors can add standalone AI skills, such as sentiment analysis, summarization, and content generation, as activities in a playbook without requiring full agentic orchestration.
        -   Playbook authors can generate an AI-generated summary of a playbook’s purpose, structure, and logic to better understand existing workflows withut additional documentation.
        -   Playbook users can select "Show Details" on an AI Agent activity card to inspect the steps executed and inputs provided during an agent run.
        -   Activity authors can configure a custom child agent within an activity to enable delegation to a specialized agent during playbook execution.
-   **Version 28.5.4 - June 2026 \(Zurich\)**
    -   New:
        -   Playbook authors can add standalone AI skills, such as sentiment analysis, summarization, and content generation, as activities in a playbook without requiring full agentic orchestration.
        -   Playbook authors can generate an AI-generated summary of a playbook’s purpose, structure, and logic to better understand existing workflows withut additional documentation.
        -   Playbook users can select "Show Details" on an AI Agent activity card to inspect the steps executed and inputs provided during an agent run.
        -   Activity authors can configure a custom child agent within an activity to enable delegation to a specialized agent during playbook execution.
-   **Version 29.2.1 - April 2026 \(Australia\)**
    -   New:
        -   Use latest AI models that offer improved accuracy for Playbook generation, hydration, and activity assist scenarios.
        -   Run hybrid Agentic activities in Playbooks as the user who triggers a playbook.
-   **Version 28.4.8 - April 2026 \(Zurich\)**
    -   New: Run hybrid Agentic activities in Playbooks as the user who triggers a playbook.
    -   Fixed:
        -   Playbook authors couldn’t resolve start rule errors after deleting a variant and returning to the base variant.
        -   The UI Layout tab was missing when editing activities that support layout configuration.
        -   Saving a trigger condition after reactivating a playbook resulted in a Missing parent record error.
        -   In the Automation tab, selecting a new data pill path didn’t update the previously selected path.
-   **Version 28.4.6 - April 2026 \(Zurich\)**
    -   Fixed:
        -   Playbook authors couldn’t resolve start rule errors after deleting a variant and returning to the base variant.
        -   The UI Layout tab was missing when editing activities that support layout configuration.
        -   Saving a trigger condition after reactivating a playbook resulted in a Missing parent record error.
        -   In the Automation tab, selecting a new data pill path didn’t update the previously selected path.
-   **Version 29.1.15 - March 2026 \(Australia\)**
    -   New:
        -   Playbooks on demand – Launch playbooks on demand to support flexible, event‑driven scenarios.
        -   Nested Playbooks \(Designer\) – Compose Playbooks using nested structures for modularity and reuse.
        -   Agentic Playbooks with expanded model support – Test new third‑party models to enhance playbook generation and agentic workflows.
        -   Emails from personal inboxes – Support email actions from personal inboxes through SOM dependency support.
    -   Changed:
        -   Playbooks on demand – UI &amp; Creation – Updated designer experience improves clarity and usability.
        -   Guided Decisions playbook controls – Designers can restrict creation to Guided Decision Playbooks for better governance.
        -   On demand launch permissions – New permissions control who can launch Playbooks on demand.
        -   Data retention for on demand Playbooks – Updated retention behavior aligns with compliance requirements.
        -   Recommended actions enhancements – Improved recommendations help designers build Playbooks more efficiently.
    -   Fixed: Accessibility improvements \(WCAG\) – Enhanced screen reader and voice over support.
-   **Version 28.4.5 - March 2026 \(Zurich\)**
    -   New:
        -   AI agent as an activity
            -   Add your own AI agent as an activity while authoring your Playbook and run AI agent during Playbook run time experience. AI agent's outputs can be reused in subsequent activities in a playbook.
        -   Agentic Playbooks authoring uplift
            -   Playbook authors will be able to understand when an activity has potential to add AI agent and when AI agents are added at activity level.
        -   Visual uplift
            -   With visual uplift, Playbook authors will be able to access playbook generation features with a distinct and uplifted experience.
-   **Version 28.3.10 - February 2026 \(Zurich\)**
    -   Fixed:
        -   Resolved an issue in the auto archiving playbook execution record script
        -   Checklist activity was not working for non-admin users
-   **Version 27.5.2 - February 2026 \(Yokohama\)**

    Fixed: Checklist activity now works for non-admin users

-   **Version 27.5.1 - January 2026 \(Yokohama\)**
    -   Removed: The now.assist.creator role for Playbook generation is removed. Playbook authors can generate Playbooks by using Now Assist if the Playbook generation skill is enabled.
    -   New: If the Playbook generation skill is not enabled, the Build with Now Assist screen displays a message prompting users to enable the skill.
-   **Version 28.3.8 - December 2025 \(Zurich\)**
    -   New:
        -   Added the ability to create decision branches between stages
        -   Added the ability to set child variants to evaluate later in a playbook
    -   Changed: EnabledAI Agents to complete activities without human intervention
-   **Version 28.2.4 - October 2025**

    Changed:

    -   Added global knowledge graph support for Agentic Playbooks
    Fixed:

    -   Corrected ACLs for Questionnaire Activity permissions
    -   Corrected left side panel behavior in Playbook Designer
    -   Removed AI Agent usage for Checklist Activity
    -   Corrected Start Rule field for Creator Studio
-   **Version 26.3.4 - October 2025**

    Changed: Updated ACLs so that only users with the playbook.write and now.assist.creator roles can use playbook generation skills

    Fixed:

    -   Corrected localization behavior
    -   Corrected behavior for playbook generation with images
    -   Corrected field and tab errors in right side panel in the Playbook Designer
    -   Made other ACL updates
-   **Version 28.1.4 - September 2025 \(Zurich\)**

    Changed: Removed unused client scripts and handled events from the Create Records Activity UI.

-   **Version 28.2.3 - September 2025 \(Zurich\)**

    New: Added agentic playbooks. Combine the power of AI agents with pre-defined, customizable playbooks, organizations can streamline processes, reduce manual effort, and achieve higher levels of efficiency. Enable form-based activities to be pre-filled by AI Agents, accelerating manual human work. Humans in the loop will review and modify or accept AI Agent suggested form values before marking activities as complete. Human agents can also view the AI Agents' reasoning and progress via the Now Assist panel.

-   **Version 27.4.5 - September 2025 \(Yokohama\)**

    New: Added ACL for playbook generation skills

-   **Version 28.1.7 - August 2025 \(Zurich\)**
    -   New:
        -   Added support for multiple triggers
        -   Added support for scheduled triggers
        -   Added custom runtime permissions for a read-only view and more granular access filters
    -   Changed:
        -   Added support for pills in HTML fields and List fields
        -   Updated Start Rules
-   **Version 27.3.2 - August 2025 \(Yokohama\)**
    -   Changed:
        -   Added Microsoft Azure, Google Gemini and Claude model support for playbook generation with text input.
        -   Added Google Gemini and Claude model support for playbook generation with image input.
-   **Version 27.2.4 - May 2025 \(Yokohama\)**

    Playbook generation is now supported by RAG based hydration. This will help in replacing placeholder activities with custom activities, out of the box activities and automation assets such as flows, sub-flows and actions.

-   **Version 26.3.1 - May 2025 \(Xanadu\)**

    New: Generate a playbook via API in other ServiceNow application experiences such as IT Operations Management.

-   **Version 27.1.8 - March 2025 \(Yokohama\)**

    Fixed: Corrected to allow delegated developers and admins to test playbooks.

-   **Version 26.2.12 - March 2025 \(Xanadu\)**
    -   Fixed:
        -   Corrected start rule and decision branch behavior for variants
        -   Corrected refresh behavior for Diagram view
-   **Version 25.3.15 - March 2025 \(Washington DC\)**
    -   Fixed:
        -   Stopped showing inactive fields in dot-walk data
        -   Stopped closing the side panel when navigating to a non-input element via keyboard and pressing enter
        -   Corrected to allow delegated developers and admins to test playbooks
-   **Version 27.1.7 - February 2025 \(Yokohama\)**
    -   New: Playbook generation API to enable playbook generation in other ServiceNow application experiences
    -   Changed:
        -   The trigger node in the playbook diagram view has been re-labeled to 'Start'
        -   Updated the Checklist activity, allowing configuration of checklists directly in the playbook designer
        -   Updated Now Assist icons and animations to indicate when Now Assist skills are in use
-   **Version 27.1.5 - February 2025**
    -   New
        -   Playbook generation API to enable playbook generation in other ServiceNow application experiences
    -   Changed
        -   The trigger node in the playbook diagram view has been re-labeled to 'Start'
        -   Updated the Checklist activity, allowing configuration of checklists directly in the playbook designer
        -   Updated Now Assist icons and animations to indicate when Now Assist skills are in use
-   **Version 26.2.11 - January 2025 \(Xanadu\)**
    -   Fixed:
        -   Corrected to display all records when configuring the Form View in the UI Layout tab
        -   Stopped closing side panel when showing additional properties with keyboard navigation
        -   Corrected playbook variant behaviors when it comes to the undo action, overridden activities, and parent variants
        -   Corrected questionnaire activity behaviors when adding questions with string format responses, editing existing questionnaire activities, and testing or activating playbooks
-   **Version 25.3.14 - January 2025 \(Washington DC\)**
    -   Fixed:
        -   Corrected to display all records when configuring the Form View in the UI Layout tab
        -   Stopped closing side panel when showing additional properties with keyboard navigation
-   **Version 26.2.7 - December 2024 \(Xanadu\)**
    -   Fixes for variant feature related bugs
    -   Generic fixes related to Diagram view
    -   Image upload size limit based on system property configuration
    -   Playbook generation bug fixes
-   **Version 25.3.13 - December 2024 \(Washington DC\)**

    Fixed: Updated to exclude inactive fields from the dot-walking experience.

-   **Version 26.1.9 - September 2024 \(Xanadu\)**
    -   Fixed:
        -   Updated recommendations to appear on placeholder activities when swapping activities.
        -   Updated schedule tab to load in the playbook properties modal.
        -   Corrected tooltip behavior on recommended activities.
        -   Added a skill\_id to playbook recommendation skill configurations.
        -   Updated the new delegated\_admin role to no longer prevent other delegated developers from performing Create, Read, Update, and Destroy operations.
        -   Updated process definition updates to move to the the currently selected update set instead of the default update set.
        -   Corrected loading for duplicated playbooks.
        -   Corrected undo function to actually remove parallel branches.
        -   Corrected notification behavior for duplicated playbooks.
        -   Added aria-labels.
-   **Version 25.3.6 - September 2024 \(Washington DC\)**
    -   Fixed:
        -   Stopped activities from starting before the specified starts with delay time.
        -   Corrected undo/redo behavior for the automation tabs.
        -   Updated the new delegated\_admin role to no longer prevent other delegated developers from performing Create, Read, Update, and Destroy operations.
        -   Updated process definition updates to move to the the currently selected update set instead of the default update set.
        -   Corrected loading for duplicated playbooks.
        -   Corrected undo function to actually remove parallel branches.
        -   Corrected notification behavior for duplicated playbooks.
        -   Updated to reload in Workflow Studio when deleting a process.
-   **Version 26.1.8 - August 2024 \(Xanadu\)**
    -   New:
        -   Added the ability to preview and modify your prompt before building your playbook.
        -   Added AI generated suggestions on activities to replace placeholder activities with.
        -   Added theQuestionnaireactivity to allow collecting up to 10 pieces of information from an agent or fulfiller to use later during a playbook run, without needing to create a data definition. Add, edit and remove questions in Workflow Studio without breaking the playbook for agents during runtime.
        -   Added the ability to reference Questionnaire answers in subsequent activities and decision branches.
    -   Changed:
        -   Improved load time of playbooks in Workflow Studio.
        -   Updated diagram view to match the builder theme.
    -   Removed: Removed theCollect User Dataactivity from the activity picker. Use theQuestionnaireactivity instead.
-   **Version 25.3.4 - August 2024 \(Washington DC\)**
    -   Fixed:
        -   Restored missing duplicate button.
        -   Fixed errors in the Playbook Generation example directions.
        -   Disabled optional activities in Creator Studio.
        -   Fixed disappearing validation errors.
        -   Fixed issues with Form Views fields saving the title instead of name of Form View.
        -   Corrected activity organization in activity picker.
        -   Fixed loading issues when editing sub-flows in Flow Designer.
        -   Fixed run conditions that were not saving.
        -   Increased timeout on activation for large playbooks.
        -   Restored missing input display preferences on upgraded process.
        -   Fixed issue where scope user session could scope when editing a playbook.
        -   Restored default activity picker in App Engine Studio.
        -   Playbook modifications now appear in correct update set.
        -   Restored ability to delete query conditions that contain pills.
        -   Fixed side panel collapse issues.
        -   Improved handling of typos in Playbook Generation.
        -   Increased timeout on playbook migrations.
        -   Improved sequential vs parallel activity handling in Playbook Generation.
        -   Fixed XML files to no longer convert to TXT files.
-   **Version 25.2.16 - July 2024 \(Washington DC\)**
    -   Fixed:
        -   Updated condition builder to save when you delete a condition field.
        -   Extended processing time from 30 to 300 seconds for large playbooks before an activation request times out and fails.
-   **Version 24.3.8 - July 2024 \(Vancouver\)**

    Fixed: Added a None visibility status for activity fields that have been removed via script. Manage the visibility of the fields in an activity in the activity's Activity Definition, under the Automation Plan tab, in the Variables section.

-   **Version 24.3.4 - April 2024 \(Vancouver\)**
    -   Fixed:
        -   Corrected reference picker fields to reset when you remove the pill value.
        -   Updated "Playbook name" field to "label".
        -   Corrected time values to show as a date after you enter and save a time condition with a "before" or "after" operator.
        -   Corrected in-app documentation links.
-   **Version 25.1.6 - March 2024 \(Washington DC\)**

    Fixed: Field list fields \(such as Form view\) in the UI Layout tab of an activity no longer reset from text fields to disabled field picker fields when you change the value of the table field \(such as Associated table\) to a pill value, and re-open the activity.

-   **Version 25.1.5 - February 2024 \(Washington DC\)**
    -   New:
        -   Restart a process from the beginning, or a specific stage or activity.
        -   Form View field of an activity:
            -   Start typing in and select the form view you want for an activity.
            -   OpenForm Builder in a newWorkflow Studio tab when editing an existing form view of an activity.
-   **Version 24.3.3 - February 2024 \(Vancouver\)**

    Changed: Keyboard navigation: Updated the Enter/Return key to save and close the side panel.

-   **Version 24.2.6 - December 2023 \(Vancouver\)**
    -   Fixed:
        -   Start with Delay is visible without refreshing Process Automation Designer.
        -   AllStart with Delay changes are saved.
        -   Decision activity performance and user experience improvements.
-   **Version 24.2.5 - November 2023**
    -   New:
        -   Use decision branches if you want a process to follow different paths for certain conditions.
        -   To better control storage consumption, admins can archive process execution records with the archive button on the process execution list.
-   **Version 24.1.4 - September 2023 \(Vancouver\)**
    -   Fixed:
        -   Added the This Activity option back for input and experience properties. This allows you to select your own activity in the pill picker.
        -   Corrected activity picker to always display when adding an activity in Diagram view.
        -   Corrected lanes to keep all valid incoming connections after reload in Diagram view.
        -   Other diagramming interaction fixes.
-   **Version 24.1.4 - September 2023 \(Vancouver\)**

    Workflow Automation on the ServiceNow AI Platform offers low and no code solutions for building and managing automation. Process Automation Designer offers a no code experience for building automated business processes. Build processes in a diagrammatic or visual task-style view. Power Playbook Experiences to guide users through every step required to complete work.


