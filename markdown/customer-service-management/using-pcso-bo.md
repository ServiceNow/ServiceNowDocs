---
title: Using Proactive Customer Service Operations for business organizations
description: Track install base service health, track outages, and view outage banners for install base items at a business organization.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/using-pcso-bo.html
release: brazil
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Using Proactive Customer Service Operations, Automate and optimize, Use, Customer Service Management]
---

# Using Proactive Customer Service Operations for business organizations

Track install base service health, track outages, and view outage banners for install base items at a business organization.

The proactive customer service and major case management has been extended to business organizations, alongside the existing support for accounts. Digital services used by businesses organizations, referred as Install Base Items, are supported as affected install base items.

The following tasks work the same way for business organizations as they do for accounts:

-   [Create a proactive case from an alert](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/case-alert-workspace.md)
-   [Manage a proactive case created from an alert](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/manage-internally-reported-case.md)
-   [Review and accept a proactive case as a major case](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/resolve-proactive-case-major-case.md)
-   [Create an outage from a major case](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/track-outages-csm.md)

When multiple business organizations are affected by the same issue, the system can propose a major case and build a [recipients list](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/major-issue-recipient-lists.md) of the affected business organizations. If the major case manager accepts the proposal, they can create child cases for each affected business organization, so every affected business organization is tracked and updated under a single major case. For more information on major cases, recipients lists, and child cases, see [Major issue management overview](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/major-issue-management.md).

**Note:** When using proactive customer service with business organizations, keep the install base items for business organizations separate from the install base items for accounts. In other words, don’t use a single configuration item for both accounts and business organizations. For more information on how to configure proactive case flows for business organizations, see [Configure proactive case flows for business organizations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/configure-flow-designer-bo.md).

## Track outages for a business organization's install base items

View outages associated with a case to keep business organizations informed about any issues affecting their install base.

Role required: sn\_customerservice\_agent

Outages can be tracked using both proactive cases and customer-reported cases.

1.  Navigate to **All** &gt; **Customer Service** &gt; **Cases** &gt; **Proactive active**.
2.  Open the proactive case related to business organization's install base item.
3.  Open the Outages related list. You can view and track the outages from here.

**Related topics**  


[Using Proactive Customer Service Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/use-pcso.md)

[Track outages and install base service health on BOSP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/view-outage-banners-bosp.md)

