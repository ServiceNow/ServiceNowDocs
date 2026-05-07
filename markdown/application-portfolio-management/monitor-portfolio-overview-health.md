---
title: Portfolio overview and health
description: Get an overview of your profile and monitor your portfolio health.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Exploring Enterprise Architecture Workspace, Enterprise Architecture Workspace, Enterprise Architecture]
---

# Portfolio overview and health

Get an overview of your profile and monitor your portfolio health.

## Portfolio overview

The Portfolio Overview section displays the overview of your portfolio in the form of numbers on different cards. You can use the refresh button to fetch the latest results. Click the number to see the full list.

The following cards are displayed:

-   Business Applications
-   Business Capabilities
-   Information Objects
-   Business Applications with High Risk
-   Business Applications with Low Score: Number of business applications with low score for a quarterly fiscal period.
-   Business Applications with TRM technical debt: Number of business applications that aren’t aligned with the TRM phases and standards.
-   Business Applications by Install Type

Use the following filters to narrow down the results for Portfolio and Health sections:

-   Application Category
-   Install Type
-   Application Type
-   Business Unit
-   Business Owner
-   IT Application Owner
-   Capability Owner

## How portfolio data and filters are populated

The Portfolio Overview and Portfolio Health sections display metrics based on business application and capability records in Enterprise Architecture Workspace. Cards reflect the current state of these records and their relationships, such as owners, capabilities, and assessments.

Filter values are populated dynamically from existing application data. Owner‑based filters use the users referenced in application and capability records, and available values depend on how those records are configured.

## Portfolio health

The Portfolio health section displays the health of your portfolio. You can see the details such as the number and percentage of business applications on different cards. Click the number or percentage to see the full list. You can use the filters to narrow down the results.

The following cards are displayed:

-   Business Applications without Capabilities
-   Business Applications without Owners: Number and percentage of business applications for which there is no IT application owner and business owner assigned.
-   Business Applications not Assessed
-   Business Applications without Application Services: Number and percentage of business applications that are not related to any application service. Business application and application service are two different configuration items which must be related through a CI relationship.
-   Business Applications without Architectural Artifacts: Number and percentage of business applications that aren’t associated to any architectural artifact. The association of Architectural Artifacts with business applications create a relationship between the artifact and related entities.
-   Business Capabilities without Business Applications
-   Business Capabilities not Assessed

The following cards are displayed only when the Digital Integration Management plugin \(com.snc.apm\_di\) is installed:

-   Digital Interfaces without Digital Integrations
-   Business Applications without Digital Interfaces

**Note:** You can zoom on this page or any of the child pages to 200% or 400% through your browser settings without the loss of content or functionality. Page layouts are transformed into a vertical, stacked view automatically.

**Parent Topic:**[Exploring Enterprise Architecture Workspace](explore-eaw.md)

