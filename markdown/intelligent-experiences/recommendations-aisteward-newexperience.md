---
title: Recommendations for your AI assets
description: Recommendations for AI assets are automatically generated for you to review and act on.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/recommendations-aisteward-newexperience.html
release: australia
topic_type: concept
last_updated: "2026-07-17"
reading_time_minutes: 2
keywords: [recommendation, Top action items, asset record]
breadcrumb: [Reviewing AI asset status, Working with AI asset records, Discover and manage AI assets, AI Control Tower, Enable AI experiences]
---

# Recommendations for your AI assets

Recommendations for AI assets are automatically generated for you to review and act on.

## Overview of recommendations

Recommendations are automatically generated so that you can identify and address issues before they escalate, without the need for manual monitoring. You can view these recommendations only if you have the AI steward \[sn\_ai\_governance\_ai\_steward\] or AI asset owner \[sn\_ai\_asset\_mgmt.ai\_asset\_owner\] role.

AI Control Tower checks for a range of conditions on your assets on a schedule that varies by recommendation type, giving you a current view of which assets need attention and why.

Recommendations include, but aren't limited to, the following:

-   Activities with no tasks: When an active life-cycle playbook activity is in an onboarding or offboarding phase but has no tasks linked to it, a recommendation is generated. This alerts you that work must be assigned before progress can continue.
-   Activities ready to be marked as complete: When every child task under an activity is complete but the activity itself is still open, a recommendation is generated. This keeps your life-cycle stages from stalling in an open state when the real work is already done.
-   A missing or incomplete asset description.
-   An asset that has been dormant long enough to be a candidate for retirement.

For the complete picture of how recommendations are generated, prioritized, and resolved across all categories, see [Recommendations and AI insights](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/aict-recommendations-ai-insights.md).

## Viewing recommendations

You can view recommendations in the following locations:

-   AI Control Tower Home page: In the **Top action items** widget.
-   Asset record page: In the **Needs attention** section on the **Overview** tab, under the **Recommendations** sub-tab. Select **See all Recommendations in Activity Center** to open the full list.
-   Activity Center: On the **Recommendations** page.

Select a recommendation to review the reasoning behind it and the asset it applies to.

To resolve a recommendation, use the primary resolution action it offers; for the full procedure, see [Resolve an AI recommendation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ac-resolve-ai-recommendation.md).

**Parent Topic:**[Reviewing AI asset status](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/reviewing-ai-asset-status.md)

