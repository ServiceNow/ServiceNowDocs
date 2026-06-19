---
title: Input forms in offline
description: Input form screens in offline mode support viewing, editing, and creating records without network connectivity. The ServiceNow apps use locally cached data to display forms, populate fields, and apply form logic, so users can continue working without interruption. Well-designed offline input forms, reduce rework and minimize sync conflicts.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/mobile/mobile-platform/offline-input-form.html
release: australia
product: Mobile Platform
classification: mobile-platform
topic_type: concept
last_updated: "2026-06-01"
reading_time_minutes: 8
breadcrumb: [Offline mode setup options, Offline mode, Before implementation, Configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Input forms in offline

Input form screens in offline mode support viewing, editing, and creating records without network connectivity. The ServiceNow apps use locally cached data to display forms, populate fields, and apply form logic, so users can continue working without interruption. Well-designed offline input forms, reduce rework and minimize sync conflicts.

Input forms opened while offline can load data captured online if it is included in the offline cache. Users can modify cached data while offline, and their changes are stored locally until synchronization. Offline forms support save progress, input actions, and descriptive elements. All operations, creating, editing, and deleting are queued in the outbox and automatically synced with the instance once connectivity is restored.

For information about input forms, see [Input form screen](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/mobile-platform/parameter-input-screen.md).

## Supported input types

Offline input forms support a predefined set of input types that rely on locally cached data. Supported types include

-   String
-   Number
-   Boolean
-   Date / Time
-   Choice
-   Reference
-   Attachment
-   Barcode

Certain input types, such as custom map, signature, and screen aren't supported offline. Unsupported fields remain visible in a read-only or inactive state depending on configuration.

## Reference input behavior

Reference inputs in offline mode display and resolve data from the local cache, enabling users to select and view reference values without connectivity. Users can search and choose from locally available records. When the required data is not cached, the reference field returns no results.

The number of available reference choices is limited to 1,000 records, with administrators determining which records are downloaded and made available offline. This allows for fine control over which references are preloaded based on business needs, such as user roles, assigned location, or active status.

For more information, see [Reference field attributes for input form screens in offline mode](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/mobile-platform/reference-fields-offline-attributes.md).

**Note:**

Dynamic reference qualifiers or filters that depend on real-time server queries aren't supported offline.

The 1,000-record cap applies per reference input, not per screen. If multiple reference inputs point to the same table across one or more screens, each input contributes its own slice of up to 1,000 records. These slices are merged and deduplicated on the device, meaning the total records stored for a single table can significantly exceed 1,000. Plan for increased device storage and longer initial sync times when multiple inputs share the same target table.

## Auto-fill form inputs and input actions

Input form fields and input actions can be automatically populated with data downloaded from the instance using data sources configured in the mobile app. The same data source configuration applies to both online and offline modes. For more information, see [Data sources](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/mobile-platform/data-sources.md).

When the device is online, the data source retrieves information directly from the instance. When the device is offline, the same data source continues to function using locally cached data downloaded as part of the offline payload. This allows fields to auto-fill with relevant values even without network connectivity.

-   **Example**

    If a form uses a data source to populate the Location field based on the selected work order, the same data source logic is applied in offline mode, provided that the work order and location tables were included in the offline payload.


## Save progress in offline mode

Users can manually save in-progress forms while offline using the **Save** button in the top navigation bar. This action stores the current state of the input form locally on the device without submitting it to the server. Saved forms can later be resumed, edited, or submitted once connectivity is restored. For more information, see [Configure input form screen actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/mobile-platform/input-form-screen-actions-config.md).

The same button configuration used for saving progress in online mode also applies in offline mode, and no additional configuration is required. When the form is offline, the Save button performs a local save instead of a server submission, ensuring that user input is preserved. To support this behavior, the local save for the offline step type is part of the writeback action steps. This step type defines how the platform handles local persistence of form data in offline mode. For more information, see [Configure action items and action steps in offline mode](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/mobile-platform/configure-action-item-offline.md).

Whether online or offline, the Save button behaves according to the same definition, with the platform determining where data is stored, either locally or on the server, based on connectivity state.

## Save and submit actions sync behavior

When users create, update, or delete a record offline, each action generates an outbox item. The outbox acts as a temporary queue that holds pending changes until connectivity is restored. Once online, the system automatically synchronizes outbox items to the instance in the order they were performed. If conflicts occur during synchronization, the system marks the item as failed, allowing users to retry or resolve the issue. For example, when the record was modified on the server while the user was offline.

## Consolidation of outbox items

By default, when users perform multiple actions while offline,such as tapping Save or Submit, each function of type action item generates its own dedicated outbox item. Each action is stored separately in the outbox and synchronized individually when connectivity is restored. For more information, see [Configure an action function](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/mobile-platform/sg-studio-config-action-function.md).

Mobile apps can be configured to consolidate consecutive outbox items created by the same form or screen into a single, merged entry. This configuration applies to both the Save and Submit buttons and helps reduce duplication, optimize synchronization, and maintains a cleaner outbox.

When consolidation is enabled, the following takes place:

-   Multiple consecutive actions of the same button and record context are merged into one outbox item. For example, multiple saves of the same form for the same record.
-   The most recent state of the record is retained, ensuring that only the final user input is synced.

## Attachments in offline mobile forms

Offline mobile forms support attachments added through both the attachment input type and attachment input actions while offline. This allows users to capture and manage files such as images, documents, or videos without connectivity. Attachments previously added while online can also be preloaded into the form when included in the offline payload, as defined in the data source configuration, enabling users to view or reference existing attachments even when working offline.

Attachments added while offline are stored locally on the device and automatically queued in the outbox for synchronization once connectivity is restored.

**Note:** By default, attachments queued in the outbox aren't reflected in the activity stream of the record while the user is offline. For example, when working on a mobile form whose context is *INC123456*, submitting the form will not immediately display the newly added attachment in the activity stream tab of that record. To add attachments to the activity stream of the record while offline, configure the writeback action offline step to reflect added attachments in the record activity stream. This conforms that the attachment appears in the activity stream immediately, even before the device reconnects and synchronizes with the instance.

For more information, see [Using action items and action item steps in ofﬂine mode](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/mobile-platform/offline-action-item-steps.md).

## Descriptive elements in offline mobile forms

Descriptive elements provide instructional or contextual information within an input form screen, helping users understand what is expected of them. Offline input forms support descriptive elements such as images, rich text, and plain text. These elements can be automatically populated with data downloaded from the instance through data sources configured in the mobile app. The same data source configuration is used for both online and offline modes, so no separate data source for offline use is required. For more information, see [Configure descriptive elements for input form screens](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/mobile-platform/descriptive-elements-script.md).

-   **[Configure reference inputs for input form screens in offline mode](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/mobile-platform/reference-fields-offline-mode.md)**  
Configure reference inputs so that users can see a list of records in offline mode on their Mobile Agent.
-   **[Associate input form attachments to the activity stream in offline](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/mobile-platform/input-form-attach-activity-stream.md)**  
Attachments added through input forms aren't displayed in the record activity stream by default, when working offline. Configure the write-back action step to associate attachments with the activity stream, so they appear immediately alongside other record updates.
-   **[Reference field attributes for input form screens in offline mode](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/mobile-platform/reference-fields-offline-attributes.md)**  
Configure the fields that you want to use and the data you want to display in offline mode by using various input attributes.

**Parent Topic:**[Offline mode setup options](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/mobile-platform/offline-setup-options.md)

