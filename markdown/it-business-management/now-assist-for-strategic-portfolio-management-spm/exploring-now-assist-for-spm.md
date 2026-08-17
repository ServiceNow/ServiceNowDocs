---
title: Exploring ServiceNow Otto for Strategic Portfolio Management
description: Use ServiceNow Now Assist skills and AI agents in multiple SPM workspaces to transform Strategic Portfolio Management \(SPM\) into a continuous value engine-embedding intelligence across every stage and to provide optimize resources and smarter investments resulting in delivering continuous value.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/it-business-management/now-assist-for-strategic-portfolio-management-spm/exploring-now-assist-for-spm.html
release: yokohama
product: Now Assist for Strategic Portfolio Management \(SPM\)
classification: now-assist-for-strategic-portfolio-management-spm
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 7
keywords: [Explore Now Assist for SPM, Now Assist for SPM overview, Now Assist for SPM skills, Feedback summarization, Multi feedback summarization, Project Doc Summarization and Actions, Planning Item Doc Summarization and Actions, or EAP Doc Summarization and Actions]
breadcrumb: [ServiceNow Otto for Strategic Portfolio Management, Strategic Portfolio Management]
---

# Exploring ServiceNow Otto for Strategic Portfolio Management

Use ServiceNow® Now Assist skills and AI agents in multiple SPM workspaces to transform Strategic Portfolio Management \(SPM\) into a continuous value engine-embedding intelligence across every stage and to provide optimize resources and smarter investments resulting in delivering continuous value.

## Skills

The ServiceNow Otto for SPM application includes the generative AI skills and features that enable your product, project, portfolio, and demand managers to leverage Now Assist skills so that they can streamline their processes and workflows.

-   **[Target generation skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-business-management/now-assist-for-strategic-portfolio-management-spm/generate-targets-for-goal.md)**

    Generate measurable targets from goal's information and optional context with the Target generation skill in Strategic Planning Workspace. The skill automatically populates key fields in the target creation form, ensuring precision and alignment to the goal. This enables teams to define clear and measurable outcomes and accelerate the target creation process.

    \[Omitted image "target-generation-skill.gif"\] Alt text: Generate targets in Strategic Planning Workspace using Target generation skill.

-   **[Identify similar records skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-business-management/now-assist-for-strategic-portfolio-management-spm/identify-similar-demand-records.md)**

    Detect similar demand records using the identify similar records Now Assist skill. The skill identifies similar demand records based on contextual similarity in the name, description, and business case content, with a minimum 85% similarity threshold. It also excludes the outdated and irrelevant records. You can trigger the skill by selecting the **Identify similar demands** button on the demand record page.

    The similar demand records identified by Now Assist are displayed in the Similar Demands related list as well as in a message banner at the top of the record page.

    \[Omitted image "similar-demand-new-color.png"\] Alt text: List of similar records identified by Now Assist.

-   **[Refine records](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-business-management/now-assist-for-strategic-portfolio-management-spm/refine-text-with-write-planning-item-skill.md)**

    Improve record quality by enabling AI assistance in the rich and long fields of Product idea, Demands, Epic, Projects, Capability, Features, Stories, Project tasks, Risks, Strategic priorities, Goals, Targets, Initiatives, Feedback, Milestones, and Story forms. You can enable text refinement with the **Elaborate** and **Shorten** options on the records to support portfolio, project, product, demand managers, and agile team members in creating and editing records content more effectively.

    \[Omitted image "write-planning-items-skill-sp.png"\] Alt text: Refine text using Refine records skill.

-   **[Agile story generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-business-management/now-assist-for-strategic-portfolio-management-spm/generate-stories-from-epics-now-assist-eap.md)**

    Generates high-quality story recommendations for an epic or feature using the Agile story generation skill in the EAP workspace. Now Assist uses the name, description, Docs content, and any existing stories of the epic or feature to provide story recommendations. Based on the recommendations, you can ask Now Assist to perform one of the following:

    -   Split a story recommendation into multiple stories.
    -   Combine multiple story recommendations into one story.
    -   Generate stories according to its original recommendations.
    -   Remove any story recommendation.
    -   Suggest modification of details within the recommendation such as story title, persona, and description.
    -   Suggest generating a new story recommendation.
    \[Omitted image "eap-na-06-story-save.png"\] Alt text: List of stories created by Now Assist.

    Thus, by using the Story generation skill of Now Assist, you can:

    -   Remove initial roadblocks to create stories for an epic or a feature.
    -   Save time and increase productivity by automating the story creation process.
    -   Ensure completeness of stories by covering personas, outcomes, and acceptance criteria.
    The Agile story generation skill is supported starting with the Yokohama patch 3 release and Strategic Planning v4.5.0. If you are on earlier versions of the Yokohama release, you can activate the Story generation skill, which generates stories from Epics only.

