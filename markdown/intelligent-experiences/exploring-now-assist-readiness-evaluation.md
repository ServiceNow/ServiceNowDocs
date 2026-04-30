---
title: Exploring Now Assist Readiness Evaluation
description: The Now Assist Readiness Evaluation app automates assessment processes, evaluates data readiness impacting implementation, and provides actionable insights to promote adopting Now Assist quickly. The app enables you to assess whether updates, installations, or customizations of your instance could affect implementation. The assessments provide direct hyperlinks to improve any issues found.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-09-18"
reading_time_minutes: 6
keywords: [explore, Now Assist Readiness Evaluation, Now Assist Readiness Evaluation app, Now Assist Readiness, Now Assist assessment, GenAI assessment, AI assessment, Agentic AI assessment]
breadcrumb: [Now Assist Readiness Evaluation, Enable AI experiences]
---

# Exploring Now Assist Readiness Evaluation

The Now Assist Readiness Evaluation app automates assessment processes, evaluates data readiness impacting implementation, and provides actionable insights to promote adopting Now Assist quickly. The app enables you to assess whether updates, installations, or customizations of your instance could affect implementation. The assessments provide direct hyperlinks to improve any issues found.

## Now Assist Readiness Evaluation overview

The Now Assist Readiness Evaluation app is a solution designed to simplify and automate the agentic AI and Now Assist implementation assessment process. The app helps to determine whether your organization's instance is ready to implement generative and agentic AI features in Now Assist. Previously, manually assessing your organization's instance readiness was time consuming and took significant effort. Now, you can use the Now Assist Readiness Evaluation app to automate gathering, processing, and analyzing instance data so that you can review your instance readiness more quickly. The app provides results within seconds, helping to reduce manual effort and promoting rapid and reliable assessments. The app includes assessment information for Now Assist by separating agentic AI solutions and generative AI solutions by tabs. Agentic AI solution information appears in the agentic\_AI ![](../image/agentic-ai-icon.png) tab and generative AI solution information appears in the ![](../image/na-assessment-icon.png) tab.

The following list details what agentic solutions for Now Assist are evaluated and assessed after the necessary scheduled jobs have run.

-   **Agentic AI for Now Assist for IT Service Management \(ITSM\)**

    Evaluates whether customizations on ITSM-related parent tables \(such as Incident and Task\) may interfere with AI agent behavior, task execution, or decision-making. The assessment identifies and flags high-risk customizations to help promote seamless agent operations and stable instance performance. Each finding includes interactive hyperlinks to the impacted records, enabling you to review, validate, and address potential issues without navigating away from the dashboard.

-   **Agentic AI for Now Assist for Customer Service Management \(CSM\)**

    Assesses whether customizations on CSM-specific tables \(such as Case and Interaction\) impact AI agent functionality. The assessment evaluates data completeness, field modifications, and scripting issues that may hinder agent-driven tasks and offers targeted estimated remediation to maintain agent efficacy. Each assessment finding includes interactive hyperlinks to the affected records, enabling you to navigate, validate, and resolve issues directly from the dashboard.


The following list details what generative AI Now Assist products are evaluated and assessed after the necessary scheduled jobs have run.

-   **Now Assist for AI Search**

    This feature provides insights into the status and configuration of AI Search, such as active or inactive profiles, widget versions, and estimated remediation efforts. The assessment also evaluates Knowledge Management by assessing article counts, categories, group restrictions, and top searches or articles viewed. Additionally, the assessment highlights areas for improvement, offering actionable feedback to enhance knowledge quality and hygiene.

-   **Now Assist for Virtual Agent \(VA\)**

    This feature checks if Virtual Agent is live, tracks active topics and catalog items, and identifies barriers to conversational functionality. The assessment highlights opportunities to convert non-conversational items to conversational ones and tracks automation in catalog items, along with estimated remediation efforts.

-   **Now Assist for IT Service Management \(ITSM\)**

    This feature reviews customizations and configurations in the Incident and Task tables, such as fields, UI actions, and scripts. The assessment highlights changes made, tracks data completeness, and provides key metrics to improve accuracy and consistency in ITSM processes. The assessment also specifies the estimated remediation effort required and reports the language used in the instance.

-   **Now Assist for Customer Service Management \(CSM\)**

    This feature reviews customizations in the Case and Task tables, tracks changes to fields, and monitors data completeness for key fields. The assessment provides insights into past cases and field-filling percentages, helping improve data accuracy in Customer Service Management. The assessment also reports the estimated remediation effort needed and the language used in the instance.

-   **Now Assist for HR Service Delivery \(HRSD\)**

    This feature analyzes customizations in the HR Core Case and Task tables, tracking field-level changes and promoting data completeness for critical fields. The assessment provides insights into historical HR Core cases, including field population percentages, to enhance data accuracy in HRSD processes. Additionally, the feature identifies estimated remediation efforts required and reports the languages used within the instance.

    **Note:** Additional configuration is needed to run the HRSD assessment successfully. For more information, see [Configure the Now Assist Readiness Evaluation guided setup](../task/configure-nare-guided-setup.md).


## Now Assist Readiness Evaluation users

|User|Description|
|----|-----------|
|Admin|Admins use the Now Assist Readiness Evaluation app to prepare for implementing generative and agentic AI features in Now Assist.|

## Now Assist Readiness Evaluation benefits

|Benefit|Feature|Users|
|-------|-------|-----|
|Run scheduled jobs for applicable agentic and generative AI Now Assist products from a single assessment job.|[Run the GenAI/AgenticAI Assessment scheduled job](../task/run-genai-agenticai-assessment-scheduled-job.md)|Admins|
|Review an overall dashboard of your issues before implementing agentic and generative AI Now Assist.|[Using Now Assist Readiness Evaluation dashboard](using-now-assist-readiness-evaluation-dashboard.md)|Admins|
|View your overall go or no-go status to implement Now Assist generative AI skills or agentic AI agents, and view the go or no-go status' issues categorized by percentage.|[Assessing readiness status](assessing-go-no-go.md)|Admins|
|Review summary information of overall implementation readiness.|[Reviewing your Now Assist assessment](reviewing-now-assist-assessment.md) and [Reviewing your Agentic AI assessment](reviewing-agentic-ai-assesment.md)|Admins|
|Improve the gaps for implementation by using the hyperlinks found in the assessments to fix issues. Direct hyperlinks to records and tables make it easier to validate, investigate, or act without switching contexts.|[Reviewing your Now Assist assessment](reviewing-now-assist-assessment.md) and [Reviewing your Agentic AI assessment](reviewing-agentic-ai-assesment.md)|Admins|
|Receive an estimated remediation effort of development work days to fix issues before implementation.|[Reviewing your Now Assist assessment](reviewing-now-assist-assessment.md) and [Reviewing your Agentic AI assessment](reviewing-agentic-ai-assesment.md)|Admins|

## What to explore next

To learn more about configuring and using the Now Assist Readiness Evaluation app, see:

-   [Configuring Now Assist Readiness Evaluation](configuring-now-assist-readiness-evaluation.md)
-   [Using Now Assist Readiness Evaluation](using-now-assist-readiness-evaluation.md)

