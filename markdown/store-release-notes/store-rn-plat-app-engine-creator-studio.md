---
title: Creator Studio release notes
description: Version history for the Creator Studio on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-plat-app-engine-creator-studio.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 7
breadcrumb: [ServiceNow Store - ServiceNow AI Platform App Engine release notes, ServiceNow Store release notes]
---

# Creator Studio release notes

Version history for the Creator Studio on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 29.2.3 - June 2026**
    -   Changed:
        -   Distinguish AI-generated apps and features using updated icons.
        -   Use improved screen reader support and keyboard navigation when interacting with forms and templates using assistive technologies.
        -   AI gradient tokens are applied to specific components on the forms page to indicate when content has been generated or influenced by Now Assist. This creates a consistent and recognizable AI identity within Creator Studio, helping you identify AI-generated content consistently.
    -   Fixed:
        -   The following accessibility issues are resolved in this release:
            -   Form elements now have accurate interactive ARIA roles, enabling screen readers to identify and announce them accurately.
            -   Rich text area and form elements are now accurately labeled, so screen readers can announce them correctly when focused.
            -   Keyboard focus now remains within the expanded template preview modal for the duration of the modal interaction.
            -   The rich text frame Long Description now has a proper label, enabling screen readers to identify and announce it correctly.
-   **Version 29.1.2 - March 2026**

    Changed: Creator Studio request types now automatically appear in App Engine Management Center using the new configurable request taxonomy.

-   **Version 28.2.1 - December 2025**
    -   New:
        -   Customizable email notifications
            -   Promote consistent branding by having admins create custom email notifications and templates, which are sent when users request something from an app, or the request was changed or closed. In support, several of the standard email notification activities are now in the public scope, and a new Configure email notifications item is available in Guided Setup.
        -   New playbook activity to update record fields
            -   Enable apps to change several fields automatically on the submitted record using the new Update submission playbook activity. In support, a new Configure playbook activities item is available in Guided Setup.
        -   New question types for forms
            -   Two new question types are available for forms: Duration and Attachment.
                -   Duration enables users to specify a length of time.
                -   Attachment enables users to upload an attachment as a question. The Attachment field differs from the Add attachment option for the form, because the Attachment question type can be used in dynamic behavior questions.
        -   Granular configuration admin roles
            -   Several new granular admin roles enable developers to complete administrative configuration tasks without requiring the full admin role.
        -   Delete unpublished forms
            -   You can now delete unpublished forms from Creator Studio, which completely removes the record for the form from the ServiceNow AI Platform.
    -   Changed:
        -   Deleting questions from unpublished forms removes the record
            -   To improved data hygiene, when you delete a question from an unpublished form, the record for the question is now removed from the ServiceNow AI Platform.
-   **Version 27.2.3 - August 2025**

    Fixes issues with App and Form metadata saving incorrectly in certain edge cases.

-   **Version 27.2.2 - May 2025**
    -   New:
        -   Navigation has been revamped to make it easier to see what's in your app.
        -   A new Try it feature enables the testing of forms to validate form and playbook behavior.
        -   Creator Studio application tables are now modifiable by admins.
        -   Users with the right permissions can open their apps in ServiceNow Studio from within the app.
    -   Changed:
        -   To support navigation changes, a new application side navigation panel enables users to see their forms and automations in one unified navigation.
        -   Form Submissions and Record details has moved to the application side panel, and the Forms Submission section has been renamed to List Configurations.
        -   Users can now search for forms and automations in their app.
        -   Form preview is now more focused on the current form.
        -   The Request App Workspace modules have been changed to better support fulfillment flows in the app. The home module has been removed, and the Analytics module has been modified to focus on app dashboards.
        -   Playbooks can now only be added to published forms to avoid mismatches between draft and published forms.
    -   Removed:
        -   App creation no longer starts with form creation.
        -   The AES Catalog Template is no longer visible during form creation. This behavior can be modified by an admin.
-   **Version 27.1.1 - February 2025**
    -   New:
        -   Generate a form from text prompts using the Build with Now Assist tab: Enable users to generate forms automatically from text prompts by using the Build with Now Assist dialog box.
        -   Auto-populate question values on a form: Help users to complete forms faster with the new Add auto-fill option, which automatically populates answers based on answers to record choice questions.
        -   Use catalog variables in playbook activities and decisions: Playbook activities and decision branches can now be triggered by answers to one or more questions on a form when you configure the conditions.
        -   Select your development experience: Seamlessly change between development environments using the new experience switcher to choose the experience that's best for you. Depending on which products and versions are installed, and what role users have, they can switch between the following environments:
            -   Creator Studio for a no-code experience
            -   ServiceNow Studio for a mid-skill coding experience
            -   ServiceNow IDE for a pro-code ServiceNow experience
    -   Changed:
        -   Search for apps on the home page: Quickly find the app that you're looking for using the new search bar on the Creator Studio home page.
        -   Save and quickly find apps with bookmarks: Bookmark apps to find them faster using the new Bookmarks pill on the home page.
        -   Form location removed from form creation: Defining the catalogs and topics for a form has been removed from the form creation process and is now editable only in the form settings. If you haven't defined a location for a form, you are prompted to before you can mark it as ready.
-   **Version 26.2.1 - November 2024**
    -   New:
        -   Dynamic behavior for forms enables users to add dynamic behaviors to forms and their questions based on how users answer questions.
        -   Administrators can define custom activities on the ServiceNow AI Platform to use in automations when building apps.
        -   App creators can now see how records generated by Creator Studio apps will appear by previewing and interacting with records on the Form submissions tab.
    -   Changed:
        -   The Form settings modal has the following changes:
            -   A new Apply button that appears when users select categories, topics, and user access provides a more intuitive way of saving changes and returning to the previous page in the modal.
            -   The Save button now automatically closes the modal when you select it after making changes to a form settings value.
        -   When you save changes to the properties for a question, the Question details panel now stays open and the question on the form stays highlighted, enabling you to keep working on the question without re-opening the panel.
    -   Fixed: The preview that appears when you create or open an app has updated styling.
-   **Version 26.1.1 - August 2024**
    -   New:
        -   Associate a topic with a form - You can now add a topic to the settings for a form, enabling users to browse forms by their related topics.
        -   New send email activity in automations - When you create a process, you can now have your app's automation automatically send an email when specified conditions are met.
        -   Add curated questions to a form using question sets - When creating forms, developers can now select from pre-configured question sets, enabling them to select curated questions without worrying about the details.
        -   Swap placeholders for other activities in your automations - You can now swap out placeholders with other activities from the automation canvas.
    -   Changed: Use questions as process triggers - You can now select one of the published questions from the app's form as a trigger for its process.
-   **Version 25.3.0 - July 2024**
    -   Fixed:
        -   Minimum version check when installing apps created with Creator Studio \(PRB1768570\)
        -   Catalog Template selection stuck on loading screen \(PRB1765155\)
        -   Catalog and Categories not loading due to empty values \(PRB1762519\)
        -   Forms not accepting values when in a 2-column layout \(PRB1773440\)
-   **Version 25.1.2 - May 2024**

    Creator Studio is designed with non-developers in mind, offering a guided, intuitive environment for building request-based applications. It breaks down the traditional barriers to app development, making it accessible for business process experts to bring their automation ideas to life. This tool is not intended to replace existing development tools like App Engine Studio, but to complement them by providing a new entry point for app creation. Creator Studio is more than just a new tool; its a new way of thinking about application development on ServiceNow. It promises to open up the platform to a broader audience, enabling more users to contribute to their organization's digital transformation journey.


