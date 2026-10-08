---
title: Install HR Service Delivery apps in the AI-Native workflow
description: Install the HR Service Delivery Implementation agent and HR Service Delivery applications via the centralized and intuitive admin configuration experience.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/hr-service-delivery/install-native-ai-hrsd.html
release: brazil
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [AI-Native HRSD Implementation, HR Service Delivery, Employee Service Management]
---

# Install HR Service Delivery apps in the AI-Native workflow

Install the HR Service Delivery Implementation agent and HR Service Delivery applications via the centralized and intuitive admin configuration experience.

## Before you begin

Role required: admin

Complete the ServiceNow Otto for Setup Platform configuration flow: [Configure the Platform module in ServiceNow Otto for Setup](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/ia-config-platform-il.md)

## About this task

HR Service Delivery applications, plugins, and dependencies are bundled into a single installable resource. Selecting install starts the installation of the full set of HR Service Delivery Foundation applications, instead of installing each application individually.

**Note:** Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents. For more information, see [ServiceNow product tiers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/ai-native-sku-overview.md).

## Procedure

1.  Install the HR Service Delivery Implementation agent \(`sn_hr_ia`\) application from the ServiceNow Store.

2.  Navigate to **All** &gt; **Admin Center** &gt; **Admin Home**.

3.  Select the HR Service Delivery tile.

    \[Omitted image "hrsd-config-hub.png"\] Alt text: In the Manage your products section, the Human Resources Service Delivery tile redirects to an HRSD-specific configuration flow

4.  In the **Apps and plugins** section, from the **Not installed** tab, select the **Install** icon for the HR Service Delivery applications you want to install.

    The **Choose what to install** window is displayed \(step 1 of 2\), with all entitled applications and their latest versions preselected.

5.  Select **Install selected items**.

    The **Review Installation Details** page is displayed \(step 2 of 2\), confirming the number of applications selected.

6.  After installation completes, the **Now you're ready to configure** window is displayed.

    \[Omitted image "hrsd-ready-to-configure.png"\] Alt text: The Now you're ready to configure window is displayed with a Configure button to proceed


## What to do next

Select **Configure** in the **Now you're ready to configure** window for a guided, AI agent-assisted configuration workflow. For the configuration steps, see [Configure HR Service Delivery in AI-Native workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/hr-service-delivery/ai-native-config-flow.md).

