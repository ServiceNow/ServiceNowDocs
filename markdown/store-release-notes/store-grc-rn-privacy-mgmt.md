---
title: GRC: Privacy Management release notes
description: Version history for the GRC: Privacy Management application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-grc-rn-privacy-mgmt.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 6
breadcrumb: [ServiceNow Store - Governance, Risk, and Compliance release notes, ServiceNow Store release notes]
---

# GRC: Privacy Management release notes

Version history for the GRC: Privacy Management application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 22.3.2 - June 2026 \(Australia\)**
    -   New:
        -   Configure the Personal Data Rights \(PDR\) external-facing form to map jurisdictions to data subject types and request types, and control whether an authorized agent can submit a request on behalf of a data subject.
        -   Enable key stakeholders to view and update processing activities that they own directly from GRC tasks in the Employee Center.
        -   Activate ready-to-use privacy content for three new authority documents, Digital Personal Data Protection Act 2023 \(DPDPA\), the Virginia Consumer Data Protection Act, and the Colorado Privacy Act, and adopt an updated privacy risk statement version that adds new risk statements.
        -   Manage Smart Assessment templates with versioning support. Create, publish, and delete template versions to support consistent assessment governance.
    -   Changed:
        -   Query range ACL's:
            -   Consistent access control: All tables include standardized query range security ACLs. These ACLs ensure that authenticated users with appropriate read permissions can query records consistently across the platform.
            -   Seamless upgrade experience: New query ACL rules are installed automatically during upgrade, with no administrator action required. Automated upgrade scripts handle the transition, including detecting and processing previously customized ACLs to ensure existing processes continue without interruption.
            -   Post-upgrade review for customized ACLs: If the instance includes administrator-modified query range ACLs, review those records after upgrade to confirm they align with the intended access policy.
        -   Enabled Audit entries support for privacy and related records.
-   **Version 22.0.2 - March 2026**
    -   New:
        -   Improved hierarchy and data lineage user experience
        -   Control objective workflow impacts implementation.
    -   Fixed: Fixed issues related to EBA and security
-   **Version 21.1.4 - December 2025 \(Zurich\)**
    -   New:
        -   Entity-based access control
            -   This feature facilitates object access through entities.
            -   Maps entities to specific users or user groups, enabling granular access control.
            -   Administrators can grant access to an entity’s related records by adding users, user groups, entity user fields, or entity user group fields, which minimizes the risk of unnecessary data exposure.
            -   Configure any user or user group field on a record to provide additional access beyond what is defined in the EBA configuration.
    -   Changed:
        -   Introduced an 'Active flag' in the GRC Choice table. Any updates to these flags are now reflected in the privacy management application.
        -   Implemented the impact of citation to control mapping feature across the dashboard and overview pages.
    -   Fixed:
        -   Resolved a security vulnerability that allowed unintended edits to read-only fields.
        -   Replaced hard-coded admin role dependencies with granular roles. This improves security and aligns with least privilege principles.
-   **Version 21.0.1 - August 2025**
    -   New:
        -   Oversee all aspects of privacy management comprehensively through a uniﬁed view using an improved dashboard.
        -   See the processing activity in a vertical layout for improved readability and easier grouping and analysis of related records.
        -   Classify data subjects to select and deﬁne multiple data subject types, providing a granular representation of processing activity.
        -   New Screening and Privacy Impact assessment templates with improved questionnaire.
    -   Fixed: Fixed issues related to access permissions.
-   **Version 20.2.1 - July 2025**

    Fixed: Enhanced security by creating Query range ACLs across multiple tables.

-   **Version 20.2.0 - June 2025**

    Fixed: Enhanced security by creating Query range ACLs across multiple tables.

-   **Version 20.1.1 - May 2025**

    Changed: Implemented accessibility, security and coral theming as part of the platform "big rock" initiative.

-   **Version 20.0.1 - February 2025**
    -   New:
        -   Integrate criticality factors into assessments and processing activities thereby simplifying the assessment process, and reducing the workload for privacy teams.
        -   Use the Smart Assessment Engine to capture details regarding information objects and hierarchies, updating all details within the assessments and eliminating the need to separately update processing activities.
        -   Implement information Object \(IO\) categories such as biometric data, to align with regulatory classifications and bridge the gap between requirements and user understanding.
    -   Changed: Empower privacy case analysts to perform assessments on privacy cases using the Smart Assessment Engine.
