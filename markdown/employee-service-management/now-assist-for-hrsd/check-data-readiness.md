---
title: Check data readiness
description: Review a snapshot of your HR data health to find gaps before you deploy AI agents. The HR Data Readiness Dashboard scores 32 metrics across six readiness areas. Each metric is flagged red, yellow, or green. Use the results to decide what to fix before you configure AI agents.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/employee-service-management/now-assist-for-hrsd/check-data-readiness.html
release: australia
product: Now Assist for HRSD
classification: now-assist-for-hrsd
topic_type: task
last_updated: "2026-10-13"
reading_time_minutes: 4
breadcrumb: [Configure, ServiceNow Otto for HR Service Delivery \(HRSD\), HR Service Delivery, Employee Service Management]
---

# Check data readiness

Review a snapshot of your HR data health to find gaps before you deploy AI agents. The HR Data Readiness Dashboard scores 32 metrics across six readiness areas. Each metric is flagged red, yellow, or green. Use the results to decide what to fix before you configure AI agents.

## Before you begin

Role required: sn\_hr\_ai\_agents.admin

Install ServiceNow Otto for HR Service Delivery \(HRSD\) \[sn\_hr\_gen\_ai\] and AI Agents for HR Service Delivery \[sn\_hr\_ai\_agents\]: [Install AI for HR Service Delivery plugins](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/now-assist-for-hrsd/install-ai-hrsd-plugins.md)

Limit the KB and Content Readiness checks to HR knowledge articles: [Scope KB readiness checks to HR knowledge](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/now-assist-for-hrsd/scope-kb-readiness-checks.md)

## About this task

The HR Data Readiness Dashboard checks whether your HR data is ready for AI agents. Use it before you scope and configure AI agents for HR Service Delivery.

AI agents depend on reliable, well-annotated data. For example, an agent that categorizes a case into an HR service needs enough case data for each service to perform as expected. The dashboard measures this and other prerequisites in one view.

## Procedure

1.  Execute the HR data readiness check script from either the **Readiness Dashboard** or by selecting the **Run Readiness Check** menu option.

<table id="table_emg_jm5_w2c"><thead><tr><th>

To

</th><th>

Do this

</th></tr></thead><tbody><tr><td>

Execute from **Readiness Dashboard**

</td><td>

1.  Go to **All** &gt; **HR Data Readiness Dashboard** &gt; **Readiness Dashboard**.
2.  Select **Regenerate Snapshot**.

The dashboard confirms that snapshot generation has been queued.

3.  When the script finishes running, reload the browser window to see the refreshed data.


</td></tr><tr><td>

Execute with the **Run Readiness Check** menu option

</td><td>

1.  Go to **All** &gt; **HR Data Readiness Dashboard** &gt; **Run Readiness Check**.
2.  Select **Execute Now**.
3.  When the script finishes running, navigate to **All** &gt; **HR Data Readiness Dashboard** to see the data.


</td></tr></tbody>
</table>    The run parses case, knowledge, and configuration data. Larger instances take longer to finish.

2.  Review the Flag for value gate bars at the top.

    \[Omitted image "hr-dashboard-flag-for-value.png"\] Alt text: Flag for value gate bars

    -   Green: ready
    -   Yellow: needs validation or enrichment
    -   Red: needs remediation before agents go live
3.  Review the Remediation backlog.

    This ranked list shows the red metrics that need the most attention.

4.  Review the Case Reason Clustering panel to find where an AI agent can deflect the most cases.

    The panel groups cases from the last 12 months by HR service and by the reason the employee contacted HR. It also shows the share of cases an LLM judge rated as high automation potential.

    1.  Select **View case reason clusters**.

    2.  Expand an HR service to see its clusters.

        Each cluster shows its case count, its share of the service, the judge’s confidence, and an automation rating.

    3.  Identify the clusters with the highest case volume and deflection potential.

        For example, in the Payroll Discrepancy service, the “Payroll and leave discrepancies” cluster has 333 cases. That is 80% of the service, which makes it a strong candidate for an AI agent.

    4.  To review examples, select **View the cases** for a cluster.

5.  Expand each of the six sections to review its metrics.

    |Section|What it shows|Why it's important|
    |-------|-------------|------------------|
    |Operational Baseline|Case volume and distribution over the past year and across services|Agents need enough historical case data for each HR service to categorize and route cases accurately. Low or uneven volume reduces agent accuracy.|
    |Knowledge Base &amp; Content Readiness|Knowledge article quality and freshness|Agents rely on knowledge articles to answer employee questions. Outdated or poorly formatted articles lead to wrong or missing answers.|
    |Platform &amp; Technical Readiness|Whether technical prerequisites for AI agents are in place|Agents can’t run or reach HR data until these prerequisites are met. Finding gaps early avoids delays during configuration.|
    |Self-Service &amp; Portal Adoption|Self-service cases compared with cases logged on a requester’s behalf|Cases that employees submit themselves reflect how they describe their own needs. Agents learn from this data, so a low self-service share limits what they can learn.|
    |Measurement &amp; Analytics Maturity|Whether you can measure outcomes after an agent goes live|Without reliable measurement, you can’t show whether agents improve results, such as faster resolution. A baseline before go-live makes later comparison possible.|
    |Table &amp; Schema Health|Customization on out-of-the-box HR tables|Agents read and write case data, so customization can interfere with them. Child tables, custom fields, and business rules that change fields can conflict with agent behavior. Checking the tables confirms that agents can record their activity.|

    To learn what a metric measures, hover over the question icon.\[Omitted image "hr-dashboard-icon.png"\] Alt text:

    Some metrics, such as misrouting rate, also support a drill-down view that lists every affected HR service in detail.\[Omitted image "hr-dashboard-more.png"\] Alt text:


-   **[Scope KB readiness checks to HR knowledge](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/now-assist-for-hrsd/scope-kb-readiness-checks.md)**  
Limit the Knowledge Base and Content Readiness checks to HR knowledge articles so the results are faster to generate and more relevant.

**Parent Topic:**[Configure ServiceNow Otto for HR Service Delivery \(HRSD\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/now-assist-for-hrsd/configure-now-assist-hr.md)

