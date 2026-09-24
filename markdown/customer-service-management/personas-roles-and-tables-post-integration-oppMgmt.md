---
title: Roles
description: After successful integration of Opportunity Management with Service Model Foundation, various roles are added to the list view menu.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/personas-roles-and-tables-post-integration-oppMgmt.html
release: brazil
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Opportunity Management for business location, Integration with Sales Customer Relationship Management, Configure Service Model Foundation, Data models, Set up your environment, Configure, Customer Service Management]
---

# Roles

After successful integration of Opportunity Management with Service Model Foundation, various roles are added to the list view menu.

## Description of roles

<table id="table_rnc_gcs_ffc"><tbody><tr><td>

Role

</td><td>

Description

</td><td>

Contains roles

</td></tr><tr><td>

Organization B2B Sales Representative \(sn\_bus\_org\_opptym.org\_b2b\_sales\_rep\)

</td><td>

Functional role for creating location Opportunity for account.

</td><td>

-   Location Org Viewer \(sn\_bus\_loc.location\_org\_viewer\)
-   Location Opportunity Creator \(sn\_bus\_org\_opptym.org\_opportunity\_creator\)
-   Location Account Viewer \(sn\_bus\_loc.location\_account\_viewer\)

</td></tr><tr><td>

Organization B2C Sales Representative \(sn\_bus\_org\_opptym.org\_b2c\_sales\_rep\)

</td><td>

Functional role for creating location opportunity for consumers.

</td><td>

This role contains the following inherited roles.

 -   Location Org Viewer \(sn\_bus\_loc.location\_org\_viewer\)
-   Location Opportunity Creator \(sn\_bus\_org\_opptym.org\_opportunity\_creator\)
-   Location Consumer Viewer \(sn\_bus\_loc.location\_account\_viewer\)

</td></tr><tr><td>

Organization Sales Manager \(sn\_bus\_org\_opptym.org\_sales\_mgr\)

</td><td>

Functional role for location opportunity managers. They can create location opportunities for accounts and consumers for their hierarchy.

</td><td>

This role contains the following inherited roles

 -   Location Org Hierarchy Viewer \(sn\_bus\_loc.location\_org\_hierarchy\_viewer\)
-   Organization B2B Sales Representative \(sn\_bus\_org\_opptym.org\_b2b\_sales\_rep\)
-   Organization B2C Sales Representative \(sn\_bus\_org\_opptym.org\_b2c\_sales\_rep\)

</td></tr><tr><td>

Organization Opportunity Relationship Manager\(sn\_bus\_org\_opptym.org\_relationship\_mgr\)

</td><td>

Functional role for enterprise partner relationship managers. They’re responsible for building and managing relationships with multiple channel partners. They can create, manage, and approve account and consumer-related opportunities within their assigned organizational hierarchy.

</td><td>

This role contains Organization Sales Manager \(sn\_bus\_org\_opptym.org\_sales\_mgr\)

</td></tr><tr><td>

sn\_bus\_org\_opptym.org\_ui

</td><td>

Granular role for organization staff to ensure consistent opportunities experience across all user interfaces.

</td><td>

None

</td></tr></tbody>
</table>If a business organization enables [Restricted Customer Access](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/associate-customers-or-bus-loc-to-so.md), the account and consumer visibility restriction also applies to sales personas such as B2B and B2C sales representatives. In other words, these personas can view only the accounts and consumers supported by their own business organization, and cannot view accounts and consumers supported by other business organizations. For upgrade customers, this restriction has no effect until an admin runs the **Remove Legacy Roles from Loc Mgr Contrib** scheduled job. For more information, see [Enable restricted customer access for Business Organizations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/remove-legacy-contributor-roles-from-loc-mgr-contrib.md)

