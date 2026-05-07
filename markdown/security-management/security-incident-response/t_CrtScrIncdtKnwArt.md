---
title: Create a security incident knowledge article
description: As you work with security incidents and response tasks, knowledge articles automatically display to provide pertinent information about the task you're performing. Your organization can create and maintain articles in the security incident knowledge base.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Managing security incidents and inbound requests, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Create a security incident knowledge article

As you work with security incidents and response tasks, knowledge articles automatically display to provide pertinent information about the task you're performing. Your organization can create and maintain articles in the security incident knowledge base.

## Before you begin

Role required: sn\_si.knowledge\_admin

## About this task

Knowledge articles share security information, document the types of cyber threats that your organization faces, and provide answers and responses to these threats.

If needed, you can organize knowledge articles into runbooks, which create associations between the articles and specific tasks. For example, you can configure a runbook with conditions that cause a knowledge base article about phishing to be displayed when you're creating a security incident for a phishing attack. For more information, see [Create a Security Incident Response runbook](../reference/setup-assistant-reference.md#).

Knowledge articles in runbooks can also be associated with specific tasks in a playbook. For more information, see [Associate a knowledge article with a playbook task](use-the-playbook.md#).

The benefits of knowledge articles include the following.

-   Employees have one source of information that is easy to search.
-   Information can be kept up-to-date, as knowledge articles have a defined life cycle: create, review and update, publish, and retire.
-   When you manually create a security request, incident, or response task, a list of relevant articles is presented as you type the short description.

**Note:** It is important to assign a knowledge manager to each security incident knowledge base.

## Procedure

1.  Navigate to **All** &gt; **Security Incident** &gt; **Catalog &amp; Knowledge** &gt; **Knowledge**.

2.  Select the Create an Article icon \(![Article icon](../image/cj-sir-add-article-icon.png)\).

3.  Fill in the fields on the form, as appropriate.

    |Field|Description|
    |-----|-----------|
    |Number|The automatically generated KB number.|
    |Knowledge base|The knowledge base selected for this article.|
    |Category|The category for this article.|
    |Published|When this knowledge article was published. This value is set when the article is created, and updated when the article is published.|
    |Valid to|When this knowledge article expires. This article will not appear in search results after this date or if a date is not selected.|
    |Image|An image that appears beside the article when searching from the legacy knowledge portal.|
    |Workflow|\[Read-Only\] The publication state of the article, such as Draft or Published. When [inserting a new article](https://www.servicenow.com/docs/access?context=t_EditingInForms&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US) from an existing article, the state of the new article is reset to **Draft**.|
    |Source|The task this knowledge article was created in response to, if any. This field is set automatically when you create the knowledge article from a task record.|
    |Attachment link|Check box for downloading an attached file automatically when a user accesses the article, instead of opening the article view. Add an attachment to the article to use this option.|
    |Display attachments|Check box for displaying attachments to users viewing this knowledge article. Attachments appear below the article text. Add one or more attachments to the article to use this option.|
    |Short description|The title of the article. This title appears when browsing and searching knowledge, and at the top of the article.|
    |Text|Content for the article. Use the WYSIWYG HTML editor to create content. A preview of the content appears when browsing and searching knowledge.|

    **Note:** If you're creating a [knowledge article to be associated with a playbook task](use-the-playbook.md#), set the **Knowledge base** field to **Security Incident Response Runbook**.

4.  Select **Submit** to create the article.


## What to do next

Any additional steps required to publish the article, such as approvals, depend on the [publishing workflow](https://www.servicenow.com/docs/access?context=r_KnowledgeWorkflows&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US) for the knowledge base.

**Related topics**  


[Create a Security Incident Response runbook](../reference/setup-assistant-reference.md#)

