---
title: CRM Outlook Add-in release notes
description: The ServiceNow CRM Outlook Add-in application captures and logs email interactions into CRM directly from Microsoft Outlook. See the following sections for release notes by version.The September 2026 release includes user experience improvements.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/release-notes/crm-outlook-add-in-rn.html
release: brazil
topic_type: topic
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Sales Customer Relationship Management release notes, Features and changes by product, Release notes for upgrading from Australia, Learn about the Brazil release, Brazil release notes]
---

# CRM Outlook Add-in release notes

The ServiceNow® CRM Outlook Add-in application captures and logs email interactions into CRM directly from Microsoft Outlook. See the following sections for release notes by version.

## About CRM Outlook Add-in

-   Capture customer emails in the CRM without leaving Microsoft Outlook by associating messages with leads, contacts, accounts, and opportunities directly from the inbox.
-   Locate CRM records such as leads, contacts, opportunities, and accounts, and associate emails to them. After you associate one email from a thread, other emails that you select from that thread link to the same record.
-   Convert inbound interest into actionable CRM records by creating leads or contacts from emails with relevant details automatically populated.
-   Configure redirect rules to automatically route high-volume email captures to your instance, keeping CRM data consistent for pipeline visibility and follow-up tracking.
-   Maintain consistent customer context by making captured email interactions available for pipeline visibility and follow-up tracking.

See [CRM Outlook Add-in](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/explore-crm-outlook-add-in.md) for more information.

## Activation and other requirements

-   **Activation information**

    Install the CRM Outlook Add-in application \(sn\_crm\_outlook\) from the ServiceNow Store. The application installs related ServiceNow® Store applications and plugins that aren't already active on your instance. After installation, download the manifest file and install the ServiceNow CRM for Outlook add-in on each user's Microsoft Outlook client. The sn\_crm\_outlook.crm\_outlook\_admin role is required to configure the add-in, and the sn\_crm\_outlook.crm\_outlook\_user role is required to use it.

-   **Additional requirements**

    Configuring email promotion requires the User Mailbox Integration plugin to be active on your instance so that emails associated through the add-in are promoted from the Staged Email \[sys\_email\_staging\] table to the Email \[sys\_email\] table, making them visible to agents in the workspace.


## Accessibility and localization

-   **Localization information**

    The CRM Outlook Add-in is available in Arabic, Brazilian Portuguese, Chinese \(Simplified and Traditional\), Czech, Dutch, English, Finnish, French \(France and Canada\), German, Hebrew, Hungarian, Italian, Japanese, Korean, Norwegian, Polish, Portuguese, Russian, Spanish, Swedish, Thai, and Turkish. Language packs are installed automatically when the corresponding ServiceNow base system language plugin is active.


**Parent Topic:**[Sales Customer Relationship Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/release-notes/sales-order-management-rn-landing.md)

## Version 1.2.1

The September 2026 release includes user experience improvements.

### What's changed

-   **[Associate an email with an existing CRM record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/associate-email-crm-outlook.md)**

    Reduce user confusion when records can't be displayed or found.

    -   Previously, users saw a blank page when a linked record couldn't be displayed. Now, users receive information that helps them understand whether the record is unavailable or access is restricted, along with guidance on next steps.
    -   Previously, users saw a blank page when searches and filters returned no matching records on the Lead, Account, Contact, and Opportunity tabs. Now, users receive guidance to help them refine their search criteria or create a new record.