-   **[Multi feedback summarization or Feedback summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-business-management/now-assist-for-strategic-portfolio-management-spm/feedback-summary-sentiment-topics.md)**

    Provides your product managers with a concise and informative summary of the lengthy customer feedback comments. The product managers can generate a summary from the name and description of one or multiple feedback records so that they can quickly understand the feedback context. The generated summary can be directly converted to an execution item. Now Assist can generate a summary from the feedback only if the feedback has at least 60 words in the fields that are used for the input data. The 60-word minimum optimizes the experience by verifying that there’s enough information to make a summary.

    The following example shows a summarization of multiple feedback records by using the multi feedback summarization skill.

    \[Omitted image "multi-feedback-summarization-example.png"\] Alt text: AI-generated summary for multiple feedback records using the multi feedback summarization skill.

-   **[Project doc summarization, Planning Item doc summarization, or EAP doc summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-business-management/now-assist-for-strategic-portfolio-management-spm/summarize-documents-genai-skill-spw.md)**

    Provides your product managers with a concise and informative summary of the selected or complete text by using Now Assist in Docs. Your product managers can summarize, elaborate, or shorten the selected or complete content on Docs to quickly understand the key information by using the Project doc summarization \(Project Workspace\), Planning item doc summarization \(Strategic Planning\), or EAP doc summarization \(Enterprise Agile Planning\) skill.

    \[Omitted image "genai-docs-skill-nowassist.png"\] Alt text: Now Assist generated summary of text in Docs.

-   **[Project insights generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-business-management/now-assist-for-strategic-portfolio-management-spm/email-project-summary-skill-pw.md)**

    Monitor the progress and changes in each project through the Project insights generation skill. With minimal effort, your project managers can schedule a cadence for generating project insights and receive it via email. They can track key elements such as the milestones, resource assignments, projects, and project tasks. They can also prioritize key elements to focus on. They can also decide the cadence of receiving project insight emails.

    \[Omitted image "email-project-summary-template.png"\] Alt text: Now Assist generated project insights in Project Workspace.

-   **[Conversational experiences for demand creation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-business-management/now-assist-for-strategic-portfolio-management-spm/demand-creation-using-now-assist.md)**

    Simplify the process of creating a Demand within the Employee Service Management \(ESC\) portal by using the Now Assist conversational catalog creation capability.

    -   Avoid searching through the list of catalog items to find the right item for demand creation.
    -   Answer contextual questions in the chat to auto-populate the relevant fields in the Demand form.
    If Microsoft Teams and Mobile are enabled as a display location for Now Assist in Virtual Agent, users can use the conversational experience to create a demand in those applications too.

    **Note:** This skill is available within the Platform category of the AI Admin Hub console.


## AI Admin Hub console

An administrator can use the AI Admin Hub console in Strategic Planning Workspace to activate and manage Now Assist features and skills in Workspace. For more information about the AI Admin Hub console, see [AI Admin Hub console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/configuring-now-assist.md).

## AI agents

The ServiceNow AI agents use LLMs \(Large Language Models\) to process tasks, from basic responses to complex problem-solving and optimize the live agent workflows. For more information on Now Assist AI agents, see [Using AI agent or agentic workflows in ServiceNow Otto for Strategic Portfolio Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-business-management/now-assist-for-strategic-portfolio-management-spm/using-na-spm-ai-agents.md).

**Related topics**  


[Exploring Now Assist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/exploring-now-assist-platform.md)

[Configure ServiceNow Otto for Strategic Portfolio Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-business-management/now-assist-for-strategic-portfolio-management-spm/configure-now-assist-for-spm.md)

[Using ServiceNow Otto for Strategic Portfolio Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-business-management/now-assist-for-strategic-portfolio-management-spm/using-now-assist-for-spm.md)

[Using AI agent or agentic workflows in ServiceNow Otto for Strategic Portfolio Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-business-management/now-assist-for-strategic-portfolio-management-spm/using-na-spm-ai-agents.md)

[ServiceNow Otto for SPM reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-business-management/now-assist-for-strategic-portfolio-management-spm/now-assist-spm-reference.md)

[AI Agent Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/ai-agent-studio.md)

