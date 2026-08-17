---
title: AI Risk and Compliance Content Pack
description: The ServiceNow AI Risk and Compliance Content Pack provides foundational content to help organizations manage AI-related risk and compliance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/ai-risk-management/airc-content-pack.html
release: australia
product: AI Risk Management
classification: ai-risk-management
topic_type: concept
last_updated: "2026-05-19"
reading_time_minutes: 7
keywords: [AI Risk and Compliance content pack, EU AI Act, NIST AI RMF, SB 53, Colorado AI Act, regulatory framework, control objectives, risk statements]
breadcrumb: [Configure, AI Risk and Compliance, Governance, Risk, and Compliance]
---

# AI Risk and Compliance Content Pack

The ServiceNow AI Risk and Compliance Content Pack provides foundational content to help organizations manage AI-related risk and compliance.

## Content pack overview

This application provides a centralized location to browse, search, and download AI regulations and frameworks to link to your internal control objectives or risk statements and run assessments against them.

\[Omitted image "airc-frameworks.png"\] Alt text: AI regulations and frameworks. For more information refer to the text that follows.

Currently, the application offers the following:

-   **EU AI Act**

    The EU AI Act is a regulatory framework that sets common rules for the use of artificial intelligence in the European Union. It follows a risk-based approach, classifying AI systems into unacceptable, high, limited, and minimal risk categories. Higher-risk AI systems are subject to stricter requirements such as risk management, transparency, human oversight, and ongoing monitoring. Authority documents and citations for the EU AI Act are available in the content pack. Pre-shipped control objective and risk statement mappings are included. for the EU AI Act. The EU AI Act content is structured into 13 chapters and contains 113 articles covering risk-based regulatory requirements for AI systems.

-   **NIST AI RMF**

    The NIST AI Risk Management Framework \(AI RMF\) provides voluntary guidance for managing risks associated with AI systems throughout their lifecycle. It focuses on building trustworthy AI by addressing risks related to governance, fairness, reliability, security, privacy, and transparency. The framework is organized around four core functions: Govern, Map, Measure, and Manage.

    Preventive controls dominate in Govern, Map, and Manage, as these functions focus on policies, risk identification, and mitigation planning. Detective controls are concentrated in Measure and the monitoring aspects of Manage, focusing on ongoing assessments, audit trails, and reporting.

    AI-specific risk libraries address both common and AI-specific risks, such as algorithmic bias, model drift, data integrity, and cybersecurity threats.

-   **Transparency in Frontier Artificial Intelligence Act \(SB 53\)**

    California Senate Bill 53 establishes transparency and safety requirements for developers of frontier AI systems. It requires developers to implement safety and security protocols and publicly disclose information about their AI systems and safety practices. Authority documents, agency mappings, and citations for SB 53 are available in the content pack.

-   **Colorado Artificial Intelligence Act \(SB 205\)**

    The Colorado Artificial Intelligence Act establishes requirements for developers and deployers of high-risk AI systems, including risk assessments, impact evaluations, and disclosure obligations to consumers affected by AI-driven decisions. Authority documents, agency mappings, and citations for the Colorado AI Act are available in the content pack.


|Category|EU AI Act|NIST AI RMF|California TFAIA \(SB 53\)|Colorado AI Act|
|--------|---------|-----------|--------------------------|---------------|
|Structure|The EU AI Act contains 13 chapters, 113 articles, 13 annexes.|4 functions, 19 categories, 72 sub-categories.|4 core mandates plus whistleblower and penalty provisions.|Part 17 C.R.S., 7 sections \(§§ 1701-1707\).|
|Type|Binding law \(extraterritorial\).|Voluntary framework \(US\).|Binding state law.|Binding state law \(in transition\).|
|Applies to|Providers and deployers of AI in the EU, tiered by risk.|Any organization; all AI systems and use cases.|Developers of frontier \(large compute\) AI models.|Developers and deployers of high-risk AI in consequential decisions.|
|Status and key dates|In force; high-risk and transparency duties apply 2 Aug 2026.|AI RMF 1.0 \(2023\) plus Generative AI Profile \(2024\).|Effective 1 Jan 2026.|SB 24-205 replaced by SB 26-189; effective 1 Jan 2027 \(AG rulemaking pending\).|
|Core requirements|Risk management, data governance, documentation, human oversight, conformity assessment.|Govern, Map, Measure, Manage lifecycle controls.|Public safety framework, transparency reports, critical-incident reporting, whistleblower protection.|Consumer notice and appeal rights, transparency, recordkeeping, vendor oversight.|

## Control objective coverage across frameworks

