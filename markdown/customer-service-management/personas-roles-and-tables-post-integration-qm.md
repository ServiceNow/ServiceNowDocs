---
title: Roles
description: After successful integration of Order Management, the following menu items and roles are added to the list view menu.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/personas-roles-and-tables-post-integration-qm.html
release: brazil
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Quote management for business organization, Integration with Sales Customer Relationship Management, Configure Service Model Foundation, Data models, Set up your environment, Configure, Customer Service Management]
---

# Roles

After successful integration of Order Management, the following menu items and roles are added to the list view menu.

## Description of roles

<table id="table_rnc_gcs_ffc"><tbody><tr><td>

Role

</td><td>

Description

</td><td>

Contains roles

</td></tr><tr><td>

Location Customer Quote Agent \(sn\_bus\_org\_qm.org\_sales\_mgr\)

</td><td>

This role enables organization staff to create and manage account-related offers at their specific organizations.

</td><td>

-   Location Quote Creator \(sn\_bus\_org\_qm.org\_quote\_creator\)
-   Location Account Viewer \(sn\_bus\_loc.location\_account\_viewer\)
-   Location Organization Viewer \(sn\_bus\_loc.location\_org\_viewer\)

</td></tr><tr><td>

Organization ConsumerQuote Agent \(sn\_bus\_org\_qm.org\_sales\_mgr\)

</td><td>

This role enables organization staff to approve account-related quotes at their specific organizations.

</td><td>

-   Location Consumer Viewer \(sn\_bus\_loc.location\_consumer\_viewer\)
-   Location Organization Viewer \(sn\_bus\_loc.location\_org\_viewer\)
-   Organization Quote Creator \(sn\_bus\_org\_qm.org\_quote\_creator\)

</td></tr><tr><td>

Relationship manager for quotes \(sn\_bus\_org\_qm.org\_relationship\_mgr\)

</td><td>

This role enables enterprise sales personas to create, manage and approve account and consumer-related quotes for their assigned organization hierarchy.

</td><td>

-   sn\_bus\_loc\_qm.location\_consumer\_quote\_agent
-   sn\_bus\_loc\_qm.location\_customer\_quote\_agent
-   sn\_bus\_loc\_qm.location\_customer\_quote\_agent

</td></tr><tr><td>

Organization Quote Manager \(sn\_bus\_loc.org\_sales\_mgr\)

</td><td>

This role enables enterprise sales personas to create, manage, and approve account and consumer-related orders for their assigned organizational hierarchy.

</td><td>

-   Organization Consumer Quote Agent \(sn\_bus\_org\_qm.org\_b2b\_sales\_rep\)
-   Organization Consumer Quote Agent \(sn\_bus\_org\_qm.org\_b2b\_sales\_rep\)
-   Location Organization Hierarchy Viewer \(sn\_bus\_loc.location\_org\_hierarchy\_viewer\)

</td></tr><tr><td>

sn\_bus\_org\_qm.org\_ui

</td><td>

Granular role for organization staff to ensure consistent sales quote experience across all user interfaces.

</td><td>

None

</td></tr></tbody>
</table>**Note:** For more information on channel partners see, [ServiceNow Quote Experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/quoting-experiences-overview.md).

If a business organization enables [Restricted Customer Access](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/associate-customers-or-bus-loc-to-so.md), the account and consumer visibility restriction also applies to sales personas such as B2B and B2C sales representatives. In other words, these personas can view only the accounts and consumers supported by their own business organization, and cannot view accounts and consumers supported by other business organizations. For upgrade customers, this restriction has no effect until an admin runs the **Remove Legacy Roles from Loc Mgr Contrib** scheduled job. For more information, see [Enable restricted customer access for Business Organizations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/remove-legacy-contributor-roles-from-loc-mgr-contrib.md)

