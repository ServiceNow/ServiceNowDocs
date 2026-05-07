---
title: Privacy Management solution overview
description: The Privacy Management solution provides you with a framework to manage your privacy-specific libraries such as citations, policies, control objectives, risk statements, privacy impact assessments, and privacy risk assessments. It also provides processing activity records to track privacy risk and compliance posture.
locale: en-US
release: australia
product: Privacy Workspace
classification: privacy-workspace
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Explore, Privacy Management, Governance, Risk, and Compliance]
---

# Privacy Management solution overview

The Privacy Management solution provides you with a framework to manage your privacy-specific libraries such as citations, policies, control objectives, risk statements, privacy impact assessments, and privacy risk assessments. It also provides processing activity records to track privacy risk and compliance posture.

Before planning your privacy program, confirm that you set up the privacy libraries according to the privacy regulations that you plan to implement. For more information on the library setup, refer to [Manage the Privacy Management library](privacy-library-setup.md).

The following figure demonstrates the Privacy Management solution.

![Privacy management solution overview.](../image/privacy-mgmt-workflow.png "Privacy management solution overview")

The Privacy Management solution is described as follows.

## Create a library

As a privacy manager, with the role sn\_privacy.manager, or privacy administrator, with the role sn\_privacy.admin, you must set up your libraries using the following.

-   Privacy impact assessments
-   Personal information objects
-   Privacy regulations, authority documents, citations, and control objectives.
-   Privacy policies and procedures
-   Privacy risk statements

## Privacy impact assessments

As part of establishing a robust privacy program, privacy managers must first identify and document the inventory of organizational assets that handle personal data. This foundational step involves discovering and classifying business processes, applications, vendors, and services that process personally identifiable information \(PII\). The following approaches outline how to discover systematically, validate, and document these inventories using entity types, screening assessments, and system-driven insights.

1.  Discover inventory: As a privacy manager, with the role `sn_privacy.manager`, identify, or discover the inventory such as business processes, business applications, vendors, and business services that process personal data. All such inventory is stored in the respective Configuration Management Database \(CMDB\) tables. The respective business owners manage the inventory. As a privacy manager, use the Entity types feature and create an entity for each inventory record. For more information about entity types, see [Exploring the entities](../../grc-common/concept/exploring-the-entities.md). At this stage, based on the discovery method, you can use one of the following approaches to create processing activities.
    1.  Search business processes or applications that process personal data: Use this approach when business processes, applications, services, or vendors are associated with information objects. Using the entity type functionality, search for entities that process \[PI\] Information objects. Based on the search results, directly create the processing activity records. This approach is used only when the business owners associate the inventory with information objects. For more information, see [Entity scoping to plan a privacy program](entity-scoping-in-privacy-mgmt.md).
    2.  Send privacy screening assessments: Use this approach when information objects aren’t associated with the inventory such as business applications and processes. In this approach, send privacy screening assessments to the respective business owners. These screening assessments contain basic questions. Some examples of the questions are as follows:

        -   Are you processing personal information as a part of the business process or application that you own?
        -   What kind of personal information you’re processing? For example, email, phone, and address.
        If the assessment responses determine that there’s personal data, processing activities are created automatically.

2.  Business users can proactively submit privacy impact assessments for new applications and processes from the Employee Center.

## Manage and update the processing activities

1.  Create or update a processing activity: As a privacy analyst, with the role sn\_privacy.analyst, send a privacy impact assessment \(PIA\) to the processing activity or business owners after a processing activity is created. The privacy impact assessment helps to understand why and how the processing activity processes personal information. The assessment collects information such as justification for storing PI data, exchange of PI data with other systems, and the security of PI data.
2.  Send or automatically initiate PIA: As a privacy analyst, send a privacy impact assessment \(PIA\) from a processing activity whenever you must collect more information. Alternatively, you can also automatically initiate the assessments based on the privacy program frequency defined by the privacy manager and the privacy administrator. An auto-initiate schedule can be created using the ServiceNow AI Platform capabilities.
3.  Apply risks and controls related to the processing activity: As a privacy analyst, after you understand how personal information is being used in the processing activity, the necessary risk statements, controls, policies, and authority documents are automatically applied to the processing activities based on the assessment responses. For more information on how to configure assessments, see [Create an assessment template](../task/create-assessment-template.md). After the controls are added, the privacy analyst can review the controls and add or remove the controls as necessary.
4.  Send control attestations: After the final set of controls is associated with the processing activity, the control attestations are sent to the business process owners or the application owners to collect the evidence for every control that is applied. When the business owners respond to control attestations with evidence for each control, compliant and non-compliant controls are identified. This identification determines the compliance posture of the processing activity.
5.  Report and monitor issues: Issues are created automatically for non-compliant controls and are assigned to their respective business owners. The privacy analyst monitors the issues.
6.  Manage issues: To manage issues, business owners can do one of the following:
    -   Resolve the issue: Resolving the issue makes the control compliant.
    -   Raise a policy exception: An exception is raised for an issue that can’t be resolved immediately. Privacy analysts can review the policy exceptions and can either accept or reject the exceptions based on the criticality of the issue.
7.  Continuous control monitoring: Privacy analysts continuously monitor the controls on a processing activity using the indicator functionality. For more information about indicators, see [Risk indicators, control indicators, and indicator templates](../../grc-risk/concept/manage-indicators-risk.md).

## Assess the criticality of processing activities

The criticality score provides the risk posture at the processing activity-level by assessing the factors at processing activity-level. When a processing activity is created or updated, a criticality assessment is performed on the processing activity to understand the high-level risk score or the criticality score.

## Perform privacy risk assessments

Privacy risk assessments are detailed assessments that are conducted if the criticality score is high. Assess each risk that is associated with the processing activity and know the aggregated risk score on the processing activity. After you assess the privacy risks, you can view the privacy risk posture on the risk heatmap in the overview section. The heatmaps provide detailed information about your inherent and residual risks.

**Parent Topic:**[Exploring Privacy Management](explore-privacy-management.md)

