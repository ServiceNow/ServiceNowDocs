---
title: Creator Studio release notes
description: The ServiceNow Creator Studio product is a guided application development experience that enables business process experts to create request-based applications without the barriers of traditional low-code development. Creator Studio was enhanced and updated in the Zurich release.The ServiceNow Creator Studio product is a guided application development experience that enables business process experts to create request-based applications without the barriers of traditional low-code development. Creator Studio was enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: topic
last_updated: "2025-12-08"
reading_time_minutes: 2
---

# Creator Studio release notes

The ServiceNow® Creator Studio product is a guided application development experience that enables business process experts to create request-based applications without the barriers of traditional low-code development. Creator Studio was enhanced and updated in the Zurich release.

## About Creator Studio

-   Create customized email notifications that are sent by the apps that you build.
-   Add playbooks with a new activity that automatically updates some fields on the app's generated record.
-   Augment forms with the new Duration and Attachment question types.

See  for more information.

## Activation and other requirements

**Important:** Creator Studio is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

-   **Activation information**

    Install Creator Studio by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).

-   **Additional requirements**

    You must have the App Engine Enterprise license to use Creator Studio.


## Accessibility and localization

-   **Accessibility information**

    -   **Dark theme**

        The new Coral theme includes a dark theme option for web and mobile experiences. This option is commonly used to alleviate eye strain and improve readability.

    For more information, see .


**Parent Topic:**[App development and low-code release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/build-automate-rn-landing.md)

## Zurich

The ServiceNow® Creator Studio product is a guided application development experience that enables business process experts to create request-based applications without the barriers of traditional low-code development. Creator Studio was enhanced and updated in the Zurich release.

### What's new

-   **Customizable email notifications**

    Promote consistent branding by having admins create custom email notifications and templates, which are sent when users request something from an app or the request was changed or closed. In support, several of the standard email notification activities are now in the public scope, and a new Configure email notifications item is available in Guided Setup.

-   **New playbook activity to update record fields**

    Enable apps to change several fields automatically on the submitted record using the new Update submission playbook activity. In support, a new Configure playbook activities item is available in Guided Setup.

-   **New question types for forms**

    Two new question types are available for forms: Duration and Attachment.

    -   Duration enables users to specify a length of time.
    -   Attachment enables users to upload an attachment as a question. The **Attachment** field differs from the **Add attachment** option for the form, because the Attachment question type can be used in dynamic behavior questions.
-   **Granular configuration admin roles**

    Several new granular admin roles enable developers to complete administrative configuration tasks without requiring the full admin role.

-   **Delete unpublished forms**

    You can now delete unpublished forms from Creator Studio, which completely removes the record for the form from the ServiceNow AI Platform.


### What's changed

-   **Deleting questions from unpublished forms removes the record**

    When you delete a question from an unpublished form, the record for the question is now also removed from the ServiceNow AI Platform.


