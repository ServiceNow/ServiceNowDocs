---
title: Model language grouping
description: Language grouping makes it easier to manage your multilingual Natural Language Understanding \(NLU\) models. You can review existing language groups and designate new language groups.
locale: en-US
release: australia
product: NLU Service
classification: nlu-service
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Multilingual model management, Natural Language Understanding, Enable AI experiences]
---

# Model language grouping

Language grouping makes it easier to manage your multilingual Natural Language Understanding \(NLU\) models. You can review existing language groups and designate new language groups.

## Language grouping

Language grouping organizes your NLU models into primary and secondary models, and indicates the primary language and primary model for the group.

If you have added a new language to a model, a language group is created automatically, so you may already have existing language groups. For more information on adding and translating a new language model, see [Translate a multilingual model](../task/translate-multilingual-model.md).

To view current language groups and inspect possible new language groups, navigate to:

`<instance_name>.service-now.com/$nlu-studio.do#/model-migration`.

The page titled **Review how we've grouped your models** opens. ![On the page titled Review how we've grouped your models, the Edit button is highlighted.](../images/model-language-grouping001V.png)

## Reviewing your grouped models

There are two things you can do on the **Review how we've grouped your model** screen when using the nlu\_admin role.

-   You can review and edit current model language groups in the upper section. For existing language groups, any intent and entity mappings from Virtual Agent \(VA\) are displayed. To update VA mappings or to make one of the secondary languages the primary language in the group, select the **Edit** button. The page titled **Review what's in this grouping** opens. When you complete your edits, select the **Save** button. ![On the page titled Review what's in this grouping, the Save button is highlighted.](../images/model-language-grouping002V.png)
-   You can manually group models in the **Here are your other models** section of the screen. Scroll down the page to view this section, if necessary. To set up a language grouping for a model, expand its **Group** button. ![In the section Here are your other models, the Group function is highlighted.](../images/model-language-grouping003V.png)

The **Group** function opens the page titled **Group what's in these models**. You can expand the list of possible Secondary models, and then select the **Save** button. Any new groups are displayed in the upper section of **Review how we've grouped your models**, after refreshing the page. ![The page titled Group what's in these models, with the Secondary models list highlighted.](../images/model-language-grouping004V.png)

**Note:** The time it takes the system to group your models depends on the number and size of your models.

