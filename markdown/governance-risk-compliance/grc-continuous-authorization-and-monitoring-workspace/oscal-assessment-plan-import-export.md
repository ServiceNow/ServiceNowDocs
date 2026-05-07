---
title: OSCAL Assessment Plan export and import
description: The OSCAL Assessment Plan \(AP\) model enables you to import testing plans from external tools and export engagement data for auditors and authorizers.
locale: en-US
release: australia
product: GRC: Continuous Authorization and Monitoring Workspace
classification: grc-continuous-authorization-and-monitoring-workspace
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [CAM OSCAL, Continuous authorization and monitoring tasks in the CAM Workspace, Using CAM, Continuous Authorization and Monitoring, Governance, Risk, and Compliance]
---

# OSCAL Assessment Plan export and import

The OSCAL Assessment Plan \(AP\) model enables you to import testing plans from external tools and export engagement data for auditors and authorizers.

## Assessment Plan \(AP\) model overview

The OSCAL Assessment Plan \(AP\) model, developed by NIST, represents what needs to be tested and how testing will be performed. The AP model enables organizations to exchange assessment planning data in a standardized format. In CAM, one Assessment Plan JSON file corresponds to one engagement. Each AP file contains the testing plan that can be distributed to auditors and attestation teams who perform control testing. When a package has multiple engagements, export generates multiple AP files, one per engagement.

## What gets exported

OSCAL Assessment Plan export generates files containing engagement and testing data. The export includes:

-   Engagement metadata \(name, status, objectives, progress percentage, timeline, budget\)
-   Parties and roles \(users involved with their role assignments\)
-   Activities representing control tests \(test descriptions, methods, status, operational assessment procedures\)
-   Assessment procedures as steps within activities
-   Reviewed controls \(which controls and requirements are in scope for testing\)
-   Reference to parent System Security Plan \(SSP\)

Custom properties are used for CAM-specific fields not natively supported by OSCAL standards. These properties use the ServiceNow namespace.

## What gets imported

OSCAL Assessment Plan import automatically creates engagements and their associated testing structures in CAM. For each AP file, the system generates:

-   One engagement with metadata \(users, roles, timeline, budget\)
-   Control tests mapped from AP activities
-   Test plans and assessment procedures mapped from AP tasks
-   User assignments with roles \(engagement lead, approvers, auditors, control test owners\)
-   Control and control objective selections specifying what will be tested

The import process creates the complete package structure if it does not exist in the target instance: boundary, package, system elements, baseline controls, and engagements. For existing packages, imported objects appear in the override list by default, allowing you to skip or overwrite existing data.

## File structure and validation in AP import process

AP import requires mandatory files: Catalog, Profile, and SSP. You can attach one or more AP files depending on the number of engagements. The system validates uploaded files against OSCAL standards during the attachment step. If validation errors occur, the system displays error messages before proceeding.

The AP file must reference the SSP UUID included in your import. If the AP references a different SSP UUID, validation fails with an error message. This ensures the assessment plan links correctly to the package being imported.

## User and role mapping for OSCAL import

During import, the system maps users from the OSCAL file to ServiceNow users. When usernames match, the system auto-maps them. When usernames do not match or the user does not exist in ServiceNow, you must manually select the corresponding ServiceNow user. The user mapping step ensures all required roles are assigned \(System Owner, ISSO, ISSM, Engagement Lead, Auditors\). If mandatory roles are missing after auto-mapping, you must manually assign users before proceeding.

## User and role mapping for OSCAL export

CAM exports engagement data to OSCAL Assessment Plan format using the following structure:

-   Engagement metadata: Name, state, objectives, progress percentage, timeline dates \(audit period, fieldwork dates, engagement duration\), and budget amounts export to the metadata section
-   Users and roles: User information \(full names, unique identifiers\) exports to the parties section; roles \(engagement lead, approvers, auditors, control test owner\) and assignments export to the roles and responsible-parties sections
-   Control tests: Map to activities in the local-definitions section, including test title, description, current state, and operational assessment procedures
-   Assessment procedures: Map to steps within activities, containing step identifiers, descriptions, and labels for control requirements
-   Reviewed controls: Identifies which controls and requirements are in scope for testing
-   SSP reference: Links the assessment plan to its parent package using the package UUID in the import-ssp section

**Parent Topic:**[CAM OSCAL](../../grc-cam-workspace/concept/oscal-cam-ws.md)

