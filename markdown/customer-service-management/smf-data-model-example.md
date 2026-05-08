---
title: Industry-specific data model scenarios
description: The Service Model Foundation data model is vital for modeling the business organization structure. It can be configured and applied across different industry verticals. Each example demonstrates how internal and external business locations, service organizations, and customer relationships are structured to support real-world operational models.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-05-07"
reading_time_minutes: 9
breadcrumb: [Data model, Overview, Configure Service Model Foundation, Data models, Set up your environment, Configure, Customer Service Management]
---

# Industry-specific data model scenarios

The Service Model Foundation data model is vital for modeling the business organization structure. It can be configured and applied across different industry verticals. Each example demonstrates how internal and external business locations, service organizations, and customer relationships are structured to support real-world operational models.

## Exploring Service Model Foundation across industries

The following examples showcase how organizations in various industries, such as Public Sector Digital Services, Financial Services Operations, Healthcare and Life Sciences, Manufacturing Commercial Operations, and Retail Operations can configure service organizations and define relationships between internal users, external entities, and customers. These scenarios highlight the flexibility of SMF in modeling complex hierarchies, managing service delivery, and aligning roles with real-world use cases.

## Use case: Managing customers and accounts across branch locations in Financial Services Operations

**Overview**: This use case demonstrates how multinational financial institutions operate through a network of business locations including corporate headquarters \(HQs\), regional HQs, company branches, and independent advisor locations.

Each location serves a specific purpose and employs staff such as managers, employees, and advisors who manage customers or accounts.

To maintain data accuracy, visibility, and access control, the organization uses Service Model Foundation to model its hierarchy, define roles, and manage relationships between employees, customers, and locations.

**Problem Scenario**: FinServe Ltd, a leading financial services organization, faced recurring issues with access inconsistencies and customer ownership conflicts across its network of internal and external branches.

Challenges observed:

-   Duplicate ownership of accounts: Multiple employees from different branches could view or modify the same customer records.
-   Access violations: External advisors were unintentionally gaining visibility into internal business accounts.
-   Ambiguous customer relationships: No clear indication of which employee or branch was responsible for a given customer or account.
-   Complex maintenance overhead: Updating location hierarchies or reassigning employees caused broken relationships and permission mismatches.

These challenges led to data governance risks, reduced customer trust, and increased manual effort to resolve access disputes.

**Personas involved**:

-   Corporate HQ employees: Manage top-level operations and key business accounts.
-   Regional HQ managers – Supervise branch activities and oversee local business accounts.
-   Branch employees – Handle day-to-day customer transactions and business relationships.
-   Independent advisors \(external users\) – Manage consumer and household customers.
-   Customers – Represent either business entities or individual consumers.

**Prerequisites**:

-   The organization’s business hierarchy \(corporate HQ, regional HQs, branches, independent advisors\) is defined in SMF as business locations.
-   Internal and external users are assigned to their respective locations with appropriate personas \(for example, manager, employee, relationship manager\).
-   Customers and accounts are registered in the system and linked to a responsible employee.

![Hierarchical diagram of internal and external business locations showing role-based relationships and data access in a financial organization.](../image/smf-fso-usecase.png "Business location and access hierarchy in a financial institution")

**Resolution workflow/ Solution implementation**:

1.  Define the business location hierarchy
    -   The organization establishes a structured hierarchy of business locations:
        -   Corporate HQ: Parent company
        -   Regional HQs: Oversee multiple internal branches
        -   Company branches: Manage business customers
        -   Independent advisor locations: External entities managing consumer and household accounts
    -   Each location type is defined as either internal or external based on ownership and access level.
2.  Assign staff to locations
    -   Corporate HQ and branches are staffed by internal users.
    -   Independent advisor locations include external users operating under partnership agreements.
    -   Each staff member is mapped to their business location and assigned a role \(like, manager, employee, and advisor\).
3.  Establish customer and account relationships

    -   Customers \(business, consumer, or household\) are linked to specific employees.
    -   Each employee has a defined responsibility:
        -   A corporate HQ employee is an account manager for a business customer.
        -   Branch employee is an account manager for a regional business customer.
        -   An independent advisor is a relationship manager for a consumer or household.
    Each employee was linked to their respective customers or accounts. This mapping removed ownership conflicts and clarified accountability.

