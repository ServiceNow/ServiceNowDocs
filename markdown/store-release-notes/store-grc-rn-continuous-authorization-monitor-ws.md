---
title: GRC: Continuous Authorization and Monitoring Workspace release notes
description: Version history for the GRC: Continuous Authorization and Monitoring Workspace application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-grc-rn-continuous-authorization-monitor-ws.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 4
breadcrumb: [ServiceNow Store - Governance, Risk, and Compliance release notes, ServiceNow Store release notes]
---

# GRC: Continuous Authorization and Monitoring Workspace release notes

Version history for the GRC: Continuous Authorization and Monitoring Workspace application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 22.3.3 - June 2026 \(Australia\)**
    -   New:
        -   This release introduces the following enhancements:
            -   Added support for importing and exporting the OSCAL Assessment Results \(AR\) model.
            -   Added package-level configuration to skip attestations for controls within a package.
            -   Implemented additional query range ACLs to enhance security.
            -   Added missing CAM-specific fields to OSCAL import and export.
    -   Fixed:
        -   This release resolves the following issues:
            -   Resolved multiple issues affecting OSCAL import and export.
            -   Pagination missing in the preview and override sections of OSCAL import.
            -   Vertical related list momentarily displaying a "No record available" message while loading.
            -   Category, Type, and Classification fields not enabled on the Control Objective related list.
-   **Version 22.0.1 - March 2026**
    -   New:
        -   Grid views for assessment procedures and control requirements
        -   Control and Control Test related lists display in grid views with hierarchical visualization of requirements and test steps.
        -   Import and export of Assessment Plan \(AP\) in OSCAL format.
        -   Export of Assessment Results \(AR\) in OSCAL format.
        -   Baseline updates \(such as adding controls, marking controls as Not Applicable, reclassifying controls, and modifying configurations\) can now be performed after the Select step in the RMF process without reverting existing controls to Draft.
        -   Ability to inherit controls from multiple Common Control Providers \(CCPs\) across different authorization packages.
    -   Fixed:
        -   Fixed security-related bugs.
        -   Resolved issues with OSCAL import functionality.
-   **Version 21.1.1 - December 2025 \(Zurich\)**
    -   New:
        -   CAM Workflow configurator is now introduced to enable administrators to configure multiple workflows based on various frameworks.
        -   CAM workspace homepage has been enhanced to support CORAL theme capabilities.
        -   Authorisation Package and Boundary layout has now been changed to vertical layout in the workspace experience.
        -   Import and Export of OSCAL POAM model is now supported from workspace.
        -   OSCAL import has been enhanced with user mapping capabilities.
    -   Changed:
        -   Hybrid controls are now displayed in the 360° View.
        -   Incident and Vulnerability-related lists for the package are now visible.
    -   Fixed:
        -   The POA&amp;M-related list is now consistently shown starting from the Implement step across both Classic and Workspace.
        -   OSCAL defect fixes.
        -   System Owner field now gets auto-populated for the Authorization boundary.
        -   Inherited control was incorrectly enabled for baseline controls marked as “Common.” This is now fixed—inheritance is disabled as expected.
        -   Fixed security defects.
-   **Version 21.0.1 - August 2025**
    -   New:
        -   CAM overlays new capability has been introduced to perform various operations like addition, subtraction, custom while applying a policy overlay to an Authorization package.
        -   Ageing of a package across different steps can now be tracked on CAM home page.
        -   An Authorization package can now be reauthorization by automated engagement creation as per the date configured in next authorization date field.
        -   Authorization documents new tab has the reporting capabilities supported in authorization package.
        -   System properties page is now introduced in workspace.
        -   OSCAL import user experience is now improved with the introduction of playbook experience.
        -   OSCAL import capabilities in preview and override stage have been improved with operations like skip and override.
        -   OSCAL import and export has been improved with support for multiple Catalog overlay files.
    -   Fixed:
        -   Controls related list in workspace now has reference field.
        -   Attestations in task page now has reference field.
-   **Version 20.1.1 - May 2025**
    -   Fixed:
        -   Fixed typography issues and color issues for CORAL theme across CAM workspace, namely CAM homepage, package, and boundary overview.
        -   Fixed accessibility issues related to label drop-down on POAM landing page.
        -   Fixed accessibility issues related to zoom issues on CAM's home page.
-   **Version 20.0.1 - February 2025**
    -   New:
        -   Export of Open Security Controls Assessment Language \(OSCAL\) Catalog.
        -   Import of OSCAL Catalog and System Security Plan \(SSP\).
        -   New Authority to Operate \(ATO\) artifacts SAP, ATO Letter, and Executive Summary shipped with default templates.
        -   Reporting capabilities now supported in word format.
        -   New module with properties to select the template format - HTML or Microsoft Word template.
    -   Changed:
        -   OSCAL export is now supported without zip plugin dependency.
        -   OSCAL export is now performed in two steps, generate OSCAL SSP followed by download OSCAL SSP.
    -   Removed: Step number is removed from stepper component of package overview page.
    -   Fixed: Minor bug fixes and security fixes.
-   **Version 19.1.1 - November 2024**
    -   Changed:
        -   Improved workspace experience for users with low vision or those who rely on assistive technology, such as screen readers. This includes optimizing zoom capabilities.
        -   Group attestations can be performed from task page.
    -   New: Executive reader and Reader roles can now access CAM workspace.
-   **Version 19.0.6 - August 2024**

    The ServiceNow Continuous Authorization and Monitoring \(CAM\) application empowers governmental agencies, contractors, and high-assurance organizations to streamline compliance with the NIST risk management framework, supporting standards such as the NIST RMF and ISO 31000. CAM drives digital transformation across the entire risk management lifecycle. This results in reduced manual effort, improved collaboration across teams, and seamless adaptation to specific processes. The application automates numerous tasks, including authorization boundary management, impact assessments, system categorization, control implementation, audits, plans of action, artifact management, attestations, continuous monitoring, and ongoing authorization. An intuitive persona-based workspace efficiently manages your RMF program. The workspace is unique to each role, such as Authorization official, Security Control Assessor, System Owner, System User, Information User, Information System Security Officer, Information System Security Manager, and CAM Admin.


