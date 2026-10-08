---
title: Create a data asset in AI Admin Center \(Lux UI\)
description: Create a dataset, generate synthetic data, and publish data collections to evaluate skills and agents.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/ai-admin-center-lux-create-data-asset.html
release: australia
topic_type: task
last_updated: "2026-10-02"
reading_time_minutes: 3
keywords: [AI Admin Center, Now Assist Center, AI, AI setup, dataset]
breadcrumb: [Managing AI assets, Setting up AI capabilities and configurations, AI Admin Center, Enable AI experiences]
---

# Create a data asset in AI Admin Center \(Lux UI\)

Create a dataset, generate synthetic data, and publish data collections to evaluate skills and agents.

**Important:** Lux is the new user experience for AI Admin Center. For more information on the Lux experience, see [AI Admin Center user experience \(Lux UI\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/ai-admin-center-lux-user-experience.md).

The Next Experience AI Admin Center workspace is being prepared for deprecation in the November store release and will no longer be supported. For more information on the Next Experience UI, see [AI Admin Center workspace \(Next Experience UI\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/now-assist-center-workspace.md).

In AI Admin Center version 6.1, the Next Experience and Lux user interfaces are both available.

## Before you begin

Role required: sn\_na\_center.nac\_admin

## About this task

Follow these steps to create a data asset.

A custom dataset and data collection in AI Data Kit is used for evaluations in AI Skill Kit.

**Note:** This topic describes the AI Admin Center feature based on the Lux user experience \(UI\). There is no Next Experience UI version of this topic.

## Procedure

1.  Navigate to **All** &gt; **AI Admin Center** &gt; **Home** or **Admin** &gt; **AI Admin Center**.

2.  Select **Asset library** \(\[Omitted image "icon-aiac-lux-nav-inventory.png"\] Alt text: Inventory icon.\) in the side navigation panel.

    The Asset library page opens.

3.  Select the **Create asset** button.

    The Create asset box opens showing options for the asset type.

4.  Select **Data asset**.

5.  Choose the type of asset you want to create.

    Select one of the following:

    -   **Create dataset**. Import data from instance tables or local files to create a dataset.
    -   **Standard synthetic dataset**. Generate synthetic data using standard templates and configurations.
    -   **Multi-table synthetic dataset**. Generate synthetic data across multiple related tables simultaneously.
    The create dataset form opens.

6.  Complete the setup based on the selection.

    -   For more information on importing data from a table or a local file as a dataset, see [Add a dataset](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/now-assist-data-kit/add-dataset.md).
    -   For more information on generating synthetic datasets, see [Generate synthetic data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/now-assist-data-kit/na-data-kit-generate-data.md).

## Result

A dataset is created and can be seen in the data assets list on the Asset library page.

**Parent Topic:**[Managing AI assets in AI Admin Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/now-assist-center-using-asset-inventory.md)

**Related topics**  


[View your AI assets in the asset inventory \(Next Experience UI\)]()

[View your AI assets in the asset library \(Lux UI\)]()

[Create an asset in the AI asset inventory \(Next Experience UI\)]()

[Create an asset in AI Admin Center \(Lux UI\)]()

[Create an intent in AI Admin Center \(Lux UI\)]()

[Edit an intent in AI Admin Center \(Lux UI\)]()

