---
title: Activate SBOM support
description: Install the required applications and verify prerequisites to enable SBOM collection in Third-party Risk Management \(TPRM\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/third-party-risk-management/sbom-activate.html
release: australia
product: Third-party Risk Management
classification: third-party-risk-management
topic_type: task
last_updated: "2026-05-12"
reading_time_minutes: 2
keywords: [SBOM, Software Bill of Materials, activation, Third-Party Risk Management, TPRM, Smart Assessment Engine]
breadcrumb: [Smart Assessment Engine assessments, Configure, Third-party Risk Management, Governance, Risk, and Compliance]
---

# Activate SBOM support

Install the required applications and verify prerequisites to enable SBOM collection in Third-party Risk Management \(TPRM\).

## Before you begin

-   Verify that the Smart Assessment Engine is enabled. SBOM collection is not supported for Classic assessments.
-   Check your entitlements to determine whether you have access to this application and all associated ServiceNow Store applications. For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030186).

Role required: admin

## About this task

An SBOM \(Software Bill of Materials\) is a structured inventory of the software components in a product. In TPRM, SBOM collection is performed through engagement-level external assessments using the Smart Assessment Engine. Installing the core SBOM applications makes the required data structures and processing capabilities available in your instance. Installing the optional vulnerability response applications adds vulnerability context for individual SBOM components.

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Install the required SBOM applications.

    Find each application using the filter criteria and search bar, then select **Install** for each one.

    |Application|ID|
    |-----------|---|
    |SBOM Core|`sn_sbom_core`|
    |Data Model for SBOM|`sn_sbom_dm`|

    Core SBOM data structures and processing capabilities are available in the instance.

3.  Install the optional vulnerability response applications if you require vulnerability insights for SBOM components.

    Find each application using the filter criteria and search bar, then select **Install** for each one.

    |Application|ID|
    |-----------|---|
    |SBOM Response|`sn_sbom_resp`|
    |Vulnerability Response|`sn_vul`|

    **Note:** These applications enable vulnerability context for SBOM components but are not required to collect SBOM files.

4.  Verify that SBOM fields and related lists are available on an engagement record.

    1.  Navigate to the Vendor Management Workspace using one of the following methods:

        -   Select **Workspaces** &gt; **Vendor Management Workspace**.
        -   Navigate to **All** &gt; **Third-party Risk Management** &gt; **Vendor Management Workspace**.
    2.  Open an engagement record.

    3.  Confirm that the **SBOM required** field is visible on the engagement record, and that the **SBOM document** related list appears on the engagement.

    The instance is ready to collect SBOM information through engagement-level external assessments.


## What to do next

After installing SBOM support, you can request an SBOM from a third party through an engagement-level external assessment. For next steps, see [Request a software bill of materials from an engagement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-sbom-collect.md).

**Related topics**  


[Exploring software bill of materials collection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-sbom-exploring.md)

[Collecting software bill of materials](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-sbom.md)

[Request a software bill of materials from an engagement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-sbom-collect.md)

[Review a software bill of materials submission from an engagement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/sbom-review.md)

[SBOM records and relationships in Third-party Risk Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-sbom-relationship.md)

