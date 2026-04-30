---
title: Perform preliminary risk assessment and impact analysis
description: Perform a preliminary risk assessment and impact analysis of the target.
locale: en-US
release: zurich
product: GRC Common Functions
classification: grc-common-functions
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Categorize targets, Process overview, \(Deprecated\) NIST RMF Use Case Accelerator, GRC use case accelerators, Common GRC features, Governance, Risk, and Compliance]
---

# Perform preliminary risk assessment and impact analysis

Perform a preliminary risk assessment and impact analysis of the target.

## Before you begin

**Note:** Starting with version 10.1.0, the NIST RMF Use Case Accelerator will be supported only for customers who currently use the product. New and existing customers should consider using the GRC: Continuous Authorization Monitoring application. For details, [Continuous Authorization and Monitoring](../../grc-cam/reference/grc-cam-landing-page.md).

Role required: sn\_irm\_nist\_rmf.risk\_executive or sn\_irm\_nist\_rmf.security\_officer

## Procedure

1.  Navigate to **All** &gt; **NIST RMF** &gt; **Categorize** &gt; **Impact Analysis**.

2.  Search for the target using the **Name** or **Profile** fields.

3.  Select and open the target record.

4.  Open the target record again and update the following fields in the NIST RMF section:

    **Note:** Review [NIST RMF supporting concepts](../reference/grc-nist-rmf-key-concepts.md), for more detailed information about these fields.

    |Field|Description|
    |-----|-----------|
    |Confidentiality|Target category based on confidentiality. Identify the security objective as: High, Moderate, or Low.|
    |Integrity|Target category based on integrity. Identify the security objective as: High, Moderate, or Low.|
    |Availability|Target category based on availability. Identify the security objective as: High, Moderate, or Low.|
    |Impact|Impact to business function if the target loses its confidentiality, integrity, or availability. Impact is automatically determined and may be overridden.|
    |Scoping Considerations|Operational or environmental scoping considerations for the target.|
    |Risk Executive|Names of the person who ensures risks are identified and managed.|
    |Authorizing Official|Name of the person who verifies that the target is operating with an acceptable level of risk.|
    |Justification|Security posture description for risk executive, authorizing official, and owner.|
    |Approval status|Status of the security compliance posture of the target.|

5.  Verify that the NIST RMF related lists are visible:

    -   Baseline Policy Statements
    -   Baseline Controls
    -   Risks
    -   Approvals
6.  Navigate to the **NIST RMF** tab and review the **Baseline Policy Statements**.

7.  Implement security controls for the target following the standard approach outlined in the Policy and Compliance Management application.


**Parent Topic:**[Categorize targets](../concept/rmf-categorize.md)

