---
title: Terminology
description: Learn more about the key concepts and terms that are used in the TPRM application.
locale: en-US
release: yokohama
product: Third-party Risk Management
classification: third-party-risk-management
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 15
breadcrumb: [Reference, Third-party Risk Management, Governance, Risk, and Compliance]
---

# Terminology

Learn more about the key concepts and terms that are used in the TPRM application.

## Third, Fourth, and nth parties

A third party is any organization or individual that you’ve interacted or entered into a business relationship with. Third parties can have subsidiaries and can contract with fourth parties. For example, departments are subsidiaries. A fourth party can contract with further parties \(referred to as nth parties—fifth, sixth, and so on\). All downstream parties \(fourth through nth parties\) carry risk in the same ways as third parties.

A vendor provides the goods or services that you use to produce or deliver your own goods or services. All vendors are third parties, but not all third parties are vendors. Here's a list of some other types of third parties:

-   Suppliers
-   Affiliates
-   Counterparties
-   Consultants
-   Partners
-   Professional services
-   Advisers
-   Franchises
-   Dealers
-   Resellers
-   Distributors
-   Customers
-   Clients
-   Outsourced staff

## Engagements

An engagement is the informal or contracted relationship that you intend to form with a third party that could potentially expose your organization to risk. The engagement outlines the services or products to be provided by the third party and other details of the relationship. These details can include the terms of payment, confidentiality requirements, and the duration of the relationship.

You can assess each engagement by using internal and external assessments. The issues, tasks, internal assessments, and external assessments are associated with the engagements.

In this example, Your Company interacts with three third parties and manages several engagements among them.

![Example hierarchy of three third parties and their associated engagements.](../image/tprm-tps-and-engagements.png)

The particular third-party engagements that you might have depend on your industry, size, and operational requirements. Each engagement brings its own set of risks and requires appropriate risk management measures \(due diligence\) to protect your interests.

-   For a detailed discussion and an example, see [Why you might have several engagements with a single third party](../concept/vrm-diffs-btw-thirdpty-and-engmnts.md).
-   For a list of the kinds of engagements that you might perform, see [Types of engagement with third parties](../../grc-workspace-vrm/reference/tprm-engagement-types.md).

## Subsidiaries

A subsidiary is an organization owned or controlled by the third party and is considered part of the third party's organization. They’re typically managed as part of the third party's risk profile. They’re different from fourth to nth parties which have contracts with a third party and aren’t owned or controlled by that third party.

Risk assessment for subsidiaries is the same as for other third parties. The risk ratings of the subsidiaries contribute to their controlling third party's score.

## IRQ—the Inherent Risk Questionnaire

During the internal assessment process, internal employees in your organization answer questions in the IRQ. These responses help with assessing the inherent risk that is associated with engaging with a third party. An inherent risk refers to the level of risk before implementing any risk mitigation measures. An IRQ supports the following activities:

-   **Determining risk factors**
    -   The nature of the services provided by the third party.
    -   The sensitivity of the data involved.
    -   The geographic location of the third party.
    -   The overall security posture of the third party.
-   **Determining scoring or rating**

    Responses to the questionnaire are often scored or rated to help quantify the inherent risk that is associated with the third party. This scoring system can aid in prioritizing risk management efforts.

-   **Decision making**

    The results of the IRQ are then used in the decision-making process. Third-party Risk \(TPR\) administrators and managers can configure IRQs to send out specific external assessment \(due diligence\) questionnaires to the third parties based on the specific responses to questions.

    -   Should you engage with the third party?
    -   What level of due diligence is required?
    -   What specific risk mitigation measures should you implement?
-   **Ongoing due diligence**

    The IRQ may also be part of ongoing management, with periodic reassessments to account for changes in the third party's operations, security practices, or other relevant factors.


## Due diligence \(DD\)

Due diligence is the process of conducting a thorough investigation or examination of the integrity, reputation, financial stability, legal compliance, operation capabilities, supply chain, and other relevant factors of a potential business partner, supplier, or vendor. Conducting due diligence on third parties is a crucial component of your comprehensive third-party risk program. You conduct due diligence to become aware of the risks that are associated with a third party so that you can confidently decide how to form your relationship. Use due diligence workflows to onboard new engagements or to reassess or retire any existing engagements. Due diligence workflows include gathering information through internal assessments, external assessments, and risk intelligence. All the scores from these steps are analyzed by the third-party risk managers to decide whether to onboard, reassess, or retire an engagement. Due diligence also has an optional contract negotiation process before closing the due diligence workflow.

See [Why you conduct due diligence](../concept/vrm-due-diligence-why.md) and [Types of due diligence](../concept/tprm-due-diligence-types.md).

## Third-party risk assessments

A third-party risk assessment \(TPRA\) is a set of questionnaires that you can send to third-party contacts or internal users to assess the third-party and engagement risks. An assessment that you send to internal users are categorized as an internal assessment. An assessment that you send to a third-party contact is called an external assessment.

