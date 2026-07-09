---
title: Creator Studio release notes
description: The ServiceNow Creator Studio product is a guided application development experience that enables business process experts to create request-based applications without the barriers of traditional low-code development. Creator Studio was enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-12-08"
reading_time_minutes: 3
---

# Creator Studio release notes

The ServiceNow® Creator Studio product is a guided application development experience that enables business process experts to create request-based applications without the barriers of traditional low-code development. Creator Studio was enhanced and updated in the Zurich release.

## Creator Studio highlights for the Zurich release

-   Create customized email notifications that are sent by the apps that you build.
-   Add playbooks with a new activity that automatically updates some fields on the app's generated record.
-   Augment forms with the new Duration and Attachment question types.

See [Creator Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/application-development/creator-studio-landing.md) for more information.

**Important:** Creator Studio is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Zurich release

-   **[Customizable email notifications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/application-development/crs-admining-notifications.md)**

    Promote consistent branding by having admins create custom email notifications and templates, which are sent when users request something from an app or the request was changed or closed. In support, several of the standard email notification activities are now in the public scope, and a new Configure email notifications item is available in Guided Setup.

-   **[New playbook activity to update record fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/application-development/creator-studio-add-activities-automation.md)**

    Enable apps to change several fields automatically on the submitted record using the new Update submission playbook activity. In support, a new Configure playbook activities item is available in Guided Setup.

-   **[New question types for forms](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/application-development/creator-studio-form-elements-ref.md)**

    Two new question types are available for forms: Duration and Attachment.

    -   Duration enables users to specify a length of time.
    -   Attachment enables users to upload an attachment as a question. The **Attachment** field differs from the **Add attachment** option for the form, because the Attachment question type can be used in dynamic behavior questions.
-   **[Granular configuration admin roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/application-development/roles-creator-studio.md)**

    Several new granular admin roles enable developers to complete administrative configuration tasks without requiring the full admin role.

-   **[Delete unpublished forms](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/application-development/crs-delete-form.md)**

    You can now delete unpublished forms from Creator Studio, which completely removes the record for the form from the ServiceNow AI Platform.


## Changed in this release

-   **[Deleting questions from unpublished forms removes the record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/application-development/creator-studio-delete-forms-questions.md)**

    When you delete a question from an unpublished form, the record for the question is now also removed from the ServiceNow AI Platform.


## Activation information

Install Creator Studio by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Additional requirements

You must have the App Engine Enterprise license to use Creator Studio.

## Accessibility information

-   **Dark theme**

    The new Coral theme includes a dark theme option for web and mobile experiences. This option is commonly used to alleviate eye strain and improve readability.


For more information, see [Dark mode in Creator Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/application-development/crs-enabling-dark-mode.md).

## Related ServiceNow applications and features

-   **[App Engine Management Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/application-development/monitor-requests-using-aemc.md)**

    Track and manage your Creator Studio requests, deployments, applications, and collaborative developers using App Engine Management Center.

-   **[App Engine Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/application-development/aes-overview.md)**

    Open Creator Studio apps in AES to add more complexity to the app, such as email notifications and additional security.

-   **[Catalog Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/servicenow-platform/catalog-builder.md)**

    Create or edit a catalog item using a visual and guided experience.

-   **[Form Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/application-development/form-view-configuration.md)**

    Visually create, configure, and customize the different form views for your users using the form editor in Form Builder.

-   **[ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/application-development/servicenow-studio-landing.md)**

    ServiceNow Studio provides a unified experience for all ServiceNow development activities, enabling admins and developers to extend base system solutions and create custom apps with ease.

-   **[Workflow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/build-workflows/workflow-studio.md)**

    Integrate workflow authoring, configuring, and monitoring into a single-page experience.

-   **[Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-user-interface/workspace-landing-page.md)**

    Address customer requests and issues in a workspace, which provides a suite of tools where agents, case managers, help desk professionals, and managers work with tools to resolve customer needs.


**Parent Topic:**[App development and low-code release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/build-automate-rn-landing.md)

