---
title: Configure Team Dev scanning properties
description: You can view and configure a variety of information, formatted into lists, that the Scan Engine uses to permit users, team leads, and admins to access content.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/impact/teamdev-scanning-properties.html
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure Scan Engine properties, Activate Scan Engine and review settings, Run Impact Guided Setup, Configuring Impact, Impact]
---

# Configure Team Dev scanning properties

You can view and configure a variety of information, formatted into lists, that the Scan Engine uses to permit users, team leads, and admins to access content.

## Team Development scanning properties

You can specify whether to scan Team Development code pushes that are pending a review, whether to approve or reject those pushes automatically, and whether developers can use Suite scans for applications.

To configure these properties, navigate to **ALL** &gt; **Impact** &gt; **Configuration** &gt; **Scan Engine Properties**, and then select the **Team Dev Scanning** tab.

If you use Team Development as a method for pushing code, the Scan Engine can be used to scan code pushes that are pending a code review. You scan these pushes for findings, and you can choose to approve or reject code reviews automatically.

**Note:** Code reviews must be enabled for Team Development scanning to work properly. Additionally, admins must perform a one-time API configuration to enable Team Development scanning. For more information, refer to [Register your instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/impact/register-your-instance.md).

Properties include:

-   **Automatically scan pushes pending Code Review** \(`auto_scan_team_dev_pushes`\)
-   **Automatically approve or reject pushes** \(`team_dev_auto_approve`\). This option becomes available after you select **Automatically scan pushes pending Code Review**.
-   **Allow Suite scanning for Applications**. When selected, developers can choose between a Full scan and a Suite scan. A Suite scan runs only selected definitions for faster validation. A Full scan runs all active definitions. When cleared, only Full scans are available.

## Team leads

To define teams and team leads that can view the Team Lead information in the Analytics Dashboard, refer to [Create a development team](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/impact/create-development-team.md).

-   **[Create a development team](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/impact/create-development-team.md)**  
Each record represents a team and a development team lead. Scan Engine findings are reported for this team in the Analytics Dashboard.

**Parent Topic:**[Configure Scan Engine properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/impact/configure-scan-engine-properties.md)

