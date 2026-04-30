---
title: Define a VRM engagement
description: Define an engagement so that you can assess the risks that are associated with the services or products offered by a third party. Engagements can also represent the products or services that are provided to the parent third party, either directly or from departments, partners, or subsidiaries that you can also assess for risk.
locale: en-US
release: yokohama
product: Third-party Risk Management
classification: third-party-risk-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Work in the VRM classic UI, Third-party Risk Management, Governance, Risk, and Compliance]
---

# Define a VRM engagement

Define an engagement so that you can assess the risks that are associated with the services or products offered by a third party. Engagements can also represent the products or services that are provided to the parent third party, either directly or from departments, partners, or subsidiaries that you can also assess for risk.

## Before you begin

Role required: sn\_vdr\_risk\_asmt.vendor\_risk\_manager or sn\_vdr\_risk\_asmt.vendor\_assessor

## Procedure

1.  On the **Risk** tab of the Vendor Management Workspace, select **Create engagement** in the Quick actions box.

    The Create third-party engagement form opens to the **Details** tab.

2.  Select **Browse** to select and add an attachment.

3.  Fill in the form and then select **Save**.

<table id="table_FloorForm"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

**Third-party engagement section**

</td></tr><tr><td>

Name

</td><td>

Unique name for the engagement. Ideally, mention the product or service that is the subject of the engagement.

</td></tr><tr><td>

Third party \(Vendor\)

</td><td>

The third party for whom you are creating this engagement record.

</td></tr><tr><td>

Type

</td><td>

Type of product or service to be provided by the engagement organization.

</td></tr><tr><td>

Start/End date

</td><td>

Enter start and end dates to define how long the engagement is valid.

</td></tr><tr><td>

Contract start date / end date

</td><td>

Preferred dates for the beginning and end of interactions with the third party.

</td></tr><tr><td>

Contract expiration date

</td><td>

The date on which the engagement ends officially and legally.

</td></tr><tr><td>

Status

</td><td>

Select the current status of the engagement.

 -   Active
-   Onboarding
-   Prospect
-   Active unauthorized
-   Terminated
-   Onboarding rejected
 **Note:** An engagement starts in the inactive state. An engagement moves to the active state when a contract is in place or you take part in an active relationship with the third party.

</td></tr><tr><td>

Risk rating

</td><td>

Displays the risk rating assigned to the engagement after an assessment has been performed.

</td></tr><tr><td>

Engagement tier

</td><td>

The tier used for this engagement. See [VRM third-party risk tiering assessments](../../grc-workspace-vrm/reference/manage-risk-tiering-assessments.md) for details of how the tier is determined.

</td></tr><tr><td>

Annual spend / Value

</td><td>

The annual monetary spend associated with this engagement's services.

</td></tr><tr><td>

Engagement manager

</td><td>

Specify the person who will monitor, prioritize, and act on responses to external questionnaires, issues, and tasks. Select the lock to lock/unlock the field.

</td></tr><tr><td>

Business owner

</td><td>

Specify the person who is familiar with the engagement organization and the product or services that will be engaged. Select the lock to lock/unlock the field.

</td></tr><tr><td>

Notes

</td><td>

Enter text that describe the engagement to other users.

</td></tr><tr><td class="sub-head" colspan="2">

**Contact section**

</td></tr><tr><td>

Street, City, State/Province, ZIP/Postal code, Country, Phone, Fax

</td><td>

Standard contact information for the engagement organization.

</td></tr><tr><td>

Latitude and Longitude

</td><td>

The **Latitude** and **Longitude** values are used to mark the location on the Risk concentration map. See [TPRM Risk concentration map](../../grc-workspace-vrm/concept/tprm-ws-risk-concentration-map.md).

</td></tr><tr><td class="sub-head" colspan="2">

**Risk Ratings section**

</td></tr><tr><td>

Computed risk rating

</td><td>

The calculated **Computed risk rating**.

 The value is overall risk rating for the third party, calculated after the assessment by rolling up all of the TPR assessors' risk ratings.

</td></tr><tr><td>

Override risk rating

</td><td>

Option to override the computed rating.

 If you select the check box, then specify the following values:

-   Overridden risk rating. Select the new risk rating.
-   Overridden on: The system auto-populates the date that the override occurred.
-   Justification: Enter the reason that you overrode the value.


</td></tr></tbody>
</table>
