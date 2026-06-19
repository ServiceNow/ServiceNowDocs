---
title: View clone status \(legacy\)
description: View the status of a legacy clone.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/ai-platform-administration/view-clone-status.html
release: australia
product: AI Platform Administration
classification: ai-platform-administration
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Manage, Instance Clone, Configure core features, Administer the ServiceNow AI Platform]
---

# View clone status \(legacy\)

View the status of a legacy clone.

## Before you begin

Role required: clone\_admin

## Procedure

1.  Navigate to **All** &gt; **Instance Clone** &gt; **Live Clones** &gt; **Active Clones**.

    The system displays the list of currently active clones.

2.  Select a clone.

3.  Under **Related Links**, select **Check Clone Status**.

    The system updates the **State** field and produces a log entry in the **Clone Log** that shows the status of the clone.

    If an error occurs, you might [roll back clone](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown) and [schedule recurring clones](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-platform-administration/schedule-cloning.md). For more information see [Clone states](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-platform-administration/clone-states.md).


