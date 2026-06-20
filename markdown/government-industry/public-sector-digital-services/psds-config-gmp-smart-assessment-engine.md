---
title: Configure the Smart Assessment Engine for Grants Management
description: The Smart Assessment Engine \(SAE\) in ServiceNow streamlines and automates assessment processes, reducing manual efforts and costs. It supports various assessment types, includes drag-and-drop functionality for designing templates, and offers end-to-end workflow automation. SAE is highly configurable, making it adaptable for a wide range of use cases, including control attestation and risk identification.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/government-industry/public-sector-digital-services/psds-config-gmp-smart-assessment-engine.html
release: yokohama
product: Public Sector Digital Services
classification: public-sector-digital-services
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Grants Management, Playbooks, Configure Agent Workspaces, Configuring Public Sector Digital Services, Public Sector Digital Services \(PSDS\)]
---

# Configure the Smart Assessment Engine for Grants Management

The Smart Assessment Engine \(SAE\) in ServiceNow streamlines and automates assessment processes, reducing manual efforts and costs. It supports various assessment types, includes drag-and-drop functionality for designing templates, and offers end-to-end workflow automation. SAE is highly configurable, making it adaptable for a wide range of use cases, including control attestation and risk identification.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Smart Assessment Engine** &gt; **Administration** &gt; **Template Categories**.

2.  Select **New** to create a template category.

3.  On the form, fill in the fields.

    In the Category role field, enter `sn_smart_asmt.template_manager`.

4.  Select **Submit**.

5.  Navigate to **Workspaces** &gt; **Assessment Workspace**

6.  Select **New Template**, and on the form, fill in the fields.

    In the Assessment targets field, enter **Grants Management Case**.

7.  Navigate to the **Questions** tab and select **Add section**.

    \[Omitted image "psds-gmp-smart-engine-questions-tab.png"\] Alt text: Smart assessment engine.

8.  On the form, fill in the details for the section, then select **Save**.

9.  Select **Add question**, and add a Single Select Drop-down Question of your choice.

    Repeat until you have added all of your desired questions.

10. Select **Publish**.