-   **Version 19.1.2 - November 2024**
    -   Fixed:
        -   Improved workspace experience for users with low vision or those who rely on assistive technology, such as screen readers. This includes optimising zoom capabilities.
        -   Security fixes.
        -   Fixed privacy lite operator &amp; risk assessment issues.
-   **Version 19.0.1 - August 2024**
    -   New:
        -   Establish a data lineage to understand how data is being consumed and shared in a given processing activity. Creating a data lineage also helps you to understand and manage the associated risks for the data being shared. This feature provides a visual representation of data lineage.
        -   Create regulatory agencies in the Privacy Workspace to identify the relevant regulatory authorities that are responsible for overseeing the businesses in the public interest. The centralised library consolidates all regulatory communications via emails.
        -   Collaborate and chat with cross-functional teams for processing activities, privacy cases, privacy assessments and personal data rights requests.
        -   View smart attestations on processing activities.
-   **Version 18.1.3 - June 2024**
    -   Changed:
        -   Implemented Form controller changes to align with platform recommendation for improved record page performance.
        -   Updated the screen and scripted conditions, UX add-on event mappings of declarative actions with Form controller.
    -   Fixed:
        -   When navigating to different list forms from privacy workspace, URLs should be changing depending on the list selected.
        -   Demo data is corrected on privacy home page
-   **Version 18.0.1 - February 2024**
    -   New: Introduced new, functional-domain configurations
    -   Changed: Updated existing features to support the functional domain
-   **Version 17.0.2 - August 2023**

    Changed: Ability to send assessment tasks to collect information from business users.

-   **Version 16.0.2 - February 2023**
    -   New:
        -   Ability to associate multiple processing activities to the same issue and vice versa.
        -   Ability to associate common controls to processing activity.
    -   Changed:
        -   Support for Localization
        -   Support for WCAG 2.1 standards
    -   Fixed:
        -   Access controls for viewing reports
        -   Privacy assessments are not getting deleted when Processing activity is deleted
-   **Version 15.0.3 - December 2022**

    Fixed: Reduction in installation size of the application.

-   **Version 15.0.2 - August 2022**
    -   Changed:
        -   Script based assessment response mapping to Processing Activity fields.
        -   New templates for Privacy Initial and Screening Assessments.
    -   Fixed:
        -   Users with Privacy role are not able to access Business Applications.
        -   Privacy Home Page : Compliance posture by month widget shows incorrect percentage.
        -   Aggregated Risks Score on Details section is not visible when only one RAM is published state
-   **Version 14.2.0 - May 2022**
    -   Fixed:
        -   Duplicate Risk data in demo data.
        -   On the Privacy Manager Home page, filters that were not applied correctly were rectified.
        -   Updated the title on Processing Activity Overview from Activity Risk Score to Criticality Score.
        -   Updated the font color for ongoing risk assessments report on the overview page.
        -   Updated list columns on Critical risks with no controls drill down page.
        -   Updated title of report on Homepage from "Compliance posture by status" to "Compliance posture by month"
-   **Version 14.1.3 - March 2022**
    -   New:
        -   Proactively request PIA for new implementations, applications, processes from the employee center. This feature enables and supports privacy-by-design concepts.
        -   Send multiple types of PIAs to various key stakeholders of a single processing activity​.
        -   Automatically map controls, risks and information objects such as email, phone, SSN and so on based on the PIA responses.
        -   Enable the Business user role to update processing activity details.
        -   Assess the privacy risk posture based on privacy risk assessments and reports by using advanced risk assessments with manual and automated factors.
        -   Obtain control and risk suggestions based on the mapped personal information with processing activities.
        -   View reports and 360-view of information object to highlight the related processing activities, applied regulations, policies, and risks on each personal data record.
        -   Monitor and track privacy regulatory changes by integrating with Regulatory Change Management. This integration requires IRM Professional or IRM Enterprise license.
-   **Version 14.0.0 - February 2022**

    Changed: Updated for San Diego platform compatibility

-   **Version 13.0.4 - September 2021**

    ServiceNow’s Privacy Management solution helps customers manage their enterprise-wide privacy program by staying on top of privacy risks and regulations. The solution also enables customers to unify and scale enterprise-wide data privacy governance on a single platform to embed privacy risk into the front-line to adopt the Privacy by design culture.


**Parent Topic:**[ServiceNow Store - Governance, Risk, and Compliance release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-grc.md)

