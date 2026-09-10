---
title: Review AI traffic detected across your organization
description: Review what Shadow AI has detected across your organization, by service, by user, or by department.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/sh-ai-review-detected-traffic.html
release: australia
topic_type: task
last_updated: "2026-08-20"
reading_time_minutes: 2
keywords: [Shadow AI, overview, detected traffic]
breadcrumb: [Assess AI exposure, Detecting shadow AI, Discover and manage AI assets, AI Control Tower, Enable AI experiences]
---

# Review AI traffic detected across your organization

Review what Shadow AI has detected across your organization, by service, by user, or by department.

## Before you begin

Role required: sn\_ai\_governance.ai\_steward

## About this task

In the Shadow AI overview, see how many AI services have been detected, how many are affected by a policy, and view detected traffic by service, by user, or by department. See [Shadow AI overview](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/sh-ai-overview.md) for what each subtab and filter shows.

## Procedure

1.  Navigate to **All** &gt; **AI Control Tower** &gt; **Home** &gt; **Inventory** &gt; **Shadow AI**.

    The **Detected AI traffic** list opens on the **AI traffic** subtab, set to **Last 30 days**.

2.  Adjust the date range for the list.

    For a complete picture, you can select **All time**, which lists services detected more than 30 days ago and now have **Limited details** status. Narrow to **Last 7 days** for a routine review, where the useful question is what's appeared since you last looked.

3.  Use the search box, or the **Category**, **Detection**, and **Status** filters, to narrow the list.

4.  Review and assess detected AI traffic, detected users, or detected departments.

<table><thead><tr><th align="left" id="d91197e154">

Subtab

</th><th align="left" id="d91197e157">

What to look for

</th></tr></thead><tbody><tr><td id="d91197e163">

**AI traffic**

</td><td>

1.  Determine which services carry the most risk by checking for a high **Events** count against a small number of **Users**, and for any service with no **Policy** applied.
2.  Check the **Detection** column to see what level of detail to expect. Armis-only detections show device and traffic signals, while ACC-covered services also show prompt and attachment content.
3.  Select a row to open that service's own record. See [Investigating a detected AI service in Shadow AI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/sh-ai-investigating-detected-services.md).


</td></tr><tr><td id="d91197e203">

**Users**

</td><td>

1.  Select the **Users** tab.
2.  Determine which people are using detected services the most by checking their **Events** count.
3.  View detailed information, including detected services they've used by selecting the user name.
 **Note:** Activity that can't be matched to a known person, typically from a personal device or a shared machine, appears under a single **Unknown user** entry instead of being dropped, with fields like email, role, and department left blank. Unknown user activity likely indicates a coverage finding rather than a usage finding.

</td></tr><tr><td id="d91197e236">

**Departments**

</td><td>

1.  Select the **Departments** tab.
2.  Determine which departments carry the most exposure by checking for high event counts across several services.
3.  Select a row to see the services used by people in that department, who's using them, and when they were last active.


</td></tr></tbody>
</table>
## What to do next

Analyze a specific service in more detail. See [Investigating a detected AI service in Shadow AI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/sh-ai-investigating-detected-services.md).

**Parent Topic:**[Assessing AI exposure](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/sh-ai-assessing-ai-exposure.md)

