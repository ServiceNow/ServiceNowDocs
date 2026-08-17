---
title: Client script summarization
description: Client script summarization uses ServiceNow Otto to create easy-to-understand explanations of client scripts within the UI Builder editor. This feature helps creators to learn what a script does without needing to read the complex code.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/client-script-summarization.html
release: australia
product: UI Builder
classification: ui-builder
topic_type: concept
last_updated: "2026-08-17"
reading_time_minutes: 1
breadcrumb: [Explore, UI generation, UI Builder, Builder library, Developing your application, Building applications]
---

# Client script summarization

Client script summarization uses ServiceNow Otto to create easy-to-understand explanations of client scripts within the UI Builder editor. This feature helps creators to learn what a script does without needing to read the complex code.

## How client script summarization works

Client scripts in UI Builder control the behavior of pages and components. Because these scripts can be complex, creators who are unfamiliar with JavaScript or the specific script logic may find it difficult to understand what a script does or how it affects the experience. Client script summarization addresses this by generating an AI-powered explanation on demand, directly within the client script editor panel.

The feature is powered by a ServiceNow Otto skill and is accessed through a dedicated right-hand panel in the **Edit client script** dialog. When a creator selects a client script and requests an explanation, the system sends the script to the skill endpoint and returns a structured summary.

## Structure of the generated summary

The summary returned by Otto is organized into two sections:

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


**Parent Topic:**[Exploring UI generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/ui-builder/exploring-ui-generation.md)

**Related topics**  


[Summarize a client script using ServiceNow Otto](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/ui-builder/client-script-summarization-generation.md)

[Use case: Summarize a client script using ServiceNow Otto](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/ui-builder/use-case-client-script-summarization.md)

