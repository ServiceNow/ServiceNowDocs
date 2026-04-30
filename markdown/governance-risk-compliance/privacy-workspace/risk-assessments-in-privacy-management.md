---
title: Risk assessments in Privacy Management
description: You can perform risk assessments on your processing activities to determine their risk scores and find out the privacy risk posture of your organization.
locale: en-US
release: yokohama
product: Privacy Workspace
classification: privacy-workspace
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Explore, Privacy Management, Governance, Risk, and Compliance]
---

# Risk assessments in Privacy Management

You can perform risk assessments on your processing activities to determine their risk scores and find out the privacy risk posture of your organization.

To understand the risk posture, the following assessments are performed.

## Criticality assessments

A criticality assessment uses risk assessment to determine the initial risk level of a processing activity. Using the resulting criticality score, the privacy team can prioritize or deprioritize the activity accordingly. An example of a criticality factor could be that the assessment questions help identify whether personal data is being processed in a way that influences key decisions or enables impactful autonomous decision making.

Criticality assessments can be performed using one of the following two methods.

-   **Manual criticality assessment**

    Using the manual method, as a privacy manager initiates the criticality assessment from a processing activity. If you're already working on a processing activity and want to assess its criticality, you can manually trigger this assessment using the **Assess criticality** action in the user interface. When you trigger the criticality assessment, the system automatically calculates the criticality score based on the information already available in the fields of the processing activity form. On the Regulatory details tab of a processing activity, you can provide the risk-related details. After entering this information, triggering the criticality assessment uses these values to calculate the risk score. The system can calculate the criticality score multiple times if triggered manually. Each time, it uses the most recent data entered in the processing activity fields and regulatory details.

-   **Automated criticality assessment**

    Using the automated method, the privacy manager uses the **Automated criticality factors** risk assessment methodology \(RAM\) that is provided by default to calculate the criticality score of a processing activity. The privacy managers must publish this RAM before it can be used. By default, the RAM is provided in the **Draft** state. When a user performs a screening assessment, they are prompted to respond to several questions, including those related to criticality and risk assessment. If the user provides answers to these criticality-related questions during the screening assessment, the system automatically calculates the criticality risk score. The calculated score is then displayed on the Overview page when the user proceeds to the processing activity. Because only two RAMs are supported at a time, they must deactivate any other existing criticality factors RAM. It is crucial to note that when an existing criticality factors RAM is deactivated, all the in-progress risk assessments associated with that RAM get canceled.


![Manually initiate criticality assessment.](../image/criticality-asmt.png)

## Privacy risk assessments

Privacy risk assessments are detailed assessments that are conducted if the criticality score is high. Assess each risk that is associated with the processing activity and know the aggregated risk score on the processing activity. After you assess the privacy risks, you can view the privacy risk posture on the risk heatmap in the overview section. The heatmaps provide detailed information about your inherent and residual risks. See the following image to understand how you can initiate the detailed risk assessment.![Perform advanced risk assessments.](../image/perform-ara-pa.png)

## Risk heatmap scores

The risk assessments results and the risk heatmaps appear on the processing activity home page as shown in the following image.

![Risk criticality score](../image/risk-score-on-pa.png "Risk scores on a processing activity")

![Risk heatmap view.](../image/risk-heatmap-on-pa.png "Risk heatmap on the processing activity")

To understand the details about how to perform the risk assessments, see [Privacy assessment configurations](privacy-assessment-configurations.md).

-   **[Risk Assessment Methodology \(RAM\)](risk-assessment-methodology-prm.md)**  
Risk Assessment Methodology \(RAM\) provides a systematic and repeatable approach to identifying, evaluating, and mitigating privacy risks associated with data processing activities.
-   **[Privacy assessment configurations](privacy-assessment-configurations.md)**  
To perform a processing activity criticality and privacy risk assessment, two risk assessment methodologies \(RAMs\) are provided by default.

**Parent Topic:**[Exploring Privacy Management](explore-privacy-management.md)

