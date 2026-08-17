---
title: Guidelines for slot filling in catalog request
description: Conversational Catalog Requests uses a large language model \(LLM\) to extract variable values from a requester's input and pre-fill catalog item questions, a capability known as slot filling.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/service-catalog/c\_slot\_filling\_ccr.html
release: australia
product: Service Catalog
classification: service-catalog
topic_type: concept
last_updated: "2026-06-25"
reading_time_minutes: 2
keywords: [slot filling, Conversational Catalog Requests, LLM, pre-fill]
breadcrumb: [LLM topic blocks, Conversational Catalog Requests reference, Conversational Catalog Requests, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Guidelines for slot filling in catalog request

Conversational Catalog Requests uses a large language model \(LLM\) to extract variable values from a requester's input and pre-fill catalog item questions, a capability known as slot filling.

When a requester describes their need in the conversational interface, ServiceNow Otto passes that input to an LLM. LLM identifies the relevant catalog item questions and extracts matching values from the requester's message. Those values are then pre-filled into the catalog item request form, reducing the number of fields the requester must complete manually.

Because LLMs are probabilistic by design, slot fill accuracy can vary across sessions even for identical inputs. Slot fill accuracy cannot be guaranteed. The goal is to maximize pre-fill accuracy.

## Catalog item question configuration

The LLM uses question labels and descriptions to determine what information to extract from the requester's input. Ambiguous or poorly written question labels are a leading cause of missed or incorrect slot fill. The following considerations apply when configuring catalog item questions for use with slot filling:

-   Keep the **Question** field label concise and unambiguous. Avoid long or multi-part labels. For example, use a single focused label such as "What issue are you experiencing?" rather than combining multiple questions into one label.
-   Avoid overlapping question names in the **Name** field. When two questions in the same catalog item have similar labels, for example "Requested For" and "On behalf of", the LLM may fill them inconsistently. Differentiate question names clearly to reduce ambiguity.
-   In the **Name** field definition, lead with the object and follow with the attribute. For example, use `date_required` rather than `required_date`. This structure enables the LLM to identify the correct question.
-   Replace system-generated prefixes and internal question names with human-readable names. For example, replace `Hardware_001_P04_power` with `Laptop_charger`.
-   Use names that reflect what the item actually is, so the LLM can match requester input to the correct question reliably.
-   Check the value of the **com.glide.cs.genai.discovery.limits.skill.slots** property, which controls how many questions are sent for slot fill. If the value is set to a value less than the default, questions beyond that limit aren't pre-filled. Restore the value to the default unless there is a specific reason to reduce it.

## Model selection

Slot fill quality is directly influenced by the capability of the LLM configured for the instance. Older or smaller models have reduced ability to interpret ambiguous input, resolve references. Such as matching a name to a user record when duplicates exist, and pre-fill multi-variable catalog items.

If slot fill failures persist on catalog items with clear, well-configured question labels, check which model is configured for the instance's Conversational Catalog skill. A more capable or recent model typically improves the following:

-   Extraction of date and relative time expressions, for example "next Tuesday" or "in two weeks".
-   Multi-variable extraction from a single requester utterance.

To review the model configuration, navigate to **AI Admin Hub** &gt; **Skills** and check the model assigned to the Conversational Catalog skill. Contact your account team for guidance on available model options for your entitlement.

**Parent Topic:**[LLM topic blocks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-catalog/llm-topic-blocks-reference.md)

