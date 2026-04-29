---
title: Risk and compliance tab in AI Control Tower
description: The Risk and compliance tab on the AI Control Tower displays the risk classification of AI assets and the compliance posture for selected authority documents and policies.
locale: en-US
release: australia
product: AI Control Tower
classification: ai-control-tower
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [AI Control Tower Home, AI Control Tower dashboard, Explore, AI Control Tower, Enable AI experiences]
---

# Risk and compliance tab in AI Control Tower

The Risk and compliance tab on the AI Control Tower displays the risk classification of AI assets and the compliance posture for selected authority documents and policies.

AI assets refer to the various components and resources that are essential for the development, deployment, and operation of artificial intelligence systems. These assets can include:

1.  AI systems: The complete software or hardware infrastructure that runs AI algorithms and processes. This can include machine learning platforms, natural language processing systems, and other AI-driven applications.
2.  AI models: The mathematical and computational models that are trained on data to perform specific tasks. These models can range from simple linear regression models to complex deep learning neural networks.
3.  AI datasets: The collections of data used to train, validate, and test AI models.

For more information, see [AI systems](https://www.servicenow.com/docs/access?context=ai-system-airc&version=australia&pubname=australia-governance-risk-compliance&ft:locale=en-US), [AI models](https://www.servicenow.com/docs/access?context=ai-model-airc&version=australia&pubname=australia-governance-risk-compliance&ft:locale=en-US), and [Datasets](https://www.servicenow.com/docs/access?context=dataset-airc&version=australia&pubname=australia-governance-risk-compliance&ft:locale=en-US).

Understanding and managing these AI assets is crucial for ensuring that AI systems are effective, reliable, and compliant with regulatory and ethical standards as defined by your organization.

The Risk and compliance dashboard has the following sections. You can drill down into the data on each widget in any section.

## Compliance overview

-   **Regulatory risk classification**

    This section displays the risk classifications of AI systems, AI models, and Datasets using donut charts. The risks are qualitatively classified as **High**, **Low**, **Medium**, and **Unacceptable**. These classifications are based on the risk assessments of the AI assets.

-   **Compliance by authority documents and policies**

    The section shows compliance based on controls implemented. By default, the compliance scores are displayed for the following frameworks that are provided in the library:

    -   NIST AI Risk Management Framework: This framework displays the four key associated citations, namely map, measure, manage, and govern. Each citation's compliance score is displayed based on its control attestations.
    -   EU Artificial Intelligence Act: This framework has multiple chapters that are displayed as citations and child citations. Each citation is mapped to a control objective to provide you with a compliance percentage score.
    You can choose to view compliance data by selecting one of two options: **Authority Documents** or **Policies**. Additionally, you can view the overall compliance score percentage, along with the number of compliant and non-compliant authority documents and policies, by using the drop-down filter to select specific authority documents or policies. You can also see all the issues that require immediate attention and AI cases related to each authority document or policy.

    The authority documents are provided solely for informational and guidance purposes to assist with the initial setup of AI Risk and Compliance frameworks. It does not constitute legal advice or assurance of regulatory compliance. You are solely responsible for ensuring that all use of the content complies with applicable laws, regulations, directives, and industry standards in their jurisdictions.

    **Note:** You can configure which authority documents and policies you want to display on the home page. For more information, see [Set up properties for compliance posture](https://www.servicenow.com/docs/access?context=configure-airc-properties&version=australia&pubname=australia-governance-risk-compliance&ft:locale=en-US).


## Risk overview

This section monitors and tracks the risk posture of the AI assets in your organization. Using the **AI asset** filter, you can filter risk posture insights by the type of AI asset inventory.

-   **AI systems by aggregated risk score**

    This section displays the classifications of AI systems by aggregated risk score using a donut chart. The risk scores are qualitatively classified as **High** and **Low**.

-   **Risk heatmap**

    The Risk heatmap widget displays the visualization of all identified risks within the AI assets. By default, the Residual risk filter is applied, but you can filter the heatmap based on Inherent risk. The heatmap is segmented, and the segmentation changes based on the filter. The activities fall under the respective combination of risk and control effectiveness, or impact and likelihood. The combination is based on the selected risk classification filter. You can filter the risk heatmap by Risk Assessment Methodology \(RAM\)when more than one methodology is available.


## Regulatory landscape overview

You need to install GRC: Regulatory Change Management application to see this section. For more information, see [Installing Regulatory Change Management](https://www.servicenow.com/docs/access?context=activate-grc-rcm&version=australia&pubname=australia-governance-risk-compliance&ft:locale=en-US).

-   **Overview**
    -   Alerts

        This section displays the risk classifications of AI systems, AI models,and AI datasets using donut charts.

    -   Change tasks

        This section displays the distribution of regulatory change tasks by workflow state or lifecycle phase using a donut chart.

-   **Assessments**

    This section displays the regulatory impact assessments and risk assessments linked to regulatory changes using a donut chart. By default, regulatory assessments filter is applied, but you can change it to risk assessments.


The following image shows the Risk and compliance dashboard.

![The dashboard monitors and manages the risk and compliance posture of the AI assets in your organization.](../image/riask-and-compliance-dashboard-aict.png "Risk and compliance dashboard")

For more information, see [AI Risk and Compliance documentation](https://www.servicenow.com/docs/access?context=ai-risk-and-compliance&version=australia&pubname=australia-governance-risk-compliance&ft:locale=en-US).

