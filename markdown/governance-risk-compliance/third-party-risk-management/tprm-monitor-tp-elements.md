---
title: Monitoring third-party elements
description: You can monitor third-party elements through scalable scoring models, relationship analysis, and due diligence workflow integration by using the Third-party Risk Management application. Monitoring third-party elements and leveraging that information can help with conducting more informed risk assessments as part of your third-party risk program.
locale: en-US
release: xanadu
product: Third-party Risk Management
classification: third-party-risk-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 6
breadcrumb: [Monitor third-party risk, Third-party Risk Management, Governance, Risk, and Compliance]
---

# Monitoring third-party elements

You can monitor third-party elements through scalable scoring models, relationship analysis, and due diligence workflow integration by using the Third-party Risk Management application. Monitoring third-party elements and leveraging that information can help with conducting more informed risk assessments as part of your third-party risk program.

## Third-party elements overview

Third-party elements \(TP elements\) are the external organizations that an engagement relies on to provide goods, services, or support. These organizations can include the suppliers, contractors, facilities, individuals, or any other external organization that can access the engagement's systems, data, or facilities.

Let's look at some TP element class and risk examples:

-   **Datacenter**

    A facility or location where an engagement or third party outsources the storage, processing, and management of their data and IT infrastructure. A datacenter could potentially experience a data breach, downtime, or compliance violation that exposes their engagements to unexpected risk. This example would be classified as a Facility TP element.

-   **Manufacturing facility**

    A facility or location where an engagement or third party outsources the production or assembly of their products. A manufacturing facility could potentially experience a supply chain disruption, a counterfeit part, or regulatory compliance issue that exposes their engagements to unexpected risk. This example would be classified as a Facility TP element.

-   **Beneficial owner**

    An individual who owns or controls an organization that is involved in a business relationship or transaction. These individuals may not be the registered or legal owners of the organization but have significant influence or control over its operations, decision-making, or financial affairs. This example would be classified as a Principal TP element.


The following infographic shows the TP element collection process.

![Infographic that shows the TP element collection process in the due diligence workflow. For the text description, refer to the text that follows.](../../grc-workspace-vrm/image/mmasset0020761-TP-element-process-vertical.png)

For more information on Third-party \(TP\) elements and examples of their associated controls and potential risks, see [Terminology](../reference/tprm-terminology.md).

## Collecting and reviewing third-party elements

Collecting and reviewing third-party elements is optional. If you have the Third-party risk \(TPR\) assessor \[sn\_vdr\_risk\_asmt.vendor\_assessor\] role and are the due diligence request owner or TPR manager \[sn\_vdr\_risk\_asmt.vendor\_risk\_manager\] role, you can start this process after your due diligence request has completed the Inherent Risk Questionnaire \(IRQ\) process.

You would follow this process to collect and review TP elements:

1.  In the Vendor Management Workspace, if TP elements are needed, the Third-party risk \(TPR\) manager or due diligence request owner selects **Start collection** and a collection task is created.
2.  The TPR manager or owner opens the external assessment for collecting elements and adds the relevant TP element collection questionnaires.
3.  The TPR manager or owner reviews and approves the questionnaires and they’re sent to the engagement. For more information on assessments, see [Assessing your third-party risk](tprm-assessing-tpr.md).
4.  In Vendor Management Workspace, the TPR manager or owner opens the questionnaires and verifies that all the required information was provided.
5.  The TPR manager or owner then navigates to the list of TP elements and manually creates a TP element record for each set of responses in each questionnaire.
6.  After all TP elements are created, the TPR manager or owner closes the collection task assessment. The system changes the state of the request from **Collection in progress** to **Collection in review**.
7.  The internal stakeholders \(TPR assessor, TPR approver, TPR manager, or TPR administrator\) review and approve the element records.

For more information, see [Create a third-party element record](../task/tprm-tp-element-create.md).

## Adding third-party elements to engagements

After the TP elements are reviewed and approved by the TPR manager and internal stakeholders in Vendor Management Workspace, the TPR manager or owner opens the engagement and manually adds the reviewed and approved TP elements as entities on the **Entities** tab of the engagement. For more information, see [Add a third-party element record to an engagement](../task/tprm-tp-element-engagement.md). After you add all TP element entities to an engagement, you can start the due diligence process. During the due diligence process, you must select and assign a questionnaire as part of an external assessment for each TP element that you created. The third-party contact completes the TP element questionnaires. For more information, see [Assessing your third-party risk](tprm-assessing-tpr.md).

## Third-party element scoring

You can categorize each TP element into one of the following types: Facility, Product, Principal, or Other. This classification helps you with organizing the assessment criteria and subsequent scoring. Scoring on a TP element is determined by averaging the risk ratings from its associated third-party risk assessments. If you conduct multiple assessments for the same TP element, the system considers only the latest assessment for each engagement for scoring, disregarding duplicates. This process helps to ensure that the TP element's risk rating reflects the most current evaluation. For example, if a TP element has assessments with risk ratings of very high and very low, the average of these ratings leads to the overall risk being moderate.

After an element is assessed and a risk rating is determined, this rating is first aggregated into a component score that is based on its classification, such as Facility. For example, all Facility-type elements are aggregated into a single component score, which contributes to the overall score of the engagement. The engagement score is then compiled by aggregating the scores from all relevant component scores within that engagement. If multiple assessments or TP elements are within an engagement, each is scored individually and then combined to form the overall engagement score. The engagement score is then rolled up to the third-party level by aggregating the scores from all the engagements that are associated with a particular third party. The aggregation at this level could be based on different rules, such as averaging, taking the minimum, or maximum scores, depending on the scoring rules set within the system. This rolled-up score represents the overall risk or performance score of the third party and reflects all the engagements and elements that are associated with it.

**Note:** You can create your own TP element classifications to meet your specific risk program requirements. For more information on creating classifications and assigning weights for scoring, see [Third-party element form](../../grc-workspace-vrm/reference/tprm-tpe-form.md) and [Define component criteria](../task/tprm-component-criteria-define.md).