Use an internal assessment to calculate the third party and engagement tiers. The classification that you use to identify the internal questionnaires in the questionnaire templates table is the Inherent Risk Questionnaire template \[irq\_template\]. You can automatically attach the required questionnaires for external assessments according to the responses that you receive from the internal assessments. You can configure this option in a questionnaire to question mapping table \[sn\_tprm\_dd\_m2m\_question\_to\_questionnaire\].

Use an external assessment to assess the risks that are associated with the third party and engagement according to the third-party contact responses that you receive. The risk ratings from an external assessment are calculated at the assessment level by using all the questionnaires that are attached to the assessment. These assessment ratings are aggregated and rolled up to the third parties and engagements. The aggregation is either MIN, MAX or AVG and can be configured in a scoring setup. Third-party contacts \(external users\) from the third-party portal `https://<myCompany>.service-now.com/svdp` respond to these external assessments.

For more information on scoring, see [Scoring calculations using the classic assessment engine](../concept/vendor-ratings-scoring.md).

## Risk intelligence providers

Risk intelligence providers generate risk scores for a variety of third-party risk domains. Your organization can purchase services from providers that return data that is analogous to personal credit scores. The scores provide insight on how trustworthy and safe a particular third party can be.

See [Integrating scores from risk intelligence providers](../concept/tprm-riskintelprvdr-overview.md).

## Risk intelligence scores

Risk intelligence scores are numerical assessments that evaluate the level of risk associated with a particular organization. These scores are generated by risk intelligence providers who collect and analyze a wide range of data sources. Scores can come in any form be it ratings or numbers. The system maps the score value to the appropriate TPRM rating. These scores can help your organization make informed decisions about engaging with third parties, managing compliance, and mitigating potential risks. Risk intelligence scores are available for third parties as of the Washington DC release. The risk ratings are calculated by the scoring rules that are associated with the engagement in the scoring setup.

## Third-party scores

Third-party scores are numerical assessments that are an aggregate of your risk intelligence scores and scores determined by external assessments \(engagement questionnaires, and third-party risk questionnaires\).

These scores help organizations make informed decisions about selecting and managing their third-party relationships, enabling alignment with their risk tolerance and compliance requirements. By assessing third-party scores, organizations can identify potential risks, prioritize due diligence efforts, and implement appropriate risk mitigation strategies.

## Risk rating components

A component is the entity for which you can assess risk. The base system includes engagements, external monitoring, subsidiaries, and third-party risk assessments. Risk is calculated for each component and then the risk is aggregated and rolled up to calculate a third-party risk rating.

A component criteria is the definition of how a component is going to be used by a third party. A component criteria is a group of components that should apply to a particular type of third party or engagement.

**Note:** You can’t add new components or modify existing ones. You can, however, define the criteria \(in terms of scoring method and weight\) to be used to assess the components.

A risk area or domain defines the type of risk to assess for a third party. This is typically aligned to the area/domain in which the third-party operates or for which they provide a product/service. For example, you might want to assess a data-management third party in terms of security risk and a bank in terms of financial risk.

A risk area criteria is the definition of how risk areas are going to be used by a Third party is defined in the risk area criteria. A third-party risk area criteria is a group \(or grouping\) of risk domains or areas that may apply to a particular type of third party. For example, security, financial, and reputational risk domains may be grouped into a risk area criteria that should apply for any third party. One can better understand and mitigate the risks that a third party poses to your organization by identifying the domains of their business to assess for risk and quantifying the importance \(weight\) of each domain.

## Scoring rules

A scoring rule provides the mechanism to apply component criteria and risk area criteria to a third-party and a risk area criteria for an engagement.

For a third party, the component criteria determine which specific components are applicable and the relevant scoring method for each component. These components may include geographic location, overall security posture, and results from internal and external assessments. The scoring methods for these components are configured in the scoring setup. For example, internal assessments for geographic location and overall security posture are part of the internal assessment process, while external assessments use methods like MIN, MAX, or AVG to calculate risk ratings. Additionally, risk intelligence scores from external providers are mapped to appropriate ratings and combined with the external assessment scores to form the overall third-party score.

For a third party, the risk area criteria determine which specific risk areas \(or domains\) are applicable and the relevant scoring method for each risk area.

These risk areas may include:

-   Data breaches
-   Downtime
-   Compliance violations
-   Supply chain disruption
-   Counterfeit parts
-   Regulatory compliance issues
-   Hidden ownership
-   Reputational risk
-   Financial risk

The scoring method for each risk area can be configured in the scoring setup and can be either MIN, MAX, or AVG, depending on the organization's preference and the nature of the risk.

For an engagement, the risk area criteria determine the applicable risk areas or domains, which include:

-   Geographic location
-   Security posture
-   Nature of services
-   Data sensitivity
-   Third-party elements

