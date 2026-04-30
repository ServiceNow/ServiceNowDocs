---
title: Exploring Now Assist for Strategic Portfolio Management \(SPM\)
description: Use Now Assist for Strategic Portfolio Management \(SPM\) in multiple SPM workspaces to includes the skills and features of generative AI that help you enhance productivity while reducing the time and effort that you put in to work on the same tasks manually. You can also schedule an email to receive project summaries of your projects.
locale: en-US
release: xanadu
product: Now Assist for Strategic Portfolio Management \(SPM\)
classification: now-assist-for-strategic-portfolio-management-spm
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 5
keywords: [Explore Now Assist for SPM, Now Assist for SPM overview, Now Assist for SPM skills, Feedback summarization, Multi feedback summarization, Project Doc Summarization and Actions, Planning Item Doc Summarization and Actions, or EAP Doc Summarization and Actions]
breadcrumb: [Now Assist for Strategic Portfolio Management \(SPM\), Strategic Portfolio Management]
---

# Exploring Now Assist for Strategic Portfolio Management \(SPM\)

Use Now Assist for Strategic Portfolio Management \(SPM\) in multiple SPM workspaces to includes the skills and features of generative AI that help you enhance productivity while reducing the time and effort that you put in to work on the same tasks manually. You can also schedule an email to receive project summaries of your projects.

## Skills

The Now Assist for SPM application includes the generative AI skills and features that enable your product, project, portfolio, and demand managers to leverage Now Assist skills so that they can streamline their processes and workflows.

-   **[Refine planning items content using write planning item skill](../task/refine-text-with-write-planning-item-skill.md)**

    Improve record quality by enabling AI assistance in the description field across these Strategic Planning Workspace forms: Product idea, Demand, Epic, Project, Capability, Feature, and Story. You can enable text refinement with the **Elaborate** and **Shorten** options on planning items to support product managers and agile team members in creating and editing content more effectively.

-   **[Agile story generation](https://www.servicenow.com/docs/access?context=epic-to-story-generation-now-assist-skill&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)**

    Generates high-quality story recommendations for an epic or feature using the Agile story generation skill in the EAP workspace. Now Assist uses the name, description, Docs content, and any existing stories of the epic or feature to provide story recommendations. Based on the recommendations, you can ask Now Assist to perform one of the following:

    -   Split a story recommendation into multiple stories.
    -   Combine multiple story recommendations into one story.
    -   Generate stories according to its original recommendations.
    -   Remove any story recommendation.
    -   Suggest modification of details within the recommendation such as story title, persona, and description.
    -   Suggest generating a new story recommendation.
    ![List of stories created by Now Assist.](../images/eap-na-06-story-save.png)

    Thus, by using the Story generation skill of Now Assist, you can:

    -   Remove initial roadblocks to create stories for an epic or a feature.
    -   Save time and increase productivity by automating the story creation process.
    -   Ensure completeness of stories by covering personas, outcomes, and acceptance criteria.
    The Agile story generation skill is supported starting with the Yokohama patch 3 release. If you are on earlier versions of the Yokohama release, you can activate the Story generation skill, which generates stories from Epics only.

-   **[Multi feedback summarization or Feedback summarization](https://www.servicenow.com/docs/access?context=now-assist-feedback-summary&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)**

    Provides your product managers with a concise and informative summary of the lengthy customer feedback comments. The product managers can generate a summary from the name and description of one or multiple feedback records so that they can quickly understand the feedback context. The generated summary can be directly converted to an execution item. Now Assist can generate a summary from the feedback only if the feedback has at least 60 words in the fields that are used for the input data. The 60-word minimum optimizes the experience by verifying that there’s enough information to make a summary.

    The following example shows a summarization of multiple feedback records by using the multi feedback summarization skill.

    ![AI-generated summary for multiple feedback records using the multi feedback summarization skill.](../images/multi-feedback-summarization-example.png "Multi feedback summarization skill")

-   **[Project doc summarization, Planning Item doc summarization, or EAP doc summarization](https://www.servicenow.com/docs/access?context=now-assist-genai-doc-skills&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)**

    Provides your product managers with a concise and informative summary of the selected or complete text by using Now Assist in Docs. Your product managers can summarize, elaborate, or shorten the selected or complete content on Docs to quickly understand the key information by using the Project doc summarization \(Project Workspace\), Planning item doc summarization \(Strategic Planning\), or EAP doc summarization \(Enterprise Agile Planning\) skill.

    ![Now Assist generated summary of text in Docs.](../images/genai-docs-skill-nowassist.png "Now Assist in Docs")

-   **[Email project summary](https://www.servicenow.com/docs/access?context=now-assist-email-summary-skill&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)**

    Monitor the progress and changes in each project through the Email project summary skill. With minimal effort, your project managers can schedule a cadence for generating a project summary and receive it via email. They can track key elements such as the milestones, resource assignments, projects, and project tasks. They can also prioritize key elements to focus on. They can also decide the cadence of receiving project summary emails.

    ![Now Assist generated summary of a project in Project Workspace.](../images/email-project-summary-template.png "Now Assist Email project summary skill")

-   **[Conversational experiences for demand creation](https://www.servicenow.com/docs/access?context=now-assist-platform-conv-experience&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US).**

    Simplify the process of creating a Demand within the Employee Service Management \(ESC\) portal by using the Now Assist conversational catalog creation capability.

    -   Avoid searching through the list of catalog items to find the right item for demand creation.
    -   Answer contextual questions in the chat to auto-populate the relevant fields in the Demand form.
    If Microsoft Teams and Mobile are enabled as a display location for Now Assist in Virtual Agent, users can use the conversational experience to create a demand in those applications too.

    **Note:** This skill is available within the Platform category of the Now Assist Admin console.


## Now Assist Admin console

An administrator can use the Now Assist Admin console in Strategic Planning Workspace to activate and manage Now Assist features and skills in Workspace. For more information about the Now Assist Admin console, see [Now Assist Admin console](https://www.servicenow.com/docs/access?context=configuring-now-assist&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US).

## AI agents

The ServiceNow AI agents use LLMs \(Large Language Models\) to process tasks, from basic responses to complex problem-solving and optimize the live agent workflows. For more information on Now Assist AI agents, see [Using AI agent agentic workflows in Now Assist for Strategic Portfolio Management \(SPM\)](using-na-spm-ai-agents.md).

**Related topics**  


[Exploring Now Assist](https://www.servicenow.com/docs/access?context=exploring-now-assist-platform&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)

[Configure Now Assist for Strategic Portfolio Management \(SPM\)](../task/configure-now-assist-for-spm.md)

[Using Now Assist for Strategic Portfolio Management \(SPM\)](using-now-assist-for-spm.md)

[Using AI agent agentic workflows in Now Assist for Strategic Portfolio Management \(SPM\)](using-na-spm-ai-agents.md)

[Now Assist for SPM reference](../reference/now-assist-spm-reference.md)

[AI Agent Studio](https://www.servicenow.com/docs/access?context=ai-agent-studio&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)

