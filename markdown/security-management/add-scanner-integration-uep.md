---
title: Configure a scanner integration using the unified exposure pipeline
description: For a scanner, normalize assets, labels, and detections into one consistent format before this data reaches Unified Security Exposure Management.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/security-management/add-scanner-integration-uep.html
release: australia
topic_type: task
last_updated: "2026-10-18"
reading_time_minutes: 1
breadcrumb: [Manage Unified Security Exposure Management integrations, Integrate, Unified Security Exposure Management, Security Operations]
---

# Configure a scanner integration using the unified exposure pipeline

For a scanner, normalize assets, labels, and detections into one consistent format before this data reaches Unified Security Exposure Management.

## Before you begin

**Important:** Both standard scanner integration applications and centralized scanner integrations can't be configured in an instance. You must disable all standard scanner integrations and clear their data before using the unified exposure pipeline.

Role required: admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Security Exposure Management** &gt; **Administration**.

2.  In the **Integrations** tab, select **Add Integration**.

3.  Select a supported scanner and select **Proceed to configure**.

4.  In the **Prerequisites** section, review the knowledge base articles for the scanner and complete prerequisite tasks.

5.  In the **Instance setup** section, specify the instance information and credentials.

6.  Select **Save and continue**.

7.  In the **Additional configurations** section, specify the description for the integration instance and any other configuration specific to the scanner.

8.  Select **Save**.

    The integration is ready to be tested.

9.  In the Integration saved dialog box, select **Test connection**.

10. Edit the scanner integration.

    1.  Navigate to the **Integrations** tab.

    2.  Select the scanner and select **Edit**.

    3.  Edit the required information in the **Instance setup** and **Additional configurations** section.

    4.  Test the connection.


