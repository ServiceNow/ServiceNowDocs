---
title: Reusable skills in adaptive desktop actions
description: Reusable skills save steps from completed adaptive desktop actions, allowing future requests with similar intent to run those steps with new data. This accelerates repeated tasks and reduces AI token consumption.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/reusable-skills-adaptive-da.html
release: brazil
topic_type: concept
last_updated: "2026-09-28"
reading_time_minutes: 3
keywords: [reusable skills, adaptive desktop actions, recording, matching skill, saved steps]
breadcrumb: [Adaptive desktop actions for desktop and web, Explore, AI Desktop Actions, AI agents and agentic workflows, Enable AI Experiences]
---

# Reusable skills in adaptive desktop actions

Reusable skills save steps from completed adaptive desktop actions, allowing future requests with similar intent to run those steps with new data. This accelerates repeated tasks and reduces AI token consumption.

**Important:**

This feature is in beta. It may change as the feature evolves. Report issues through ServiceNow Support.

Generative AI may produce inaccurate or incomplete information. Always validate AI-generated content.

## Reusable skills overview

**Note:** This feature is managed by the sn\_desktop\_core.enable\_reusable\_assets system property. This is set to `false` by default. You must set the value to `true` to use this feature. For more information, see [Components installed with AI Desktop Actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/components-installed-with-agentic-desktop.md).

When the AI agent runs an adaptive desktop action, it plans each step at run time. Planning every step on every run takes time, even when you repeat a task that the AI agent completed before.

When the sn\_desktop\_core.enable\_reusable\_assets system property is set to `true`, the application records the steps of each run and saves the recording to your instance. The instance divides the recording into skills, one for each sub-task. For example, a single run might produce one skill for logging in to an application and another skill for filling in a form.

The next time you submit a request with the same intent but different data, the AI agent searches for a matching skill. If it finds one, it runs the saved steps with the data from your new request instead of planning each step again. The AI agent uses the defined desktop action approach and reduces AI token consumption.

## Key benefits

Reusable skills provide the following benefits:

-   Shorter run time for repeated tasks, because a matching skill runs saved steps instead of planning each step.
-   Saves AI token consumption.
-   No change to how you work, because you describe tasks the same way and the AI agent searches for matching skills automatically.

## Supported applications and actions

Reusable skills work with the following types of applications:

-   Native macOS applications, such as TextEdit and Notes
-   Installed applications that provide macOS accessibility information
-   Web applications in Google Chrome

UI actions are saved as skills because they run on the UI. These include selecting an element, entering text in a field, or choosing an item from a list.

Non-UI actions, such as working with Microsoft Excel, Microsoft Word, or the file system, aren't saved as skills because they run in the background. The AI agent plans those actions each time the task runs.

## Taking control while a skill runs

If you take control during a skill's execution and then return it to the AI agent, the AI agent replans them. The agent does not use the saved steps. This applies only to the current skill. Subsequent skills in your request run their saved steps as usual \(unless you take control again\).

For example, your request uses two skills with five steps each. You take control during step two of the first skill, then return control. The AI agent replans the remaining steps of the first skill \(using adaptive desktop action approach\). The agent runs the second skill using the saved steps \(using defined desktop actions approach\).

**Note:** For information on the Take control feature, see [Take control of AI Desktop Actions execution](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/control_ai_desktop_actions_execution_adaptive.md).

## Considerations

Consider the following when you use reusable skills:

-   The AI agent might not find a matching skill even when one exists for the same intent. When this happens, the AI agent plans and runs the steps as usual and records the run.
-   Saved steps rely on the accessibility information that a desktop application provides, such as field labels or a unique ID for each field. If a desktop application doesn't provide this information, saved steps might enter data in the wrong field. For example, a phone number might be entered in an email address field. This consideration doesn't apply to web applications in Google Chrome.

**Related topics**  


[Adaptive desktop actions for desktop and web-based tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/ai_desktop_actions_adaptive.md)

[Execute adaptive desktop actions for desktop and web](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/use_ai_desktop_actions_adaptive.md)

