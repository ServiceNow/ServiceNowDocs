---
title: Client script summarization
description: Client script summarization uses Now Assist to create easy-to-understand explanations of client scripts within the UI Builder editor. This feature helps creators to learn what a script does without needing to read the complex code.
locale: en-US
release: australia
product: Now Assist for Creator
classification: now-assist-for-creator
topic_type: concept
last_updated: "2026-05-09"
reading_time_minutes: 1
breadcrumb: [Explore, UI generation, Use generative AI, Now Assist for Creator, Vibe coding and AI app development on the ServiceNow AI Platform, Building applications]
---

# Client script summarization

Client script summarization uses Now Assist to create easy-to-understand explanations of client scripts within the UI Builder editor. This feature helps creators to learn what a script does without needing to read the complex code.

## How client script summarization works

Client scripts in UI Builder control the behavior of pages and components. Because these scripts can be complex, creators who are unfamiliar with JavaScript or the specific script logic may find it difficult to understand what a script does or how it affects the experience. Client script summarization addresses this by generating an AI-powered explanation on demand, directly within the client script editor panel.

The feature is powered by a Now Assist skill and is accessed through a dedicated right-hand panel in the **Edit client script** dialog. When a creator selects a client script and requests an explanation, the system sends the script to the skill endpoint and returns a structured summary.

## Structure of the generated summary

The summary returned by Now Assist is organized into two sections:

-   **Summary**

    A concise, plain-language description of what the script does. For example, a script that resets a modal form would be described in terms of its effect on the user experience, without requiring the reader to parse individual API calls.

-   **Code explanation**

    A more detailed, line-by-line or block-by-block walkthrough of how the script achieves its purpose. This section describes which APIs are used, what each state variable does, and which parameters are or are not used by the script.


## Benefits

Client script summarization provides the following benefits:

-   **Faster onboarding**

    Creators who are new to a project or to JavaScript can quickly learn about the existing scripts.

-   **Reduced context-switching**

    Explanations appear inside the editor panel, so creators don't have to leave UI Builder to look up documentation.

-   **Improved script literacy**

    Creators with limited coding experience gain visibility into what scripts do, which helps them make informed decisions about whether to modify or replace a script.


**Parent Topic:**[Exploring UI generation](exploring-ui-generation.md)

**Related topics**  


[Summarize a client script using Now Assist](../task/client-script-summarization-generation.md)

[Use case: Summarize a client script using Now Assist](use-case-client-script-summarization.md)

