---
title: Risk and compliance tab
description: The Risk and compliance tab on the privacy management dashboard provides a centralized view of privacy-related risk exposure and regulatory compliance performance.
locale: en-US
release: xanadu
product: Privacy Workspace
classification: privacy-workspace
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Privacy Workspace for the privacy manager, Explore, Privacy Management, Governance, Risk, and Compliance]
---

# Risk and compliance tab

The Risk and compliance tab on the privacy management dashboard provides a centralized view of privacy-related risk exposure and regulatory compliance performance.

The Risk and compliance tab on the privacy management dashboard enables organizations to monitor the risk and compliance postures of the privacy program within the organization. It helps evaluate how effective current privacy controls are in mitigating identified risks and supporting compliance.

Using this dashboard, teams can track adherence to major regulatory frameworks, including NIST SP 800-53 and the EU GDPR. The dashboard presents data through intuitive visualizations such as heatmaps, compliance scores, and summaries of control objectives that need attention. These visuals provide immediate insights into risk exposure and compliance gaps across the organization. Privacy teams can identify high-risk areas and assign priority to remediation tasks based on real-time data.

The dashboard also assists in confirming continuous regulatory alignment as requirements evolve, or new risks emerge. By consolidating risk and compliance insights into one view, it supports faster decision-making and improved accountability across privacy functions.

The visualization and data-driven layout support informed decision-making for privacy teams, confirming adherence to industry standards and legal obligations. This dashboard displays the following widgets.

-   **Risk overview**

    This donut chart displays the distribution of processing activities across different aggregated risk levels. By default, the distribution is based on the aggregated residual risk scores. However, you can apply a filter to view the distribution based on aggregated inherent risk classification instead. Each activity is color-coded by its associated risk level.

    The Risk heatmap widget displays the visualization of all identified risks within each processing activity. By default, residual risk filter is applied, but you can filter it based on inherent risk level. The heatmap is segmented, and the segmentation changes based on the filter. The activities fall under the respective combination of risk and control effectiveness, or impact and likelihood. The combination is based on the selected risk classification filter.

-   **Compliance overview**

    This section summarizes compliance posture across different regulatory frameworks like NIST SP 800-53 and GDPR. It also provides a consolidated view. You can filter compliance information with specific Authority documents. Filtering the data by Policies shows compliance posture across privacy policies; for example, Employee Data Privacy Policy, Customer Data Privacy Policy, or third-party Privacy Policy. Select the appropriate authority document or policy in the drop-down filter to view compliance score.

    Use the `sn_privacy.highlighted_policy` and `sn_privacy.highlighted_authority_document` properties to configure the top two policies and authority documents that appear on this widget.

-   **Control objectives needing attention**

    This section highlights specific control objectives requiring immediate remediation, along with the number of impacted processing activities. Each control objective is hyperlinked for detailed review.

-   **Regulatory change management**

    The Activity overview widget displays the status of change-related activities triggered by regulatory updates. Each segment is represented using donut charts with status-based color coding.

    The Impact assessment widget shows ongoing Impact Assessments related to Regulatory Assessments. The drop-down menu enables you to change the assessment category.

    **Note:** These widgets are available only when you have the Regulatory Change Management application installed.


The following image shows the Risk and compliance dashboard.

![Risk and compliance tab on the privacy management home page.](../image/risk-and-compliance-tab.png "Risk and compliance dashboard")

**Parent Topic:**[Privacy Workspace for the privacy manager](privacy-mgmt-ws-privacy-compliance-manager.md)

