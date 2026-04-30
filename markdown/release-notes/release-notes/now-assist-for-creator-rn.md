---
title: Now Assist for Creator release notes
description: The ServiceNow Now Assist for Creator application includes generative AI skills that can make developing on the ServiceNow AI Platform more efficient. Now Assist for Creator was enhanced and updated in the Yokohama release.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-07-23"
reading_time_minutes: 11
---

# Now Assist for Creator release notes

The ServiceNow® Now Assist for Creator application includes generative AI skills that can make developing on the ServiceNow AI Platform more efficient. Now Assist for Creator was enhanced and updated in the Yokohama release.

## Now Assist for Creator highlights for the Yokohama release

[Yokohama Patch 11](../quality/yokohama-patch-11.md)

-   Review changes to Now Assist usage measurement.
-   Create, edit, and deploy fully functional ServiceNow applications using the Build Agent in the ServiceNow IDE.
-   Generate catalog items conversationally and preview them during the creation process with Now Assist in Catalog Builder.
-   Choose an AI model provider for all Now Assist for Code skills in the script editor.

[Yokohama Patch 8](../quality/yokohama-patch-8.md)

-   Removed the now.assist.creator role as a requirement for test generation.

[Yokohama Patch 6](../quality/yokohama-patch-6.md)

-   Use Google Gemini and Anthropic Claude on AWS as AI model providers for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.

    **Note:** Additional AI model providers are supported for the following Now Assist for Creator skills:

    -   App generation
    -   App summarization
    -   Catalog item generation
    -   Code generation
    -   Flow generation
    -   Flow summarization
    -   Playbook generation
    -   Process Mining
    -   RPA bot generation
    -   Spoke generation
    -   Test generation

[Yokohama Patch 3](../quality/yokohama-patch-3.md)

-   Summarize what a flow or subflow does by using generative AI.
-   Generate playbooks from inputs that refer to active actions, flows, subflows, content from installed spokes, or activity definitions.
-   Create automation and UI components in Now Assist for app generation.
-   Use the code explain and summarize feature of Now Assist for Code to explain and summarize the code. This feature is supported by both Now LLM Service and the Azure OpenAI model providers.
-   Use the Client Script Summarization skill to generate a high-level summary and a detailed explanation of a client script.

[Yokohama Patch 1](../quality/yokohama-patch-1.md)

-   Enable your users to create applications by using the Now Assist for app generation skill even if they don't have the admin role.
-   Use the improved application preview before generating an application by using the Now Assist for app generation skill.
-   Enable your RPA Desktop Design Studio users to create and edit automations and activities, and extend automation logic flow with Now Assist for RPA Hub.
-   Enable your ServiceNow Studio users to generate a summary of an app.
-   Use the **Quick Actions** button in the Now Assist for Code enabled script editor to edit code and add comments.
-   Use the prompt modal in inline or floating mode with Now Assist for Code.
-   Now Assist for Code now supports both Now LLM Service and Azure OpenAI model providers. When you select the Azure OpenAI model provider, all requests for the Now Assist for Code model are redirected to Azure OpenAI for evaluation and response. Additionally, you get access to the Code Explain and Code Summarize features.
-   Use the auto-complete feature of Now Assist for Code to get contextually relevant code suggestions while typing.

