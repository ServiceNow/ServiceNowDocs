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

See [Creator Studio](https://www.servicenow.com/docs/access?context=creator-studio-landing&version=zurich&pubname=zurich-application-development&ft:locale=en-US) for more information.

**Important:** Creator Studio is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Zurich release

-   **[Customizable email notifications](https://www.servicenow.com/docs/access?context=crs-admining-notifications&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

    Promote consistent branding by having admins create custom email notifications and templates, which are sent when users request something from an app or the request was changed or closed. In support, several of the standard email notification activities are now in the public scope, and a new Configure email notifications item is available in Guided Setup.

-   **[New playbook activity to update record fields](https://www.servicenow.com/docs/access?context=creator-studio-add-activities-automation&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

    Enable apps to change several fields automatically on the submitted record using the new Update submission playbook activity. In support, a new Configure playbook activities item is available in Guided Setup.

-   **[New question types for forms](https://www.servicenow.com/docs/access?context=creator-studio-form-elements-ref&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

    Two new question types are available for forms: Duration and Attachment.

    -   Duration enables users to specify a length of time.
    -   Attachment enables users to upload an attachment as a question. The **Attachment** field differs from the **Add attachment** option for the form, because the Attachment question type can be used in dynamic behavior questions.
-   **[Granular configuration admin roles](https://www.servicenow.com/docs/access?context=roles-creator-studio&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

    Several new granular admin roles enable developers to complete administrative configuration tasks without requiring the full admin role.

-   **[Delete unpublished forms](https://www.servicenow.com/docs/access?context=crs-delete-form&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

    You can now delete unpublished forms from Creator Studio, which completely removes the record for the form from the ServiceNow AI Platform.


## Changed in this release

-   **[Deleting questions from unpublished forms removes the record](https://www.servicenow.com/docs/access?context=creator-studio-delete-forms-questions&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

    When you delete a question from an unpublished form, the record for the question is now also removed from the ServiceNow AI Platform.


## Activation information

Install Creator Studio by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Additional requirements

You must have the App Engine Enterprise license to use Creator Studio.

## Accessibility information

-   **Dark theme**

    The new Coral theme includes a dark theme option for web and mobile experiences. This option is commonly used to alleviate eye strain and improve readability.


For more information, see [Dark mode in Creator Studio](https://www.servicenow.com/docs/access?context=crs-enabling-dark-mode&version=zurich&pubname=zurich-application-development&ft:locale=en-US).

## Related ServiceNow applications and features

-   **[App Engine Management Center](https://www.servicenow.com/docs/access?context=monitor-requests-using-aemc&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

    Track and manage your Creator Studio requests, deployments, applications, and collaborative developers using App Engine Management Center.

-   **[App Engine Studio](https://www.servicenow.com/docs/access?context=aes-overview&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

    Open Creator Studio apps in AES to add more complexity to the app, such as email notifications and additional security.

-   **[Catalog Builder](https://www.servicenow.com/docs/access?context=catalog-builder&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US)**

    Create or edit a catalog item using a visual and guided experience.

-   **[Form Builder](https://www.servicenow.com/docs/access?context=form-view-configuration&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

    Visually create, configure, and customize the different form views for your users using the form editor in Form Builder.

-   **[ServiceNow Studio](https://www.servicenow.com/docs/access?context=servicenow-studio-landing&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

    ServiceNow Studio provides a unified experience for all ServiceNow development activities, enabling admins and developers to extend base system solutions and create custom apps with ease.

-   **[Workflow Studio](https://www.servicenow.com/docs/access?context=workflow-studio&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US)**

    Integrate workflow authoring, configuring, and monitoring into a single-page experience.

-   **[Workspace](https://www.servicenow.com/docs/access?context=workspace-landing-page&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US)**

    Address customer requests and issues in a workspace, which provides a suite of tools where agents, case managers, help desk professionals, and managers work with tools to resolve customer needs.


**Parent Topic:**[App development and low-code release notes](build-automate-rn-landing.md)

