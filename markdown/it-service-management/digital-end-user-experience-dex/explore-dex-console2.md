---
title: Exploring Digital End-User Experience
description: The Digital End-User Experience \(DEX\) suite offers proactive visibility to help you understand and improve the end-user experience across your organization. It includes Application and Device Health, DEX Content Playbook, Desktop Assistant, Digital Experience Score​, and Proactive Engagement to provide unique benefits to diagnose and address negative experiences.
locale: en-US
release: yokohama
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 6
breadcrumb: [Digital End-User Experience, IT Service Management]
---

# Exploring Digital End-User Experience

The Digital End-User Experience \(DEX\) suite offers proactive visibility to help you understand and improve the end-user experience across your organization. It includes Application and Device Health, DEX Content Playbook, Desktop Assistant, Digital Experience Score​, and Proactive Engagement to provide unique benefits to diagnose and address negative experiences.

## Digital End-User Experience overview

The Digital End-User Experience \(DEX\) provides end-to-end visibility into the health of applications, networks, and end-user devices. DEX provides such features as application, user and device navigation, trend analysis, and various useful metrics. With DEX you can identify the root cause of an issue, rather than just treating the symptoms.

## Digital End-User Experience users

For examples of how different people in your organization would use DEX Application and Device Health, see these users and roles.

<table id="table_gvc_l53_dxb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

DEX administrator \[sn\_dex.admin\]

</td><td>

Responsible for managing user access to DEX, managing the applications that are being monitored, and handling onboarding or offboarding-related tasks. They also troubleshoot any issues that arise within the application.

</td><td>

-   sn\_dex.user
-   sn\_dex.engineer
-   agent\_client\_collector\_admin
-   report\_admin

</td></tr><tr><td>

DEX engineer \[sn\_dex.engineer\]

</td><td>

Responsible for accessing and executing the remedial actions.

</td><td>

sn\_dex.user

</td></tr><tr><td>

DEX user \[sn\_dex.user\]

</td><td>

Responsible for accessing and using the features provided by DEX.

</td><td>

-   dependency\_views
-   agent\_client\_collector\_user
-   sow\_incident\_read
-   mbplus\_reader
-   sam\_user
-   evt\_mgmt\_user

</td></tr><tr><td>

DEX Service Desk agent\[sn\_dex.service\_desk\_user\]

</td><td>

Responsible for L1 or L2 support representatives accessing DEX from the incident platform to explore and investigate the details of the devices linked to the incident.Also responsible for accessing and executing the remedial actions allowed for this role.

</td><td>

Not applicable

</td></tr></tbody>
</table>For examples of how different people in your organization would use Desktop Assistant, see these use cases.

<table id="table_gk2_5vt_mwb"><thead><tr><th>

User

</th><th>

Responsibilities

</th></tr></thead><tbody><tr><td>

Desktop Assistant administrator\[sn\_dex\_desktop.admin\]

</td><td>

Responsible for managing configurations and resolving any issues that might arise within the application.

</td></tr><tr><td>

Desktop Assistant user\[sn\_dex\_desktop.user\]

</td><td>

Responsible for using Desktop Assistant. User can't configure any items within the application.

</td></tr></tbody>
</table>## Digital End-User Experience workflow

Depending on your role, you can use Digital End-User Experience for a variety of scenarios.

![Digital End-User Experience overview](../image/dex-workflow-diagram.png "Digital End-User Experience overview")

## Digital End-User Experience benefits

Having a positive digital experience can lead to numerous benefits, including the following:

-   **Proactive visibility into the end-user experience**

    Gain insights into the digital experience of your application and services from the end-user viewpoint, regardless of their location, device type, or network connectivity. Identify and measure the health of user systems — view what applications and system crashes are happening. All this reliability data is brought together in one central workspace, letting your IT team dive deeper into more detailed data without deploying additional monitors.

-   **Increased productivity**

    Access digital tools and resources easily to troubleshoot IT issues, reset passwords, or access software. This ability can lead to increased productivity by reducing the burden on IT staff. The DEX Content Playbook includes policies and checks for metrics and subsequent actions required for different operating systems.

-   **Issue analysis**

    Identify and analyze issues by providing insights into pain points, usage patterns, performance, and impact. By analyzing DEX data, organizations can identify areas for improvement and make data-driven decisions to enhance the digital workplace experience for their end users.

-   **Performance evaluation**

    Provide insights into the productivity, efficiency, user behavior, and engagement. DEX provides a wealth of device performance and health information. This data can help IT teams understand how a given application is being used and identify areas for improvement.

-   **Enhanced engagement**

    Promote end-user experience and productivity by continuously measuring and monitoring application and device health metrics. Gain end-to-end visibility and insights into the overall user experience and quickly identify users, applications, and devices with poor experiences that need your attention. A positive digital experience helps you to improve end-user engagement leading to increased motivation, better job satisfaction, and lower turnover rates.

-   **Optimized end-user digital experience**

    Empower your employees with Desktop Assistant – a centralized hub that provides a comprehensive view of requests and device health, enables internet connection testing, and offers a usage metrics dashboard for seamless communication with the ServiceNow® instance.


## Better together

-   **[DEX for Service Desk Agents](../../service-operations-workspace/reference/features-of-investigation-tab.md)**

    As a Service Desk agent, navigate to the DEX device health page from the ServiceNow Core UI incident experience or from the Investigate tab within the Incident experience in Service Operations Workspace \(SOW\). Configure a computer Configuration Item \(CI\) and install the DEX plugin for the ability to analyze device metrics from within the platform, getting valuable insights for effective issue investigation.

    Use incident investigation with DEX to review device health, detected issues, and suggested resolutions. Implement resolutions and remedial actions directly from your workspace and monitor the status of actions. For more information, see .

    Use the DEX issue diagnosis and resolution agentic workflow to resolve detected issues with automated root cause analysis, targeted resolution plans, and documentation of resolution summary in incident records. For more information, see [DEX issue diagnosis and resolution agentic workflow](../../now-assist-itsm/concept/now-assist-itsm-dex-diagnosis-resolution-workflow.md).

-   **[Software Asset Management](https://www.servicenow.com/docs/access?context=c_SoftwareAssetMgmt&version=yokohama&pubname=yokohama-it-asset-management&ft:locale=en-US)**

    Unifying the experience of DEX application with Software Asset Management \(SAM\) software enables you to access SAM-normalized software content. This integration provides software metering data from DEX to integrate with SAM for software licensing reclamation and, in turn, reduce software license costs. For more information, see [Using DEX or SAM for application monitoring](using-dex-or-sam-for-app-monitoring.md).


## What to explore next

To learn more about configuring and using Digital End-User Experience, see:

-   [Configure Digital End-User Experience](config-dex-console.md).
-   [Monitor and manage the digital workplace with Digital End-User Experience.](use-dex-console.md)
-   [Use the Desktop Assistant.](use-dex-desktop-exp.md)
-   [Get information about the DEX Workspace administration](../reference/dex-console-reference.md).
-   [Tracking digital experience using Digital Experience Score​ dashboard](../../dex-score/concept/dexscr-using-dex-score.md).

