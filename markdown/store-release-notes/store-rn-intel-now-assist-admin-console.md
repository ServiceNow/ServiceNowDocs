---
title: Now Assist Admin Console release notes
description: Version history for the Now Assist Admin Console application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-intel-now-assist-admin-console.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 15
breadcrumb: [ServiceNow Store - Platform Analytics release notes, ServiceNow Store release notes]
---

# Now Assist Admin Console release notes

Version history for the Now Assist Admin Console application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 10.0.11 - June 2026**
    -   Skill Archival: Instance and system administrators can now archive custom skills directly from the Now Assist Skills page. Archiving is not supported for ServiceNow out-of-box \(OOB\) skills. Archived skills can be restored at any time.
    -   Skill Details Page: View Detail button is now available alongside the Activate button for OOB skills on the Now Assist Skills page. The Skill detail view provides administrators and users with key information about a skill including its benefits, prerequisites, recommended model provider, and related skills — enabling informed activation decisions.
    -   Prompt Injection Enhancements: Prompt injection protection can now be configured at both the instance level and the product level \(CSM, ITSM, and others\), giving administrators more granular control over enforcement across workflows.
    -   Model Version Management — Guided Tour: Administrators can now launch a guided tour walkthrough directly from the " Manage Model Versions"  section within Settings section in now assist admin. The guided tour provides a step-by-step introduction to the model version management workflow, helping admins understand version lifecycle, deprecation alerts, and available actions.
-   **Version 9.1.8 - May 2026 \(Zurich, Australia\)**
    -   As part of this release following features are released:
        -   1.Skill details view: User will now be able to view details about a particular skill in now assist admin console, now assist skills page.By clicking on "view details" for a particular skill now assist admin users can view relavant information about a skill like description, key benefits, prerequisite skills.
        -   2.Archiving skills: User can now remove skills from now assist skills page and push those in archival section in now assist admin console.Archival section can be accessed by clicking on now assist skills, archived skills section.
        -   3.Model version fallback and non availability: In model version section users will be informed with alerts about model version when a particular model version is unavailable in a specific region and when a particular model version fallbacks to a different model version.
-   **Version 9.0.5 - April 2026**
    -   In this release:
        -   ServiceNow is introducing three AI-native subscription tiers — Foundation, Advanced, and Prime — designed to align Now Assist capabilities with your organization's AI adoption journey.Now assist admin console now surfaces skills relevant to your active subscription tier, giving administrators a focused view of the skills available as per there subscription type.
        -   Manage model versions section now surfaces timely alerts when a model version is approaching deprecation or has been retired, giving administrators a clear, consolidated view of model version health across their Now assist skills.
        -   Filters section under Now assist admin console settings now includes support for Customer Service Management \(CSM\), expanding the scope of sensitive data configuration beyond HR service delivery.
-   **Version 8.0.7 - March 2026**
    -   Horizontal Design System Updates The Now Assist Admin Console has been updated to deliver an AI-native experience through the horizontal design system, including a redesigned Generate button in the filters section for improved usability and visual consistency.
    -   Manage Model Versions The Manage Model Versions section now features an intuitive overview panel displaying all model versions categorized as active or deprecated. Model version management is also tightly integrated with AI Control Tower via an approval mandate — when enabled, stewards can approve or reject model versions, and only approved versions are eligible for selection in the Target Model Version configuration.
    -   Manage Model Providers Manage Model Providers has been enhanced with contextual tooltips for inline guidance, a dedicated Impacted Skills panel to view skills affected by a model provider, the ability to switch model providers when fallback is disabled, and a redesigned Manage Integration view with tabular navigation for easier configuration management.
    -   Guardrail Service Providers The Now Assist Guardian section introduces a new Guardrail Service Provider configuration area. Users can select a third-party model service provider for guardrails or configure and apply custom guardrails tailored to their specific organizational needs.
-   **Version 7.0.17 - January 2026**
    -   Query optimization for multiple SQL calls are being implemented for context menu API.
    -   We have fixed the API calls where query was done on skills rather than one capability.
