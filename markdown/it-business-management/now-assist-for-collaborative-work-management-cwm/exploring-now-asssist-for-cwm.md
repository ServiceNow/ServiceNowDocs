---
title: Exploring Now Assist for Collaborative Work Management \(CWM\)
description: Learn more about the generative AI capabilities of Now Assist for CWM and how they can help you save time and improve efficiency for the actions your team performs within the CWM workspace.
locale: en-US
release: zurich
product: Now Assist for Collaborative Work Management \(CWM\)
classification: now-assist-for-collaborative-work-management-cwm
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Now Assist for CWM, Strategic Portfolio Management]
---

# Exploring Now Assist for Collaborative Work Management \(CWM\)

Learn more about the generative AI capabilities of Now Assist for CWM and how they can help you save time and improve efficiency for the actions your team performs within the CWM workspace.

## Skills

-   **[Generate scrum tasks for stories](../task/generate-scrum-tasks-for-stories-cwm.md)**

    Accelerate your sprint planning by using Now Assist to generate scrum tasks based on user story descriptions and acceptance criteria. Instead of manually creating each task, you receive a relevant set of scrum tasks as a starting point for further refinement.

    Generate scrum tasks from the story form or create them inline from the List or Sprint planning views. Now Assist analyzes the user story description and acceptance criteria to propose tasks that align with the required work. For stories that already have scrum tasks, Now Assist considers existing tasks when generating new ones to avoid duplication and maintain continuity.

    You can review and edit AI-generated tasks before adding them to your story. There is no limit on the number of tasks generated, giving you flexibility to capture all necessary work breakdown items. This capability reduces the time spent on repetitive task creation and helps teams establish a consistent starting point for sprint execution.

    ![Generated scrum tasks for a user story displayed in Now Assist for CWM.](../images/na-cwm-scrum-tasks-generated.png)

-   **Generate formulas from natural language**

    Create formula columns faster by describing your calculation in natural language and letting Now Assist generate the formula for you.

    Instead of manually building complex formulas, type what you want to calculate in the Formula Builder panel. For example, enter descriptions like `days between start date and end date` or `total estimated hours for all subtasks`. Now Assist analyzes your description and generates a valid formula using the available columns in your List view.

    Review the generated formula to verify that it matches your intent. Insert the formula into the editor with a single click, then make any adjustments if needed. This capability removes the need to memorize formula syntax, making calculated columns accessible to team members of all technical skill levels.

    ![image.na-cwm-formula-instruction-side-panel]

-   **[Generate acceptance criteria for stories](../task/generate-acceptance-criteria-for-stories-in-cwm.md)**

    As a product manager, generate clear, comprehensive, and testable acceptance criteria for your user stories, instead of spending hours writing and refining them manually.

    You can review and refine the suggested options to ensure they meet your story requirements without slowing down planning. By helping you streamline generating acceptance criteria as a process, this skill helps save time, improve quality, and speed up delivery with cleaner backlogs and better collaboration.

    ![Sprint planning view in CWM showing a story detail panel with the Acceptance criteria field open and the Now Assist menu displaying the Generate acceptance criteria option.](../images/na-cwm-acc-criteria.png)

-   **[CWM Doc generation and insights](../task/generate-summarize-and-refine-content-of-docs-with-now-assist.md)**

    Generate content with Now Assist for CWM directly in your Docs using custom prompts. In addition, summarize existing sections, elaborate where needed, and refine drafts to help improve your productivity.

    You can interact with Now Assist directly in your Doc to create new content, add context, or improve existing sections. This helps you draft faster, refine ideas, and keep your work relevant without leaving the page.

    -   **Work with content of the whole page**

        Some examples are:

        -   For Marketing teams: `Create a compelling product launch announcement highlighting the key benefits and emotional appeal for our target audience.`
        -   For Legal teams: `Write a plain-language summary of the privacy policy in this doc, that customers can easily understand.`
        -   For product teams: `Analyze the customer feedback comments in this Doc, group into top 5 themes, and suggest top 3 enhancements for highest impact.`
        Now Assist uses the context from your Doc page to generate a response.

    -   **Refine, elaborate, or improve the existing content within the page**

        Some examples are:

        -   If you have a list of stakeholders, you can ask `Elaborate on the scope of these roles.`
        -   `Rewrite this in a casual tone.`
        ![CWM Doc page showing the Now Assist inline context menu open over selected stakeholder text, with the prompt 'Elaborate on the scope of these teams.' entered in the text field.](../images/na-inline-open-text.png)

    -   **Take assistance on a blank page**

        Some examples are:

        1.  `Generate 5 icebreaker questions for a virtual team-building session.`
        2.  `Write a 3-paragraph blog post explaining why [industry trend] is changing how businesses operate.`
        3.  `Generate an outline for the Instagram campaign tasks for a Hackathon initiative.`

            ![Blank CWM Doc page with the Now Assist prompt open in the toolbar, showing the example prompt 'Generate an outline for the Instagram campaign tasks for a Hackathon initiative.'](../images/na-blank-page-nacm.png)

    -   **Answer questions in the context of this Doc**

        Whether the content in the Doc is added manually or generated using Now Assist, you can ask questions to find anything in the page's context.

        For example, if you have a project charter document, you can try asking `What is the total budget of this project and which part is the most expensive?`

        ![Ask questions in the context of the document. Here, user asks questions on project budget, in the context of a Project Charter document.](../images/cwm-nacm-ask-questions.png)

