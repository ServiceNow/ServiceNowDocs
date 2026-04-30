---
title: Automate CrowdStrike Falcon Sandbox submissions using Flow Designer
description: The CrowdStrike Falcon X Sandbox integration includes flow templates created using the Workflow Studio that work with security incident records.
locale: en-US
release: yokohama
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [CrowdStrike Falcon X Sandbox integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Automate CrowdStrike Falcon Sandbox submissions using Flow Designer

The CrowdStrike Falcon X Sandbox integration includes flow templates created using the Workflow Studio that work with security incident records.

## Before you begin

-   Verify that you have created a [Sandbox submission configuration](setup-sandbox-submission-configurations.md) and have enabled one configuration as the **Default configuration for automated submission**. When the flow is triggered, the sandbox submission occurs on your default configuration.

Role required: sn\_si.admin

## About this task

These flows are primarily designed to get you started when you want to automate file or URL submissions as part of your incident response workflow.

When you activate a sample flow, your phishing file attachments are automatically submitted if you define the security incidents as phishing in your sample flow. Alternatively, you can submit all .exe files when this file type is attached to an observable record.

You can modify these sample flows to trigger an automated submission under different conditions, categories, compound conditions, and so on.

The sandbox integration consists of two base system flows that are deactivated by default.

-   **Submit file when category is phishing**: This flow submits a file to the sandbox for malware analysis when the security incident category is defined as phishing. You must attach a file to the observable record on the security incident. If you are using the User Reported Phishing \(URP\) functionality, any email attachment is automatically parsed and added to the SIR incident record as an observable record. No further action is required to automate the submission.
-   **Submit when file type for observable is exe**: This flow submits a file to the sandbox for malware analysis when the security incident observable is an exe. Similar to the phishing category flow, a you must attach a file to an observable record on the security incident. You can do this manually by uploading the file or automatically if a phishing email attachment, or other mechanism that is creating the incident, is associated with the observable records.

When the flows are configured and incident conditions satisfy the parameters, the sandbox submissions trigger automatically when you review the security incident. Review the Work note that indicates that a submission has been initiated, a tag appears if enabled in the configuration, and a pending submission results record.

The sandbox integration also contains multiple subflows. The subflows are internal components of the overall integration submission capabilities. You can customize and edit the subflows to suit your security criteria.

You can refer the subflows to troubleshoot issues with sandbox submissions. An Execution record is created every time you invoke a subflow. This record indicates where in the flow a particular error occurred and enables you to fix the problem.

![The sandbox integration contains multiple subflows.](../image/subflows.png "Sandbox Integration- Multiple workflows")

**Note:**

-   If you choose to customize the default flows, then you should verify that the Submit Observable for Automated submission subflow is included in your flow to trigger automatic submissions.
-   You can customize and define your file extensions for an exe. Create a copy of the flow **Submit when file type for observable is exe**, and make changes to the copy. The content type and file extensions are mapped in the SandboxUtils script. To access script includes, navigate to **System Definitions &gt; Script Includes** and search for SandboxUtils.

    ![Access and modify the SandboxUtils script.](../image/sandboxutils.png "SandboxUtils script")


## Procedure

1.  Navigate to **All** &gt; **Flow Designer** &gt; **Designer** &gt; **Flows**.

2.  Filter the flows by the **Application** type.

    For example, \*crowd filters the two CrowdStrike Falcon X Sandbox flows.

    ![Sandbox integration provides two default flows.](../image/flow-designer.png)

3.  Select a flow to view the details.

    The example below shows the Submit file when category is phishing flow.

    ![Activate the base system flow or customize your flow.](../image/flow-activate.png)

4.  Click **Activate** and then click **OK** when the confirmation message appears.


## What to do next

After you configure automated submission flows, you can [View the sandbox submission results](view-sandbox-submission-results.md) to analyze any threats.

