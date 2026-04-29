---
title: Dynamic related records
description: Display related records in the Contextual side panel in CSM Configurable Workspace that dynamically change based on the context of the current record or playbook activity.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configure dynamic related records, Agent tools, Organize agent workspaces, Configure, Customer Service Management]
---

# Dynamic related records

Display related records in the Contextual side panel in CSM Configurable Workspace that dynamically change based on the context of the current record or playbook activity.

The dynamic related records feature provides customer service agents with easy access to the information they need when they need it. Agents can view related records in the Contextual side panel without navigating away from the current tab and searching for information in other related lists. This feature also enables users to display related records without requiring any type of reference or parent-child relationship.

Different types of agents can use dynamic related records to see different information. For example:

-   A front-line agent creating a new case can see similar, recently opened cases.
-   A middle-office agent reviewing a complaint case can see active contracts for the customer.
-   A back-office agent can view emails for a selected playbook activity.

To view related records, click the Related Records tab in the Contextual side panel in CSM Configurable Workspace. Records appear in the Related Records list as read-only cards.

![Tab that displays record cards with brief descriptions of recent cases relevant to the current record or playbook task.](../image/csm-playbook-related-records-tab.png "Related Records tab in the Contextual side panel")

## Configuring dynamic related records

System administrators can configure the dynamic related records feature and define the following information:

-   Context records that specify the type of record for which related records are displayed, such as a case record or a playbook activity. A context can also specify any conditions for the record type that must be met in order for related records to be displayed.
-   Definitions for each specific type of related record to display, such as SLAs or contracts.
-   Relationships between context records and their associated definition records.

System administrators can also configure the related record card format. For more information, see [Configuring dynamic related records](dynamic-related-records-configure.md).

## Using dynamic related records

Agents can search the Related Records list by entering text in the search field or filter the list to display records of a specific type, such as SLAs or active customer contracts. Agents can expand a card to show more a more detailed view or open the list in a sub-tab. If agents have create permission, they can also create new related records of the selected type.

For more information about these agent actions, see [Using the Related Records tab in the contextual side panel](using-dynamic-related-records.md).

## Dynamic related records plugin

The Dynamic Related Records for Configurable Workspace plugin \(com.snc.uib.sn\_dyn\_rel\_rec\) is available from the ServiceNow Store.

Install any ServiceNow Store applications by requesting them from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

This plugin provide agents with access to related information based on the context of the current record or playbook activity. System administrators can configure related record definitions that make data available in context to the action that the agent is performing.

This plugin adds the Dynamic Related Record menu and the following modules to the application navigator:

-   Related Record Contexts
-   Related Record Definitions

This plugin also adds several related record definitions. For more information, see [Related record definitions included with the plugin](dynamic-related-records-configure.md#section_khj_gwl_jpb).

## Using dynamic related records with Playbooks for Customer Service Management

The Playbooks for Customer Service Management plugin \(sn\_csm\_playbook\) adds the dynamic related records feature to CSM Configurable Workspace. It also includes the Case context record and several related record definitions.

The Case Playbook for Onboarding, Case Playbook for Complaints, and Case Playbook for Product Support applications include additional context records and related record definitions.

**Related topics**  


[Configure dynamic related records](dynamic-related-records-configure.md)

[Using the Related Records tab in the contextual side panel](using-dynamic-related-records.md)

