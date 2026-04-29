---
title: Retirement definitions
description: Specify a retirement definition for a class, to reflect protocols in your organization applicable to the class and to its child classes. These definitions support the transition of CIs through life cycle stages as implemented by CMDB Data Manager life-cycle policies. A class can have a retirement definition by derivation, or by a retirement definition specified for that class.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [CMDB data management, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Retirement definitions

Specify a retirement definition for a class, to reflect protocols in your organization applicable to the class and to its child classes. These definitions support the transition of CIs through life cycle stages as implemented by CMDB Data Manager life-cycle policies. A class can have a retirement definition by derivation, or by a retirement definition specified for that class.

## CMDB Data Manager requirement and usage

An active retirement definition is required for each targeted class in a Retire, Archive, or Delete CMDB Data Manager policy. A retirement definition is used to flag a CI as retired according to the CI’s class retirement definition in effect. When retiring a CI, the CI's attributes are set according to the retirement definition for the CI's class. A subsequent operation such as delete or archive, that needs to be applied to retired CIs, first checks if a CI is in a retired state by verifying that it satisfies the retirement definition for its class.

Retirement definitions are used in life-cycle policies as follows:

-   Setting target CIs in Retire policies, according to their associated class retirement definitions.
-   Filtering out target CIs In Retire policies, that are determined to already be in a retired state according to their associated retirement definitions. Those CIs aren’t targeted even if they meet the policy filter.
-   Identifying CIs as being ready to be processed by an Archive or Delete policies. Archive and Delete policies can only process CIs that are in a retired state that matches their associated class retirement definition. Therefore, target CIs in Archive and Delete policies, are checked against their associated class retirement definition to verify that they are in a retired state before they can be archived or deleted.

## Derivation across the CMDB hierarchy

Retirement definitions are derived throughout the CMDB hierarchy in the same way that rules, such as identification rules, are derived. Child classes extended from a parent class with a retirement definition, derive that definition unless there’s a retirement definition defined at the child class level.

When retirement definitions for classes exist in different levels in the class hierarchy, then the retirement definition that applies is the one that is most specific for a class. For example, if there are retirement definitions for both, the Computer and the Configuration Item class, then the Computer class definition also applies to its descendant classes. All other classes that aren't descendants of the Computer class, use the Configuration Item retirement definition.

Always be aware of the automatic derivation of retirement definitions throughout the class hierarchy. For example, an active retirement definition for the Configuration Item \[cmdb\_ci\] class can potentially be in effect throughout the entire CMDB hierarchy \(aside from classes with their own retirement definition\).

## Predefined retirement definitions

The base system includes predefined retirement definitions for key classes such as Hardware \[cmdb\_ci\_hardware\] and Application \[cmdb\_ci\_appl\], and are stored in the CMDB Retirement Custom Definitions \[cmdb\_retirement\_custom\_definitions\] table. For example, the predefined retirement definition for the Service \[cmdb\_ci\_service\] class specifies that for a retired CI, the value of the attributes \[operational status\], \[Phase\], and \[Status\] is **Retired**.

Retirement definition for the Configuration item \[cmdb\_ci\] class behaves in the following important ways:

-   It is active by default and you can't deactivate it.
-   You can't delete it.
-   By default, it is in effect throughout the entire CMDB hierarchy due to derivation.

The rest of the predefined retirement definitions are inactive by default, and you must activate a retirement definition that corresponds to a targeted class in a Retire, Archive, or Delete CMDB Data Manager policy.

You can use the default retirement definitions, or customize a definition to reflect practices in your organization. You can also add a custom retirement definition for a class. However, each CMDB class can be associated with only a single retirement definition.

To manage or delete a retirement definition, see [Manage retirement definitions](../task/data-manager-manage-ret-def-wrkspc.md#).

