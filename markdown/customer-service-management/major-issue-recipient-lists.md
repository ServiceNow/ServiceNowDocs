---
title: Recipients lists
description: Use recipients lists that contain account or consumer information to create the child cases for a major case.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Major issue management overview, Administer Customer Service Management, Customer Service Management]
---

# Recipients lists

Use recipients lists that contain account or consumer information to create the child cases for a major case.

Major issue managers and customer service managers can select the desired list in the **Affected Customers** field on the Major Case form. Selecting **Create Child Cases** then creates a child case for each account or consumer in the recipients list.

Managers can change the recipients list before child cases are created. After child cases are created, the **Affected Customers** field becomes read only.

## Creating recipients lists

Recipients lists are created using the [Targeted Communications](c_TargetedCommunications.md) application. With this application, managers can select the type of list to create and the method used to create the list: by uploading files, selecting dynamic conditions, or using scripts.

The Targeted Communications application creates several types of recipients lists, including accounts, contacts, consumers, and internal users. The recipients list for a major case must be of type accounts or consumers. Recipients lists are limited to one specific type and can’t contain mixed types, for example accounts and consumers.

**Note:** The Major Issue Management plugin is dependent on the Targeted Communications plugin. If Targeted Communications is active, recipients lists can be created for internal users. If Targeted Communications and Customer Service Management are both active, recipients lists can also be created for accounts, contacts, and consumers.

## Manually editing a recipients list

Major issue managers and customer service managers can manually add or remove accounts or consumers from a recipients list by navigating to the Recipients List form, selecting **Edit** in the **Recipients** related list, and then using the arrows to add or remove records.

The **Recipients** related list includes the **Dynamically Added** column which displays either True or False, depending on how a record was added:

-   True for records that are dynamically generated, either by using the condition builder or by running a script.
-   False for records that are added manually, either by using the **Edit** button on the **Recipients** related list or by file upload.

The **Active Communication** column is set to True by default for both dynamically and manually added records. This field indicates whether the recipient requires active communication.

## Refreshing a recipients list

Refresh a recipients list by selecting **Refresh Recipient List** on the Recipients List form. For major issue management, the following guidelines apply to refreshing a recipients list:

-   Refreshing a recipients list doesn’t impact manually created records.
-   If you remove a manually created record from a recipients list, it doesn’t reappear when the list is refreshed unless it meets the dynamic conditions used to filter the list.
-   If you remove a dynamically generated record from a recipients list, it may reappear when the list is refreshed if it meets the dynamic conditions used to filter the list.
-   If the **Active Communication** field is set to false for a record, this setting doesn’t change when a recipients list is refreshed.
-   If created using the Upload File method, you don’t need to refresh the recipients list.

**Related topics**  


[Create a recipients list](../task/t_TargetCommCreateRecipientList.md)

