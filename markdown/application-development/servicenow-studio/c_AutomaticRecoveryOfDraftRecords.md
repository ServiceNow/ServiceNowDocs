---
title: Legacy - Automatic recovery of draft records
description: Studio can maintain a version of any open existing record with unsaved changes. Users can recover unsaved changes when their user session ends unexpectedly due to network latency, session timeout, or service interruption.
locale: en-US
release: xanadu
product: ServiceNow Studio
classification: servicenow-studio
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Legacy - ServiceNow Studio, Building pro-code applications, Developing your application, Building applications]
---

# Legacy - Automatic recovery of draft records

Studio can maintain a version of any open existing record with unsaved changes. Users can recover unsaved changes when their user session ends unexpectedly due to network latency, session timeout, or service interruption.

**Important:** Starting with the Xanadu release, the legacy version of ServiceNow Studio is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported. For details on the deprecation process, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

Try building and editing apps in the current version of ServiceNow Studio instead. For more information, see [Building applications with ServiceNow Studio](../../servicenow-studio/concept/servicenow-studio-landing.md).

Automatic recovery only applies to:

-   Records open in Studio. The system does not save all draft records.
-   Changes made in desktop \(non-mobile\) browsers. The system does not save draft records from mobile browsers.
-   Changes made to existing records. The system does not save draft changes to new records.
-   Records containing unsaved changes that are the most recent update to the record. The system discards draft changes when another user has updated the same record.
-   Records for tables that extend the Application File \[sys\_metadata\] table.

After the user re-establishes a session, Studio displays a message for each record with recovered changes.

![The automatic recovery message reads, Previous unsaved edits to this record have been recovered. Continue to edit or clear the changes.](../image/AutorecoveryUnsavedChanges.png "Automatic recovery message")

For each recovered record, users can:

-   Continue editing and save the record.
-   Clear the changes from the recovery cache.

The system automatically clears changes from the recovery cache when a user:

-   Saves the record. The system removes the saved record from the recovery cache.
-   Confirms navigating away from a record without saving changes. The system removes the abandoned record from the recovery cache.
-   Reaches the recovery cache limit of 5 MB of changes. The system removes the record with the oldest update date-time stamp.

By default, automatic recovery is enabled for all Application File \[sys\_metadata\] tables while working from Studio.

Administrators can configure automatic recovery properties to:

-   Disable or re-enable automatic recovery.
-   Specify a list of field types to exclude from automatic recovery.

Users can enable or disable automatic recovery as a user preference.

-   **[Legacy - Auto recovery properties](../reference/r_AutoRecoveryProperties.md)**  
Administrators can configure how Studio handles the recovery of draft records by navigating to **Auto Recovery** &gt; **Properties**.
-   **[Legacy - Auto recovery dictionary attribute](../reference/r_AutoRecoveryDictionaryAttributes.md)**  
Administrators can configure how the Studio handles the recovery of draft records with a dictionary attribute.

**Parent Topic:**[Legacy - ServiceNow Studio](c_ServiceNowStudio.md)

**Related topics**  


[User preferences](https://www.servicenow.com/docs/access?context=c_UserPreferences&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US)

