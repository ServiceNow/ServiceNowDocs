---
title: Submit to Zscaler Sandbox analysis
description: Use the Zscaler Internet Access products sandbox service to analyzes files in a virtual environment to detect malicious behavior.
locale: en-US
release: xanadu
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Security Incident Response integration with Zscaler, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Submit to Zscaler Sandbox analysis

Use the Zscaler Internet Access products sandbox service to analyzes files in a virtual environment to detect malicious behavior.

## Before you begin

Role required: sn\_si.admin

## About this task

When you create a Zscaler configuration, a Zscaler sandbox submission is created by default in the Zscaler Sandbox Configuration module.

The name and source fields are auto-filled, and the configuration is enabled by default. You can edit only the display tag and the active options. Zscaler Internet Access product enables you to fetch only the sandbox report for the MD5 hash type observables.

The analysis for the file that is associated with the MD5 hash should be complete and the corresponding report should be in the Zscaler sandbox. If the MD5 hash that you send does not have a report in Zscaler, you get an error message.

![Pre-filled sandbox submission configuration record.](../image/zscaler-sandbox-submission.png "Zscaler Sandbox Submission")

## Procedure

1.  Navigate to **All** &gt; **Security Incident** &gt; **Incidents** &gt; **Show All Incidents**.

2.  Select the security incident that you want to run the sandbox analysis on.

3.  Click **Show All Related Lists** and the **Associated Observables** tab.

4.  Select an MD5 hash type observable and then from the Actions menu, select **Submit to Sandbox**.

    Create an MD5 hash type observable if you do not find an existing MD5 hash type observable.

5.  In the File Submission dialog box, select the **Zscaler - Sandbox Submission - Server** option in the Submission configuration and click **Submit to sandbox**.

    After you initiate the sandbox submission, you can view the Work notes to see the status of your submission. A tag is also appended to the security incident.

6.  In the Work notes, click the link in the Sandbox Submission Result post.


## Result

You can also view the results from the Show All Related Lists and Sandbox Submission Results tab.

