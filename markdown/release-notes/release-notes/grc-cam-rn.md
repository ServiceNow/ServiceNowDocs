---
title: Continuous Authorization and Monitoring release notes
description: The ServiceNow Continuous Authorization and Monitoring \(CAM\) application provides a standardized approach to defining an authorization package and walking through the seven stages of the NIST Risk Management Framework \(NIST RMF\). Continuous Authorization and Monitoring \(CAM\) was enhanced and updated in the Xanadu release.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 4
---

# Continuous Authorization and Monitoring release notes

The ServiceNow® Continuous Authorization and Monitoring \(CAM\) application provides a standardized approach to defining an authorization package and walking through the seven stages of the NIST Risk Management Framework \(NIST RMF\). Continuous Authorization and Monitoring \(CAM\) was enhanced and updated in the Xanadu release.

## Continuous Authorization and Monitoring highlights for the Xanadu release

-   Use the added features in the CAM Workspace to help streamline your work and have an efficient end-to-end user experience.
-   Export System Security Plan \(SSP\) files in the OSCAL format, which includes models like Catalog, Profile, and SSP.
-   Use the lite roles introduced in CAM for lighter business operations.
-   Group similar controls into a family-related and club-related to help identify and understand the controls.

See [Continuous Authorization and Monitoring](https://www.servicenow.com/docs/access?context=grc-cam-landing-page&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US) for more information.

**Important:** Continuous Authorization and Monitoring is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Xanadu release

-   **[CAM Workspace](https://www.servicenow.com/docs/access?context=cam-ws-home-page&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US)**

    Use the CAM Workspace for an end-to-end user experience. The Home page, overview pages of authorization boundary and authorization package, unified tasks page, and the dashboards help you capture information and give you a better insight into the data that aids in decision making.

    CAM Workspace includes exclusive features with which you can:

    -   Add related control objectives.
    -   View controls by family for a control objective and report based on families for NIST 800-53.
    -   Add attachments to assessment procedures and document notes.
    -   View all Plan of Actions and Milestones \(POA&amp;M\) in a single pane.
-   **[CAM supports the OSCAL format to export control-related information](https://www.servicenow.com/docs/access?context=oscal-support-cam&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US)**

    Export SSP files in the OSCAL format based on various models such as SSP, Profile, Catalog, and Catalog overlay. The generated report is compatible to share the information with other systems. CAM supports the National Institute of Standards and Technology \(NIST\) recommended OSCAL format to provide control-based information in machine-readable formats.

-   **[CAM ATO artifacts](https://www.servicenow.com/docs/access?context=generate-ato-artifacts-cam-ws&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US)**

    Generate ATO artifacts from an authorization package in Microsoft Word format for the following reports:

    -   SSP
    -   Security Assessment Report \(SAR\)
    -   POA&amp;M
-   **[Enhancements in CAM user roles](https://www.servicenow.com/docs/access?context=assign-cam-roles&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US)**

    The existing user roles in CAM application have been enhanced with the following privileges:

    -   Use the Information Owner \(sn\_irm\_cont\_auth.information\_owner\) role to view and update the information types of an authorization package.
    -   Use the Audit reader \(sn\_audit.reader\) lite role to view audit-related entities, such as engagements.
    -   Create and manage issues as a system user.

## Changed in this release

-   **[Role changes for Continuous Authorization and Monitoring Workspace users](https://www.servicenow.com/docs/access?context=cam-roles-list&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US)**

    Reader \(sn\_irm\_cont\_auth.reader\), Authorization Official \(sn\_irm\_cont\_auth.authorization\_official\), and Executive Reader \(sn\_irm\_cont\_auth.executive\_read\) can now access Continuous Authorization and Monitoring Workspace.

-   **[OSCAL Catalog model export](https://www.servicenow.com/docs/access?context=oscal-support-cam&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US)**

    In exporting the control-related information as part of the Catalog model, the child control objectives of a control objective are mapped to the Control field. Furthermore, related control objectives of the control objective are mapped to the Links field.

-   **[Enhancements in CAM Workspace](https://www.servicenow.com/docs/access?context=cam-ws-home-page&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US)**

    The following enhancements have been made in CAM Workspace:

    -   New pop-ups with additional capabilities are added to the hybrid controls creation.
    -   POA&amp;Ms include all authorization package issues.
    -   The **Family** field and **Family ID** field are added to the Control objective page.
    -   The **Notes** field and **Attachment** field are added to the Assessment procedure page.
    -   The **360° View** button is configured in all pages of CAM Workspace.
-   **[CAM user role changes](https://www.servicenow.com/docs/access?context=assign-cam-roles&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US)**

    Defining roles and assigning privileges and permissions for approvals is critical to ensure security in the CAM application. The user role changes are:

    -   The Information Owner \(sn\_irm\_cont\_auth.information\_owner\) role can also update information types of an authorization package, and the role also contains the Audit user \(sn\_audit.user\) role in addition to the Reader \(sn\_irm\_cont\_auth.reader\) role.
    -   The Information System Security Manager \(sn\_irm\_cont\_auth.info\_system\_sec\_manager\) role can update the authorization package, and the role contains the Compliance user \(sn\_compliance.user\) and Reader \(sn\_irm\_cont\_auth.reader\) roles.
    -   The Information System Security Officer \(sn\_irm\_cont\_auth.info\_system\_sec\_officer\) role can update the authorization package.
    -   The Reader \(sn\_irm\_cont\_auth.reader\) role contains the Audit reader \(sn\_audit.reader\) role.
    -   The System User \(sn\_irm\_cont\_auth.system\_user\) role contains the Audit user \(sn\_audit.user\) role.
    -   The System Owner \(sn\_irm\_cont\_auth.system\_owner\) role also contains the Audit user \(sn\_audit.user\) and Compliance user \(sn\_compliance.user\) roles.

## Removed in this release

-   The Authorization Official \(AO\) \(sn\_irm\_cont\_auth.authorization\_official\) role no longer contains the sn\_audit.user and sn\_compliance.user roles. The AO role can only read and approve an authorization package.
-   The Information System Security Officer \(sn\_irm\_cont\_auth.info\_system\_sec\_officer\) role no longer contains the sn\_audit.user role.
-   The Reader \(sn\_irm\_cont\_auth.reader\) role no longer contains the sn\_audit.user role.

## Activation information

Install Continuous Authorization and Monitoring by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

**Parent Topic:**[Governance, Risk, and Compliance release notes](grc-rn-landing.md)

