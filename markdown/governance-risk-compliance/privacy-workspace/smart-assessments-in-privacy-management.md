---
title: Smart assessments in Privacy Management
description: The new and improved assessment experience in Privacy Management uses the Smart Assessment Engine \(SAE\) application. The assessment engine enables you to perform privacy screening and privacy impact assessments to collect the necessary information for the privacy teams.
locale: en-US
release: australia
product: Privacy Workspace
classification: privacy-workspace
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Explore, Privacy Management, Governance, Risk, and Compliance]
---

# Smart assessments in Privacy Management

The new and improved assessment experience in Privacy Management uses the Smart Assessment Engine \(SAE\) application. The assessment engine enables you to perform privacy screening and privacy impact assessments to collect the necessary information for the privacy teams.

In Privacy Management, assessments play an important role. There are two types of assessments.

-   Privacy screening assessment: A privacy screening assessment is a preliminary evaluation used to determine whether a processing activity involves personal data and whether it may pose privacy risks. It’s a high-level review conducted to identify whether a more detailed privacy review, such as a privacy impact assessment \(PIA\), is necessary. For example, when a new business application or process is created, the privacy teams must understand if the application or the business process processes personal data or not. To determine this, the screening assessments are sent to the business application or business process owners. After the assessment is approved by the privacy manager, a processing activity is created.
-   Privacy impact assessment: After a screening assessment is performed, based on the responses, a privacy impact assessment may be generated. A Privacy impact assessment is a comprehensive evaluation of how a business application, system, or process affects personal data privacy. It assesses the privacy risks associated with processing activities and identifies measures to mitigate these risks. Each time a privacy impact assessment is performed, the risks are revisited to determine if the risk score changed. This helps the privacy teams remain vigilant and address the risks as required.

To perform these assessments, you can use the Smart Assessment Engine application. This application provides several benefits such as configuration of templates, workflows, guidance for questions, and reviewing of assessment results with actionable insights. For more information about the Smart Assessment Engine application, refer to [Exploring Smart Assessment Engine](../../assessment-engine/concept/smart-assessment-engine-cf-explore.md).

**Note:** To use Smart Assessment Engine, you must enable the**sn\_privacy.enable\_smart\_assessment** property that is located under system properties.

## Benefits of using the new assessment experience

The new assessment experience offers the following benefits.

-   Capture all the required information during the assessment eliminating the need for manually adding details to the processing activity.
-   Capture the hierarchy or flow of data and specify where the data is coming from and where is the data going.
-   Collect the lawful basis of collecting and processing data.
-   Create multiple sections for logical grouping of questions
-   Migrate assessments from older systems.
-   Provide inline guidance for questions.
-   Reassign the assessment to the correct responder.
-   Create highly configurable templates.

## Types of assessment templates

To perform the screening and the impact assessments, you require assessment templates. While the assessment templates are based on the Smart Assessment Engine, there are some additional configurations provided for the users of Privacy Management.

Starting with the Zurich release, two assessment templates, **Privacy Screening Assessment \[V4\]** and **Privacy Impact Assessment \[V4\]** are provided to perform smart assessments. **Privacy Screening Assessment \[V3\]** and **Privacy Impact Assessment \[V3\]** templates are also available. Some important differences between these templates and the additional configurations are explained as follows.

-   **Privacy screening assessment**

    Starting with the Zurich release, a new template for Privacy screening assessment \(Privacy Screening Assessment \[V4\]\) is available.

    For a screening assessment template, there are three sections:

    -   **General**: In this section, you specify the assessment template category as **Privacy category** and also specify the assessment targets. For a screening assessment, the assessment targets are entities and privacy tasks.
    -   **Questions**: This section contains questions for the assessment responders. This section also contains data elements which are single units of information that represent a specific attribute or characteristic about a data subject or entity. Examples of data elements are name, email address, date of birth, and so on. In this section, you’ll also find a section titled **Criticality factors** and these questions are used to calculate the criticality score.
    -   **Automations**: In this section, you can define the rules that allow the automatic creation of processing activities based on the responses to questions. This section uses Workflow Studio. These automations are mapped to their relevant questions. Automation streamlines various processes, including the application of risk statements and control objectives based on user responses. When users select specific responses during an assessment, the system automatically applies the appropriate risks and controls to the relevant records. For example, consider an organizational policy stating that personal data can only be transferred outside the EU with explicit consent. During an assessment, if a user indicates that data is being transferred outside the EU, the system will automatically apply the Data Transfer risk to the processing activity: Assign Explicit Consent as a control to mitigate the identified risk. This automation ensures consistency, saves time, and reduces the likelihood of human error in managing risks and controls.
    For detailed information on how to configure a screening assessment template, see [Configure smart assessment templates for screening assessments](../task/configure-a-smart-assessment-template.md).

    ![Privacy screening assessment page.](../image/privacy-screening-asmt.png "Privacy screening assessment")

-   **Privacy impact assessment**

    Starting with the Australia release, a new template for Privacy impact assessment \(Privacy Impact Assessment \[V4\]\) is available.

    For a privacy impact assessment template, like the screening assessment template, you have the **Overview** and **Details** sections, and while by default, the **Automations** section is present, it does not contain any predefined automations. You can add automations if you require them. For an impact assessment template, apart from the questionnaire, you can add the personal data elements. For detailed information on how to configure an impact assessment template, see [Configure smart assessment templates for impact assessments](../task/configure-smart-assessment-template-for-impact-assessment.md).

    ![Privacy impact assessment landing page.](../image/privacy-impact-assessment.png "Privacy impact assessment screen")


**Note:** Only published templates are available for assessments.

## Review of an assessment

When privacy analysts receive an assessment, they review the assessment. During the review, they can either request for a revision of the assessment or directly approve it. During the **Review** state, the privacy managers can view the following items:

-   **Information objects**: The information objects tab displays the information objects identified as part of the screening assessment.
-   **Hierarchy**: The hierarchy of where data comes from and where it goes.
-   **Outcomes**: The outcomes tab displays the risk statement and the control objectives associated with the assessment.

**Parent Topic:**[Exploring Privacy Management](explore-privacy-management.md)

**Related topics**  


[Add instructions and questions to an assessment template](../../assessment-engine/task/sae-asmnt-template-populate.md)

