---
title: Monitor the submission results in the sandbox
description: Results for all Sandbox submissions are shown in the Sandbox Submission Results tab for every security incident.
locale: en-US
release: xanadu
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [CrowdStrike Falcon X Sandbox for Security Operations integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Monitor the submission results in the sandbox

Results for all Sandbox submissions are shown in the **Sandbox Submission Results** tab for every security incident.

## Before you begin

Role required: sn\_si.analyst

## Procedure

1.  Open the security incident that you are working with and verify that the sandbox submission is successful.

    ![Review the activities section for successful sandbox submissions.](../../../security-incident-response/image/work-notes.png)

2.  Review the Work notes for more information and learn how to proceed if you can't verify that the scan is successful.

3.  Either click the complete results link in the Work notes or at the bottom of the security incident, navigate to **Show All Related Lists**&gt; **Sandbox Submission Results**.

    Results are displayed in the Sandbox Submission Results tab.

4.  Click open any record to view the complete sandbox analysis.

    ![Review the sandbox submission results.](../image/sandbox-submission-results-new.png)

5.  Click **Resubmit to Sandbox** to reprocess the observable.


## Result

-   The **Threat lookup results** tab provides the threat assessment, including malicious findings, threat scores, and additional details. These details are provided in the standard threat lookup format structure for all ServiceNow threat lookup integrations.
-   The **Indicators of compromise** tab provides the malicious or suspicious sandbox results with the Confidence scores. The Confidence scores are similar to other Indicator information that is stored in the ServiceNow platform. Indicators that are classified as informational are not included in this tab.
-   The external link provides you with a view the Sandbox results in the CrowdStrike Falcon X Sandbox portal.

    **Note:** This option requires that you have the CrowdStrike Falcon X Sandbox role to view the results.


You can also monitor the sandbox submission results for all security incidents by navigating to **CrowdStrike Falcon Sandbox** &gt; **Sandbox Submission Results**.