-   **Version 7.0.12 - December 2025**
    -   As part of this release following features are released in Now Assist Admin:
        -   1.Model Versioning
            -   Customers can visit Ai model provider section to access version management in now assist admin. Version management allows you to update a model version\(of model providers\) at instance and skill level
        -   2. Added new workflow - Data and Analytics - in Now Assist Admin &amp; update “analytics” tab in now assist admin top navigation to “performance”
        -   3. Now LLM LTS Model Availability
            -   Customer with Finserv SKU who want a consistent underlying model for now llm as a model provider will have a model provider now llm lts
        -   4. Enhancements in Now assist admin
            -   A.BYOK\(Bring your own key\) model providers can now be used to activate a skill
            -   A1.As an admin, user would be able to activate a skill which is using a BYOK model provider.
            -   A2.For regulated markets &amp; commercial markets, all models configured with BYOK provider are visible
            -   A3.AICT\(Ai control tower\) policy is not applicable\(Fallback, model provider policy - are not applicable\) for regulated and commercial markets in case of BYOk providers.
            -   A4. BYOK provider skills will not come in non compliant skills
            -   B.Activation of custom skills with allowed model provider selected in AI control tower
            -   B1.Only allowed model provider custom skills should be visible in NAA for activation
            -   B2. \(For program\) impose the right behaviour by ensuring that custom skill are not created by internal servicenow team on unallowed providers
        -   5. Feedback in now assist admin
            -   Users will now be able to provide feedback for now assist admin at “overview” page and after they deactivate a skill in now assist skills page.
        -   6. Skill listing enhancements on “now assist skills” page
            -   Add filters upfront on skill listing page at the top for Features and Status.
        -   7. Role masking in now assist admin
            -   Role masking is a enhanced security control where only restricted roles will have access to tools, databases and APIs in run time.Role masking as a feature is part of enhanced security and will be visible for skills in "Define Access" step. Role restricted can be configured for edited in NASK skills, custom skills, make a copy skills while it is view only for OOB skills.
-   **Version 6.3.8 - October 2025**

    As part of this release below changes were made:

    -   Employee Center Pro Plus customers will be able to view and activate Now Assist Guardian
    -   Employee Center Pro Plus customers will be able to view account section inside Now Assist Admin Console
    -   Employee Center Pro Plus customers will now have Now Assist panel by default disabled for users.
    -   For regulated markets customers topic based skills \(using a topic for execution\) like GAF ITSM grouping, GAF HR grouping, navigation, document summarization under platform workflow will be now visible for users for usage.
    -   Managed integrations feature under settings section of now assist admin will be now visible for commercial customers. As part of managed integrations user can switch from OEM version to BYOK \(bring your own key\).
    -   For regulated markets customers users can now view and activate for catalog item generator \(a skill under Creator Workflow\) when the model provider is switched to Now LLM, in Now Assist Admin Console.
-   **Version 6.3.7 - October 2025**
    -   Employee Center Pro Plus customers will be able to view and activate Now Assist Guardian.
    -   Employee Center Pro Plus customers will be able to view account section inside Now Assist Admin Console.
    -   Employee Center Pro Plus customers will now have Now Assist panel by default disabled for users.
    -   For regulated markets customers topic based skills \(using a topic for execution\) like GAF ITSM grouping, GAF HR grouping, navigation, document summarization under platform workflow will be now visible for users for usage.
    -   Managed integrations feature under settings section of now assist admin will be now visible for commercial customers. As part of managed integrations user can switch from OEM version to BYOK \(bring your own key\).
    -   For regulated markets customers users can now view and activate for catalog item generator \(a skill under Creator Workflow\) when the model provider is switched to Now LLM, in Now Assist Admin Console.
-   **Version 6.0.20 - October 2025**

    As part of this release, the following features are released for customers:

    -   Dynamic translation is now available for all regulated market customers.
        -   Users can now turn on dynamic translation from the 'Settings' tab in now assist admin console.
    -   Manage model provider section is now available for all regulated market customers.
        -   Users can now change model providers from the 'Manage LLMs' section inside 'Settings' tab in now assist admin console.
            -   Users can choose the provider as 'Now LLM' and select 'Save' to ensure that a particular features and its corresponding skills run on 'Now LLM'.
    -   Define access step is now added as part of skill guided setup in now assist admin console for regulated market customers. This step ensures that only necessary roles have access to a skill when it is executed.
        -   Users can now view and edit a ACL \(access control log\) for a skill as shown below in 'Define access' step
        -   Users can now add a ACL \(access control log\) for a skill.
        -   When a user has completed configuring roles in 'Define access' step and has come to 'Select display' step, certain roles are not added in the ACL which are part of modalities in 'Select display' step. In this scenario, the system will ask the user to sync roles \(this means that the roles mentioned will be automatically added to ACL\).
            -   By selecting 'Sync roles', the roles mentioned in the modal will be added to the ACL that is present in the 'define access' step
