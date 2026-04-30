---
title: Import OSCAL SSP
description: From the OSCAL Import landing page, import SSP OSCAL data into the CAM Workspace. This action enables you to seamlessly integrate security control assessments and compliance data, streamlining the process of managing and assessing security controls within your organization.
locale: en-US
release: yokohama
product: GRC: Continuous Authorization and Monitoring Workspace
classification: grc-continuous-authorization-and-monitoring-workspace
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Importing in OSCAL format, CAM OSCAL, Continuous authorization and monitoring tasks in the CAM Workspace, Using CAM, Continuous Authorization and Monitoring, Governance, Risk, and Compliance]
---

# Import OSCAL SSP

From the OSCAL Import landing page, import SSP OSCAL data into the CAM Workspace. This action enables you to seamlessly integrate security control assessments and compliance data, streamlining the process of managing and assessing security controls within your organization.

## Before you begin

Role required: sn\_irm\_cont\_auth.info\_system\_sec\_manager, sn\_irm\_cont\_auth.info\_system\_sec\_officer, and sn\_irm\_cont\_auth.admin

**Note:**

-   The catalog file that you want to import must be in the JSON format and validated using the OSCAL-CLI tool for any validation error. For more information on the OSCAL-CLI tool, see [usnistgov/oscal-cli](https://github.com/usnistgov/oscal-cli) on GitHub.
-   When the import process is complete, recipients are notified through email.
-   User who should be mapped for CAM specific personas.

The OSCAL SSP import is a synchronous process.

## Procedure

1.  Navigate to **Workspaces** &gt; **CAM Workspace**.

2.  In the primary navigation, select the OSCAL import landing page icon \(![OSCAL import](../image/cam-oscal-import-icon.png)\).

3.  Select **SSP** from the **OSCAL Model** drop-down list.

4.  Enter the **Source** name.

5.  Enter the **Import status recipients** name.

    You can list the users you want to be notified once the OSCAL import is complete. The recipient receives an email notification on the import status.

6.  Under the **User Information** section, select the users to map them from the current system to the required roles.

7.  In the **Attachments** section, attach the individual files.

    **Note:** Catalog, Profile, and SSP are required and must be attached.

    -   **Catalog**: Contains the details of the control objectives and its related objects.
    -   **Catalog Overlay**: Contains information regarding overlay policies and its control objectives.
    -   **SSP**: Contains the details of the authorization boundary, authorization package, system elements, information types, controls, common controls, inherit, hybrid controls, and others.
    -   **Data flow diagram**, **Boundary diagram**, and **Network diagram**: These diagrams are attached to the authorization boundary.
8.  Verify the files that you have uploaded by selecting **Import**.

    ![OSCAL SSP import.](../image/cam-oscal-import-ssp2.png)

9.  In the **SSP import** pop-up window, verify the details that are to be created or skipped and select **Import**.

10. Refresh the page.

    In the **Import status** section, you can view the import status report.

    All the records displayed in the **SSP import** pop-up window are created.


**Parent Topic:**[Importing in OSCAL format](../concept/import-oscal.md)