4.  Determine access control and data visibility

    SMF automatically applied access rules based on persona and business location.

    -   Access to records such as accounts or customer profiles is based on:
        -   The employee’s assigned business location.
        -   Their relationship role \(for example, account manager, relationship manager, and the likes\).
        -   The hierarchy defined in SMF.
    -   For example:
        -   Employee 2 at a corporate HQ can access Business Customer 1.
        -   Employee 2 at Branch 1 can access Business Customer 2.
        -   Advisor Employee 1 can view and manage Consumer 1.
5.  Manage location relationships

    -   Corporate HQ staff, such as Employee 2, may act as location relationship managers, maintaining oversight of external advisor locations.
    -   Similarity, HQ Employee 2 can review activity for advisor locations 1 and 2.
    This confirms that external partner activities align with company standards and compliance policies.


**Result**:

By applying the Service Model Foundation data model, FinServe Ltd resolved access inconsistencies and ownership conflicts across multiple business locations. The framework provided a unified, secure, and transparent approach to managing customer relationships in a large-scale financial environment.

## Use case: Managing patients, healthcare providers, and accounts in Healthcare and Life Sciences

**Overview**: This use case demonstrates how a multinational healthcare organization operates through a network of business locations, including corporate headquarters \(HQs\), regional clinical HQs, hospitals or clinics, and independent provider or research locations.

Each location serves a specific purpose and employs staff such as administrators, clinicians, and external partners who manage patient accounts, clinical studies, or healthcare services.

To maintain data accuracy, visibility, and access control, the organization uses Service Model Foundation to model its hierarchy, define roles, and manage relationships between employees, patients, and locations.

**Problem Scenario**: HealthCorp Ltd, a leading healthcare organization, faced recurring issues with access inconsistencies and patient/account management conflicts across its internal and external locations.

Challenges observed:

-   Duplicate patient records: Multiple employees from different locations could view or modify the same patient data.
-   Access violations: External research or provider partners were unintentionally gaining visibility into internal clinical records.
-   Ambiguous account ownership: No clear indication of which employee, clinician, or location was responsible for a given patient or clinical study.
-   Complex maintenance overhead: Updating location hierarchies or reassigning staff caused broken relationships and permission mismatches.

These challenges led to compliance risks, reduced patient trust, and increased manual effort to resolve access disputes.

**Personas involved**:

-   Corporate HQ administrators: Manage top-level operations, approvals, and key accounts.
-   Regional HQ managers: Supervise hospitals or clinical branches and oversee local patient or clinical accounts.
-   Hospital or clinic staff: Handle day-to-day patient care, appointments, and healthcare service delivery.
-   Independent providers or research partners \(external users\): Manage patient interactions, clinical studies, or research programs.
-   Patients or clinical participants: Represent either individual patients, households, or healthcare accounts.

**Prerequisites**:

-   The organization’s business hierarchy \(corporate HQ, regional HQs, hospitals or clinics, independent providers\) is defined in SMF as business locations.
-   Internal and external users are assigned to their respective locations with appropriate personas \(for example, administrator, clinician, researcher, relationship manager\).
-   Patients and healthcare accounts are registered in the system and linked to a responsible employee.

![Hierarchical diagram of internal and external business locations showing role-based relationships and data access in a healthcare organization.](../image/smf-hcls-usecase.png "Business location and access hierarchy in Healthcare and Life Sciences")

**Resolution workflow/ Solution implementation**:

1.  Define the business location hierarchy
    -   The organization establishes a structured hierarchy of business locations:
        -   Corporate HQ: Parent organization
        -   Regional HQs: Oversee multiple hospitals or clinics
        -   Hospitals or clinics: Manage patient and clinical accounts
        -   Independent provider or research locations: External entities managing patient or research accounts
    -   Each location type is defined as either internal or external based on ownership and access level.
2.  Assign staff to locations
    -   Corporate HQ and hospitals or clinics are staffed by internal users.
    -   Independent provider or research locations include external users operating under partnership agreements.
    -   Each staff member is mapped to their business location and assigned a role \(for example, administrator, clinician, researcher, relationship manager\).
