---
title: Verify the NIST RMF Use Case Accelerator
description: After installing the GRC: NIST RMF Use Case Accelerator, review the NIST RMF application structure, core content, and demo data, if selected during installation.
locale: en-US
release: zurich
product: GRC Common Functions
classification: grc-common-functions
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [\(Deprecated\) NIST RMF Use Case Accelerator, GRC use case accelerators, Common GRC features, Governance, Risk, and Compliance]
---

# Verify the NIST RMF Use Case Accelerator

After installing the GRC: NIST RMF Use Case Accelerator, review the NIST RMF application structure, core content, and demo data, if selected during installation.

## Before you begin

**Note:** Starting with version 10.1.0, the NIST RMF Use Case Accelerator will be supported only for customers who currently use the product. New and existing customers should consider using the GRC: Continuous Authorization Monitoring application. For details, [Continuous Authorization and Monitoring](../../grc-cam/reference/grc-cam-landing-page.md).

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **User Administration** &gt; **Roles** and review the roles installed with the NIST RMF application.

    These roles contain nist\_rmf in their names; for example, sn\_irm\_nist\_rmf.security\_officer. The roles are associated with NIST RMF application modules to provide access based on the user's role.

    **Note:** Use the basic NIST RMF user role is to access the application. This role contains the reader or user roles from the ServiceNow® GRC suite of applications.

2.  In the Application Navigator, type **NIST RMF**, and verify the application core content.

    |Navigate to|Verify|
    |-----------|------|
    |**NIST RMF** &gt; **Content** &gt; **Control Objective**|Review the Policies and Control objectives installed for NIST RMF.|
    |**NIST RMF** &gt; **Content** &gt; **Risk Statements**|Review the Risk Frameworks and Risk Statements installed for NIST RMF.|
    |**NIST RMF** &gt; **Content** &gt; **Test Templates**|Review the Test Templates installed for NIST RMF.|
    |**NIST RMF** &gt; **Content** &gt; **Indicator Templates**|Review the Indicator Templates installed for NIST RMF.|
    |**NIST RMF** &gt; **Content** &gt; **Attestation Types**|Review the Control Attestation Types installed for NIST RMF.|
    |**NIST RMF** &gt; **Content** &gt; **Assessment Types**|Review the Risk Assessment Types installed for NIST RMF.|

3.  Validate the application demo content, if loaded.

    |Navigate to|Verify|
    |-----------|------|
    |**NIST RMF** &gt; **Impact Analysis**|Review the sample Targets installed in the system for use with the NIST RMF application.|
    |**User Administration** &gt; **Users**|Review the sample Persona users installed in the system for use with the NIST RMF application. The User IDs for these users end with .RMF and their names contain RMF.|
    |**Policy and Compliance** &gt; **Scoping** &gt; **Profile Classes**|Perform a search for profile classes with the **Name** field containing **with NIST**. Review their relationships by reviewing their roll up to field in respective profile classes.|
    |**Policy and Compliance** &gt; **Scoping** &gt; **Profile types**|Perform a search for profile types with the **Name** field starting with **NIST RMF**.|
    |**Policy and Compliance** &gt; **Policies and Procedures** &gt; **All Controls**|Perform a search for all controls referencing **Control Objectives** with a **Source = NIST 800-53-r4**.|
    |**Risk** &gt; **Risk Register** &gt; **All Risks**|Perform a search for all risks referencing **Risk Statements** with a **Source = NIST 800-53-r4**.|
    |**Audit** &gt; **Audit Testing** &gt; **Test Plans**|Perform a search for test plans with **Test Templates** that begin with **NIST RMF**.|
    |**Policy and Compliance** &gt; **Indicators** &gt; **Indicators**|Perform a search for all indicators where **Item.Content.Source = NIST 800-53-r4**.|
    |**Risk** &gt; **Indicators** &gt; **Indicators**|Perform a search for all indicators where **Item.Content.Source = NIST RMF**.|
    |**Policy and Compliance** &gt; **Issues** &gt; **All Issues**|Perform a search for all issues where**Item.Content.Source = NIST 800-53-r4**.|
    |**Risk** &gt; **Issues** &gt; **All Issues**|Perform a search for all issues where **Item.Content.Source = NIST 800-53-r4**.|
    |**Policy and Compliance** &gt; **Remediation Tasks** &gt; **All Open Remediation Tasks**|Perform a search for all Remediation tasks where an issue identified on the remediation task has**Item.Content.Source = NIST 800-53-r4**.|
    |**Risk** &gt; **Remediation Tasks** &gt; **All Open Remediation Tasks**|Perform a search for all Remediation tasks where an issue identified on the remediation task has **Item.Content.Source = NIST 800-53-r4**.|


**Parent Topic:**[\(Deprecated\) NIST RMF Use Case Accelerator](../concept/grc-and-nistrmf-usecase-accelerator.md)

