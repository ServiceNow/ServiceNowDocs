---
title: Logik.ai 2025/05/02 release notes
description: Logik.ai 2025/05/02 release notes include new enhancements and minor bug fixes.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/other-release-notes/oob-rn-logik-ai-2025-05-02.html
release: other
topic_type: reference
last_updated: "2025-11-25"
reading_time_minutes: 3
breadcrumb: [Logik.io available versions, OOB Other release notes]
---

# Logik.ai 2025/05/02 release notes

Logik.ai 2025/05/02 release notes include new enhancements and minor bug fixes.

## Schedule

|Sector|Upgrade|
|------|-------|
|Demo|Thursday, May 01, 2025, 8 pm CT|
|Test|Thursday, May 15, 2025, 8 pm CT|
|Prod|Friday, Jun 06, 2025, 8 pm CT|

Example: an environment with URL https://\[YourLogikURL\].prod.logik.io receives this build Jun 06, 2025.

## Release notes

This release version includes the following new enhancements and fixes.

## New enhancement: Admin access control

Admins can now limit access to the following areas:

-   Deploy
-   Utilities
-   Configuration
-   Transaction Manager
-   Managed Tables
-   End user

Users will be able to add/remove/update user permissions via CSV.

Permissions levels will be None, Read, Write, and Admin. For some areas these permissions are collapsed \(such as deploy only having None or Admin\).

Turning this feature on requires a support ticket. The behavior users will see when enabling this feature is non-disruptive, meaning all current admin users have full admin privileges until you upload a CSV file changing those privileges.

For more information, see [ServiceNow CPQ Admin: User Access Control](https://www.servicenow.com/docs/r/order-management/logik_admin_user_access_control.html).

## New enhancement: Admin Managed Tables updates

Managed Tables received a major UX and functionality rework.

-   Columns in Managed Tables are now resizable by the user
-   Autosave now occurs when you click out of a row rather than out of a cell, meaning that a row won't change until you are done editing the entire row - when a row has autosaved, it flashes green
-   Managed Tables now support sorting and filtering
-   Managed Tables now allow you to scroll left and right to see your expanded data
-   Managed Tables allow for freezing columns as you scroll left and right
-   Users can now disable autosave to edit multiple rows then save manually after they are done to keep multiple rows in sync
-   When a Managed Table is filtered the export functionality allows for exporting a subset of rows
-   After downloading a partial set of managed table data if you make changes and uploading via matrix loader data is now patched to the current data rather than replacing the entire table dataset

## New enhancement: Library functions

Library functions are reusable functions that enable the user to create a script that is callable across rules advanced conditions and advanced actions. Library functions can be enabled via support ticket.

A new “Function Library” section has been added to the Utilities menu. This enables the creation of library functions. In this new section of the Admin users are able to manage their functions.

Calling library functions inside advanced scripts can be done by typing fn.&lt;LibraryFunctionName&gt;.

What you can do inside a library function:

-   Execute table lookups
-   Execute typical Array, String, Boolean, and Mathematical operations
-   Set default values per parameter and create docstrings

What you can't do inside a library function:

-   Directly reference fields: these must be passed in to your parameters if you want to use their value within your function
-   Update the value of a field
-   Call another library function

## New enhancement: Transaction Manager

Easily download a 90-day history of field edits for any transaction. Available in the Utilities section—just enter a Transaction ID to get the edit history as a Parquet file.

## New enhancement: Flightpath for Transaction Manager

Easily debug rules with Flightpath—a visual tool in the Runtime UI that shows how the rules engine responds to user inputs and events. Intended for Admin use only.

## New enhancement: Smooth Scroll

New `autoScrollIntoView` layout property smooths the scroll interaction between the transaction body and LIG.

## New enhancement: Long text support

New `supportLongText` layout property for LIG and Product Search List Result fields displays a popover when an enabled field is selected. This supports use cases for fields with long text values.

## New enhancement: Field Type textArea - LIG expandable editable field

The textArea field type supports an expandable editable field in the Line Item Grid.

## Bug fixes

|Fix|Short description|
|---|-----------------|
|LGK-16808|Fixed a bug where dynamic picklists were not able to find associated tables|
|LGK-16998|Fixed a bug in Transaction Manager that could cause errors upon reconfigure of a product while changing the quantity of child line items|
|LGK-17023|Resolved an issue where deployment time of Solution Configuration Blueprints was slower than expected|
|LGK-17049, LGK-17059|Resolved issues in Transaction Manager where product search was not properly paginated|

## Additional resources

-   Request new features or enhancements through the [Idea portal](https://support.servicenow.com/ideas) on [Now Support](https://support.servicenow.com/now).
-   Connect with other Logik.io users at [Now Community](https://www.servicenow.com/community/)

**Parent Topic:**[Logik.io available versions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/other/markdown/other-release-notes/oob-rn-logik-io.md)