3.  Establish patient and account relationships

    -   Patients or accounts \(individuals, households, clinical studies\) are linked to specific employees.
    -   Each employee has a defined responsibility:
        -   A corporate HQ employee is an account manager for a large healthcare account.
        -   A hospital clinician is responsible for patient accounts.
        -   An independent provider or researcher manages clinical or research participants.
    Each employee is linked to their respective patients or accounts, removing ownership conflicts and clarifying accountability.

4.  Determine access control and data visibility

    SMF automatically applies access rules based on persona and business location.

    -   Access to records such as patient data, clinical studies, or accounts are based on:
        -   The employee’s assigned business location.
        -   Their relationship role \(for example, clinician, researcher, account manager, and the likes\).
        -   The hierarchy defined in SMF.
    -   For example:
        -   Employee 2 at a corporate HQ can access Corporate Patient Account 1.
        -   Clinician Employee 1 at Clinic Branch 1 can access Clinic Patient Account 2.
        -   Research Partner Employee 1 can view and manage participants in a clinical study.
5.  Manage location relationships

    -   Corporate HQ staff may act as location relationship managers, maintaining oversight of independent provider or research locations.
    -   Similarity, HQ Employee 2 can review activity for multiple external research locations.
    This confirms that external partner activities align with company standards and compliance policies.


**Result**:

By applying the Service Model Foundation data model, HealthCorp Ltd resolved access inconsistencies and account ownership conflicts across multiple healthcare locations. The framework provided a unified, secure, and transparent approach to managing patient and clinical accounts in a large-scale HCLS environment.

## Use case: Managing citizen households, government services, and staff in Public Sector Digital Services

This use case demonstrates how a public sector organization manages the delivery of digital services such as child support and other welfare programs across multiple internal business locations including state HQs, regional centers, and local offices.

Each center has staff responsible for assigned citizen households, confirming accurate data, role-based access, and efficient service delivery through the Service Model Foundation data model.

**Problem Scenario**: The Department of Social Services \(DSS\) encountered challenges managing relationships and access controls across its network of centers and households.

Challenges observed:

-   Duplicate records across centers.
-   Unauthorized access to other centers’ cases.
-   Unclear ownership of households.
-   Maintenance issues when reassigning staff or locations.

These challenges led to data inconsistencies, compliance risks, and service inefficiencies.

**Personas involved**:

-   State HQ staff: Oversee statewide programs and compliance.
-   Center employees: Manage local household cases.
-   Relationship managers: Primary contacts for assigned households.
-   Citizens: Household members, including head of household and authorized representatives.

![Hierarchical diagram of internal and external business locations showing role-based relationships and data access in a public sector organization.](../image/smf-psds-usecase.png "Business location and access hierarchy in Healthcare and Life Sciences")

**Resolution workflow/ Solution implementation**:

1.  Define the business location hierarchy
    -   The organization establishes a structured hierarchy of business locations like, State HQ → Centers → Households.
    -   Each location defined as internal and tied to defined service delivery responsibilities.
2.  Assign staff to locations
    -   HQ employees \(HQE1 and HQE2\): Manage statewide accounts and monitor regional activity.
    -   Center staff \(C1E1, C1E2, and the likes\): Manage specific households and their services.
3.  Establish household and case relationships
    -   Households \(for example, Parker Household and Collins Household\) are linked to employees managing their cases.
    -   Each household includes members with defined roles such as head of household and authorized representatives.
    -   Employees act as relationship managers for their assigned households.
4.  Determine access control

    SMF automatically applies access rules based on location, role, and relationships.

    -   Center employees see only their assigned households.
    -   HQ employees maintain oversight without modifying local records.
    -   Authorized household members can represent others within their household.
5.  Manage inter-location relationships
    -   HQ staff can review household data across centers for compliance.
    -   Center staff collaborate when households span multiple service areas \(for example, shared members or foster care scenarios\).

**Result**:

By implementing the Service Model Foundation data model, DSS achieved:

-   Clear household ownership and accountability across centers.
-   Consistent access controls aligned with staff roles and business hierarchy.
-   Improved data accuracy and reduced record duplication.
-   Streamlined operations and compliance with data governance policies.

The framework enabled a unified, transparent, and secure management approach for Public Sector Digital Services delivery.

