---
title: Now Assist Readiness Evaluation system properties
description: Use system properties to customize your readiness assessment results. Access these properties from the System Property \[sys\_properties\] table.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2026-01-05"
reading_time_minutes: 1
keywords: [Now Assist Readiness Evaluation, Now Assist Readiness Evaluation app, Now Assist Readiness, Now Assist assessment, GenAI assessment, AI assessment, Agentic AI assessment]
breadcrumb: [Reference, Now Assist Readiness Evaluation, Enable AI experiences]
---

# Now Assist Readiness Evaluation system properties

Use system properties to customize your readiness assessment results. Access these properties from the System Property \[sys\_properties\] table.

<table id="table_x43_5b2_hgc"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_assess.assessment\_limit

</td><td>

Reduce performance issues when a large volume of data is assessed. Adjust this system property, if needed, so that the job can run successfully. The default value is `10000`.

</td></tr><tr><td>

sn\_assess.effort\_visibility

</td><td>

Customize the estimated remediation effort for select efforts. This property controls multiple sections associated with remediation effort. The default value is `false`. When this system property is set to `true`, the **Remediation properties** tab appears on the Now Assist Readiness Evaluation dashboard. You customize the estimated remediation efforts via the **Remediation properties** tab. All input values represent estimated remediation efforts in days. After making changes to the estimated remediation efforts, select **Save**, and then re-run the assessments to see the updated remediation efforts reflected.

</td></tr><tr><td>

sn\_assess.task\_limit

</td><td>

Decide the maximum number of records to process for the ITSM assessment. The default value is `50`. Be cautious of setting a higher limit or leaving the value empty since that would fetch all active records which could impact performance.

</td></tr></tbody>
</table>