See [Now Assist for Creator](https://www.servicenow.com/docs/access?context=now-assist-for-creator-landing&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US) for more information.

**Important:** Now Assist for Creator is available in ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Yokohama release

-   **[Build Agent, an autonomous AI agent for ServiceNow application development](https://www.servicenow.com/docs/access?context=build-agent&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US)**

    Build Agent, located in a chat panel within the ServiceNow IDE, functions as an autonomous AI agent capable of independently generating a complete ServiceNow application. It can handle various code-related tasks, such as rewriting tables, explaining code, validating and improving existing applications, fixing application errors, and more.

-   **[Generate catalog items conversationally with Now Assist in Catalog Builder](https://www.servicenow.com/docs/access?context=create-catalog-item-using-now-assist&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US)**

    Create catalog items and record producers efficiently using the conversational interface within Catalog Builder. Communicate your requirements and specifications for your desired catalog items through guided conversation. Now Assist for catalog generation helps to simplify and streamline the catalog item creation process.


-   **[New third-party AI model provider options available for Now Assist](https://www.servicenow.com/docs/access?context=manage-large-language-models&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    Google Gemini 2.0 Flash, Google Gemini 2.5 Pro, and AWS Claude 3.7 Sonnet are available for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI GPT-4.1 and GPT-4.1 mini.

    **Note:** Additional AI model providers are supported for the following Now Assist for Creator skills:

    -   App generation
    -   App summarization
    -   Catalog item generation
    -   Code generation
    -   Flow generation
    -   Flow summarization
    -   Playbook generation
    -   Process Mining
    -   RPA bot generation
    -   Spoke generation
    -   Test generation

-   **[Add columns to existing tables with Now Assist for app generation](https://www.servicenow.com/docs/access?context=sns-app-gen-review-apps&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US)**

    Add columns to existing tables in Now Assist for app generation.

-   **[Add flows in Now Assist for app generation](https://www.servicenow.com/docs/access?context=sns-app-gen-add-flow&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US)**

    Create a flow when creating an application in Now Assist for app generation. Enhance an existing application by adding a flow.

-   **[Add workspaces in Now Assist for app generation](https://www.servicenow.com/docs/access?context=sns-app-gen-add-workspace&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US)**

    Create a workspace when creating an application in Now Assist for app generation. Enhance an existing application by adding a workspace.

-   **[Configure an event handler with Now Assist](https://www.servicenow.com/docs/access?context=configure-an-event-handler-with-now-assist&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US)**

    Use Now Assist in UI Builder to configure event handlers. At present, you can configure links to a destination, open or close modals, and view load requested event handlers using Now Assist in UI Builder.

-   **[Create a flow or subflow from an image](https://www.servicenow.com/docs/access?context=exploring-flow-generation-with-images&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US)**

    Create a flow or a subflow from an image by using Now Assist. Capture the detailed process in an image and attach the image to Workflow Studio. Now Assist generates a preview of the flow that you can modify and regenerate.

-   **[Enable Code Explain and Summarize](https://www.servicenow.com/docs/access?context=enable-code-explain-and-summarize&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US)**

    Support Code Explain and Code Summarize features with the Now LLM Service. Ensure compliance with any regional restrictions and help APAC users who may face limitations with US-based models.

-   **[Summarize client scripts](https://www.servicenow.com/docs/access?context=client-script-summarization-generation&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US)**

    Use client script summary generation to get both a high-level summary and a detailed explanation of the client scripts.

-   **[Summarize a flow or subflow](https://www.servicenow.com/docs/access?context=flow-summarization&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US)**

    Summarize what a flow or subflow does by using generative AI.

-   **[Support additional components in the RPA Bot generation skill](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1808191)**

    Support 97 additional components with Now Assist for RPA Hub.

-   **[Support Retrieval Augmented Generation \(RAG\) with playbook generation](https://www.servicenow.com/docs/access?context=playbook-assist&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US)**

    Generate playbooks from inputs that refer to custom actions, flows, subflows, content from installed spokes, or activity definitions. Include the names of commonly used and recently published actions, subflows, flows, and activity definitions that are available on your instance in your playbook generation requests.

-   **[Time out long running app summaries](https://www.servicenow.com/docs/access?context=sns-now-assist-app-summarize-landing&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US)**

    Time out app summary generation after two minutes.

-   **[Use the Now LLM Service with Now Assist for app generation](https://www.servicenow.com/docs/access?context=sns-exploring-now-assist-gen&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US)**

    Choose Now LLM Service or OpenAI GPT-4o to ensure compliance with any regional restrictions. This feature is helpful for APAC users who may face limitations with US-based models, such as GPT-4.0.


-   **[Create applications in ServiceNow Studio by using Now Assist with the guided app creator role](https://www.servicenow.com/docs/access?context=sns-app-gen-using-landing&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US)**

    Enable your users with the guided app creator role \(in addition to users with the admin role\) to create applications with the Now Assist for app generation skill.

-   **[Create and edit automations and activities and extend automation logic flow in RPA Desktop Design Studio by using Now Assist](https://www.servicenow.com/docs/access?context=rpa-now-assist-studio&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US)**

    Use the Robotic Process Automation \(RPA\) bot generation skill in RPA Desktop Design Studio to create and edit automations and activities through short text instructions and preview options. This feature helps you to accelerate automation development because new and existing users can develop and build faster automations.

    Enhance the automation logic by using the **Build automation** option, starting from components or from an empty design surface that is based on text instructions.

-   **[Summarize an app in ServiceNow Studio](https://www.servicenow.com/docs/access?context=sns-now-assist-app-summarize-landing&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US)**

    Use the new Now Assist for app summary generation skill to quickly generate a summary of an app. You can then copy the summary to the app description, and then use the summaries to find duplicate or redundant apps.

-   **[Generate and edit automated tests faster by using the Test generation skill](https://www.servicenow.com/docs/access?context=test-generation-intro&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US)**

    Use the new Test generation skill to generate automated tests faster by simply describing your test requirements. Review the generated test, make edits directly, or refine your original prompt to generate a revised version of the test.


## UI changes

-   **[Find files faster when previewing an application in the Now Assist for app generation skill](https://www.servicenow.com/docs/access?context=sns-app-gen-using-landing&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US)**

    Filter the app files list and narrow the search when previewing an application that is created with the Now Assist for app generation skill.

-   **[Enhanced visibility of apps created by the Now Assist for app generation skill](https://www.servicenow.com/docs/access?context=sns-app-gen-review-apps&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US)**

    On the ServiceNow Studio home page, apps that are generated by AI display the AI indicator.


## Changed in this release

-   **[Changes to Now Assist usage measurement](https://www.servicenow.com/docs/access?context=monitoring-now-assist-usage&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

    Starting with Yokohama Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).

-   **[Some Now Assist skills, agents, and agentic workflows are turned on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    The skills are automatically available to appropriate role users for the application, such as ITIL roles on incident forms or change forms. This change simply activates the skill and does not touch the roles that may be needed to use the skill. The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills and agentic workflows are turned on automatically.
    -   Existing customers who are upgrading \(starting with Yokohama Patch 11\): Any previously unconfigured skill, agent, or agentic workflow is turned on automatically \(the AI asset was never configured and turned on, then turned off again\). Previously configured skills and agentic workflows that were turned on, then off, remain inactive.
-   **[Configure ACLs for AI agents and agentic workflows](https://www.servicenow.com/docs/access?context=aia-security-implementation&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    Configure the access control lists for who can discover and trigger AI agents and agentic workflows in their guided setups in AI Agent Studio. You can determine whether an AI agent or agentic workflow behaves as a dynamic user or as an AI user. You can also specify if an AI agent or agentic workflow can be available to all authenticated users or publicly available.


-   **[More easily identify changes when previewing and updating applications](https://www.servicenow.com/docs/access?context=sns-app-gen-using-landing&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US)**

    When previewing an application, any requested changes made by the Now Assist for app generation skill are listed when the preview pane loads.

-   **[Edit applications without having to change the scope manually](https://www.servicenow.com/docs/access?context=sns-app-gen-review-apps&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US)**

    When editing applications, the Now Assist for app generation skill now changes the scope that you’re working in to the scope of the application automatically.

-   **[More easily query Analytics Generation](https://www.servicenow.com/docs/access?context=analytics-assist-landing-page&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US)**

    Analytics Generation now uses a semantic filter instead of Natural Language Query \(NLQ\), resulting in less rigid requirements for queries.


-   **[Improved query engine for Analytics Generation](https://www.servicenow.com/docs/access?context=analytics-assist-landing-page&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US)**

    Starting in Yokohama Patch 1, analytics generation supports GPT-4o for generating queries, to provide better accuracy in responses. These improvements include support for up to two levels of dot-walking based on user utterances.


## Removed in this release

[Yokohama Patch 12](../quality/yokohama-patch-12.md)

-   Spoke generation has been removed from Now Assist for Creator. See the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website for additional information.

## Activation information

Install Now Assist for Creator by requesting it from ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Related ServiceNow applications and features

-   **[App Engine Studio](https://www.servicenow.com/docs/access?context=aes-overview&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US)**

    ServiceNow® App Engine Studio \(AES\) is a development tool for creators of varying skill levels to build applications that meet the immediate needs of your organization.

-   **[Integration Hub](https://www.servicenow.com/docs/access?context=integrationhub&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US)**

    Automate integration tasks using ServiceNow components for ServiceNow® Workflow Studio, or develop custom integrations. A separate subscription is required.

-   **[Integration Hub available spokes](https://www.servicenow.com/docs/access?context=spokes-list&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US)**

    Activate spokes to enhance your Workflow Studio experience with integration-specific content. Use prebuilt flows and actions to automate your integrations or create your own integration automation.

-   **[MID Server](https://www.servicenow.com/docs/access?context=mid-server-landing&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US)**

    The Management, Instrumentation, and Discovery \(MID\) Server is a Java application that runs as a Windows service or UNIX daemon on a server in your local network. The ServiceNow® MID Server enables communication and the movement of data between a ServiceNow instance and external applications, data sources, and services.

-   **[Now Assist](../analytics-intelligence-reporting/now-assist-rn.md)**

    Use AI recommendations to select the next component in your flow. The system generates recommendations based on the current position in the flow and the flow component names listed before.

-   **[Process Automation Designer](https://www.servicenow.com/docs/access?context=process-automation-designer&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US)**

    ServiceNow® Playbooks enables process owners to author cross-enterprise workflows and create a single, unified process. You can also use Playbooks to provide end users with a simplified, task-oriented view of your process.

-   **[Robotic Process Automation \(RPA\) Hub](https://www.servicenow.com/docs/access?context=rpa-main-landing-page&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US)**

    Use the ServiceNow® Robotic Process Automation \(RPA\) Hub to enable end-to-end automation for your organization. With a combination of UI interactions, element-based automations, and APIs that interact between the various business applications, you can emulate user actions and eliminate mundane and repetitive human activities.


**Parent Topic:**[App development and low-code release notes](build-automate-rn-landing.md)

**Parent Topic:**[Now Assist and agentic AI release notes](../now-assist/now-assist-rn-landing.md)