The AI Control Objective Universe defines 300 control objectives spanning every AI lifecycle stage. Of these, 162 objectives \(54%\) map to all four frameworks and form the core set of universal controls.

|Framework|Control objectives linked|
|---------|-------------------------|
|NIST AI RMF|258|
|EU AI Act|249|
|Colorado AI Act|224|
|California AI Act|176|

Each control objective is rationalized against regulation using the following approach.

1.  Controls map to provisions whose intent and requirement align, not by keyword match \(semantic alignment\).
2.  One control can satisfy multiple articles, and one article can support multiple controls \(many-to-many model\).
3.  Original article and section IDs, for example EU Art. 9 or NIST MAP 2.3, are preserved for audit traceability \(framework-native citations\).
4.  The coverage count signals which controls are universal, since four-framework controls form the compliance backbone \(cross-jurisdictional validation\).

## AI risk domains

AI risk is organized into seven domains. Each domain is a distinct category of AI-specific risk with its own drivers, regulatory obligations, and control requirements. The seven domains collectively define 28 level 2 risk statements.

|Domain|Description|
|------|-----------|
|Security and Cyber|Threats that exploit AI as an attack surface, including adversarial inputs, training data poisoning, model theft, and denial-of-service attacks. Unlike traditional cybersecurity, AI attacks can remain undetected while corrupting outputs at scale.|
|Compliance|Risk of violating laws governing AI use, including data protection regulations \(GDPR, CCPA\), sector-specific rules \(HIPAA\), and emerging AI legislation \(EU AI Act\). The regulatory landscape evolves rapidly, so compliance today might not hold in 18 months.|
|Algorithmic|Risks inherent to algorithm design and training, including structural bias, poor generalization \(overfitting\), accuracy degradation over time \(drift\), and deep-learning opacity that makes decisions difficult to audit or explain.|
|Data|Risks tied to the data that trains and feeds AI systems, including corrupted or incomplete training inputs, mishandled personal data in pipelines, non-representative datasets that embed bias, and cyberattack exposure through large data stores.|
|Operational|Day-to-day risks of running AI in production, including model performance degrading without retraining, infrastructure that cannot scale, legacy system incompatibility, service outages, and shortages of qualified AI engineers.|
|Ethical and Societal|Broader human impact, including amplification of racial, gender, and socioeconomic bias, job displacement, erosion of accountability in high-stakes decisions, privacy intrusions, and unintended social harms.|
|AI Business Risks|Strategic and commercial consequences, including reputational damage from harmful outputs, IP theft if model weights are stolen, over-reliance on third-party AI vendors, competitive disruption, and increasing compliance costs.|

## Key Value Benefits

AI Control Tower consolidates the EU AI Act, NIST AI RMF, California TFAIA, and Colorado AI Act into a single source of truth for AI governance.

|Capability|Description|
|----------|-----------|
|Single source of truth|One inventory of AI assets, models, and agents across the enterprise reduces shadow AI.|
|Common controls alignment|A control mapped once satisfies EU AI Act, NIST AI RMF, California TFAIA, and Colorado AI Act requirements simultaneously, without duplicate work.|
|Speed to compliance|A pre-mapped foundation activates on day one instead of building a compliance framework from scratch.|

## Regulatory support statement

**Note:**

The ServiceNow Risk products help customers address regulatory requirements under various jurisdictions. However, we do not guarantee compliance and customers are ultimately responsible for their own compliance with applicable regulations.

ServiceNow aims to provide software updates for new or updated major regulations and requirements within twelve to eighteen months of the regulation's publication. For regulations for which ServiceNow provides a level of support in the base system, ServiceNow aims to provide software updates for minor regulatory changes within 12 months and for major regulatory changes within up to 18 months depending on scope and impact. We differentiate between typical regulatory content updates, which do not require software updates or enhancements, and regulatory updates, which do require software updates or enhancements. Content updates are generally delivered on a shorter cadence than if software update or enhancement is required for the regulatory update or change.

**Related topics**  


[Install AI Risk and Compliance content](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/ai-risk-management/install-ai-risk-content-pack.md)

[Activate or update NIST Risk Management Framework](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/ai-risk-management/activate-or-update-nist-using-the-content-accelerator.md)

[Activate or update EU Artificial Intelligence Act](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/ai-risk-management/activate-or-update-eu-artificial-intelligence-act.md)

[Activate or update the Colorado Artificial Intelligence Act](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/ai-risk-management/activate-or-update-colorado-ai-act.md)

[Activate or update the Transparency in Frontier Artificial Intelligence Act \(SB 53\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/ai-risk-management/activate-or-update-sb53.md)

