---
title: Risk &amp; compliance tab
description: The Risk &amp; compliance tab on the AI Risk and Compliance displays the risk classification of an AI asset inventory and the compliance posture for the selected authority documents and policies.
locale: en-US
release: zurich
product: AI Risk Management
classification: ai-risk-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [AI Risk and Compliance workspace, Explore, AI Risk and Compliance, Governance, Risk, and Compliance]
---

# Risk &amp; compliance tab

The Risk &amp; compliance tab on the AI Risk and Compliance displays the risk classification of an AI asset inventory and the compliance posture for the selected authority documents and policies.

AI assets refer to the various components and resources that are essential for the development, deployment, and operation of artificial intelligence systems. These assets can include:

1.  [AI systems](ai-system-airc.md): The complete software or hardware infrastructure that runs AI algorithms and processes. This can include machine learning platforms, natural language processing systems, and other AI-driven applications.
2.  [AI models](ai-model-airc.md): The mathematical and computational models that are trained on data to perform specific tasks. These models can range from simple linear regression models to complex deep learning neural networks.
3.  [Datasets](dataset-airc.md): The collections of data used to train, validate, and test AI models.

Understanding and managing these AI assets is crucial for ensuring that AI systems are effective, reliable, and compliant with regulatory and ethical standards as defined by your organization.

The Risk &amp; compliance dashboard has the following sections. You can drill down into the data on each widget in any section.

**Note:** Dashboards in the AI Risk and Compliance Workspace \(Risk and Compliance, Operations, and AI Cases\) display data for **Managed** AI assets only. AI assets that are marked as **Unmanaged** are excluded from dashboard widgets, metrics, and summary counts, but remain visible in inventory and list views. If you have the AI steward \[sn\_ai\_governance\_ai\_steward\] role, you can mark assets as Managed or Unmanaged. For more information, see [Assets list- managed and unmanaged assets](https://www.servicenow.com/docs/access?context=assets-list-managing-and-unmanaging-assets&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

## Compliance overview

-   **Regulatory risk classification**

    This section displays the risk classifications of AI systems, AI models, Datasets using donut charts. The risks are qualitatively classified as **High**, **Low**, **Medium**, and **Unacceptable**. These classifications are based on the risk assessments of the AI assets.

-   **Compliance by authority documents and policies**

    The section shows compliance based on controls implemented. By default, the compliance scores are displayed for the following frameworks that are provided in the library:

    -   NIST AI Risk Management Framework: This framework displays the four key associated citations, namely map, measure, manage, and govern. Each citation's compliance score is displayed based on its control attestations.
    -   EU Artificial Intelligence Act: This framework has multiple chapters that are displayed as citations and child citations. Each citation is mapped to a control objective to provide you with a compliance percentage score.
    You can choose to view compliance data by selecting one of two options: **Authority Documents** or **Policies**. Additionally, you can view the overall compliance score percentage, along with the number of compliant and non-compliant authority documents and policies, by using the drop-down filter to select specific authority documents or policies. You can also see all the issues that require immediate attention and AI cases related to each authority document or policy.

    The authority documents are provided solely for informational and guidance purposes to assist with the initial setup of AI Risk and Compliance frameworks. It doesn’t constitute legal advice or assurance of regulatory compliance. You’re solely responsible for ensuring that all use of the content complies with applicable laws, regulations, directives, and industry standards in their jurisdictions.

    **Note:** You can configure which authority documents and policies you want to display on the home page. For more information, see [Set up properties for compliance posture](../task/configure-airc-properties.md).


## Risk overview

This section monitors and tracks the risk posture of the AI assets in your organization. Using the **AI asset** filter, you can filter risk posture insights by the type of AI asset inventory.

-   **AI systems by aggregated risk score**

    This section displays the classifications of AI systems by aggregated risk score using donut chart. The risk scores are qualitatively classified as **High** and **Low**.

-   **Risk heatmap**

    The Risk heatmap widget displays the visualization of all identified risks within the AI assets. By default, a residual risk filter is applied, but you can filter it based on inherent risk level. The heatmap is segmented, and the segmentation changes based on the filter. The activities fall under the respective combination of risk and control effectiveness, or impact and likelihood. The combination is based on the selected risk classification filter. You can filter the risk heatmap by Risk Assessment Methodology \(RAM\), if you have more than one risk RAMs published.


## Regulatory landscape overview

You need to install GRC: Regulatory Change Management application to see this section. For more information, see [Installing Regulatory Change Management](../../grc-rcm/task/activate-grc-rcm.md).

-   **Overview**
    -   Alerts

        This section displays the distribution of regulatory alerts by workflow state or life cycle phase using a donut chart.

    -   Change tasks

        This section displays the distribution of regulatory change tasks by workflow state or life cycle phase using a donut chart.

-   **Assessments**

    This section displays the regulatory impact assessments and risk assessments linked to regulatory changes using a donut chart. By default, the regulatory assessments filter is applied, but you can change it to risk assessments.


The following image shows the Risk &amp; compliance dashboard.

![The dashboard monitors and manages the risk and compliance posture of the AI assets in your organization.](../image/ai-risk-compliance-workspace.png "Risk & compliance dashboard")

