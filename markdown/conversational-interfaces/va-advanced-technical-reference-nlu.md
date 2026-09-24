---
title: \(Legacy\) Virtual Agent NLU technical reference
description: Use these topics to learn more about scripting methods, NLU system entities, and the Virtual Agent Interactions table.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/conversational-interfaces/va-advanced-technical-reference-nlu.html
release: brazil
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 2
keywords: [Virtual Agent, technical, reference]
breadcrumb: [NLU reference, \(Legacy\) Virtual Agent for NLU, Conversational Interfaces]
---

# \(Legacy\) Virtual Agent NLU technical reference

Use these topics to learn more about scripting methods, NLU system entities, and the Virtual Agent Interactions table.

Virtual Agent utilizes a queuing system to process incoming messages coming from asynchronous channels. Dedicated worker threads pull from this queue and process the messages in their own transactions. This enables Virtual Agent to scale to meet traffic volume. Virtual Agent transactions run as non-interactive \(the scriptable method **gs.isInteractive\(\)** will return false\).

Various roles and tables are available when you activate Virtual Agent. For more information, see [\(Legacy\) Plugins installed with Virtual Agent for NLU](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/installed-wth-virtual-agent.md). Virtual Agent also has a data retention policy to manage table size. For more information, see [Data management in Conversational Interfaces](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/va-data-mgmt.md)

The following technical reference topics are available.

-   **[\(Legacy\) Domain separation and Virtual Agent for NLU](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/domain-separation-virtual-agent-nlu.md)**  
Domain separation is supported in the Virtual Agent application. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
-   **[\(Legacy\) Virtual Agent roles for NLU](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/VA-roles-nlu.md)**  
Virtual Agent adds several roles for users operating as Virtual Agent administrators.
-   **[\(Legacy\) Live agent chat context variables for NLU](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/live-agent-chat-context-vars-nlu.md)**  
Use chat context variables to pass certain information from the topic to share with a live agent or to control how bot conversations are routed to live agents. Virtual Agent includes some default variables, and you can define new ones.
-   **[\(Legacy\) NLU system entities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/nlu-system-entities.md)**  
Use globally defined NLU entities to identify system information that Virtual Agent can extract from the conversation. You can define entities as "nodeless" input variables for a topic. These variables can be slot-filled from NLU service provider predictions or provided outside of the scope of the topic.
-   **[\(Legacy\) Prebuilt Virtual Agent topics, topic blocks, and ServiceNow NLU models](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/prebuilt-topics-ITSM.md)**  
Prebuilt Virtual Agent conversations \(topics\), reusable topic blocks, and ServiceNow NLU models are available for the Virtual Agent platform and various business applications, such as Customer Service Management, HR Service Delivery, IT Service Management, and more.

**Parent Topic:**[\(Legacy\) Virtual Agent NLU reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/va-parent-reference-nlu.md)

