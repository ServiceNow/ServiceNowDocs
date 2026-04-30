---
title: Register a risk intelligence provider
description: Create a record for each risk intelligence provider from which you’ll request reports. The risk scores and ratings that risk intelligence providers generate are analogous to personal credit scores. The scores provide insight on how trustworthy and safe a particular third party can be.
locale: en-US
release: xanadu
product: Third-party Risk Management
classification: third-party-risk-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Scores from risk intelligence providers, Integrate, Third-party Risk Management, Governance, Risk, and Compliance]
---

# Register a risk intelligence provider

Create a record for each risk intelligence provider from which you’ll request reports. The risk scores and ratings that risk intelligence providers generate are analogous to personal credit scores. The scores provide insight on how trustworthy and safe a particular third party can be.

## Before you begin

Role required: sn\_vdr\_risk\_asmt.vendor\_assessment\_reviewer

## Procedure

1.  Navigate to **All** &gt; **Third-party Risk Management** &gt; **Risk Intelligence Provider Setup** &gt; **Providers**.

2.  Select **New**, fill in the form, and then select **Submit**.

    |Field|Description|
    |-----|-----------|
    |Name|Unique name of the risk intelligence provider.|
    |Short description|Description of the provider and possibly of the services provided.|
    |Is multi-factor|Option to specify that the provider can return multiple different score types, for example, Financial risk or Security risk.|
    |Order reports|Option to specify that the provider can be selected for risk intelligence report requests.|
    |URL|Provider's website URL. This enables colleagues to visit and review the provider.|
    |Note|Text comments that provide additional information for your colleagues, for example, descriptions of the available scoring services or why your organization has decided to use the provider.|
    |Provider logo|Image of the provider's logo. This image appears on TPRM reports for the provider.|


## Result

You can now specify the services and levels of service that you might later request from the provider.

Services that you have associated with the provider appear in the Risk intelligence provider services related list. To add a service, select **New** in the related list and then follow the instructions in [Set up a risk intelligence provider service](tprm-riskintelprvdr-set-up.md).

**Important:** The **Order reports** option on the Risk intelligence provider form must be selected for providers to be available for risk intelligence report requests.

**Parent Topic:**[Integrating scores from risk intelligence providers](../concept/tprm-riskintelprvdr-overview.md)

