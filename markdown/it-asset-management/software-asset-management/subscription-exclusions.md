---
title: Subscription exclusions for SaaS and SSO applications
description: Define subscription exclusions for your SaaS and SSO applications to optimize your licensing costs by keeping the excluded subscriptions out of license cost calculations.Define exclusions for your subscription identifiers to keep them excluded from the Software Asset Management application's license calculations. Subscription identifiers uniquely identify your SaaS and SSO applications.Define exclusions for certain user subscriptions to keep them excluded from the Software Asset Management application's license calculations.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-asset-management/software-asset-management/subscription-exclusions.html
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [License exclusions, Configuring Software Asset Management, Software Asset Management, IT Asset Management, Asset Management]
---

# Subscription exclusions for SaaS and SSO applications

Define subscription exclusions for your SaaS and SSO applications to optimize your licensing costs by keeping the excluded subscriptions out of license cost calculations.

You can keep certain low-value and high-volume user subscriptions from being charged during the Software Asset Management application's licensing calculations. You can define two types of subscription exclusions: Identifier-based exclusions and User-based exclusions.

**Important:** Identifier-based exclusions are specific to individual subscription profile types, whereas User-based exclusions apply across all SaaS integration profiles.

**Parent Topic:**[License exclusions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-asset-management/software-asset-management/software-asset-management-license-exclusions.md)

## Define identifier-based exclusions for SaaS and SSO applications

Define exclusions for your subscription identifiers to keep them excluded from the Software Asset Management application's license calculations. Subscription identifiers uniquely identify your SaaS and SSO applications.

### Before you begin

Role required: sam\_admin

### About this task

Subscription identifiers help you track your software subscriptions and understand your license calculations. You can optimize your licensing costs by defining subscription identifier-based exclusions so that these identifiers aren't included while calculating your licensing costs.

**Note:** If you’re using the Software Asset Workspace, the option to navigate to the integration profile in Core UI is inactive.

### Procedure

1.  Navigate to the integration profile.

    |Interface|Action|
    |---------|------|
    |**Core UI**|Navigate to **All** &gt; **Software Asset** &gt; **SaaS License** &gt; **Direct Integration Profiles**.|
    |**Software Asset Workspace**|Navigate to **License operations** &gt; **User Subscriptions** &gt; **Direct integration profiles**.|

2.  Select an integration profile for which you're defining an identifier-based exclusion.

3.  Select the Subscription Identifier Exclusion Rule related list.

4.  Select **New**.

5.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Subscription identifier|The subscription identifier for which you're creating the exclusion rule.|
    |Profile type|Type of integration profile.|
    |Domain|Domain to which the data belongs.|
    |Active|The option when the exclusion rule is active.|

6.  Select **Save**.


### Result

The identifier-based exclusion rule is created for the subscription identifier. The specified subscription identifier remains excluded when the scheduled job is executed for license calculations.

## Define user-based exclusions for SaaS and SSO applications

Define exclusions for certain user subscriptions to keep them excluded from the Software Asset Management application's license calculations.

### Before you begin

Role required: sam\_admin

### About this task

You can create subscription user exclusion rules so that these user subscriptions aren’t included while calculating your licensing costs. The exclusion rules for these user subscriptions help you optimize your licensing costs.

### Procedure

1.  Navigate to the integration profile.

    |Interface|Action|
    |---------|------|
    |**Core UI**|Navigate to **All** &gt; **Software Asset** &gt; **SaaS License** &gt; **Direct Integration Profiles**.|
    |**Software Asset Workspace**|Navigate to **License operations** &gt; **User Subscriptions** &gt; **Direct integration profiles**.|

2.  Select an integration profile for which you're defining a user-based exclusion.

3.  Select the Subscription User Exclusion Rule related list.

4.  Select **New**.

5.  On the form, fill in the fields.

<table id="table_rzk_52z_rfc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

User principal name

</td><td>

User name or email address of the user.

</td></tr><tr><td>

Profile type

</td><td>

Type of integration profile.This field is not visible in the default view. You can add this field to the form using the custom view.

</td></tr><tr><td>

Domain

</td><td>

Domain to which the data belongs.

</td></tr><tr><td>

Active

</td><td>

The option when the exclusion rule is active.

</td></tr></tbody>
</table>6.  Select **Save**.


### Result

The user-based exclusion rule is created for the subscription identifier. The specified subscription identifier remains excluded when the scheduled job is executed for license calculations.

