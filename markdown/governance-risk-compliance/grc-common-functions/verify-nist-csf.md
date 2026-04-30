---
title: Verify the NIST CSF Use Case Accelerator
description: After installing the GRC: NIST Cybersecurity Framework \(CSF\) Use Case Accelerator, review the NIST CSF application structure, core content, and demo data, if selected during installation.
locale: en-US
release: zurich
product: GRC Common Functions
classification: grc-common-functions
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [NIST CSF Use Case Accelerator, GRC use case accelerators, Common GRC features, Governance, Risk, and Compliance]
---

# Verify the NIST CSF Use Case Accelerator

After installing the GRC: NIST Cybersecurity Framework \(CSF\) Use Case Accelerator, review the NIST CSF application structure, core content, and demo data, if selected during installation.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **User Administration** &gt; **Roles** and review the roles installed with the NIST CSF application.

    These roles contain nist\_csf in their names; for example, sn\_irm\_nist\_csf.security\_officer. The roles are associated with NIST CSF application modules to provide access based on the user's role.

    **Note:** The basic NIST CSF user role is needed to access the application. This role contains the reader or user roles from the ServiceNow® GRC suite of applications.

2.  In the Application Navigator, type **NIST CSF**, and verify the application core content.

<table id="table_csf_core_content"><thead><tr><th>

Navigate to

</th><th>

Verify

</th></tr></thead><tbody><tr><td>

**NIST CSF** &gt; **Content** &gt; **Authority Documents**

</td><td>

Review the Authority Documents installed for NIST CSF.

</td></tr><tr><td>

**NIST CSF** &gt; **Content** &gt; **Citations**

</td><td>

Review the Citations installed for NIST CSF.

</td></tr><tr><td>

**NIST CSF** &gt; **Content** &gt; **Control Objectives**

</td><td>

Review the Control objectives installed for NIST CSF.

</td></tr><tr><td>

**NIST CSF** &gt; **Content** &gt; **Risk Statements**

</td><td>

Review the Risk Frameworks and Risk Statements installed for NIST CSF.

</td></tr><tr><td>

**NIST CSF** &gt; **Content** &gt; **Test Templates**

</td><td>

Review the Test Templates installed for NIST CSF.

</td></tr><tr><td>

**NIST CSF** &gt; **Content** &gt; **Indicator Templates**

</td><td>

Review the Indicator Templates installed for NIST CSF.

</td></tr><tr><td>

**NIST CSF** &gt; **Content** &gt; **Attestation Types**

</td><td>

Review the Control Attestation Types installed for NIST CSF.

</td></tr><tr><td>

**NIST CSF** &gt; **Content** &gt; **Assessment Types**

</td><td>

Review the Risk Assessment Types installed for NIST CSF.

</td></tr></tbody>
</table>3.  Validate the application demo content, if loaded.

<table id="table_csf_demo_content"><thead><tr><th>

Navigate to

</th><th>

Verify

</th></tr></thead><tbody><tr><td>

**NIST CSF** &gt; **Orient Targets**

</td><td>

Review the sample Targets installed in the system for use with the NIST CSF application.

</td></tr><tr><td>

**User Administration** &gt; **Users**

</td><td>

Review the sample Persona users installed in the system for use with the NIST CSF application. The User IDs for these users end with .CSF and their name contains CSF.

</td></tr><tr><td>

**Policy and Compliance** &gt; **Scoping** &gt; **Profile Classes**

</td><td>

Perform a search for profile classes with the **Name** field containing **with NIST**. Review their relationships by reviewing their roll up to field in respective profile classes.

</td></tr><tr><td>

**Policy and Compliance** &gt; **Scoping** &gt; **entity types**

</td><td>

Perform a search for entity types with the **Name** field starting with **NIST CSF**.

</td></tr><tr><td>

**Policy and Compliance** &gt; **Policies and Procedures** &gt; **All Controls**

</td><td>

Perform a search for all controls referencing **Control Objectives** with a **Source = NIST CSF**.

</td></tr><tr><td>

**Risk** &gt; **Risk Register** &gt; **All Risks**

</td><td>

Perform a search for all risks referencing **Risk Statements** with a **Source = NIST CSF**.

</td></tr><tr><td>

**Audit** &gt; **Audit Testing** &gt; **Test Plans**

</td><td>

Perform a search for test plans with **Test Templates** that begin with **NIST CSF**.

</td></tr><tr><td>

**Policy and Compliance** &gt; **Indicators** &gt; **Indicators**

</td><td>

Perform a search for all indicators where **Item.Content.Source = NIST CSF**.

</td></tr><tr><td>

**Risk** &gt; **Indicators** &gt; **Indicators**

</td><td>

Perform a search for all indicators where **Item.Content.Source = NIST CSF**.

</td></tr><tr><td>

**Policy and Compliance** &gt; **Issues** &gt; **All Issues**

</td><td>

Perform a search for all issues where**Item.Content.Source = NIST CSF**.

</td></tr><tr><td>

**Risk** &gt; **Issues** &gt; **All Issues**

</td><td>

Perform a search for all issues where **Item.Content.Source = NIST CSF**.

</td></tr><tr><td>

**Policy and Compliance** &gt; **Remediation Tasks** &gt; **All Open Remediation Tasks**

</td><td>

Perform a search for all Remediation tasks where an issue identified on the remediation task has**Item.Content.Source = NIST CSF**.

</td></tr><tr><td>

**Risk** &gt; **Remediation Tasks** &gt; **All Open Remediation Tasks**

</td><td>

Perform a search for all Remediation tasks where an issue identified on the remediation task has **Item.Content.Source = NIST CSF**.

</td></tr></tbody>
</table>
**Parent Topic:**[NIST CSF Use Case Accelerator](../concept/grc-csf-usecase-accelerator.md)

