---
title: Manage and create opportunity types in Opportunity Marketplace
description: As an Opportunity Marketplace admin \[sn\_opp\_market.admin\], you can manage Opportunity types that are provided with the base system or create custom opportunity types.
locale: en-US
release: xanadu
product: Opportunity Marketplace
classification: opportunity-marketplace
topic_type: task
last_updated: "2024-08-14"
reading_time_minutes: 2
breadcrumb: [Install and configure Opportunity Marketplace, Opportunity Marketplace, Talent Development, Employee Service Management]
---

# Manage and create opportunity types in Opportunity Marketplace

As an Opportunity Marketplace admin \[sn\_opp\_market.admin\], you can manage Opportunity types that are provided with the base system or create custom opportunity types.

## Before you begin

Role required: Opportunity Marketplace admin \[sn\_opp\_market.admin\]

## About this task

The opportunity types provided by the base system cover Gig opportunities, Project opportunities, and Volunteer opportunities. If you have special requirements for an opportunity, you can add custom opportunity types for your enterprise.

**Note:** If an Opportunity Marketplace admin modified or removed any of these fields in the **Record Producer** form for an opportunity, there could be an unintended impact to the matching score for an opportunity.

-   **Opportunity Title**
-   **Opportunity Owner**
-   **Start or End date**

## Procedure

1.  Navigate to **All** &gt; **Opportunity Marketplace** &gt; **Opportunity Type Configuration**.

2.  To create a custom opportunity type, select **New**.

3.  Fill in the **Opportunity type new record** form.

<table id="table_fvj_byv_jcc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**Title**

</td><td>

This field is visible to users. The title of an opportunity type should be descriptive to help opportunity owners and applicants understand the purpose of the opportunity type.

</td></tr><tr><td>

**Role display**

</td><td>

-   **Embedded within opportunity \(1 role only\)**

Select this option for an opportunity that needs only a single role.

-   **Embedded within opportunity \(1 or more roles\)**

Select this option so that you can embed multiple roles within an opportunity.

</td></tr><tr><td>

**User criteria**

</td><td>

Select from the list of available user criteria. **User Criteria Records** are created and maintained from **All** &gt; **Change** &gt; **Administration** &gt; **User Criteria**, see [Create a user criteria record for Change Management](https://www.servicenow.com/docs/access?context=create-user-criteria&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US).

</td></tr><tr><td>

**Opportunity details**

</td><td>

Opportunity details are created and maintained by the OPM admin. The Opportunity details are stored in the Service Catalog as a Record producer item under **All** &gt; **Service catalog** &gt; **Record Producers** with the application scope set to Opportunity Marketplace.

</td></tr><tr><td>

**Roles and requirements**

</td><td>

A list of existing Opportunity types that you can select to define an opportunity type's roles and requirements.

</td></tr><tr><td>

**Description**

</td><td>

The information is this field is visible to applicants and opportunity owners. The description helps opportunity owners and applicants under the intent of the type of opportunity and its scope.

</td></tr><tr><td>

**Active**

</td><td>

Select **Active** to enable the opportunity type to be used by others.

</td></tr><tr><td>

**Icon**

</td><td>

Add an icon that represents the type of opportunity.

</td></tr><tr><td>

**Help link label**

</td><td>

The text displayed to opportunity owners for a link to help for this form.

</td></tr><tr><td>

**Help link URL**

</td><td>

A URL that links to help for this form.

</td></tr></tbody>
</table>4.  Select **Submit**.


**Parent Topic:**[Install and configure Opportunity Marketplace](../concept/egd-oppt-mrktplc-inst-config.md)

