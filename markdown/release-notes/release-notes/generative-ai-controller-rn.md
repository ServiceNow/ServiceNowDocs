---
title: Generative AI Controller release notes
description: The ServiceNow Generative AI Controller application enables you to use generative AI capabilities with third-party large language models \(LLM\) providers on the ServiceNow AI Platform. You can reduce complexity and enhance the user experience in your organization by generating and summarizing content, analyzing user sentiment, and writing unique prompts. Generative AI Controller was enhanced and updated in the Xanadu release.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 3
---

# Generative AI Controller release notes

The ServiceNow® Generative AI Controller application enables you to use generative AI capabilities with third-party large language models \(LLM\) providers on the ServiceNow AI Platform. You can reduce complexity and enhance the user experience in your organization by generating and summarizing content, analyzing user sentiment, and writing unique prompts. Generative AI Controller was enhanced and updated in the Xanadu release.

## Generative AI Controller highlights for the Xanadu release

Xanadu Patch 3

-   Review a read-only metadata log table for generative AI requests.
-   Use the improved language support for skills and capabilities, including the Dynamic Translation services and native translation by the LLMs.

Xanadu Patch 1

-   Updated prompts for capabilities, semantic filtering, and recursive summarization that improve latency and processing for Generative AI Controller capabilities and Now Assist skills.

See [Generative AI Controller](https://www.servicenow.com/docs/access?context=generative-ai-controller&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US) for more information.

## New in the Xanadu release

-   **[Metadata log table for generative AI requests](https://www.servicenow.com/docs/access?context=reference-for-generative-ai-controller&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)**

    Use the new metadata log table that includes information about the requesting conversation, the capability definition, provided feedback \(if any\), and error codes.

-   **[Translation for Now Assist](https://www.servicenow.com/docs/access?context=translation-for-now-assist&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)**

    Support users who speak different languages with new language information in LLM request metadata, better controls for Dynamic Translation, and translated text logging.


-   **Global Model selection for conversational skills**

    Enable Now Assist Admins to choose between GPT4.o and Now Assist LLM model for data routing at a global level. This ensures compliance with any regional restrictions and helpful for APAC users who may face limitations with US-based models, such as GPT-4.0.


## Changed in this release

-   **[Directions for generative AI updates for Generative AI Controller](https://www.servicenow.com/docs/access?context=reference-for-generative-ai-controller&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)**

    The prompts, which are the instructions to the large language model \(LLM\), for all four capabilities \(Generic Prompt, Generate Content, Summarization, and Sentiment Analysis\), semantic filtering, and recursive summarization have been updated.


## Activation information

Generative AI Controller is a ServiceNow AI Platform feature that is available with activation of any ServiceNow® Now Assist application. For details, see [Installing Generative AI Controller](https://www.servicenow.com/docs/access?context=installing-generative-ai-controller&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US).

## Localization information

Generative AI Controller uses [Microsoft Azure OEM for Dynamic Translation in Now Assist](https://www.servicenow.com/docs/access?context=dynamic-translation-na-ms-azure-oem&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US) for multi-language support. You can enable dynamic translation from the Now Assist Admin console.

## Related ServiceNow applications and features

-   **[Now Assist](https://www.servicenow.com/docs/access?context=platform-now-assist-landing&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)**

    Now Assist includes the Now Assist Admin console to set up, configure, monitor, and use Now Assist skills on the ServiceNow AI Platform. The Now Assist panel enables users to interact with Now Assist skills in the ServiceNow® Next Experience.

-   **[Agent Chat](https://www.servicenow.com/docs/access?context=ci-use-agent-chat&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US)**

    ServiceNow® Agent Chat provides various features that agents and requesters can use to streamline the agent and end-user chat experience. Agent Chat also provides features that managers can use to monitor and assist agents.

-   **[Customer Service Management](https://www.servicenow.com/docs/access?context=c_CustomerServiceManagement&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US)**

    The ServiceNow® Customer Service Management application enables you to provide the service and support that your external customers need. For example, your customers can communicate and get the help through the web, email, chat, telephone, and social media.

-   **[Field Service Management](https://www.servicenow.com/docs/access?context=fsm-application-landing-page&version=xanadu&pubname=xanadu-field-service-management&ft:locale=en-US)**

    ServiceNow® Field Service Management enables you to manage work orders and related tasks, resources, skills, assets, and locations. Use this application to dispatch work order tasks and agents to the customer location for performing any kind of field work, such as installing, repairing, or maintaining equipment.

-   **[Flow Designer](https://www.servicenow.com/docs/access?context=flow-designer&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US)**

    ServiceNow® Workflow Studio is a ServiceNow AI Platform feature that enables process owners to automate work. Build multi-step flows from reusable components without having to code.

-   **[HR Service Delivery](https://www.servicenow.com/docs/access?context=hr-service-delivery&version=xanadu&pubname=xanadu-employee-service-management&ft:locale=en-US)**

    The ServiceNow® HR Service Delivery application gives your employees the service experience that they deserve. By providing employees with a single place to manage their work needs while shielding them from back-end complexity, you can deliver a great experience to meet the demands of a modern-day workforce.

-   **[IT Service Management](https://www.servicenow.com/docs/access?context=r_ITServiceManagement&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

    The ServiceNow® IT Service Management \(ITSM\) solution provides scalable workflows to manage and deliver IT services to your users all through a single cloud-based platform. The ITSM solution can help increase your agents' productivity, resolve issues quickly, and improve user satisfaction.

-   **[Workspace](https://www.servicenow.com/docs/access?context=workspace-landing-page&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US)**

    ServiceNow® Workspace is a graphical user interface that puts multiple tools on one page, including the tools that agents must find, research, and use to resolve issues.


**Parent Topic:**[Intelligent Experiences release notes](intelligent-experiences-rn-landing.md)

**Parent Topic:**[Now Assist release notes](../now-assist/now-assist-rn-landing.md)

