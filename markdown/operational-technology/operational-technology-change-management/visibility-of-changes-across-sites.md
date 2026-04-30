---
title: Managing change requests across sites
description: You can view, create, or edit the change requests that belong to your site or other sites by using the Operational Technology Change Management application. By viewing the change requests from other sites, you can implement similar changes at your site.
locale: en-US
release: xanadu
product: Operational Technology Change Management
classification: operational-technology-change-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Use, Operational Technology Change Management, Operational Technology]
---

# Managing change requests across sites

You can view, create, or edit the change requests that belong to your site or other sites by using the Operational Technology Change Management application. By viewing the change requests from other sites, you can implement similar changes at your site.

## Change requests across sites overview

If you have the sn\_ot\_change\_write role, you can do the following tasks:

-   View and edit the Operational Technology \(OT\) change requests that are assigned to you or the change requests that belong to your site.
-   Create the OT change requests.
-   View the OT change requests that belong to the other sites.

The main benefit of having the sn\_ot\_change\_write role is that you have read-only visibility of changes across sites. Viewing other changes across sites can help you implement similar changes at your site.

**Note:** You can only edit OT change requests belonging to sites you have access to. Learn more about additional roles required for managing cross-site OT change requests in the following sections.

## Other OT roles and permissions that you need with the sn\_ot\_change\_write role

The following table describes the additional roles that you, as a user with the sn\_ot\_change\_write role, need so that you can access the change requests for your site or any site.

|Role|Permissions|
|----|-----------|
|sn\_ot\_change\_write with the cmdb\_ot\_isa\_editor role|Create and edit the change requests for your site.|
|sn\_ot\_change\_write with cmdb\_ot\_isa\_viewer role|Create and edit the change requests for your site.|
|sn\_ot\_change\_write and cmdb\_ot\_isa\_viewer\_all|Create and edit the change requests for any site.|
|sn\_ot\_change\_write with no site role|View the change requests for any site.|

## Other OT roles and permissions that you need with the sn\_ot\_change\_read role

The following table describes the additional roles and permissions that you, as a user with the sn\_ot\_change\_read role, need so that you can view the change requests for your site or any site.

|Role|Permissions|
|----|-----------|
|sn\_ot\_change\_read with the cmdb\_ot\_isa\_editor role|View the change requests for your site.|
|sn\_ot\_change\_read with cmdb\_ot\_isa\_viewer role|View the change requests for your site.|
|sn\_ot\_change\_read and cmdb\_ot\_isa\_viewer\_all|View the change requests for any site.|
|sn\_ot\_change\_read with no site role|View the change requests for any site.|

## Where to view or edit change requests

The following OT change request lists are available in the Lists module on the Industrial Workspace:

-   Assigned to me: View and edit your assigned change records by navigating to **OT Change Requests** &gt; **Assigned to me**.
-   Belong to my sites: View and edit the change records that belong to your sites by navigating to **OT Change Requests** &gt; **Belong to my sites**.
-   View the existing change records at different sites by navigating to **OT Change Requests** &gt; **All**.

**Parent Topic:**[Using Operational Technology Change Management](using-operational-technology-change-management.md)

