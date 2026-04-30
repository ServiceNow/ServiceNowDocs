---
title: NIST RMF supporting concepts
description: Familiarize yourself with these concepts, developed from the NIST RMF guidance.
locale: en-US
release: yokohama
product: GRC Common Functions
classification: grc-common-functions
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [NIST RMF Use Case Accelerator, GRC use case accelerators, Common GRC features, Governance, Risk, and Compliance]
---

# NIST RMF supporting concepts

Familiarize yourself with these concepts, developed from the NIST RMF guidance.

**Note:** Starting with version 10.1.0, the NIST RMF Use Case Accelerator will be supported only for customers who currently use the product. New and existing customers should consider using the GRC: Continuous Authorization Monitoring application. For details, [Continuous Authorization and Monitoring](../../grc-cam/reference/grc-cam-landing-page.md).

<table id="table_ybb_jkv_3hb"><thead><tr><th>

Concept

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Target

</td><td>

The target is the foundation of the NIST RMF Use Case Accelerator and all related concepts.

 The target is a shared table between the ServiceNow® GRC products and several Use Case Accelerators. They are similar to the concept of profiles in the core GRC applications. They are optionally linked to profiles, but are used for any attributes that are specific to the Use Case Accelerators.

**Note:** Each NIST RMF Target uniquely represents a single profile throughout its RMF life-cycle.

</td></tr><tr><td>

Confidentiality \(C\)

</td><td>

Confidentiality is a security objective of a Target, and is defined as the act of preserving authorized restrictions on information access and disclosure, including means for protecting personal privacy and proprietary information. Confidentiality is expressed as High, Moderate, and Low values

</td></tr><tr><td>

Integrity \(I\)

</td><td>

Integrity is a security objective of a Target is defined as act of guarding against improper information modification or destruction, and includes ensuring information non-repudiation and authenticity. Integrity is expressed as High, Moderate, and Low values

</td></tr><tr><td>

Availability \(A\)

</td><td>

Availability is a security objective of a Target is defined as act of ensuring timely and reliable access to and use of information. Availability is expressed as High, Moderate, and Low values

</td></tr><tr><td>

Baseline controls

</td><td>

Baseline Controls are recommended set of security controls from National Institute of Standards and Technology \(NIST\) which when implemented and determined to be effective, would mitigate security risk while complying with security requirements. Baseline controls have a designated impact value which is a combination of High, Moderate, or Low values.

</td></tr><tr><td>

Impact analysis

</td><td>

Impact analysis determines the extent to which proposed or actual changes to the Target or its environment of operation can affect or have affected the security state of the Target. A Target in which all three CIA security objectives evaluate to Low is considered Low-impact and uses any of the security controls which are tagged as Low impact value. Likewise, a Target in which any of the three CIA security objectives evaluate to Moderate is considered Moderate-impact and uses any of the security controls which are tagged as Moderate impact value. Likewise, a Target in which any of the three CIA security objectives evaluate to High is considered High-impact and uses any of the security controls which are tagged as High impact value.

</td></tr><tr><td>

Assurance

</td><td>

Assurance controls increase both the strength of security and degree of confidence that the functionality of Targets is correct, complete, and consistent and would mitigate the security risk and assists in complying with security requirements

</td></tr><tr><td>

Common

</td><td>

Common controls are controls that are inheritable by one or more Targets

</td></tr><tr><td>

Compensating

</td><td>

Compensating controls are controls which can be employed in lieu of recommended baseline security controls and provide equivalent or comparable protection for the Targets

</td></tr><tr><td>

Supplemental

</td><td>

Supplemental controls are controls which can be employed as added security controls to adequately meet the risk management needs of a Target

</td></tr><tr><td>

Tailoring

</td><td>

Tailoring is a process by which a security control baseline is modified based on: \(i\) Targets scoping guidance; \(ii\) specification of the security controls, for example, compensating, if needed; and \(iii\) the specification of organization — defined parameters in the security controls via explicit assignment and selection statements

</td></tr></tbody>
</table>**Parent Topic:**[NIST RMF Use Case Accelerator](../concept/grc-and-nistrmf-usecase-accelerator.md)

