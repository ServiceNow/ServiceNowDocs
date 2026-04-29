---
title: ITOM Content Service use case
description: This ITOM Content Service use case demonstrates how organizations can achieve enhanced visibility into their environment.
locale: en-US
release: australia
product: ITOM Visibility
classification: itom-visibility
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [ITOM Content Service, ITOM Visibility, IT Operations Management]
---

# ITOM Content Service use case

This ITOM Content Service use case demonstrates how organizations can achieve enhanced visibility into their environment.

## Use case overview

The Application Configuration Items \(CIs\) class is a key component of an organization’s data platform within the Common Service Data Model \(CSDM\). Application CIs help log software activities and support critical IT operations.

Many products and applications rely on application CIs for essential tasks. A few key examples are:

-   Service Mapping: Uses application CIs to create service maps
-   ITOM AIOps: Monitors application health and resolves incidents using application CIs
-   IT Asset Management \(ITAM\): Tracks and manages software applications and their associated licenses with application CIs
-   IT Service Management \(ITSM\): Analyzes service impact and calculates blast radius with application CIs
-   Enterprise Architecture \(EA\): Leverages application CIs to generate business outcomes

## Challenge

A large organization with numerous applications requires accurate discovery. Managing application CIs is essential, yet the IT team finds it challenging to maintain visibility over its growing infrastructure.

ITOM Visibility offers several methods for discovering products within an organization’s infrastructure, such as Discovery and Service Mapping Patterns. This method provides detailed visibility into a product's information. When a wide range of applications is in use, not all can have a dedicated pattern. If an application does not have a dedicated pattern, discovery populates only the Running Process \[cmdb\_running\_process\] table without identifying the product or creating a CI for it.

Without an application CI, the organization lacks accurate visibility into its infrastructure and might struggle to optimize the following essential actions:

-   Bind CIs with monitoring alerts and open incidents regarding the CIs
-   Schedule automated software upgrades
-   Automate scripts to optimize or troubleshoot the product
-   Perform impact assessments and change impact analysis
-   Create security workflows

## Solution

ITOM Content Service enhances the discovery process by tagging and classifying process fingerprints. This service provides details about the publisher, product, and the essential component of the CI. Unlike pattern-based discovery, ITOM Content Service identifies applications directly within the organization’s environment without requiring published pattern classifiers. This approach enables the continuous delivery of content without being constrained by a scheduled release cycle.

For example: Discovery identifies the Elipse Software E3 Database Engine process \(E3DBEngine.exe\) and lists it in the Running Process \[cmdb\_running\_process\] table. If the E3DBEngine.exe process classification condition isn’t set to trigger a pattern, it doesn't launch a pattern and a CI isn't created. However, with ITOM Content Service, the E3DBEngine.exe process is tagged and classified, enabling Discovery to turn the process into a CI during the next scan.

## Result

Discovery using ITOM Content Service creates a CI record by tagging and classifying the publisher, product, and essential component for all applications in the organization’s environment. This method provides enhanced and continuous visibility into the application landscape, enabling effective monitoring, proactive actions, and ongoing optimization.

