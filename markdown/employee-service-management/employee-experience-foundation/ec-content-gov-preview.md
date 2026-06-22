---
title: Previewing and approving a content request item
description: Content requesters can preview content request items before they approve it to be published.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/employee-service-management/employee-experience-foundation/ec-content-gov-preview.html
release: zurich
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Managing content requests, Manage, Employee Center Pro, Unified Employee Experience, Employee Service Management]
---

# Previewing and approving a content request item

Content requesters can preview content request items before they approve it to be published.

When a content creator sends the completed content for review, the system assigns a new task to the requester and any additional approvers.

\[Omitted image "content-gov-request-review.png"\] Alt text: The requester and other reviewers access the review request from the My Tasks button in the portal

The content requester can preview the content item that appears in a preview portal with the content item highlighted.

**Note:** Only rich content, news, and portal type content can be previewed.

The portal used for previews is determined by the sn\_ca.campaign.preview.portal\_url\_suffix system property found in **Properties** under Content Experiences Configurations. For more information, see [Properties installed with Content Publishing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/employee-experience-foundation/properties-with-content-delivery.md) and [Properties installed with Content Experiences](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/employee-experience-foundation/properties-installed-with-content-auto.md).

## Email notification

An email notification is sent to the content requester and appears as a to-do under **My Tasks** in the Employee Center Pro. A link is provided to the to-do.

For information on setting up email notifications, see [Create an email notification](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/ai-platform-administration/t_CreateANotification.md).

