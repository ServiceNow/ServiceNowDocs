---
title: Instance Security Center to ServiceNow Security Center migration
description: Learn the key differences when migrating from Instance Security Center \(ISC\) to ServiceNow Security Center \(SSC\).
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Instance Security Center, Platform Security]
---

# Instance Security Center to ServiceNow Security Center migration

Learn the key differences when migrating from Instance Security Center \(ISC\) to ServiceNow Security Center \(SSC\).

**Important:**

Instance Security Center is a legacy product that will reach the end of sales by September 2024. ServiceNow Security Center is the recommended solution for customers to adopt going forward. For more information, see the [deprecation process](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0867184) article \(KB0867184\) in the Now Support knowledge base.

ServiceNow Security Center \(SSC\) is a security application that consists of a set of purpose-built tools designed to help organizations maintain the security of their ServiceNow deployments. Using SSC, organizations can improve their security posture, strengthen their compliance levels, and do so with a seamless user experience.

Use this document to learn about SSC enhancements in functionality and how to execute tasks in SSC that were previously done in ISC.

## Security hardening

<table id="table_lnh_hx3_1cc"><thead><tr><th>

Feature enhancements

</th><th>

ISC vs SSC

</th></tr></thead><tbody><tr><td>

User interaction updates

</td><td>

-   Review latest score by navigating to the Overview or hardening comparison page.
-   Manually update latest score by navigating to Overview and selecting update score.
-   Change setting configuration by selecting a setting name link on any of these pages and then make edits on the **Settings detail** page:
    -   Overview
    -   **Hardening** &gt; **All settings**
    -   **Hardening** &gt; **Comparison**

</td></tr><tr><td>

Set a schedule for to recalculate your compliance score

</td><td>

Using SSC, you can set when the system triggers a refresh of your compliance score.1.  Navigate to the Scheduled Script Executions \[sysauto\_script\] table.
2.  Find and open the `SC - Calculate Compliance Monthly` record.
3.  Use the **Run**, **Day**, **Time zone**, and **Time** fields to set your preferred schedule. ![Fields used to configure compliance calculation schedule](../images/compliance-schedule.png)
4.  Select **Update** to save your changes.

</td></tr></tbody>
</table>## Security KPIs and metrics

<table id="table_esd_b1j_1cc"><thead><tr><th>

Feature enhancements

</th><th>

ISC vs SSC

</th></tr></thead><tbody><tr><td>

Enhancements to KPIs

</td><td>

Using SSC, you can:-   See the trend of the score over time.
-   Monitor all KPIs and metrics using the same interface and analytical capabilities.

</td></tr><tr><td>

Enhancements to metrics

</td><td>

SSC includes these metrics enhancements:-   Over 65 metrics have been added.
-   Monitor and analyze KPIs and metrics from a single user interface.
-   Create targets and thresholds for metrics.

</td></tr><tr><td>

User interaction updates

</td><td>

Access Metrics in SSC by navigating to **Overview** &gt; **Metrics**, and then selecting metric from the navigation menu. Alternatively, you can navigate to **All metrics**.

</td></tr></tbody>
</table>## Security scanner

<table id="table_ayw_lcj_1cc"><thead><tr><th>

Feature enhancements

</th><th>

ISC vs SSC

</th></tr></thead><tbody><tr><td>

New functionality

</td><td>

SSC includes these functions:-   Manually execute scans or schedule them to run at specific times.
-   Create your own scan checks.
-   Create your own scan suite.
-   Compare the results of two scans.

</td></tr><tr><td>

Enhanced email functionality

</td><td>

Set up email notifications to stay informed about security events on your instance.

</td></tr><tr><td>

User interaction updates

</td><td>

-   Run the Auditor scan by navigating to **Overview** &gt; **Scan** &gt; **Suites** and selecting **Auditor suite** from the list.
-   See scan results by navigating to **Overview** &gt; **Scan** &gt; **Results**.

</td></tr></tbody>
</table>## Additional security features

<table id="table_t1z_zdj_1cc"><thead><tr><th>

Feature enhancements

</th><th>

ISC vs SSC

</th></tr></thead><tbody><tr><td>

Monitor sessions functionality

</td><td>

-   Visualize session activities using the [Analytics Hub](https://www.servicenow.com/docs/access?context=c_UsePerformanceAnalyticsScorecards&version=australia&pubname=australia-now-intelligence&ft:locale=en-US).
-   Monitor session activity by navigating to **Metrics** &gt; **Sessions**.

</td></tr><tr><td>

Find resources

</td><td>

Access all learning resources in a single page at **Overview** &gt; **Learning**.

</td></tr></tbody>
</table>## Opt out of Security Center features

To disable Security Center features on your instance, follow the steps provided in [KB1702514: Guidelines to disable Instance Security Center components \(while using Security Center\)](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1702514).

**Parent Topic:**[Instance Security Center](../../security/concept/instance-security-center.md)

**Related topics**  


[Monitor security events](../../security/concept/instance-sec-center-event-ribbon.md)

[Check the daily compliance score and configure security property settings](../../security/concept/instance-sec-center-hardening.md)

[Scan for incorrect security definitions](../../security/concept/scan-for-incorrect-security-definitions.md)

[Monitor instance metrics](../../security/concept/monitoring-user-email-antivirus-metrics.md)

[Activate the ISC Virtual Agent interface](../../security/task/activating-virtual-agent-interface.md)

