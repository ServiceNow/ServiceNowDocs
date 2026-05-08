---
title: Public Sector Digital Services release notes
description: The ServiceNow Public Sector Digital Services application enables government agencies to provide citizens, businesses, and other agencies with important services such as public records, licenses, permits, and social services. Public Sector Digital Services was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 4
---

# Public Sector Digital Services release notes

The ServiceNow® Public Sector Digital Services application enables government agencies to provide citizens, businesses, and other agencies with important services such as public records, licenses, permits, and social services. Public Sector Digital Services was enhanced and updated in the Australia release.

## Public Sector Digital Services highlights for the Australia release

-   Consolidate the case narrative, evidence, entities, team assignments, investigative tasks, and related cases into a single record page with Investigative Case Management Foundation.
-   Manage persons, property, vehicles, organizations, locations, and events, including specialized entity types like firearms with detailed identification, specifications, origin, and ballistic information, and link them to cases and to each other with Investigative Case Management Entity Management.
-   Manage physical and digital evidence tied to investigative cases, with structure fields for collection details, source and context, security classification, and links to related entities such as persons, vehicles, locations, and organizations using Investigative Case Management Evidence Management.
-   Create Chain of custody documentation in every evidence record, capturing each transfer from the moment of collection.
-   Synthesize narratives, entities, evidence, and activity history into a structured summary using Investigative Case Management Case Summarization.
-   Validate large volumes of uploaded documents, verify information, flag issues, and highlight key details for case agents with the Document Screening Al Skill, used with Now Assist for Public Sector Digital Services \(PSDS\).

See Public Sector Digital Services \(PSDS\) for more information.

**Important:** Public Sector Digital Services is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Important information for upgrading Public Sector Digital Services to Australia

After the upgrade, certain public sector menus and menu items in CSM Configurable Workspace revert to their original CSM label names. You can relabel these items for public sector use by updating the labels for the Customer, Accounts, and Service Organizations UX list category records. For more details on relabeling, navigate to **All** &gt; **Constituent Service** &gt; **Administration** &gt; **Guided Setup**, and select **Configurable Workspace for Public Sector Digital Services** &gt; **Customize Workspace Labels Manually**.

## New in the Australia release

-   **Investigative Case Management**

    Create an investigative case using Investigative Case Management. Investigative Case Management guides investigators through the process of organizing, tracking, and resolving investigations, ​developing case details,​ assigning investigators and team members​, and track evidence with logging and metadata. The following features are available as part of Investigative Case Management:

    -   Entity Management
    -   Evidence Management
    With Entity Management, investigators can create investigative tasks and workflows for investigative activities with automated metadata capture \(time, source, entities, classification\)​, as well as define processing with teams and attorneys and collaborate across agencies/divisions. With Evidence Management, investigators can log and triage evidence metadata \(digital, physical, testimonial\)​ and maintain an audit trail \(Chain of Custody logging\), as well as draft, review, and create reports with supporting evidence​​.

-   **Use Now Assist for Public Sector Digital Services \(PSDS\) Skills to create case narratives and screen documents**

    Complete case narratives and make refinements to investigative case records using Now Assist for PSDS Gen-AI skills. Investigators can streamline case narrative refinement byedit, adjust tone, and regenerate narrative content for clarity and completeness.

-   **Document Screening AI Skill for Social Benefits Playbook**

    Validate large volumes of uploaded documents, verify information, flag issues, and highlight key details for case agents using the Social Benefits Playbook with the Document Screening Al Skill, part of Now Assist for Public Sector Digital Services \(PSDS\).

-   **Granular configuration admin roles**

    Several new granular admin roles enable admins to complete administrative configuration tasks on the Public Sector Digital Services platform without requiring the full admin role. These granular access roles enable a high-level administrator to define and assign custom roles that contain only the specific permissions a user needs, decreasing the number of users with full administrative power over the instance. For more information on granular admin roles, see Granular admin roles.


## UI changes

-   **Updated Coral theme**

    The Coral theme has been improved to enhance usability across web, mobile, and portal experiences that use Next Experience and Core UI:

    -   A fully overhauled color system for smoother gradients and better contrast.
    -   Softer outlines and more rounded components for a modern, accessible look.
    -   A significantly improved dark mode with deeper blue tones for reduced eye strain.
    -   New AI gradient styles and subtle animations to highlight intelligent features.
    -   Smarter focus behavior that reduces visual clutter for mouse users.
-   **Enhancements to Constituent Service Portals**

    UI Enhancements have been made to all Public Sector Digital Services constituent portals by replacing legacy widgets \(for example, portal banners, data lists\) with standardized, CSM Configurable Widgets and components. The update verifies backward compatibility, migration guidance, usage analytics, and provide training for admins, and also enables dynamic data rendering, and better filtering across service flows.


## Changed in this release

-   **ServiceNow product tiers**

    The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets, and create your own
    Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.


## Activation information

Install Public Sector Digital Services by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Related ServiceNow applications and features

-   **Customer Service Management**

    The ServiceNow®Customer Service Management application enables customer service organizations and service operations to collaborate and resolve customer problems.

-   **CSM Configurable Workspace**

    The ServiceNow®CSM Configurable Workspace application provides government agents with the tools to research information, respond to questions from the public, and resolve cases.

-   **Now Assist**

    The ServiceNow®Now Assist application uses generative AI that is designed to enhance user productivity and efficiency through conversation and proactive experiences.


**Parent Topic:**[Features and changes by product](../new-features-changes.md)

