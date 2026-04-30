---
title: Create a domain configuration
description: Create a domain configuration to define which domains to collect scores from and how to store scores within the domain hierarchy.
locale: en-US
release: yokohama
product: Performance Analytics
classification: performance-analytics
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Domain configurations, Domain separation, Configure Performance Analytics advanced features, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Create a domain configuration

Create a domain configuration to define which domains to collect scores from and how to store scores within the domain hierarchy.

## Before you begin

Role required: pa\_admin or admin

The Performance Analytics - Domain Support plugin \(com.snc.pa.domain\_support\) must be activated.

## Procedure

1.  Navigate to **All** &gt; **Performance Analytics** &gt; **Domain Configuration** and create a new record.

<table id="table_mff_5qm_tw"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration type

</td><td>

Specify how you want to determine which domains to include in this configuration. Select **Visibility group** to include all domains visible to a specific group, based on existing visibility domains associated with that group.

 Select **Conditions** to specify the domains directly, using conditions.

</td></tr><tr><td>

Visibility group

</td><td>

When **Configuration type** is **Visibility group**, select or create a Group \[sys\_user\_group\] that has at least one visibility domain. All visibility domains available to this group are included in this domain configuration. For more information about visibility domains, see [Visibility domains and Contains domains](https://www.servicenow.com/docs/access?context=c_DomainVisibility&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US).

</td></tr><tr><td>

Conditions

</td><td>

When **Configuration type** is **Conditions**, specify conditions to determine which domains are included in this configuration. The conditions you select apply to the Domain \[domain\] table. For example, select \[\[Type\]\[is\]\[MSP\]\] to select all managed service provider domains.

</td></tr><tr><td>

Collect aggregate

</td><td>

Aggregate scores from the specified domain hierarchy. Aggregate scores are stored in a separate domain that exists outside of the domain hierarchy and contains only scores. One aggregate domain is created for each domain configuration where **Collect aggregate** is selected. The name of this domain is displayed in the read-only **Aggregate domain** field.

 Aggregate domains are stored as children of the Performance Analytics Aggregation Container domain.

</td></tr><tr><td>

Collect children

</td><td>

Select this option to collect scores from children of the specified domains. Scores are collected from all child domains, not only those domains that are direct children of the specified domains. Scores collected from a child domain are stored in that domain.

</td></tr><tr><td>

Roll up

</td><td>

Select this option to roll collected scores of child domains up to the top-level parent domain in the hierarchy.

</td></tr><tr><td>

Roll up type

</td><td>

Select **All child domains** to roll up scores from the specified domains and all of their child domains. Select **Only selected domains** to roll up scores only from the child domains that are explicitly included in the domain configuration. For a visibility group, a domain configuration explicitly includes a child domain if it and its parent domain are in a visibility domain of the group. For conditions, a domain configuration explicitly includes a child domain if the conditions select that domain and its parent domain.

</td></tr></tbody>
</table>
**Parent Topic:**[Grouping domains in Performance Analytics domain configurations](../concept/pa-domain-separation-msp.md)

**Related topics**  


[Domain separation setup and administration](https://www.servicenow.com/docs/access?context=c_DomainSeparationSetup&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US)

