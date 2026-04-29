---
title: Software subscription fields
description: Software subscription form fields, their descriptions, and the SaaS integrations for which these fields are populated.
locale: en-US
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Software Asset Management references, Software Asset Management, IT Asset Management]
---

# Software subscription fields

Software subscription form fields, their descriptions, and the SaaS integrations for which these fields are populated.

Some of the fields in the Software subscription table get populated for specific SaaS integrations while some get populated for all SaaS integrations.

<table id="table_m3g_ggh_xgc"><thead><tr><th>

Field

</th><th>

Description

</th><th>

Is pulled from the portal?

</th><th>

SaaS integration

</th></tr></thead><tbody><tr><td>

Display name

</td><td>

Name of the subscription downloaded from the SaaS portal.

</td><td>

Yes

</td><td>

All SaaS integrations

</td></tr><tr><td>

Publisher

</td><td>

The publisher for the subscription.

</td><td>

Yes

</td><td>

All SaaS integrations

</td></tr><tr><td>

Product

</td><td>

The software product for the subscription.

</td><td>

Yes

</td><td>

All SaaS integrations

</td></tr><tr><td>

Version

</td><td>

Version of the software product.

</td><td>

Yes

</td><td>

All SaaS integrations

</td></tr><tr><td>

Edition

</td><td>

Edition of the software product.

</td><td>

Yes

</td><td>

All SaaS integrations

</td></tr><tr><td>

Software model

</td><td>

A standardized version of a software product for the subscription. The software model is automatically created for SaaS integrations.

</td><td>

No \(Automatically created by ServiceNow\)

</td><td>

All SaaS integrations

</td></tr><tr><td>

User

</td><td>

The ServiceNow user record in the User \[sys\_user\] table representing a real person within an organization. In general, the User table is populated through the Active directory integration in the organization.

</td><td>

 

</td><td>

All SaaS integrations

</td></tr><tr><td>

User principal name

</td><td>

A unique identifier for a user in the SaaS portal. This is typically the email address of the user in the SaaS portal.

</td><td>

Yes

</td><td>

All SaaS integrations

</td></tr><tr><td>

Last activity

</td><td>

The date when the subscription record was last active. For Microsoft 365 products, this field is populated from the Software Usages \[samp\_sw\_usage\] table and Microsoft 365 Apps Usage Reports \[samp\_m365-apps-usage-report\] table. This field determines usage-based optimization recommendation.

</td><td>

Yes

</td><td>

All SaaS integrations except CrowdStrike and Docusign

</td></tr><tr><td>

Inactive days

</td><td>

Number of days for which a user's subscription has been inactive.This field is visible on the Software Subscriptions form when the **Last activity** field isn’t empty. Inactive days are calculated using the value in the **Last activity** field.

</td><td>

No \(Automatically determined\)

</td><td>

All SaaS integrations except CrowdStrike

</td></tr><tr><td>

Subscription profile

</td><td>

Display name of the integration profile.

</td><td>

No \(Automatically created by ServiceNow\)

</td><td>

All SaaS integrations

</td></tr><tr><td>

Licensable software model

</td><td>

Name of the software model relevant for licensing purposes.

</td><td>

No \(Automatically determined\)

</td><td>

All SaaS integrations

</td></tr><tr><td>

Subscription identifier

</td><td>

A unique technical identifier provided by the SaaS provider, such as a service plan ID, that indicates the specific product or plan a user is subscribed to. This identifier allows ServiceNow to correctly map the subscription to the corresponding software model.For example, identifiers like VISIOCLIENT and ENTERPRISEPACK map to specific products such as Microsoft Visio Plan 2 and Office 365 E3, respectively.

</td><td>

Yes

</td><td>

All SaaS integrations

</td></tr><tr><td>

Inferred suite

</td><td>

The inferred suite model that this software subscription belongs to.

</td><td>

No \(Automatically determined\)

</td><td>

Microsoft 365 integration

</td></tr><tr><td>

Discovered user

</td><td>

The record in the Discovered User \[samp\_discovered\_user\] table that represents a user identity discovered from an external system.

</td><td>

No \(Automatically determined\)

</td><td>

All SaaS integrations

</td></tr><tr><td>

Active

</td><td>

Indicates if the subscription record is active.

</td><td>

No \(Automatically determined\)

</td><td>

All SaaS integrations

</td></tr><tr><td>

Is reconciled

</td><td>

Indicates whether the SaaS subscription has been reconciled.This field is populated after reconciliation is run.

</td><td>

No \(Automatically determined\)

</td><td>

All SaaS integrations

</td></tr><tr><td>

License metric result

</td><td>

License metric result of the software product that is populated after reconciliation. For more information on license metric results, see [Software reconciliation results](../concept/software-reconciliation-results.md).

</td><td>

No \(Automatically determined\)

</td><td>

All SaaS integrations

</td></tr><tr><td>

Product result

</td><td>

Product result of the software product that is populated after reconciliation. For more information on product results, see [Software reconciliation results](../concept/software-reconciliation-results.md).

</td><td>

No \(Automatically determined\)

</td><td>

All SaaS integrations

</td></tr><tr><td>

Software model result

</td><td>

Software model result of the software product that is populated after reconciliation. For more information on software model results, see [Software reconciliation results](../concept/software-reconciliation-results.md).

</td><td>

No \(Automatically determined\)

</td><td>

All SaaS integrations

</td></tr><tr><td>

Unlicensed subscription

</td><td>

Indicates whether the subscription remains unlicensed after reconciliation due to insufficient available licenses. This field is updated with a true or false value to reflect the licensing status.

</td><td>

No \(Automatically determined\)

</td><td>

All SaaS integrations

</td></tr></tbody>
</table>**Parent Topic:**[Software Asset Management references](references.md)

