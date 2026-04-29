---
title: Configure a related list screen for a record screen
description: Create a related list screen to give your users easy access to records related to the record they're already viewing.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Record screen, Mobile screen types, Mobile screens, Mobile app components, Building mobile apps, Mobile Platform]
---

# Configure a related list screen for a record screen

Create a related list screen to give your users easy access to records related to the record they're already viewing.

A related list appears in a tab on your mobile form, and displays a list of records relating to the record on the form. For example. If you are viewing a problem record, you may want your related list to display all incident records associated with that problem record.

**Note:** Supported relationships are defined by a reference field between two tables. Custom relationships created using the Relationships \[sys\_relationship\] table or scripted relationships aren't supported with this component.

Creating a related list involves three tasks:

-   **1. [Create a parametrized data item for your related list](../task/sg-create-related-list.md)**

    Create a parametrized data item to contain the records that display in your related list.

-   **2. [Create a list screen to use as a related list](../task/sg-create-related-list-2.md)**

    Create a related list using your parametrized data item. This list appears for your users when they select the related list tab on their form screen.

-   **3. [Update your record screen to display a related list](../task/sg-create-related-list-3.md)**

    Update your record screen to display a list of related records, and define the relationship between your record screen and the related list.


