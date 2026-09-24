---
title: AI Risk and Compliance
description: The AI Risk and Compliance \(AIRC\) application gives your risk and compliance team a dedicated workspace to assess AI-specific risks, attest to controls, demonstrate regulatory compliance, and manage AI-related cases for the AI capabilities and other AI assets your organization deploys.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/platai-ai-risk-and-compliance.html
release: brazil
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 3
keywords: [AI Risk and Compliance, AIRC, AI governance, AI risk management, AI compliance, Now Assist governance, AI Control Tower, EU AI Act, NIST AI RMF]
breadcrumb: [Establishing AI governance, Enable AI Experiences]
---

# AI Risk and Compliance

The AI Risk and Compliance \(AIRC\) application gives your risk and compliance team a dedicated workspace to assess AI-specific risks, attest to controls, demonstrate regulatory compliance, and manage AI-related cases for the AI capabilities and other AI assets your organization deploys.

## Why AI Risk and Compliance matters

Generative AI introduces a class of risks that traditional risk and control frameworks weren't built to address. AI systems can produce biased outputs, expose sensitive data, or fall under emerging regulations such as the EU AI Act, NIST AI RMF, Colorado's SB 205, or California's SB 53. Without a coordinated way to assess and document those risks, organizations either slow AI adoption or accept exposure they can't measure.

The AI Risk and Compliance application gives your risk and compliance team the structure needed to govern AI responsibly while keeping AI deployments moving. Impact and risk assessments quantify exposure for each AI system, model, and dataset. A regulatory content pack maps requirements from major AI frameworks to your internal controls. AI case management captures investigations, exceptions, and incidents without disrupting development.

## How AI Risk and Compliance works with AI Control Tower

AI Risk and Compliance and AI Control Tower work as a coordinated governance framework. AI Control Tower serves as the system of record for AI assets, managing inventory, life cycle state, and progression across phases. AI Risk and Compliance performs the independent risk, regulatory, and control governance activities that determine whether an AI system can advance through those phases.

A typical interaction follows this pattern: an AI use case is submitted through the Employee Center. AI Control Tower creates the inventory record and manages the asset through its life cycle. AI Risk and Compliance evaluates impact and risk during assessment, validates that required controls are implemented during build, and approves or blocks deployment based on residual risk. After deployment, AIRC monitors for new risks and manages the cases and inquiries that arise.

Neither application replaces the other; together they provide consistent oversight from demand through life cycle closure.

## Key capabilities

-   **Intake and risk-based classification**

    Intake requests provide a structured entry point for new AI use cases, models, and datasets. Responses to screening questions in the Use and Purpose section drive an initial risk classification \(High, Medium, Low, or Unacceptable\), so the appropriate level of governance attention is applied from the start of the life cycle.

-   **Impact and risk assessments**

    Risk Assessment Methodologies \(RAMs\) define the scoring frameworks used to classify AI systems and evaluate the individual risks tied to each asset. Default RAMs cover regulatory classification and quantitative risk scoring across AI systems, models, and datasets. Administrators can configure custom RAMs to match organizational requirements.

-   **Regulatory content pack**

    The AI Risk and Compliance Content Pack ships with authority documents and citations for the EU AI Act, NIST AI RMF, California's SB 53, and Colorado's SB 205. Citations are mapped to control objectives across frameworks, so a single attested control can satisfy requirements from multiple regulations.

-   **Control attestation and issue management**

    Controls associated with AI assets can be attested as part of the build and validation phase. Issues that surface during attestation are tracked and remediated, and policy exceptions can be raised and documented when controls can't be implemented as designed.

-   **AI case management**

    AI cases and inquiries support investigation, exception handling, and regulatory response after AI systems are deployed. Cases capture governance events, document decisions, and trigger reassessment when changes in risk warrant it, without breaking life cycle continuity.

-   **AI Risk and Compliance workspace**

    The workspace is the central hub for AI risk and compliance managers. The Risk and Compliance dashboard shows risk posture and assessment status. The Operations dashboard tracks controls, issues, and exceptions. The AI Cases dashboard surfaces active investigations and inquiries.


## Explore further

For details on configuring and using AI Risk and Compliance, see [AI Risk and Compliance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/ai-risk-and-compliance.md).

