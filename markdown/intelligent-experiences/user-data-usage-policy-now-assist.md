---
title: User data usage policy for Now Assist
description: Now Assist is designed to keep user data safe and secure. You can also mask sensitive data or opt-out of sharing data for model improvements.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
keywords: [Now Assist, user, data, usage, policy, mask sensitive data, data sharing]
breadcrumb: [Now Assist reference, Now Assist, Enable AI experiences]
---

# User data usage policy for Now Assist

Now Assist is designed to keep user data safe and secure. You can also mask sensitive data or opt-out of sharing data for model improvements.

## How your data is sent and stored

Your AI workloads are securely sent using Transport Layer Security \(TLS\) 1.2 from your ServiceNow instance to one of three centralized ServiceNow compute hubs \(datacenters with GPUs for AI workloads\), where the AI prediction processing takes place. The data used to generate the response is deleted from the compute hubs after the response has been generated. The result is then returned to the ServiceNow instance.

The input and output data isn’t cached or stored on the compute hub and is transient.

Your data isn’t commingled with other customer data when using Now LLM Service for generative AI.

Also, there’s no commingling of data for domain-separated instances when you use Generative AI services.

When appropriate, ServiceNow might leverage third-party endpoint services \(for example Azure OpenAI Service\) to augment Now LLM Service to power Now Assist capabilities. Azure OpenAI is a third-party model, but policies same as the company's, apply, as it's hosted in our compute hubs.

Further, to confirm quality of service, ServiceNow might use Azure-hosted GPUs for Now LLM Service capacity bursting in case of high customer demand. Data processed by third-party endpoints isn’t subject to use or access by third-party providers and are operated within the ServiceNow network boundary.

## Mask sensitive data

Sensitive data can be masked before sending it to LLMs using Now Assist for Data Privacy. To learn more, see [Configuring Data Privacy for Now Assist](https://www.servicenow.com/docs/access?context=configure-now-assist-data-privacy&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

After you enable the plugin, it’s designed to mask sensitive data before it’s sent to the LLM, but could result in less accurate results because the specific data isn’t included within the prompt.

**Note:** This plugin, within the context of generative AI products, doesn’t mask the sensitive data that exists in records within your instance, nor does it help prevent new sensitive data from being stored on the instance itself.

ServiceNow might use Retrieval Augmented Generation \(RAG\) for selected AI features \(for example NowAssist for AI Search\) and passes information to the LLM based on what the requester can access within the system. If a user searches for something in the portal using Now Assist in AI Search, AI Search finds the article and then sends that to the LLM as a part of the prompt. Because AI Search knows what the user has access to, it won't send an article that the user isn't able to access.

**Note:** For some features, such as case summarization, the agent generating the summary might have more permissions than other people who have access to the record. If they choose to paste that summary to the work notes, the agent should check to confirm that the data they're sharing in the work notes is appropriate to share with others who have access to that record.

## Opt out of data sharing

Data Sharing helps ServiceNow to continuously advance and improve its Now LLMs, based on the latest customer usage. If you no longer want to participate in the customer data-sharing program, you’re able to opt out.

To opt out, follow the instructions in [Opt out of data sharing for Now Assist](../task/opt-out-of-data-sharing-for-now-assist.md).

**Parent Topic:**[Now Assist reference](../reference/now-assist-reference-landing.md)