-   **Version 6.2.12 - September 2025**
    -   Key Capabilities:
        -   ACL \(Access Control\) in Now Assist Admin: As part of this feature a user can add, modify, update a ACL inside a skill. This step can be used inside a skill guided setup with the name 'Define Access' and user can view decision types, user roles and update
        -   DT \(Dynamic Translation\) visible to GCC customers in regulated markets; As part of this feature DT\(Dynamic translation\) will be visible for regulated market customers.
-   **Version 6.1.11 - August 2025**
    -   Manage AI model provider: ServiceNow is introducing a 3P Model strategy where all the OOB skills, custom skill and AI agents will support 4 LLM providers \(ServiceNow, Anthropic, Google, Microsoft Azure\). Users will be able to select model providers at individual skills, skill groups and instance levels.
    -   Multilingual Service in Now Assist Admin Console: Native translation can now be configured as per the model policy update in AI control tower. Users can now switch seamlessly between native and dynamic translation while selecting supported languages.
-   **Version 6.0.11 - June 2025**
    -   As part of this release following features have been released:
        -   Skill listing changes inside now assist admin console: Users would now be able to seamlessly view skills with options for switching to list view, use filter and view skills with detailed focus on now assist skills.
        -   Data privacy integration with now assist admin: Privacy policies with respect to now assist can now be accessed through now assist admin console. Users would now be able to explore, view and navigate to data privacy related policies with now assist admin.
-   **Version 6.0.5 - May 2025**
    -   As part of this release following features have been released:
        -   1. Skill listing changes inside now assist admin console: Users would now be able to seamlessly view skills with options for switching to list view, use filter and view skills with detailed focus on now assist skills.
        -   2. Data privacy integration with now assist admin: Privacy policies with respect to now assist can now be accessed through now assist admin console. Users would now be able to explore, view and navigate to data privacy related policies with now assist admin.
-   **Version 5.0.7 - March 2025**
    -   New:
        -   Model selection capability for conversational skills: As part of this capability, a admin will be able to select Microsoft azure in addition to now llm for conversational skills
        -   Streaming enabling inside Now Assist Admin Console: This feature is available when dynamic translation is turned off. Streaming is enabled only when dynamic translation is off.
        -   VA\(Virtual Agent\) as a modality addition in custom skills: As part of this capability a user can choose VA as a modality once a skill is published from Now assist skill kit\(custom skills only\). Once a user publishes a custom skill, a user should be able to select assistants for particular custom skill from now assist admin console
        -   Multiple skill being active for selection of tables In summarization skills: As part of this capability a user can select multiple table\(s\) selection in 'choose input' step\(either a extended table or table being extended\) inside skill guided setup. A user should be able to create multiple skills with each unique table selections.
-   **Version 4.4.0 - March 2025**
    -   Changed: The below features are now XP7 compatible
        -   Model selection capability for conversational skills: As part of this capability, a admin will be able to select Microsoft azure as model in addition to now llm for conversational skills
        -   Streaming enabling inside Now Assist Admin Console: This feature is available when dynamic translation is turned off. Streaming is enabled only when dynamic translation is off.
        -   VA\(Virtual Agent\) as a modality addition in custom skills: As part of this capability a user can choose VA as a modality once a skill is published from Now assist skill kit\(custom skills only\). Once a user publishes a custom skill, a user should be able to select assistant\(s\) for particular custom skill from now assist admin console
        -   Multiple Skill Being Active For Selection Of Tables In Summarization Skills: As part of this capability a user can select multiple table\(s\) selection in 'choose input' step\(either a extended table or table being extended\).A user should be able to create multiple skills with each unique table selections.
        -   Data overflow processing integration in Now Assist Admin Console: As part of this capability, the data steward can opt out of Azure bursting. If data privacy steward doesn't want data to be processed outside ServiceNow data centers, they can opt out from the Now Assist Admin Console.
        -   Activating OOB skill edited inside Now Assist Skill Kit: As part of this capability a user can open and edit a OOB skill inside Now Assist Skill Kit and then activate that skill from Now Assist Admin Console
        -   Activating skills with flow action as a modality from Now Assist Skill Kit: As part of this capability a user who has chosen flow action as a modality in Now Assist Skill Kit can activate the skill inside Now Assist Admin console.
        -   Data Sharing available inside settings section: As part of this feature we are ensuring that data sharing is available inside settings page
