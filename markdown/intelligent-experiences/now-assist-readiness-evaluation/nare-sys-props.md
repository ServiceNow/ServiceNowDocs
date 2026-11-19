---
title: AI Readiness Evaluation system properties
description: Use system properties to customize your readiness assessment results. Access these properties from the System Property \[sys\_properties\] table.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/now-assist-readiness-evaluation/nare-sys-props.html
release: zurich
product: Now Assist Readiness Evaluation
classification: now-assist-readiness-evaluation
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [Now Assist Readiness Evaluation, Now Assist Readiness Evaluation app, Now Assist Readiness, Now Assist assessment, GenAI assessment, AI assessment, Agentic AI assessment]
breadcrumb: [Reference, AI Readiness Evaluation, Enable AI experiences]
---

# AI Readiness Evaluation system properties

Use system properties to customize your readiness assessment results. Access these properties from the System Property \[sys\_properties\] table.

<table id="table_x43_5b2_hgc"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_assess.assessment\_limit

</td><td>

Reduce performance issues when a large volume of data is assessed. Adjust this system property, if needed, so that the job can run successfully. The default value is 10000.

</td></tr><tr><td>

sn\_assess.effort\_visibility

</td><td>

Control whether remediation effort estimates appear on the AI Readiness Evaluation.The default value is false. When this system property is set to **true**, both assessment tabs display effort cards and finding cards. The **Remediation properties** tab appears on the dashboard where you can customize estimated remediation efforts. All input values represent estimated remediation efforts in days. After making changes to the estimated remediation efforts, select **Save**, and then re-run the assessments to see the updated remediation efforts reflected.

</td></tr><tr><td>

sn\_assess.va

</td><td>

Enables or disables the scheduled job for the AI Assessment - Virtual Agent. Set to **true** to enable, or **false** to disable. The default value is true. If set to **false**, the scheduled job will not run and no Virtual Agent assessment data will be generated. For the Virtual Agent assessment to run, the following prerequisites must all be met: -   Virtual Agent \(com.glide.cs.chatbot\) must be enabled on the instance.
-   Catalog Conversational Coverage \(sn\_catalog\_con\_cov\) must be active. This plugin is installed with ServiceNow Otto for Conversational Catalog Request \(sn\_now\_assist\_cr\), which is included with ServiceNow Otto for Platform \(sn\_genai\_platform\).

</td></tr><tr><td>

sn\_assess.itsm

</td><td>

Enables or disables the scheduled job for the AI Assessment - ITSM. The default value is true. If set to **false**, the scheduled job will not run and no ITSM assessment data will be generated.

</td></tr><tr><td>

sn\_assess.csm

</td><td>

Enables or disables the scheduled job for the AI Assessment - CSM. The default value is true. If set to **false**, the scheduled job will not run and no CSM assessment data will be generated.

</td></tr><tr><td>

sn\_assess.hrsd

</td><td>

Enables or disables the scheduled job for the AI Assessment - HRSD. The default value is true. If set to **false** the scheduled job will not run and no HRSD assessment data will be generated.

</td></tr><tr><td>

sn\_assess.ai\_search

</td><td>

Enables or disables the scheduled job for the AI Assessment - AI Search. The default value is true. If set to **false**, the scheduled job will not run and no AI Search assessment data will be generated.

</td></tr><tr><td>

sn\_assess.Threshold

</td><td>

Defines the percentage threshold used to evaluate assessment results on the AI Readiness Evaluation home page, determining whether the status is displayed as Good or Action Required. The default value is 75% for all modules \(ITSM, AI Search, CSM, Virtual Agent, and HRSD\). If not set correctly, status indicators may be inaccurate.

</td></tr><tr><td>

sn\_assess.TShirtMetric

</td><td>

Assigns numeric effort values to specific issue types and customizations, which power the remediation effort calculations displayed throughout the application. The default value is a JSON configuration. If modified, effort calculations will reflect updated values after the next assessment run. Review sn\_assess.TShirtSize at the same time — if the two are out of sync, displayed effort estimates can may be inconsistent. If this property is not set, the system can't calculate remediation effort.

</td></tr><tr><td>

sn\_assess.TShirtSize

</td><td>

Maps T-shirt size labels to effort in days. The default values are: Small = 5 days, Medium = 10 days,Large = 30 days, XL = 90 days, and XXL = 180 days. These mappings appear in effort pills and the Legends in the AI Readiness Evaluation dashboard. Review sn\_assess.TShirtMetric at the same time when customizing. If not set correctly, effort pills will not display accurate effort in days and the Legends may show incorrect or missing information.

</td></tr><tr><td>

sn\_assess.task\_limit

</td><td>

Decides the maximum number of records to process for the ITSM assessment. The default value is 50. Be cautious about setting a higher limit or leaving the value empty because that would fetch all active records which could impact performance.

</td></tr></tbody>
</table>