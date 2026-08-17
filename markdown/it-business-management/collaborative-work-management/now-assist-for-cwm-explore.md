---
title: AI skills for Collaborative Work Management \(CWM\)
description: Learn more about the generative AI capabilities of ServiceNow Otto for CWM. These capabilities can help you save time and improve efficiency for the actions your team performs within the CWM workspace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-business-management/collaborative-work-management/now-assist-for-cwm-explore.html
release: zurich
product: Collaborative Work Management
classification: collaborative-work-management
topic_type: concept
last_updated: "2026-06-08"
reading_time_minutes: 7
keywords: [explore]
breadcrumb: [Explore, Collaborative Work Management, Strategic Portfolio Management]
---

# AI skills for Collaborative Work Management \(CWM\)

Learn more about the generative AI capabilities of ServiceNow Otto for CWM. These capabilities can help you save time and improve efficiency for the actions your team performs within the CWM workspace.

Now Assist introduced AI on the platform. As that experience has evolved, there's a new name for the experience. ServiceNow Otto® is the conversational AI platform integrated into ServiceNow workflows. It provides agentic capabilities, supports multimodal interactions across web, mobile, and messaging channels, and enables autonomous orchestration for cross-system workflows.

**Note:** Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents. For more information, see .

**Important:**

-   Not all model providers are available for customers with in-country SKUs, and some AI products/features are currently unavailable for in-country customers. For more information, see the [KB1584492](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1584492) article in the Now Support Knowledge Base. Be sure to check for model provider availability updates in future releases.
-   Some AI products/features are currently unavailable for customers in the FedRAMP, NSC DOD IL5, or Australia IRAP-Protected data centers, self-hosted customers, or in other restricted environments. For more information, see the [KB0743854](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0743854) article in the Now Support Knowledge Base. Be sure to check for availability updates in future releases.
-   Some AI products/features are currently available only for customers in some regions. Be sure to check for availability updates in future releases.
-   Some AI products and skills are not available in Regulated Markets. For more information, see [KB2593939: Regulated Markets AI Products/Skills Not Available](https://support.servicenow.com/kb?id=kb_article_view&sys_kb_id=e8d7cc82475aba90b7832920326d4362). Be sure to check for availability updates in future releases.

## Skills

-   **[Generate scrum tasks for stories](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/collaborative-work-management/generate-scrum-tasks-for-stories-cwm.md)**

    Accelerate your sprint planning by using ServiceNow Otto to generate scrum tasks based on user story descriptions and acceptance criteria. Instead of manually creating each task, you receive a relevant set of scrum tasks as a starting point for further refinement.

    Generate scrum tasks from the story form or create them inline from the List or Sprint planning views. ServiceNow Otto analyzes the user story description and acceptance criteria to propose tasks that align with the required work. For stories that already have scrum tasks, ServiceNow Otto considers existing tasks when generating new ones to avoid duplication and maintain continuity.

    You can review and edit AI-generated tasks before adding them to your story. There is no limit on the number of tasks generated, giving you flexibility to capture all necessary work breakdown items. This capability reduces the time spent on repetitive task creation and helps teams establish a consistent starting point for sprint execution.

    \[Omitted image "na-cwm-scrum-tasks-generated.png"\] Alt text: Generated scrum tasks for a user story displayed in ServiceNow Otto for CWM.

-   **[Generate acceptance criteria for stories](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/collaborative-work-management/generate-acceptance-criteria-for-stories-in-cwm.md)**

    As a product manager, generate clear, comprehensive, and testable acceptance criteria for your user stories, instead of spending hours writing and refining them manually.

    You can review and refine the suggested options to ensure they meet your story requirements without slowing down planning. By helping you streamline generating acceptance criteria as a process, this skill helps save time, improve quality, and speed up delivery with cleaner backlogs and better collaboration.

    \[Omitted image "na-cwm-acc-criteria.png"\] Alt text: Sprint planning view in CWM showing a story detail panel with the Acceptance criteria field open and the ServiceNow Otto menu displaying the Generate acceptance criteria option.

-   **[CWM Doc generation and insights](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/collaborative-work-management/generate-summarize-and-refine-content-of-docs-with-now-assist.md)**

    Generate content with ServiceNow Otto for CWM directly in your Docs using custom prompts. In addition, summarize existing sections, elaborate where needed, and refine drafts to help improve your productivity.

    You can interact with ServiceNow Otto directly in your Doc to create content, add context, or improve existing sections. This helps you draft faster, refine ideas, and keep your work relevant without leaving the page.

    -   **Work with content of the whole page**

        Some examples are:

        -   For Marketing teams: `Create a compelling product launch announcement highlighting the key benefits and emotional appeal for our target audience.`
        -   For Legal teams: `Write a plain-language summary of the privacy policy in this doc, that customers can easily understand.`
        -   For product teams: `Analyze the customer feedback comments in this Doc, group into top 5 themes, and suggest top 3 enhancements for highest impact.`
        ServiceNow Otto uses the context from your Doc page to generate a response.

    -   **Refine, elaborate, or improve the existing content within the page**

        Some examples are:

        -   If you have a list of stakeholders, you can ask `Elaborate on the scope of these roles.`
        -   `Rewrite this in a casual tone.`
        \[Omitted image "na-inline-open-text.png"\] Alt text: ServiceNow Otto inline context menu over selected text with prompt 'Elaborate on the scope of these teams.'

    -   **Take assistance on a blank page**

        Some examples are:

        1.  `Generate 5 icebreaker questions for a virtual team-building session.`
        2.  `Write a 3-paragraph blog post explaining why [industry trend] is changing how businesses operate.`
        3.  `Generate an outline for the Instagram campaign tasks for a Hackathon initiative.`

            \[Omitted image "na-blank-page-nacm.png"\] Alt text: Blank CWM Doc page with the ServiceNow Otto prompt open in the toolbar. The example prompt reads 'Generate an outline for the Instagram campaign tasks for a Hackathon initiative.'

    -   **Answer questions in the context of this Doc**

        Whether the content in the Doc is added manually or generated using ServiceNow Otto, you can ask questions to find anything in the page's context.

        For example, if you have a project charter document, you can try asking `What is the total budget of this project and which part is the most expensive?`

        \[Omitted image "cwm-nacm-ask-questions.png"\] Alt text: Ask questions in the context of the document. Here, user asks questions on project budget, in the context of a Project Charter document.

-   **[Doc summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/collaborative-work-management/summarize-doc-now-assist-cwm.md)**

    Gain insights into the contents of the page by summarizing it in CWM Docs. Whether you're reviewing long documents or preparing for meetings, Doc summarization skill helps you stay informed and efficient.

    With the Doc summarization skill, you can also elaborate and shorten content, resulting in improved content quality in the CWM Doc pages. Quickly shorten lengthy paragraphs, paraphrase bullet points, or expand on key points ensuring that your content is tailored to specific needs.

    \[Omitted image "cwm-na-doc-summarization.png"\] Alt text: CWM Doc page titled 'Phases and milestones' with the ServiceNow Otto panel showing an AI-generated summary of the document's key milestones.

-   **[Generate CWM Tasks from Docs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/collaborative-work-management/generate-tasks-cwm-docs-now-assist.md)**

    Creating tasks with detailed descriptions for your CWM Board requires significant time and manual effort. If the tasks aren’t detailed enough, it can lead to confusion and misalignment within the team, affecting their understanding of the expected outcomes. To avoid this manual effort and improve time to value, ServiceNow Otto can generate tasks for your Board using the information in your Docs. This way, you can ensure clear and comprehensive task descriptions, allowing you to focus more on execution and less on the administrative work.

    Based on the recommendations, you can ask ServiceNow Otto to perform one of the following:

    -   Generate task according to its original recommendations.
    -   Split a task recommendation into multiple tasks.
    -   Combine multiple task recommendations into one task.
    -   Remove any task recommendation.
    \[Omitted image "cwm-task-generation-now-assist.png"\] Alt text: CWM planning Doc page with the ServiceNow Otto panel showing generated tasks for a hackathon, including logistics, cross-functional meetings, and project management.

    Thus, by using the Task generation skill within CWM, you can:

    -   Remove initial roadblocks to create tasks for a CWM Board.
    -   Save time and increase productivity by automating the task creation process.

You can use Now LLM Service, Azure OpenAI, Google Gemini or Anthropic Claude on AWS as the AI model provider for all generative AI skills and AI agents. Use the Configuration Controls in [AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/ai-model-providers.md) to define which options are available, then set the skill-level preferences in the [AI Admin Hub console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/manage-large-language-models.md). For more information, see [Large language models on the ServiceNow AI Platform®](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/exploring-large-language-models.md).

## ServiceNow Otto console

An administrator can activate and manage ServiceNow Otto features and skills for the CWM workspace using the ServiceNow Otto console. For more information, see [Overview tab in AI Admin Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/configuring-now-assist.md).

## ServiceNow Otto panel in CWM workspace

A knowledge worker can use the ServiceNow Otto panel in CWM workspace. This conversational interface enables the user to generate CWM tasks from the context of a Doc page. For more information about the ServiceNow Otto panel, see [ServiceNow Otto panel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-panel-overview.md).

## What to explore next

To learn more about configuring and using ServiceNow Otto, see:

-   [Configure ServiceNow Otto for Collaborative Work Management \(CWM\) \(CWM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/collaborative-work-management/configure-now-assist-for-collaborative-work-management.md)
-   [Generate tasks from Docs in Collaborative Work Management \(CWM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/collaborative-work-management/generate-tasks-cwm-docs-now-assist.md)

