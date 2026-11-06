---
title: Test and activate the AIOps AI Specialist
description: Run the AI Specialist with a real alert to preview its output before it goes live as an active member of your NOC team.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-operations-management/test-activate-ai-specialist.html
release: australia
topic_type: task
last_updated: "2026-10-18"
reading_time_minutes: 2
keywords: [test, activate AI specialist, AI specialist, AIOps, NOC]
breadcrumb: [Onboard the AIOps specialist, AIOps AI Specialist, ITOM AIOps specialists, AI in ITOM AIOps, ITOM AIOps, IT Operations Management]
---

# Test and activate the AIOps AI Specialist

Run the AI Specialist with a real alert to preview its output before it goes live as an active member of your NOC team.

## Before you begin

-   the AIOps Specialist has completed the onboarding. See [Onboard the AIOps specialist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/onboard-ai-specialist.md).
-   At least one alert available that matches the configured scope.
-   Role required: evt\_mgmt\_admin or evt\_aiops\_manager

## Procedure

1.  On the AIOps AI Specialist page, select the **Test** tab.

    The test panel opens.

2.  Select a single alert from your environment to run the test against.

    **Tip:** Choose an alert that falls within the scope you configured. This gives you the most representative output. Test against an alert type that your team considers representative, not the easiest case. If the AI performs well on a typical, moderately complex alert, you can be confident in its day-to-day output.

3.  Select **Run**.

    The AI Specialist processes the alert and returns its findings.

    \[Omitted image "ai-specialist-test-actions-taken-tab.png"\] Alt text: Action taken tab shows the full output generated across all steps for testing the alert.

    \[Omitted image "ai-specialist-test-alert-insights-tab.png"\] Alt text: Alert insights tab with an overview of the detected issue, probable cause, and recommended next steps.

4.  Evaluate the quality of the output.

    If the output is not what you expected, go back and adjust the scope or module configuration, then run the test again. You can repeat the test as many times as needed.

5.  Select **Save**.

6.  When you're satisfied with the results, select **Add to team**.


## Result

The AI Specialist is active and immediately starts receiving alerts that match its configured scope. Monitor its workload, queue, and performance in the [AI Specialist dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/ai-specialist-dashboard-metrics.md) in the **AI supervising** tab.

To pause the AI Specialist, deactivate it from its profile page. Your configuration is still preserved. For more information, see [Deactivate the AIOps AI Specialist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/deactivate-ai-specialist.md).

**Parent Topic:**[Onboard the AIOps specialist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/onboard-ai-specialist.md)

