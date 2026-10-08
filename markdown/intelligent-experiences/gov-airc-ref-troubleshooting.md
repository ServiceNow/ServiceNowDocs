---
title: Risk score and compliance score dashboard errors
description: Properties and scheduled jobs that resolve No data found errors in the risk score and compliance score dashboards on the AI asset record and landing pages.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/gov-airc-ref-troubleshooting.html
release: australia
topic_type: reference
last_updated: "2026-10-05"
reading_time_minutes: 1
keywords: [troubleshooting, No data found, risk score, compliance score, scheduled jobs, AI Risk and Compliance]
breadcrumb: [Reference, Managing risk and compliance, Govern AI assets, AI Control Tower, Enable AI experiences]
---

# Risk score and compliance score dashboard errors

Properties and scheduled jobs that resolve `No data found` errors in the risk score and compliance score dashboards on the AI asset record and landing pages.

## No data found errors

A `No data found` error can appear in the Risk and Compliance dashboards on the AI asset record page or the landing page. To resolve the error, an administrator must complete the following actions for the score that doesn't appear. If the error persists, create a case on the Now Support portal for further investigation.

The following table lists the actions to complete, in order, for each score.

|Score that doesn't appear|Order|Action|Location|
|-------------------------|-----|------|--------|
|Risk score|1|Set the **Migrate to Advanced Risk Assessments** property to **Yes**.|**All** &gt; **Advanced Risk assessment** &gt; **Administration** &gt; **Properties**|
|Risk score|2|Run the **GRC rollup assessment scores** scheduled job.|**All** &gt; **System Definition** &gt; **Scheduled Jobs**|
|Risk score|3|Run the **AI inventory risk score rollup** scheduled job.|**All** &gt; **System Definition** &gt; **Scheduled Jobs**|
|Compliance score on the landing page|1|Run the **AIRC daily compliance score scheduled job**.|**All** &gt; **System Definition** &gt; **Scheduled Jobs**|
|Compliance score of an AI system|1|Run the **Compliance Score V2** scheduled job.|**All** &gt; **System Definition** &gt; **Scheduled Jobs**|
|Compliance score of an AI system|2|Run the **AI system Compliance score calculation** scheduled job.|**All** &gt; **System Definition** &gt; **Scheduled Jobs**|

**Note:**

On the Advanced Risk Assessment Properties page, a banner can state that the record is in the GRC: Advanced Risk application while another application is current. To edit the property, select the link in the banner.

