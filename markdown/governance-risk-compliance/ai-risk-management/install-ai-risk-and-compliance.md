---
title: Install AI Risk and Compliance
description: You can install the AI Risk and Compliance application \(sn\_grc\_ai\_gov\) if you have the admin role. The application includes demo data and installs related ServiceNow Store applications and plugins if they are not already installed.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/ai-risk-management/install-ai-risk-and-compliance.html
release: brazil
product: AI Risk Management
classification: ai-risk-management
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 4
breadcrumb: [AI Risk and Compliance, Governance, Risk, and Compliance]
---

# Install AI Risk and Compliance

You can install the AI Risk and Compliance application \(`sn_grc_ai_gov`\) if you have the admin role. The application includes demo data and installs related ServiceNow® Store applications and plugins if they are not already installed.

## Before you begin

-   Ensure that the application and all of its associated ServiceNow Store applications have valid ServiceNow entitlements. For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030186).
-   Review the AI Risk and Compliance application listing in the ServiceNow Store for information on dependencies, and release compatibility.
-   Check your entitlements to determine whether you have access to AI Risk and Compliance.

Role required: admin

## About this task

Some AI Risk and Compliance capabilities are available only when specific plugins are installed. Review the following requirements for your deployment:

-   AI Risk and Compliance Integration with AI Control Tower \(soft dependency\)

    This plugin \(sn\_grc\_ai\_irm\_intg\) enables core capabilities in this application.

    -   Automatically provisioned when AI Control Tower \(com.sn\_aict\) is installed. No separate installation is required.
    -   This plugin is not available from the ServiceNow Store. It can only be obtained through AI Control Tower.
    -   Included capabilities:
        -   AI Risk and Compliance Management
        -   Advanced Risk
        -   AI Case Management
-   AI Risk and Asset Management with Now Assist

    To enable these capabilities in AI Control Tower with Now Assist, install the AI Risk and Asset Management for Now Assist plugin \(sn\_aict\_irm\_aiam\), which requires:

    -   AI Risk and Compliance Integration with AI Control Tower \(sn\_grc\_ai\_irm\_intg\)—automatically provisioned with AI Control Tower
    -   AI Asset Management \(sn\_ai\_asset\_mgmt\)
-   AI Control Tower governance scope
    -   AI Control Tower supports governance of both enterprise AI assets and ServiceNow AI assets.
    -   AI Control Tower with Now Assist supports governance of ServiceNow AI assets only.
-   AI intake request forms requirement

    When AI Control Tower Core \(sn\_ai\_governance\) is used with AI Risk and Compliance in a new IRM deployment, the IRM Standard \(sn\_irm\_std\) plugin is required to enable AI intake request forms. These forms allow users to submit requests through the Employee Portal for registering AI systems, AI models, and datasets for governance and risk evaluation.

    This requirement applies only to AI intake request forms. It does not apply to AI cases, inquiries, or the Anonymous Reporting Center. For information on applicable requests, see , , and .


-   For the complete list of dependencies, see the AI Risk and Compliance listing in the ServiceNow Store.

-   For more information on AI Control Tower, see [Activation and installation of AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/activation-and-installation-of-ai-control-tower.md) for complete setup and plugin dependency guidance.

-   For more information on roles, see [Roles and responsibilities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/ai-risk-management/roles-installed-with-ai-risk-and-compliance.md).
-   For more information on tables, see [System tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/ai-risk-management/tables-installed-with-ai-risk-and-compliance.md).

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the AI Risk and Compliance application \(`sn_grc_ai_gov`\) using the filter criteria and search bar.

    You can search for the application by its name or ID. If you cannot find the application, you might have to request it from the ServiceNow Store.

    In the list next to the **Install** button, the versions that are available to you are displayed.

3.  Select a version from the list and select **Install**.

    In the Review Installation Details dialog box, any dependencies installed with your application are listed.

4.  If you're prompted, follow the links to the ServiceNow Store to get any additional entitlements for dependencies.

5.  If demo data is available and you want to install it, select the **Load demo data** check box.

    Demo data are the sample records that describe application features for common use cases. Load the demo data when you first install the application on a development or test instance.

6.  Select **Install**.


## Result

The AI Risk and Compliance application is installed and ready to configure on your instance.

## What to do next

Install the AI Risk and Compliance content application to add predefined governance content to your instance, including control objectives, risk statements, and assessment templates. For more information, see [Install AI Risk and Compliance content](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/ai-risk-management/install-ai-risk-content-pack.md).

You can also configure the workspace and system properties to customize your governance setup. For more information, see [https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/ai-risk-management/configuring-ai-risk-and-compliance.md](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/ai-risk-management/configuring-ai-risk-and-compliance.md).

**Related topics**  


[Install AI Risk and Compliance content](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/ai-risk-management/install-ai-risk-content-pack.md)

[Configure AI Risk and Compliance Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/ai-risk-management/configure-airc-workspace.md)

[https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/ai-risk-management/configuring-ai-risk-and-compliance.md](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/ai-risk-management/configuring-ai-risk-and-compliance.md)

[Roles and responsibilities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/ai-risk-management/roles-installed-with-ai-risk-and-compliance.md)

