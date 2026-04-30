---
title: Create a VRM third party record
description: Set up the key data and contact information for a third party that your organization will engage.
locale: en-US
release: xanadu
product: Third-party Risk Management
classification: third-party-risk-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Work in the VRM classic UI, Third-party Risk Management, Governance, Risk, and Compliance]
---

# Create a VRM third party record

Set up the key data and contact information for a third party that your organization will engage.

## Before you begin

Contact your system administrator before you update the portfolio of third parties.

Role required: sn\_vdr\_risk\_asmt.vendor\_risk\_manager or sn\_vdr\_risk\_asmt.vendor\_risk\_admin

## About this task

In addition to adding new records, TPR managers make ongoing updates to third-party information, including risk security scores, risk tiers, critical third-party contacts, and the business services that the third parties fulfill.

You can import third-party data from a spreadsheet, integrate the data from an onboarding system, or import data from the vendor table.

## Procedure

1.  Use either of the following methods to start the process:

    -   In the Vendor Management Workspace, select the list icon ![](../../grc-workspace-vrm/image/ws-list-icon.png) and then navigate to **Third parties** &gt; **All Third parties**.
    -   Navigate to **All** &gt; **Third-party Risk Management** &gt; **All Third parties**.
2.  Select **New** and then fill in the fields.

<table id="table_epy_qrq_f5"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Third party name.

</td></tr><tr><td>

Website

</td><td>

URL for the third party.

</td></tr><tr><td>

DUNS number

</td><td>

Unique numeric identifier for the single business entity. A DUNS number is not legally required for a business.

</td></tr><tr><td>

Industry

</td><td>

Type of industry.

</td></tr><tr><td>

Vendor type

</td><td>

Specify the type of product or service that the third party will provide.

</td></tr><tr><td>

Parent

</td><td>

If you set up third-party hierarchies, and this third party is a subsidiary, select the parent third party.

</td></tr><tr><td>

Total annual spend

</td><td>

Expected amount that you expect to spend annually on this third party.

</td></tr><tr><td>

Security Score

</td><td>

The security score provided by a risk intelligence provider.

</td></tr><tr><td>

Score provider

</td><td>

The risk intelligence provider that provided the normalized security score.

</td></tr><tr><td>

Status

</td><td>

Status of the third party.

</td></tr><tr><td>

Contract start date

</td><td>

Date that the contracted engagement should start.

</td></tr><tr><td>

Risk rating

</td><td>

After third-party risk assessment responses have been received, this weighted average of the components \(that is, the risk ratings of assessments, engagements, and subsidiaries\) is calculated. For more information, see [Setting up VRM third-party hierarchies and engagements](../concept/vendor-hierarchy-engagements.md).

</td></tr><tr><td>

Rank tier

</td><td>

Type of supplier.

</td></tr><tr><td>

Third-party tier

</td><td>

Risk tier for the third party calculated by mapping the tiering score to a risk tier.

</td></tr><tr><td>

Vendor manager

</td><td>

The employee assigned as the manager to this third party.

</td></tr><tr><td>

Business owner

</td><td>

The employees that use this third party in their daily business.

</td></tr><tr><td>

Notes

</td><td>

Additional information.

</td></tr><tr><td class="sub-head" colspan="2">

**Contact tab**

</td></tr><tr><td>

Street

</td><td>

Street address of third party.

</td></tr><tr><td>

City

</td><td>

City of third party.

</td></tr><tr><td>

State / Province

</td><td>

State or Province of the third party.

</td></tr><tr><td>

Zip / Postal code

</td><td>

Zip code or postal code of the third party.

</td></tr><tr><td>

Country

</td><td>

Country of the third party.

</td></tr><tr><td>

Phone

</td><td>

Phone number of the third party.

</td></tr><tr><td>

Fax phone

</td><td>

Fax number of the third party.

</td></tr><tr><td class="sub-head" colspan="2">

**Profile tab**

</td></tr><tr><td>

Publicly traded

</td><td>

Is the third party publicly traded?

</td></tr><tr><td>

