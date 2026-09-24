---
title: Getting started with AI on the ServiceNow AI Platform
description: Prepare your instance for AI by learning about the applications and roles involved, exploring the AI Admin Center, and evaluating your data and configuration readiness.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/platai-getting-started-ai.html
release: brazil
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 3
keywords: [Now Assist, Now Assist Center, AI readiness, AI implementation, AI administration roles, readiness evaluation]
breadcrumb: [Enable AI Experiences]
---

# Getting started with AI on the ServiceNow AI Platform

Prepare your instance for AI by learning about the applications and roles involved, exploring the AI Admin Center, and evaluating your data and configuration readiness.

Implementing AI on the ServiceNow AI Platform begins with learning what is available, confirming that your environment is ready, and building the foundation that all AI capabilities depend on. A few key steps prepare your data, verify your applications, and align your organization's AI policies with your implementation.

Now Assist introduced AI on the platform. As that experience has evolved, there's a new name for the experience. ServiceNow Otto® is the conversational AI platform integrated into ServiceNow workflows. It provides agentic capabilities, supports multimodal interactions across web, mobile, and messaging channels, and enables autonomous orchestration for cross-system workflows.

## ServiceNow® AI implementation

A successful AI implementation depends on three things:

-   Familiarity with the applications and features that make up the AI experience
-   Clearly assigned roles for everyone involved in managing AI on the ServiceNow AI Platform
-   A shared vocabulary for the concepts behind generative AI and agentic AI capabilities

Platform administrators, AI administrators, data stewards, knowledge managers, and business stakeholders each play a distinct part in an AI implementation. Existing platform engineers and domain experts can implement AI when they have clear role definitions and the right access.

To review the applications and features that make up the AI experience, the roles for everyone who manages AI on the platform, and a glossary of terms, see [Implementing AI on the ServiceNow AI Platform](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/sn-ai-implementation-landing.md).

## AI Admin Center

AI Admin Center is a single workspace where you set up, manage, and optimize your generative AI solutions on the ServiceNow AI Platform. The home page is tailored to your environment, role, and business objectives, and surfaces AI-generated actionable use cases to help you implement AI adoption and best practices. AI Agent Advisor analyzes your instance data to identify leading automation opportunities and estimates the potential time savings for each one.

AI Admin Center also tracks performance of recently activated AI solutions with usage trend lines, provides direct access to AI readiness assessments, and links to other AI applications on the platform such as AI Agent Studio, AI Control Tower, and the AI Admin Hub.

To set up, manage, and optimize your generative AI solutions from one workspace and act on the automation opportunities AI Agent Advisor surfaces, see [AI Admin Center \(formerly Now Assist Center\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/now-assist-center-landing-page.md).

## Assessing your AI readiness

-   **AI Readiness Evaluation**

    The AI Readiness Evaluation app automates the assessment process by gathering, processing, and analyzing instance data, then delivering results within seconds with direct hyperlinks to improve any issues found. Each assessment provides an overall go or no-go status along with estimated remediation effort.

-   **Data readiness**

    High-quality data that is complete, accurate, and contextually relevant is the foundation for delivering precise and trustworthy AI responses. Evaluate whether your records, knowledge articles, and catalog items are prepared for AI.

-   **Application readiness**

    AI depends on several platform applications to deliver AI capabilities. Preparing these applications for AI spans the following areas:

    -   Knowledge base readiness: Verify that articles are current, well-structured with consistent templates, and populated with complete metadata so that ServiceNow Otto can deliver accurate responses across AI Search and Q&amp;A Genius Results.
    -   Service Catalog readiness: Confirm that catalog items have clear names, user-friendly descriptions, and manageable variable counts, and identify which items can be made conversational for use with ServiceNow Otto for Virtual Agent.
    -   AI Search readiness: Verify that AI Search is active, configure search sources and search profiles, and install ServiceNow Otto for AI Search to power Q&amp;A Genius Results across your portals.
    -   ServiceNow Otto for Virtual Agent readiness: Install and configure an LLM assistant, review your Virtual Agent topic inventory, and migrate NLU topics to LLM to enable AI-driven conversational experiences.

To prepare your knowledge base, Service Catalog, AI Search, and Virtual Agent for AI, see [Application readiness for Now Assist on the ServiceNow AI Platform](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/sn-ai-impl-app-readiness.md).

