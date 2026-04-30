---
title: Content page links in email notifications
description: Links to CMS pages can be put in notifications to make it easy for the reader to access the pages.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Links to records in email notifications, Create an email notification, Email and SMS notifications, System notifications, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Content page links in email notifications

Links to CMS pages can be put in notifications to make it easy for the reader to access the pages.

The link takes the following format: **$\{CMS\_URI+&lt;site&gt;/&lt;page&gt;\}**.

For example, to link the email recipient to a page called Incident in the content site ESS, with the current incident as the target document, use the following format: **$\{CMS\_URI+ess/incident\_detail\}**

The resulting email URL has this format: `https://<instance name>.service-now.com/ess/incident_detail.do?sysparm_document_key=incident,46e18c0fa9fe19810066a0083f76bd56`

**Parent Topic:**[Links to records in email notifications](c_EnablingLinksToServiceNowRecords.md)