-   **Version 5.0.4 - February 2025**
    -   New:
        -   Data overflow processing integration in Now Assist Admin Console. Data stewards can opt out of Azure bursting.
        -   Voice input enablement for Now Assist panel inside Now Assist Admin Console. Enabling this option in the Admin console allows users to configure their accessibility preferences to turn on voice-to-text in the Now Assist panel.
        -   Activating ServiceNow skills edited with Now Assist Skill Kit. Once you've made changes to a ServiceNow skill in Skill Kit, you can activate the updated skill in the Now Assist Admin console.
        -   Activating skills with flow action as a modality from Now Assist Skill Kit. You can create custom skills in Skill Kit that act as flow actions, and you can activate those skills in the Now Assist Admin console.
    -   Changed: Data sharing settings has moved to a new section with data overflow processing.
-   **Version 4.1.16 - December 2024**

    This is a patch release for bug fixes and XP3 compatability.

-   **Version 3.1.4 - December 2024**
    -   As part of this release below items were released:
        -   SPP Enhancement across NAA
        -   US Commercial Data center details to be added in the Region tab
        -   Backporting changes for Now Assist troubleshooting integration to NAA for Washington
        -   Integration of monitor config logs in now assist admin for now assist skill kit
-   **Version 4.1.9 - November 2024**
    -   New:
        -   Now Assist Guardian \[Offensiveness, Prompt Injection, Filters\]: Allows customers to monitor and control guardrails via Now Assist Admin. Outputs are blocked if offensive content or prompt injection attempts are detected and blocking is enabled.
        -   Proactive Error Monitoring Integration within Now Assist Admin \(NAA\).
        -   Added an 'Advanced Script' field to the Now Assist Skill Config UI, enabling the configuration of scripts to control skill visibility. This feature restricts Playbook generation and other skills using the GPT-4o model, which is currently unsupported in the APAC region.
        -   Introduced a new table, Now Assist Skill Config Status. Previously, fields such as 'active,' 'in\_product\_active,' and 'in\_product\_roles' were updated when customers set up skills via guided setup, marking skill configuration records as customer-updated. Consequently, any updates in subsequent releases weren't reflected in customer instances. To address this, fields have been moved to the newly introduced table, reducing the need for BU or skill owners to write fix scripts to update records with the latest changes.
    -   Changed: Renamed 'Write with Now Assist' to 'Now Assist Context Menu.'
-   **Version 4.0.9 - September 2024**
    -   New: As part of September release, we are releasing now assist admin troubleshooting feature where we will provide:
    -   Provide a summary report of the diagnosis with the following:
        -   Issue Proposal is to define the right categories of issues
        -   Recommended actions
    -   For the diagnosis, the user can choose to download it as a report to trace afterwords.
-   **Version 4.0.5 - August 2024**
    -   New:
        -   Platform Skills activation: ServiceNow admins will have a mechanism to configure and activate the Navigation Platform skill.
        -   Write with Now Assist activation: admins can enable their agents to use Now LLM Service capabilities to write emails, notes for addressing relevant requestor cases, or responses to user chats.
        -   Custom skill activation: admins can use Now Assist Skill Kit to create custom skills which are powered by 3rd party LLMs and activate them using the Now Assist Admin console to unlock new generative AI capabilities across agent, requestor, and fulfiller personas.
-   **Version 3.1.2 - July 2024**

    Fixed: GCC skills flow.

-   **Version 3.0.5 - June 2024**
    -   New: Manage multi-language support and dynamic translations across Now Assist applications to support users who speak different languages
    -   Fixed: Domain separation defects
-   **Version 1.2.5 - November 2023**
    -   New:
        -   Content changes, support app UI updates after skill configuration
        -   VA Skill cards
    -   Fixed: Guided setup config issues, UI issues, etc.
-   **Version 1.0.20 - September 2023**

    The Now Assist Admin Console provides a way to activate, manage, and monitor the Now Assist applications.

    It has overview, features, and platform settings sections to separate the tasks you can perform. It includes helpful resources like links to more in-depth information and FAQs.


