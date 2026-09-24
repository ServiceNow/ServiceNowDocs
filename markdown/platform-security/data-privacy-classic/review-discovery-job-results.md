---
title: Review default discovery job results
description: After the default discovery job completes, review the findings to understand sensitive data exposure on your instance and plan protective measures.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/data-privacy-classic/review-discovery-job-results.html
release: brazil
product: Data Privacy \(Classic\)
classification: data-privacy-classic
topic_type: task
last_updated: "2026-09-24"
reading_time_minutes: 1
breadcrumb: [Default data discovery job, Default data privacy configurations, Data Privacy, Platform Privacy]
---

# Review default discovery job results

After the default discovery job completes, review the findings to understand sensitive data exposure on your instance and plan protective measures.

## Before you begin

Role required: data\_privacy\_admin

## Procedure

1.  Navigate to the discovery findings in the Data Privacy module.

    Go to **System Security** &gt; **Data Discovery** &gt; **Discovery Findings** \(or access findings from the completed job record\).

2.  Filter findings by the default discovery job.

    1.  If multiple discovery jobs have run, apply a filter to show only results from the default job.

    2.  You can also filter by date range to see results from the most recent job run.

3.  Review the summary statistics for the default job findings.

    1.  Note the total number of records scanned.

    2.  Observe the total number of sensitive data instances detected.

    3.  Identify the breakdown by data type \(credit cards, SSN, email, phone numbers, etc.\).

    4.  Review which tables and fields contained the most sensitive data.

    Summary statistics give you a high-level understanding of your sensitive data exposure.

4.  Examine individual findings in detail.

    1.  Click on specific findings to view the actual record and context of the detected sensitive data.

    2.  Verify that detected data is actually sensitive \(check for false positives\).

    3.  Note the table, field, and record information for each finding.

    4.  Document any unexpected patterns or data sources.

    Detailed review helps you understand the actual sensitive data exposure and assess which areas need protection.

5.  For comprehensive inventory, consider creating a custom discovery job.

    The default discovery job provides a quick sample \(1,000 records or 30 days\). If you need a complete inventory of all sensitive data on your instance, create a custom discovery job with extended scan scope.


