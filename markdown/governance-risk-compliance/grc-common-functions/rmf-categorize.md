---
title: Categorize targets
description: Within the NIST RMF application, the Categorize section facilitates the categorization of targets through a preliminary risk assessment and an impact analysis.
locale: en-US
release: australia
product: GRC Common Functions
classification: grc-common-functions
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Process overview, NIST RMF Use Case Accelerator, GRC use case accelerators, Common GRC features, Governance, Risk, and Compliance]
---

# Categorize targets

Within the NIST RMF application, the **Categorize** section facilitates the categorization of targets through a preliminary risk assessment and an impact analysis.

**Note:** Starting with version 10.1.0, the NIST RMF Use Case Accelerator will be supported only for customers who currently use the product. New and existing customers should consider using the GRC: Continuous Authorization Monitoring application. For details, [Continuous Authorization and Monitoring](../../grc-cam/reference/grc-cam-landing-page.md).

First, a target is created from an entity or an entity type. The application flow begins at Impact Analysis. The user locates a target and sets it up for use with NIST RMF providing basic information. Next, the user performs a preliminary risk assessment determining the potential impact value on each of the following parameters: **Confidentiality**, **Integrity**, and **Availability**. The highest impact rating of these values determines the **Impact** value.

**Note:** The user can override the **Impact** value, as necessary.

The **Impact** value is used to identify the baseline security policy statements recommended for the target, based on the NIST 800-53.r4 special publications catalog. The user reviews the baseline security policy statements and implements security controls for that target \(for example, Profile\). The standard approach is outlined in the Policy and Compliance Management application.

-   **[Generate target from profile or entity type](../task/generate-target-from-profile.md)**  
Generate a target record for a profile to track NIST RMF attributes.
-   **[Set up a target for use with NIST RMF](../task/set-up-target-nist-rmf.md)**  
Set up a target and populate the basic information.
-   **[Perform preliminary risk assessment and impact analysis](../task/perform-risk-assess-impact-analysis.md)**  
Perform a preliminary risk assessment and impact analysis of the target.
-   **[Monitor the NIST RMF Categorize Overview](../task/monitor-rmf-categorize-dashboard.md)**  
The NIST RMF categorization activity dashboard provides insights into the overall status of the target.

**Parent Topic:**[NIST RMF process overview](nist-rmf-process.md)

