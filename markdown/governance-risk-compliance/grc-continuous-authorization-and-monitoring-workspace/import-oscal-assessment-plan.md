---
title: Import an OSCAL Assessment Plan
description: Import OSCAL Assessment Plan files to automatically create engagements, control tests, and assessment procedures in your authorization package.
locale: en-US
release: australia
product: GRC: Continuous Authorization and Monitoring Workspace
classification: grc-continuous-authorization-and-monitoring-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [OSCAL Assessment Plan export and import, CAM OSCAL, Continuous authorization and monitoring tasks in the CAM Workspace, Using CAM, Continuous Authorization and Monitoring, Governance, Risk, and Compliance]
---

# Import an OSCAL Assessment Plan

Import OSCAL Assessment Plan files to automatically create engagements, control tests, and assessment procedures in your authorization package.

## Before you begin

-   OSCAL Assessment Plan file is validated using the OSCAL CLI tool
-   The corresponding Catalog, Profile, and SSP files must be available
-   If importing for an existing package, the provider packages must exist in the instance with matching source identifiers \(for inherited controls\)

Role required: sn\_irm\_cont\_auth.info\_system\_sec\_manager, sn\_irm\_cont\_auth.info\_system\_sec\_officer, or sn\_irm\_cont\_auth.admin

## About this task

Importing with the OSCAL Assessment Plan model creates the complete package structure including boundary, package, controls, engagements, control tests, and assessment procedures. Each AP file creates one engagement. You can import multiple AP files together for packages with multiple engagements.

The import wizard guides you through file attachment, user mapping, and preview before creating records. After import, an asynchronous job processes the files in sequence and creates all related objects.

## Procedure

1.  Navigate to **CAM Workspace** &gt; **OSCAL Import**.

2.  In the CAM Workspace, select the OSCAL import landing page icon.

3.  In the OSCAL Import page, select **New Import**.

4.  From the OSCAL **Model** drop-down, select **AP**.

5.  In the **Source** field, enter the source system identifier.

    The source identifier helps maintain uniqueness when importing from external systems. Use a consistent source name for packages from the same external instance.

6.  In the **Import status recipients** field, select the users who should be notified when the import completes.

    Recipients receive an email notification after the import is complete.

7.  Select **Next** to proceed to file attachments.

8.  Attach the mandatory files:

    1.  Under Catalog, select **Attach files** and upload the catalog JSON file.

    2.  Under Profile, select **Attach files** and upload the profile JSON file.

    3.  Under SSP, select **Attach files** and upload the SSP JSON file.

    You can also include boundary, data flow, network, and enterprise architecture illustrations, if necessary.

9.  Select **Next** to proceed to attach additional files.

10. If your package includes overlays, select **Overlay Attachment** and upload one or more overlay JSON files.

11. Under Overlay attachment, select **Assessment Plan Attachments** and upload one or more AP JSON files.

12. If your package includes POA&amp;Ms, select **POAM Attachment** and upload the POA&amp;M JSON file.

13. Select **Next**.

    The system validates all attached files against OSCAL standards. If validation fails, error messages display indicating which files have issues. If validation succeeds, the wizard proceeds to user mapping.

14. In the user mapping screen, review the list of users from the OSCAL file.

    OSCAL users are automatically mapped to ServiceNow users and appear with the following mapping status:

    -   Auto-mapped: Indicates that a ServiceNow user with a matching username is found.
    -   Blank: Indicates no matching ServiceNow user is found, and that manual mapping is required.
15. For OSCAL users without a corresponding ServiceNow user, select the appropriate ServiceNow user from the drop-down.

16. Verify mandatory roles are assigned:

    Required roles include:

    -   System Owner
    -   Information System Security Officer \(ISSO\)
    -   Information System Security Manager \(ISSM\)
    If any mandatory role is unassigned after auto-mapping, manually select a user for that role.

17. Select **Next** to proceed to the preview screen.

18. Review the preview section.

    The preview displays objects that will be created, overridden, or skipped based on whether the package exists in the target instance.

    **For new packages:**

    All objects display as "Create New":

    -   SSP-related objects: Baseline controls, inherited controls, hybrid controls, information type definitions
    -   AP-related objects: Engagements, control tests, test plans, entity to engagement mappings
    On import, all objects are created.

    **For existing packages:**

    All SSP and AP related objects display as "Override" by default. If you skip the package, all related objects are skipped automatically, including baseline controls, information type definitions, inherited controls, hybrid controls, engagements, test plans, control tests, and entity to engagement mappings.

    Objects that skip automatically:

    -   Information type definitions already in the library
    -   Policies already existing in the instance
    Information type definitions and policies skip because they exist independently of packages and are not tightly coupled with authorization boundaries.

19. To skip specific object types, select them and choose **Skip**.

    You can skip objects at the boundary or package level. When you skip an authorization package, all child objects \(baseline controls, engagements, test plans, control tests\) skip automatically due to parent-child relationships.

20. Select **Import** to begin the import process.

    A confirmation message displays indicating the import process has started.

21. On the status screen, monitor the import progress.

    The status screen displays each model being processed:

    -   Pending - Queued for processing
    -   In Progress - Currently processing \(shows start date\)
    -   Success - Completed \(shows start and end dates\)
    -   Error - Failed \(shows error details\)
    The Assessment Plan typically takes a few minutes to process depending on the number of controls and control tests being created.

22. After all models show Success status, navigate to the authorization package to verify the import results.

    Verify engagements were created, control tests exist for expected controls, and test plans are populated with assessment procedures.


**Parent Topic:**[OSCAL Assessment Plan export and import](../concept/oscal-assessment-plan-import-export.md)

