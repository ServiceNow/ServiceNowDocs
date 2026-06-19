---
title: Manually submit files or URLs to Sandbox
description: You can manually submit a file or URL to a sandbox when certain incident criteria, such as category is phishing, are met.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/security-incident-response/submit-files-or-urls-to-sandbox.html
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [CrowdStrike Falcon X Sandbox integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Manually submit files or URLs to Sandbox

You can manually submit a file or URL to a sandbox when certain incident criteria, such as category is phishing, are met.

## Before you begin

Role required: sn\_si.analyst

## About this task

After reviewing the security incident and the file or URL, you can select the **Submit to Sandbox** option to perform a malware analysis.

## Procedure

1.  Navigate to **All** &gt; **Security Incident** &gt; **Incidents** &gt; **Show All Incidents** and open a security incident to which you want to submit a file or URL observable type record.

2.  Select the **Show IoC** related link.

3.  On the **Observables** tab, select a record or multiple records for which you want to perform malware or threat analysis and select **Submit to Sandbox**.

    \[Omitted image "submit-to-sandbox.png"\] Alt text: Submit to sandbox for malware analysis.

4.  When the File Submission filter appears, select your preferred sandbox configuration in **Submission configuration**, and select **Submit to Sandbox**.

    \[Omitted image "observable-submission-sandbox.png"\] Alt text: Filter and submit files to the sandbox.

5.  Select **Additional runtime options** if you want to provide further custom options.

    \[Omitted image "observable-submission-dialog-box.png"\] Alt text: File submission with additional runtime options.

    |Field|Description|
    |-----|-----------|
    |Custom commandline|Regular application command line or a special operation.|
    |System date|System date in yyyy-MM-dd format.|
    |System time|System time in HH:mm format.|

    After you initiate the submission, you can view the Work notes to see the status of your submission. For further information on the status of the submission or to analyze the results, view the **Sandbox Submission Results**.

    **Note:** In CrowdStrike Falcon X Sandbox, quick scan isn’t supported for URLs. If the work notes has too much information, you can use the Filter option to drill down to the required work notes that is relevant to you.


## What to do next

When you submit the observables to the sandbox for malware analysis, [view the sandbox submission results](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/view-sandbox-submission-results.md) to take the next steps on potential threats.

