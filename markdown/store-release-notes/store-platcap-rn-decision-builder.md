---
title: Decision Builder release notes
description: Version history for the Decision Builder application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-platcap-rn-decision-builder.html
release: store
topic_type: reference
last_updated: "2024-02-01"
reading_time_minutes: 5
breadcrumb: [ServiceNow Store - Other ServiceNow AI Platform Capabilities applications, ServiceNow Store - ServiceNow AI Platform Capabilities release notes, ServiceNow Store release notes]
---

# Decision Builder release notes

Version history for the Decision Builder application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 6.1.0 - February 2024**
    -   New:
        -   Integrated Decision Builder into the new Workflow Studio alongside Flows, Processes, and more, so users can view and create all logic and automation from a single entry point.
        -   Added a create code snippet feature to execute the decision table from any script and make it easier to replace hardcoded logic with decisions.
        -   Added a duplicate row feature to make it easier and faster to build decision tables in the Decision Builder interface.
        -   Added a duplicate decision table feature that allows users to copy full decision tables under 300 rows or the decision table structure \(inputs and columns\) for large decision tables.
        -   Added a view related objects feature so developers can see which flows are leveraging the decision table and better understand the impact of any changes.
    -   Changed:
        -   Changed the experience for advanced decision rows to left align and shorten the expression snippet that appears in condition cells.
        -   Made significant changes to both execution APIs to reduce the time it takes to evaluate decision tables.
    -   Fixed: Fixed UI timeout errors that were occurring as a result of large operations like saving many new decision rows or deleting condition columns.
-   **Version 5.0.0 - August 2023**
    -   New:
        -   Added draft authoring, which enables users to create decision tables in draft mode before publishing to make them available for execution via script or Flow Designer logic. Published tables can be edited in draft mode and republished with changes.
        -   Added a Test feature that allows users to choose a version and execution method and enter sample input data to run through the decision table logic.
        -   Added UI support for reference filters on inputs and result columns. Reference filters can be used to limit drop-down lists in the decision table for condition columns that evaluate reference records and reference result columns.
        -   Added support for the duration field type in result columns.
        -   Added support for editing decision tables containing advanced rows in Excel. Tables with advanced rows can now be edited in Excel but advanced rows are read-only.
    -   Fixed:
        -   Resolved issues using decision results in subsequent Flow Designer actions.
        -   Resolved issue that was preventing import from Excel if template was exported by user with Decision Rule Author or Decision Result Editor roles.
        -   Removed default answer decision from scriptable API response if decision table does not have a default result specified.
        -   Other minor fixes.
-   **Version 4.1.2 - May 2023**
    -   New: Added ability for users to reference existing choice lists when creating inputs and result columns where type = choice. Users can use choice fields from tables where the scope matches the decision table scope.
    -   Changed:
        -   Updated page theming to align with ServiceNow brand updates
        -   Improved accessibility support in Decision Builder; optimized page for browsers zoomed up to 200% and improved tab order and screen reader navigation
        -   Updated behavior of Close button in Decision Builder UI to follow new logic - if you navigate to Decision Builder by a method that opens it in the same browser tab, selecting Close returns you to the originating environment. If you navigated to Decision Builder by a method that opened it in a new browser tab, selecting Close closes the browser tab
-   **Version 4.0.0 - February 2023**
    -   New:
        -   Added the default result row which enables users to specify default result values for any result columns. Default values are returned if the decision table execution does not yield a result
        -   Added input, condition column, and result column support for the currency field type
        -   Added result column support for the date, date/time, and due date field types
        -   Added a new system property \(com.glide.decision\_table.excel\_hide\_references\). When set to true, decision tables exported to Excel will not include drop-down lists of records for condition or result columns with type = reference
    -   Changed: Decision tables created prior to v4.0 will now display a default result row in Decision Builder. Unless a user specifies a default result, the row will be empty and the decision table execution results will not change.
    -   Fixed:
        -   Choice labels will display in the user's language
        -   Addressed import from Excel reference column issues related to permissions
        -   Other minor fixes
-   **Version 3.1.0 - November 2022**
    -   New:
        -   decision\_rule\_author role:
            -   With this role, user has read access to all decision table data.
            -   In Decision Builder, user can create, edit, rearrange, and delete decision rows, including all cells in them.
        -   decision\_result\_editor role:
            -   With this role, user has read access to all decision table data.
            -   In Decision Builder, user can modify result cells for any existing decision rows.
            -   User cannot modify condition cells or create, delete, or rearrange rows.
    -   Minor fixes
-   **Version 3.0.1 - August 2022**
    -   New:
        -   Users can now export decision tables to Microsoft Excel. Excel can be used to manage decision rows and users can import changes back into Decision Builder.
        -   Added support for localization in the Decision Builder UI.
        -   Added UI support for Change Approval Policies.
        -   All decision rows can now be opened in Decision rule view to enable complex rules. Decision tables with complex rules do not support the Edit in Excel feature.
    -   Changed:
        -   Reference qualifiers on inputs will be applied to condition columns where the Data to evaluate = Reference record.
        -   Minor fixes.
-   **Version 2.0.2 - June 2022**

    Minor fixes.

-   **Version 2.0.1 - May 2022**

    Minor fixes.

-   **Version 2.0.0 - March 2022**
    -   New:
        -   Get Multiple Results With Decision Tables. Each decision table can now have one or more result columns and each rule can have one or more result values.
        -   Additional Field Types for Results. You can now have any of the following field types for results.Previously, only the reference records were supported as results.
            -   Choice
            -   Decimal
            -   Integer
            -   Long
            -   Reference
            -   String
            -   String \(Full UTF-8\)
            -   True/False
        -   Integrate Decision Table Builder with App Engine Studio. App Engine Studio \(AES\) users can now create decision tables using an AES wizard and access new and existing decision tables in AES.
    -   Changed:
        -   Updated keyboard navigation experience
        -   Updated behavior of plus sign between conditions and results to add both condition and result columns
    -   Fixed: Minor usability issues
-   **Version 1.1.2 - December 2021**
    -   Fixed:
        -   Access record lists for reference fields when the data type is Reference
        -   Condition column with Reference data type supports input types, Choice and Text
        -   Application loads as expected when the Accessible From field's value is set to This application scope only
        -   Minor usability fixes
-   **Version 1.1.0 - October 2021**
    -   New:
        -   Decision Designer is rebranded as Decision Builder
        -   Decision Builder now supports the Quebec and Rome releases
-   **Version 1.0.2 - September 2021**

    Decision Designer enables developers to decouple decision logic from their code to create and maintain decision rules in applications. With Decision Designer, it’s seamless to update your business rules anytime as you can modify decision rules without changing the code.


