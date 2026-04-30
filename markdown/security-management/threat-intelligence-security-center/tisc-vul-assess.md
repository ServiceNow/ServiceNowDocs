---
title: Create Vulnerability Assessment from a Vulnerability
description: Use this feature to create a vulnerability assessment for a specific vulnerability.
locale: en-US
release: zurich
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2026-03-26"
reading_time_minutes: 1
breadcrumb: [Access Vulnerability Downstream actions, Threat Intelligence Security Center Library, Use, Threat Intelligence Security Center, Security Operations]
---

# Create Vulnerability Assessment from a Vulnerability

Use this feature to create a vulnerability assessment for a specific vulnerability.

## Before you begin

Role required: sn\_sec\_tisc.analyst

## About this task

Before you begin, ensure the following:

-   The Vulnerability Exposure Assessment application is installed.
-   The required role `sn_vul_analyst.emergency_response` is assigned.

    **Note:** This role isn't assigned by default. System administrators must explicitly grant access.


## Procedure

1.  Navigate to **Workspaces** &gt; **Threat Intelligence Security Center**.

2.  Select the **Threat Intel Library** icon on the workspace.

3.  Go to **Vulnerability Artifacts** &gt; **All Vulnerabilities**.

4.  Open a vulnerability record.

5.  Select **Create Vulnerability Assessment**.

    ![Create Vulnerability Assessment dialog with Title and Primary CVE fields.](../image/tisc-create-vul-assessment.png)

6.  Fill in the required details such as **Title** and **Primary CVE**.

7.  Select **Submit**.

    A confirmation message appears indicating that Vulnerability assessment \{\*\*\*\*\*\*\*\*\} created successfully.

    **Note:**

    -   When you click the link from the confirmation message, the Vulnerability assessment record opens in read-only mode. The record includes a reference to the originating vulnerability, and relevant fields are automatically populated to maintain consistency.
    -   A corresponding work note is also added to the vulnerability record. To view it, navigate to the **Details** section and view the **Activity** stream.

## Result

**Verify your assessments**

1.  Navigate to the **Internal Intelligence** section on the Vulnerability record.
2.  View all associated vulnerability assessments under the **Vulnerability Response** section.

    ![Vulnerability Assessments list showing assessment details in the Internal Intelligence tab.](../image/tisc-view-vul-assessments.png)

3.  Link or unlink existing assessments as needed.

**Parent Topic:**[Access Vulnerability Downstream actions](../concept/downstream-actions-from-the-vulnerability-form-view.md)

