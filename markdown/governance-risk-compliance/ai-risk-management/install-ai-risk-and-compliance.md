---
title: Install AI Risk and Compliance
description: You can install the AI Risk and Compliance application \(sn\_grc\_ai\_gov\) if you have the admin role. The application includes demo data and installs related ServiceNow Store applications and plugins if they are not already installed.
locale: en-US
release: australia
product: AI Risk Management
classification: ai-risk-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configure, AI Risk and Compliance, Governance, Risk, and Compliance]
---

# Install AI Risk and Compliance

You can install the AI Risk and Compliance application \(sn\_grc\_ai\_gov\) if you have the admin role. The application includes demo data and installs related ServiceNow® Store applications and plugins if they are not already installed.

## Before you begin

-   Ensure that the application and all of its associated ServiceNow Store applications have valid ServiceNow entitlements. For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030186).
-   Review the AI Risk and Compliance application listing in the ServiceNow Store for information on dependencies, licensing or subscription requirements, and release compatibility.
-   Check your entitlements to determine whether you have access to AI Risk and Compliance.

**Note:**

Some AI capabilities are available only when the required plugins are installed.

-   AI Risk and Asset Management capabilities in AI Control Tower with Now Assist require the AI Risk and Asset Management for Now Assist plugin \(sn\_aict\_irm\_aiam\), which depends on:
    -   AI Risk and Compliance Integration with Control Tower \(sn\_grc\_ai\_irm\_intg\)
    -   AI Asset Management \(sn\_ai\_asset\_mgmt\)
-   AI Control Tower supports governance of both enterprise AI assets and ServiceNow AI assets, while AI Control Tower with Now Assist supports governance of ServiceNow AI assets only.
-   When AI Control Tower Core \(sn\_ai\_governance\) is used with AI Risk and Compliance in a new IRM deployment, the IRM Standard \(sn\_irm\_std\) plugin is required to make AI intake request forms available. These intake forms are used to submit requests through the Employee Portal for registering AI systems, AI models, and datasets for governance and risk evaluation.

    This requirement applies only to AI intake request forms and does not apply to AI cases, inquiries, or the Anonymous Reporting Center. For more information on applicable requests, see [Request an AI use case](request-ai-system.md), [Request an AI model](request-ai-model.md), and [Request a dataset](request-dataset.md).


For information about AI Control Tower setup and plugin dependencies, see [Activation and installation of AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-control-tower/activation-and-installation-of-ai-control-tower.md).

Role required: admin

## About this task

The following items are installed with AI Risk and Compliance:

-   Plugins
-   Store applications
-   Roles
-   Tables

For more information, see [AI Risk and Compliance reference](../reference/ai-risk-and-compliance-reference.md).

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the AI Risk and Compliance application \(sn\_grc\_ai\_gov\) using the filter criteria and search bar.

    You can search for the application by its name or ID. If you cannot find the application, you might have to request it from the ServiceNow Store.

    In the list next to the **Install** button, the versions that are available to you are displayed.

3.  Select a version from the list and select **Install**.

    In the Review Installation Details dialog box, any dependencies installed with your application are listed.

4.  If you're prompted, follow the links to the ServiceNow Store to get any additional entitlements for dependencies.

5.  If demo data is available and you want to install it, select the **Load demo data** check box.

    Demo data are the sample records that describe application features for common use cases. Load the demo data when you first install the application on a development or test instance.

6.  Select **Install**.