The scoring method for a specific risk area can be configured as MIN, MAX, or AVG. This method aggregates the risk ratings from internal and external assessments to determine the overall third-party score.

**Note:**

For more information on assessment configuration and scoring, see [Classic assessment configuration](../../grc-vendor-risk-implementation/concept/tprm-ongoing-config.md), [Scoring calculations using the classic assessment engine](../concept/vendor-ratings-scoring.md), and [Verifying scoring calculations using the classic assessment engine](../concept/tprm-verif-q.md).

## Third-party elements

Third-party elements are the external organizations that a third party or engagement relies on to provide goods, services, or support. These organizations can include vendors, suppliers, contractors, individuals, or any other external organization that has access to the third party or engagement's systems, data, or facilities. Any vulnerabilities or failures in these third-party elements can have a significant impact on the third party or engagement's operations, reputation, and security. By implementing these controls and addressing associated risks, organizations can enhance their ability to manage and mitigate the potential negative impacts of third parties and their third-party elements. Regularly reassessing and updating these controls is essential to adapting to changes in the business environment and regulatory landscape.

Here are some examples of Third-party elements and their associated controls and potential risks.

-   **Datacenter**

    Facilities or locations where third parties or engagements outsource the storage, processing, and management of their data and IT infrastructure.

    Controls:

    -   Vendor security assessments: Assess regularly the security measures and practices of third-party vendors providing services such as cloud hosting or data storage.
    -   Data encryption: Confirm that data stored in the datacenter is encrypted to protect it from unauthorized access.
    -   Access controls: Implement strict access controls to limit physical and virtual access to the datacenter facilities and servers.
    -   Incident response plan: Develop and maintain a comprehensive incident response plan to address any security incidents promptly.
    Risks:

    -   Data Breaches: A breach in the third-party datacenter could lead to unauthorized access and compromise of sensitive information.
    -   Downtime: Reliance on a third-party datacenter puts the organization at risk of downtime if the service provider experiences technical issues.
    -   Compliance Violations: Failure by the datacenter to adhere to industry or regulatory compliance standards could lead to legal and financial consequences for the organization.
-   **Manufacturing facility**

    Facilities or locations where third parties or engagements outsource the production or assembly of their products.

    Controls:

    -   Supplier Audits: Regularly audit and assess the security practices of suppliers providing critical components or services for the manufacturing process.
    -   Quality Assurance Standards: Enforce quality assurance standards for third-party suppliers to promote the integrity and safety of raw materials and components.
    -   Supply Chain Visibility: Maintain visibility into the entire supply chain to identify and address potential vulnerabilities.
    -   Contractual Agreements: Establish clear contractual agreements with suppliers outlining security requirements and consequences for non-compliance.
    Risks:

    -   Supply Chain Disruption: Dependency on third-party suppliers exposes the organization to the risk of supply chain disruptions, impacting production.
    -   Counterfeit Parts: Inadequate controls on the supply chain may lead to the use of counterfeit or substandard components, compromising product quality.
    -   Regulatory Compliance Issues: Failure by suppliers to comply with regulatory standards can result in legal and regulatory consequences for the manufacturing facility.
-   **Beneficial owners**

    Individuals who ultimately own or control an organization that is involved in a business relationship or transaction. These individuals may not be the registered or legal owners of the organization but have significant influence or control over its operations, decision-making, or financial affairs.

    Controls:

    -   Due Diligence: Incorporate a robust due diligence process to identify and verify beneficial owners, including background checks, document reviews, and interviews where necessary.
    -   Contractual Obligations: Include clauses in contracts with third parties that require them to disclose any changes in beneficial ownership and confirm compliance with applicable laws and regulations.
    -   Monitoring and Reporting: Establish a system for ongoing monitoring of beneficial owners to detect any changes or developments that may impact the risk profile of the third party.
    -   Training and Awareness: Provide training to relevant staff on the importance of understanding and monitoring beneficial ownership, including red flags and reporting procedures.
    -   Regulatory Compliance Program: Develop and maintain a program that verifies compliance with all relevant laws and regulations related to beneficial ownership, including reporting and disclosure requirements.
    -   Escalation Procedures: Establish clear escalation procedures for cases where concerns or irregularities related to beneficial ownership are identified, promoting timely and appropriate action.
    Risks:

    -   Hidden Ownership: Beneficial owners might deliberately conceal their ownership, making it challenging to assess the potential risks associated with their influence on the third party.
    -   Reputational Risk: If the beneficial owners have a questionable reputation, involvement with them may harm the reputation of your organization.
    -   Regulatory Compliance: Failure to comply with regulations related to beneficial ownership reporting and transparency can lead to legal and regulatory consequences.
    -   Financial Risk: Beneficial owners with financial instability or involvement in fraudulent activities may pose financial risks to the third party and, consequently, to your organization.

**Parent Topic:**[Third-party Risk Management reference](../concept/tprm-reference.md)