Stock symbol

</td><td>

Stock symbol of the third party.

</td></tr><tr><td>

Revenue per year

</td><td>

Annual revenue of the third party.

</td></tr><tr><td>

Number of employees

</td><td>

Count of the third party's employees.

</td></tr><tr><td>

Banner image

</td><td>

Banner image for the third party.

</td></tr><tr><td>

Banner text

</td><td>

Banner text for the third party.

</td></tr><tr><td class="sub-head" colspan="2">

**Risk Scoring tab**

</td></tr><tr><td>

Computed risk rating

</td><td>

Average of the third-party risk area risk ratings.

</td></tr><tr><td>

Override risk rating

</td><td>

Enables you to override the computer risk rating for the third party.

</td></tr><tr><td>

Assessment risk rating

</td><td>

Calculated risk assessment rating. The risk rating scale helps business users better understand risk assessment results. For example, in the default settings, risk scores in the 20 through 39 range indicate high risk, while scores in the 60 through 79 range indicate low risk.

</td></tr><tr><td>

Engagement risk rating

</td><td>

Calculated engagement rating. The risk rating scale helps business users better understand risk assessment results. For example, in the default settings, risk scores in the 20 through 39 range indicate high risk, while scores in the 60 through 79 range indicate low risk.

</td></tr><tr><td>

Subsidiary risk rating

 Child third-party risk rating

</td><td>

Calculated risk rating for subsidiaries. The risk rating scale helps business users better understand risk assessment results. For example, in the default settings, risk scores in the 20 through 39 range indicate high risk, while scores in the 60 through 79 range indicate low risk.

</td></tr><tr><td>

Risk intelligence rating

</td><td>

See [Integrating scores from risk intelligence providers](../concept/tprm-riskintelprvdr-overview.md).

</td></tr><tr><td>

Overridden risk rating

</td><td>

If you selected **Override risk rating**, enter the new risk rating.

</td></tr><tr><td>

Overridden on

</td><td>

If you selected **Override risk rating**, date that the override occurred.

</td></tr><tr><td>

Justification

</td><td>

If you selected **Override risk rating**, you must enter a reason for the override.

</td></tr></tbody>
</table>3.  If Third-party Risk Management is integrated with other GRC applications, or if you set up vendor hierarchies \(that is, third-party risk domains, component criteria, and risk scoring rules\), the form can include some or all of the following related lists.

    For more information, see [Setting up VRM third-party hierarchies and engagements](../concept/vendor-hierarchy-engagements.md).

    **Note:** Risk domains are called "risk areas" in some platform applications.

    -   **Child Vendors:** This table stores all information for subsidiaries. Subsidiary risk ratings are automatically aggregated and displayed on the **Risk Rating** tab on the Third-party form.
    -   **Vendor Contacts:** This table stores information for all of the third-party stakeholders. Typically, the customer creates one primary third-party contact and one or more secondary contacts. The primary contact adds other contacts to the list.
    -   **Business Services:** The Services table is part of the CMDB. It relates the third parties to the services they provide. For example, assume the IT team has a service called “Video Conference Services” that is used for internal employees to communicate internally and with customers. That business service, they have decided, comes from Zoom rather than building anything in-house.
    -   **Vendor Engagements:** This table stores all engagement information for third parties. Engagements risk ratings are automatically aggregated as displayed on the **Risk rating** tab on the Third-party form.
    -   **Tiering Assessments:** This table stores the history of tiering assessments.
    -   **Repeating Assessments:** This table stores the history of recurring assessments.
    -   **Assessments:** This table stores the history of assessments. Assessment risk ratings are automatically aggregated and displayed on the **Risk rating** tab on the Third-party form.
    -   **Vendor Risk Components:** This table stores all third-party risk components. If third-party risk components \(that is, assessments, engagements, or subsidiaries\) are present, their risk ratings are automatically aggregated and displayed on the **Risk rating** tab on the Third-party form.
    -   **Issues:** This table stores the history of issues.
    -   **Tasks:** This table stores the history of tasks.

