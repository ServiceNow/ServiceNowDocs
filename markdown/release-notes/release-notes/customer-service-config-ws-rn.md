---
title: Agent experience for CSM release notes
description: The ServiceNow Agent experience for CSM provides customer service agents with the tools that they need to find, research, and resolve customer issues and questions. Agent experience for CSM was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 6
---

# Agent experience for CSM release notes

The ServiceNow® Agent experience for CSM provides customer service agents with the tools that they need to find, research, and resolve customer issues and questions. Agent experience for CSM was enhanced and updated in the Australia release.

## Agent experience highlights for the Australia release

-   Minimize drafts of comments, work notes, and emails to a dock at the bottom of CSM Configurable Workspace and keep track of documents in this centralized location.
-   Enable agents to work from a single location with the ability to view CSM Configurable Workspace record pages in other workspaces.
-   Populate interaction wrap-up codes and notes by using AI, saving agents time.
-   Auto-populate record fields and email drafts with dynamic values using form templates.

See CSM Configurable Workspace for more information.

**Important:** CSM Configurable Workspace is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Australia release

-   **Dock in CSM Configurable Workspace**

    Enable agents to minimize drafts of comments, work notes, or emails to a dock at the bottom of the workspace page. This centralized location provides agents with the ability to see all current drafts at a glance.

-   **Form template enhancements**

    Save time and promote consistency by creating conditional templates, setting field-level conditions, and automatically populating email body text. Populate these fields using dynamic values from the Case table and related tables. Preview template changes before applying them to a record.

-   **Workspace record page interoperability**

    Enable agents to use record pages between CSM Configurable Workspace and ITSM Service Operations Workspace. The following ITSM pages are interoperable across CSM:

    -   Incident page
    -   Change page
-   **AI interaction wrap-up**

    Provide agents with AI assistance during the interaction wrap-up period. This feature generates wrap-up content for interaction records, such as the wrap-up code and notes.

-   **Highlight fields with unsaved changes**

    Use visual indicators in CSM Configurable Workspace such as icons and background colors to indicate form fields with unsaved changes.

-   **Knowledge Center article editor available in CSM Configurable Workspace**

    Use the Knowledge Center article editor to create and edit knowledge articles in CSM Configurable Workspace. Agents can access the editing capabilities available in the article editor to format knowledge article content such as text, images, and media.

-   **Unread email count on interaction tabs**

    Displays the number of unread email messages on interaction tabs in CSM Configurable Workspace. Hovering over a tab displays a tooltip with a preview of the most recent email.

-   **Activity timer log**

    Track the time that agents spend working on cases and interactions in CSM Configurable Workspace. View a time log report to see detailed records of the time spent on projects and tasks.


## Changed in this release

-   **Editable record headers**

    Enables agents to edit the short description of a record directly from the header field. This feature is available on the following record pages:

    -   Front-line case page
    -   CSM Interaction record page
    -   CSM default record page
-   **Collaborate component in CSM Configurable Workspace**

    Use the Collaborate component in the contextual side panel in CSM Configurable Workspace to communicate and collaborate with stakeholders in real time to resolve cases.

-   **SLA component on the Front-line case page**

    Use the Service Level Agreement \(SLA\) component in the contextual side panel on the Front-line case page to view SLAs. The SLA cards appear in the Record Information tab below the record information card.

-   **Email Interaction record page enhancements**

    Minimize drafts to a dock at the bottom of the workspace page in the inline modeless composer. View activities in the activity feed at the top of the page in reverse order, with the newest entries displayed at the bottom.

-   **Lookup component added to the Email Interaction record page**

    Enable agents to look up contacts and consumers by name, phone number, or email address and link them to a record.

-   **Create actions on the Front-line case page**

    Create different types of records by using the **Create** button on the Front-line case page. Selecting an action from the Create button, such as creating an incident or a knowledge gap, opens the form in a modeless dialogue.

