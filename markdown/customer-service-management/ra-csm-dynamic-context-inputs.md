---
title: Context inputs in Recommended Actions
description: A context input enables you to associate entities beyond just the context table with a context ensuring that recommendations are updated dynamically as the context evolves.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [Context inputs in Recommended Actions]
breadcrumb: [Recommended Actions, Recommended Actions configuration, Implement Intelligence, Configure, Customer Service Management]
---

# Context inputs in Recommended Actions

A context input enables you to associate entities beyond just the context table with a context ensuring that recommendations are updated dynamically as the context evolves.

You can create a context input from the Context inputs related list in the Context form. These dynamic JSON-based context inputs enable you to include real-time updates such as user selections, additional table records, and so on, to refine recommendations and support multiple active contexts. This enhances recommendation relevance and operational efficiency. For example, you can create a context input for the Incident table and use in the Case context record.

**Note:** You can create multiple active context inputs for a context.

The following data types are supported for a context input:

-   String
-   List
-   Integer
-   Long
-   Choice
-   True- false
-   Reference
-   Reference dot walked
-   Sys id

## Configuring a context using a context input

Configuring a context using context inputs includes the following steps:

-   Creating a context input. For more information on how to create a context input, see [Create a context input in Recommended Actions](../task/ra-csm-create-context-inputs.md).

    **Note:**

    -   If a context has a parent context defined, you can’t create context inputs for it.
    -   You can have multiple active context inputs simultaneously.
-   Mapping the context input to the following according to your requirement:
    -   default search term by adding it in the Contextual AI Search Config section on Context form.
    -   rules by using it in the condition builder on Rules form.
    -   recommendations by adding it in fields of the Action inputs section on Recommendations form.
    -   resource generators by adding it in the fields of Generator inputs section on Resource Generators form.
-   Adding the JSON-format of the context inputs to the Recommended Actions component for the required record pages in the UI Builder. For more information, see [Configuring Recommended Actions UIB component for context inputs](ra-csm-dynamic-context-inputs.md#section-config-ra-ci).

The context inputs appear along with the context table in the appropriate fields of Rule, Recommendation and Resource generator forms so that you can include the data other than that of the context table to update the recommendations.

## Configuring Recommended Actions UIB component for context inputs

As an RA author or admin, you must add the JSON-format of the context inputs in the **Context input** field of Recommended Actions UIB component of a record page to pass the values. You can get the JSON-format of the context input by selecting the **Copy input JSON** button on the Context input related list in the Context form. The JSON-format includes all the active context inputs. When a context input is deleted or deactivated after configuring the Recommended Actions UIB component, an empty value is passed for these context inputs in UIB from the upcoming iterations.

**Note:** If you set a context input as [mandatory](../task/ra-csm-create-context-inputs.md#entry-ci-mandatory) in the Context input form and fail to set contextual inputs on Recommended Actions component of the record page in the UIB, the recommendations are not be generated.

## Context Input configuration limitations

The limitations for context inputs configuration are as follows:

-   You can either define a parent context or configure context inputs for a context.
-   When context inputs are defined for a parent content, then it's rules and recommendations cannot be inherited by its child contexts. In other words, the parent context does not appear in the Parent context field of the Child context.
-   To define context inputs for a context which has a parent context defined already, delete the parent context in the Parent context field so that the Context inputs related list appears. And in the Context inputs related list, select the New button to create context inputs.
-   When a context input is defined for a parent context which has a child context associated, then the parent-child context link is broken. In the child context, the inherited rules and recommendations will be removed from the Inherited Rules and Recommendations related list respectively.

