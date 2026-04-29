---
title: Deleting an external procurement application integration profile
description: If you want to stop using an external procurement application for creating software requisitions through Software Asset Management, you can delete the integration profile.
locale: en-US
release: australia
product: Procurement
classification: procurement
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Integrating with external procurement applications, Procurement, Asset Management, IT Service Management]
---

# Deleting an external procurement application integration profile

If you want to stop using an external procurement application for creating software requisitions through Software Asset Management, you can delete the integration profile.

A sam\_admin can delete an integration profile by selecting **Delete** on the integration profile record.

When you delete a direct integration profile, all scheduled jobs and the job results associated with the profile gets deleted. The integration profile references are also removed from the Purchase Order records on ServiceNow.

After you delete the integration profile, Software Asset Management doesn’t consider any in progress requests. Ensure that all the requests in progress are completed before you delete the integration profile.

