---
title: Enable enhanced address model for accounts
description: Use the Account Address table in the enhanced address data model feature to link a location with multiple accounts without creating duplicate location records.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Enhanced address data model for accounts, Customer data, Set up your environment, Configuring Customer Service Management, Customer Service Management]
---

# Enable enhanced address model for accounts

Use the Account Address table in the enhanced address data model feature to link a location with multiple accounts without creating duplicate location records.

## Before you begin

Role required: admin

## Procedure

1.  Take a backup of the location data associated with accounts from the Location \[cmn\_location\] table.

2.  Create the custom relationship fields in the Account Address \[account\_address\_relationship\] table if they have already been created in the Location table.

    The newly created fields in the Account Address table need to have the same name and type as the fields in the Location table. The base system provides two relationship fields.

    -   **Type**
    -   **primary**
    These relationship fields are created in the Account Address \[account\_address\_relationship\] table. For more information on creating new fields within a table, see [Add and customize a field in a table](https://www.servicenow.com/docs/access?context=t_CreatingNewFields&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

3.  Update the custom code that references the Account Address table.

    The custom code can include elements that fetch the address of accounts in the Account Address table. Such elements can be reference qualifiers, script includes, business rules, and ACLs pointing to the Location table.

4.  Move the account related data from the Location table to the Account Address table.

5.  Run the following migration script.

    ```
    var customRelationshipFields = []; //Add custom relationship fields (if any).​
    var account = ""; //You must specify the sys_id of the account if you wish to migrate location data for that account (mostly to be used during re-run).​
    var migrateChildAccountLocations = false; // This value must be set to true if you wish to migrate the locations of the child accounts associated with the specified account (mostly to be used during re-run).​
    new sn_cs_base.CSDataFix().migrateLocationDataToAccountAddress(customRelationshipFields, account, migrateChildAccountLocations);​
    ```

    Performing a re-run of the script if there is a difference between the number of records that must be migrated and the number of records already migrated. In the event of a re-run, already migrated locations will not be migrated again. To re-run migration for already migrated locations, delete the corresponding records in the account address table.

6.  Prevent accidental data entry by deactivating the Account and Custom Relationship fields from the Location table.

    **Note:** You must not deactivate Type and Primary attributes.

    This deactivation will remove the Account and the Custom Relationship fields from the location-related forms, lists, and related lists.

7.  Set the system property **enable\_account\_address\_sharing** to true.

    This property enables the enhanced address data models for accounts. The Account Addresses related list is displayed on the account and location form.


