---
title: Finance Close Automation release notes
description: Version history for the Finance Close Automation application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-finance-close-auto.html
release: store
topic_type: reference
last_updated: "2020-06-18"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - Finance Close Automation release notes, ServiceNow Store release notes]
---

# Finance Close Automation release notes

Version history for the Finance Close Automation application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 6.7.1 - June 2020**
    -   New:
        -   Global search capability in Finance Workspace, enabling users to easily search for finance close records, such as close tasks, journal entries, or follow-up tasks
        -   Create dependencies from within workspace between close tasks when the workbook is in the Planning state
        -   Mass update of close tasks
        -   Added Weighted Progress field to allow calculating close progress by Entity and Region in future
    -   Changed:
        -   Modified configuration to prevent changing the planned date of the successor task after creating a dependency between tasks
        -   Create follow-up tasks even after a close task is complete
    -   Fixed: Close Assist logic now displays prior period journal entries
-   **Version 6.6.0 - May 2020**
    -   New:
        -   Define and track service level agreements \(SLAs\) on tasks.
        -   View and monitor task SLAs in the Finance Close Dashboard using SLA reports.
        -   Configure the property to set when the business rule is to be triggered synchronously for rolling up task state upon state change.
    -   Fixed: Performance latency fixes
-   **Version 6.1.0 - March 2020**
    -   New:
        -   Use Finance Workspace, an intuitive multi-tab interface, to manage your work.
        -   Use the Finance Close dashboard for reporting and analytics.
        -   Select whether a task with JE workflow should be completed manually or automatically.
    -   Fixed: Journal entry validation performance fixes
-   **Version 5.2.4 - January 2020**
    -   New:
        -   Use the NetSuite ERP integration for the automated posting of journal entries to your NetSuite ERP system.
        -   Configure the sheet name that will be used when uploading the Excel file to create journal entries.
        -   Upload a CSV file to import journal entries.
    -   Fixed:
        -   Journal entry workflow issue on changing the task type.
        -   Error handling during journal entry import.
-   **Version 5.2.3 - November 2019**
    -   New:
        -   Group assignment for close tasks.
        -   Mass approval and rejection of close tasks and journal entries.
        -   Extension point to configure edit permissions for close tasks.
        -   Auto-push journal entries for the reversal in case of reversal failure.
    -   Changed:
        -   Posted journal entries now shown by JE type.
        -   Modification to Groups feature in the application: Changed module name from JE Approval Groups to Groups. Changed group type from Journal Approver to Finance Close. Groups of type Finance Close have finance close roles also associated with them.
    -   Fixed:
        -   Reversal issue fixes for synch and error handling.
        -   Date formats supported in reversals.
        -   Modifications to journal entry reversal field validations for JE type.
        -   Minor fixes to close task owner validations so they can't be both JE preparer and approver.
        -   Changes to entity code logic for multiple ERP scenarios.
-   **Version 5.2.0 - September 2019**
    -   The ServiceNow Finance Close Automation application enables you to use workflows and automation to reduce your finance close risk and accelerate your finance close.
        -   Task management and automated journal entries
        -   Easy and intuitive portal for managing Finance Close
        -   Integrated Policy and Compliance
        -   Real-time ERP integration \(SAP and Oracle Connectors\)
        -   Easy configuration with Guided Setup