-   **View attachments in modeless dialogs**

    Enable agents to access and review attachments in modeless dialogs instead of workspace tabs. Agents can easily view attachments while also viewing case information and drafts of emails, comments, or work notes.

-   **Auto-dismiss alerts in CSM Configurable Workspace**

    Reduce visual clutter through auto-dismissible alerts, which are enabled by default for Info, Low, and Moderate alerts, with a default timer of five seconds. Critical and High alerts remain persistent to ensure important notifications stay visible.

-   **Maximum number of active tabs in CSM Configurable Workspace**

    Agents can open up to 20 active tabs \(previously 10\) in CSM Configurable Workspace to handle multiple tasks simultaneously without losing context.

-   **Open multiple lists in separate primary tabs**

    Agents can now open multiple lists in different CSM Configurable Workspace primary tabs, enabling seamless context switching between lists without losing their current workspace view.

-   **Granular admin roles**

    Enhance security, reduce over-privileged accounts, and enable flexible, task-focused permission management by assigning granular, feature-specific roles to replace broad admin access.


## Activation information

CSM Configurable Workspace is available with activation of the Customer Service plugin \(com.sn\_customerservice\). For details, see Activate Customer Service Management.

Install CSM Configurable Workspace by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Plugin information

-   **New plugins**

    The following plugins are new in Australia:

    -   Special Handling Notes \(sn\_shn\): Create notes to bring to the user's attention important information about individual records, such as a case or account record.
    -   Special Handling Notes Demo Data \(com.snc.shn\_demo\): Provides the Special Handling Notes application demo data.
-   **Deprecated plugins**

    The following plugin is deprecated in Australia:

    Customer Service CTI Demo Data \(com.snc.customerservice\_cti\_demo\): ServiceNow Voice with Amazon Connect provides the latest experience for this functionality.

-   **Plugins planned for deprecation**

    The listed plugins are planned for deprecation in a future release.

    Beginning with the Australia release, these plugins will be migrated to store applications. Upgrading your instance to the Australia release automatically installs the store applications.

    -   CSM Configurable Workspace Special Handling Notes \(com.snc.uib.special\_handling\_notes\)
    -   CSM Account Hierarchy \(com.snc.sn\_csm\_account\_hierarchy\_uib\)
    -   Resolution Shaper \(com.sn\_resolutionshaper\)
    -   sn-component-workspace-ribbon \(com.sn\_component\_workspace\_ribbon\)
    -   Special Handling Instruction \(app\_sn\_shn\)
    -   Special Handling Notes Demo Data \(app\_sn\_shn\)
    -   sn-component-account-hierarchy \(com.sn\_component\_account\_hierarchy\)
    -   sn-component-workspace-shn \(com.sn\_component\_workspace\_shn\)
    For more information, see Plugins activated with Customer Service Management.


## Browser requirements

ServiceNow workspaces don’t support mobile devices, Internet Explorer, or Microsoft Edge. Instead, use Microsoft Edge - Chromium or one of the other supported browsers listed in Browser support.

## Related ServiceNow applications and features

-   **Customer Service Management**

    Use the Customer Service Management application to provide the service and support that your external customers need.

-   **Now Assist for Customer Service Management \(CSM\)**

    Use the ServiceNow® Now Assist for CSM application to summarize customer chat conversations on interactions, summarize case details, and generate case resolution notes.

-   **Next Experience UI Builder**

    Next Experience UI Builder is a low-code web user interface builder that enables developers to build pages for workspace and portal web-based experiences. Use the base system and custom web components to build your pages.

-   **Workspace UI**

    ServiceNow® Workspace is a graphical user interface that puts multiple tools on one page, including the tools that agents need to find, research, and resolve issues. CSM Configurable Workspace is a customer service-specific implementation that provides tier 1 agents with the tools that they need to respond to customers and to resolve cases.


**Parent Topic:**[Customer Service Management release notes](customer-service-mgmt-rn-landing.md)

