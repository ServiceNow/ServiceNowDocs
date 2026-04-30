---
title: Change Management release notes
description: The ServiceNow Change Management application provides a systematic approach to control the life cycle of all changes, facilitating beneficial changes to be made with minimum disruption to IT services. Change Management was enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
---

# Change Management release notes

The ServiceNow® Change Management application provides a systematic approach to control the life cycle of all changes, facilitating beneficial changes to be made with minimum disruption to IT services. Change Management was enhanced and updated in the Zurich release.

## Change Management highlights for the Zurich release

-   Review and authorize change requests and review recently implemented changes in the Change Advisory Board Workbench in the Service Operations Workspace \(SOW\).
-   Track conflict detection using the Change - Conflict Detection flow and the Change Management Worker table instead of Progress Workers.
-   Limit the number of conflict records for each conflict type through the **change.conflict.max\_count** system property.
-   Coral is the new default theme for Next Experience and Core UI, offering a more modern experience.


See [Change Management](https://www.servicenow.com/docs/access?context=c_ITILChangeManagement&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US) for more information.

## Important information for upgrading Change Management to Zurich

As part of the update to use Flow instead of Progress Workers for conflict detection, the Conflict Checker Progress UI Formatter record references a new UI macro, change\_conflict\_worker\_progress\_gate. This macro checks the **change.conflict.useprogressworker** system property to determine the conflict detection mechanism and then displays the corresponding UI macro to work with either Progress Workers or the Change Management Worker table. For more information, see [Conflict detection](https://www.servicenow.com/docs/access?context=c_ConflictDetection&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US).

## New in the Zurich release

-   **[Control opening of CAB meetings](https://www.servicenow.com/docs/access?context=attend-cab-meeting-using-cab-workbench&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

    Control the opening of a CAB meeting from the CAB Meeting calendar in the CAB Meeting workbench in Service Operations Workspace or in the Core UI through the **sn\_change\_cab.com.snc.change\_management.cab.use\_sow\_meeting** system property. For more information, see [Change Management properties](https://www.servicenow.com/docs/access?context=r_ChangeManagementProperties&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US).

-   **[Track conflict detection](https://www.servicenow.com/docs/access?context=c_ConflictDetection&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

    Track the progress of conflict detection using the Change - Conflict Detection flow \(that runs as a system user\) and the Change Management Worker table instead of Progress Workers. You can choose between the Flow and Progress Worker options by updating the **change.conflict.useprogressworker** system property.

    A new UI formatter **change\_conflict\_worker\_progress\_gate.xml** has been introduced to the change request form to replace the existing **change\_request\_conflict\_progress.xml**. This update supports the **change.conflict.useprogressworker** system property when you upgrade to Zurich. The new formatter displays the same Conflict tab but selects the macro version to render the form according to the value of the new system property.

-   **[Define the maximum records for conflict detection](https://www.servicenow.com/docs/access?context=configure-conflict-properties&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

    Limit the maximum number of conflict records that can be generated for each conflict type when conflict detection runs through the **change.conflict.max\_count** system property; create this system property if it is not already present.


## UI changes

-   **Coral theme**

    Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.


## Changed in this release

-   **[Propose a standard change template in Service Operations Workspace](https://www.servicenow.com/docs/access?context=propose-standard-change-sow&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

    As a user with the itil role, you can create a standard change template proposal in Service Operations Workspace.


## Activation information

Change Management is a ServiceNow AI Platform feature that is active by default.

## Accessibility information

-   **Dark theme**

    The new Coral theme includes a dark theme option for web and mobile experiences. This option is commonly used to alleviate eye strain and improve readability.


**Parent Topic:**[IT Service Management release notes](it-service-management-rn-landing.md)