-   **[Doc summarization](../task/summarize-doc-now-assist-cwm.md)**

    Gain insights into the contents of the page by summarizing it in CWM Docs. Whether you're reviewing long documents or preparing for meetings, Doc summarization skill helps you stay informed and efficient.

    With the Doc summarization skill, you can also elaborate and shorten content, resulting in improved content quality in the CWM Doc pages. Quickly shorten lengthy paragraphs, paraphrase bullet points, or expand on key points ensuring that your content is tailored to specific needs.

    ![CWM Doc page titled 'Phases and milestones' with the Now Assist panel showing an AI-generated summary of the document's key milestones.](../images/cwm-na-doc-summarization.png)

-   **[Generate CWM Tasks from Docs](generate-tasks-cwm-docs-now-assist.md)**

    Creating tasks with detailed descriptions for your CWM Board requires significant time and manual effort. If the tasks aren’t detailed enough, it can lead to confusion and misalignment within the team, affecting their understanding of the expected outcomes. To avoid this manual effort and improve time to value, Now Assist can generate tasks for your Board using the information in your Docs. This way, you can ensure clear and comprehensive task descriptions, allowing you to focus more on execution and less on the administrative work.

    Based on the recommendations, you can ask Now Assist to perform one of the following:

    -   Generate task according to its original recommendations.
    -   Split a task recommendation into multiple tasks.
    -   Combine multiple task recommendations into one task.
    -   Remove any task recommendation.
    ![CWM planning Doc page with the Now Assist panel showing generated tasks for a hackathon, including logistics, cross-functional meetings, and project management.](../images/cwm-task-generation-now-assist.png)

    Thus, by using the Task generation skill within CWM, you can:

    -   Remove initial roadblocks to create tasks for a CWM Board.
    -   Save time and increase productivity by automating the task creation process.

You can use Now LLM Service, Now LLM Long Term Stable models \(LTS\), Azure OpenAI, Google Gemini or Anthropic Claude on AWS as the AI model provider for all Now Assist skills and AI agents. Use the Configuration Controls in [AI Control Tower](https://www.servicenow.com/docs/access?context=ai-model-providers&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US) to define which options are available, then set the skill-level preferences in the [Now Assist Admin console](https://www.servicenow.com/docs/access?context=manage-large-language-models&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US). For more information, see [Large language models on the ServiceNow AI Platform®](https://www.servicenow.com/docs/access?context=exploring-large-language-models&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

## Now Assist Admin console

An administrator can activate and manage Now Assist features and skills for the CWM workspace using the Now Assist Admin console. For more information, see [Overview tab in Now Assist Admin](https://www.servicenow.com/docs/access?context=configuring-now-assist&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

## Now Assist panel in CWM workspace

A knowledge worker can use the Now Assist panel in CWM workspace. This conversational interface enables the user to generate CWM tasks from the context of a Doc page. For more information about the Now Assist panel, see [Now Assist panel](https://www.servicenow.com/docs/access?context=now-assist-panel-overview&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

## What to explore next

To learn more about configuring and using Now Assist for CWM, see:

-   [Configure Now Assist for Collaborative Work Management \(CWM\)](../task/configure-now-assist-for-collaborative-work-management.md)
-   [Generate tasks from Docs in Collaborative Work Management \(CWM\)](generate-tasks-cwm-docs-now-assist.md)
-   [Now Assist for Collaborative Work Management \(CWM\) reference](now-assist-for-cwm-reference.md#)

