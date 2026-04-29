---
title: Activate a Now Assist in Document Intelligence skill
description: Activate the Now Assist in Document Intelligence skills that agents can use to help analyze and extract information from documents with generative AI.
locale: en-US
release: australia
product: Now Assist in Document Intelligence
classification: now-assist-in-document-intelligence
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
keywords: [Now Assist, Gen AI, Generative AI, Document Intelligence]
breadcrumb: [Configure, Now Assist in Document Intelligence, Enable AI experiences]
---

# Activate a Now Assist in Document Intelligence skill

Activate the Now Assist in Document Intelligence skills that agents can use to help analyze and extract information from documents with generative AI.

## Before you begin

Now Assist in Document Intelligence skills are turned on by default. The skills will be automatically available to appropriate role users for the application. The new default behavior works as follows:

-   **New customers**

    When you install a Now Assist product, designated skills are turned on automatically.

-   **Existing customers who are upgrading \(starting with Australia Patch 1\)**

    There is no change to skills that are currently enabled and customized. A skill is turned on if:

    -   The Now Assist plugin is installed, but the skill was never turned on.
    -   An admin has never adjusted roles for the skill.
    A skill is not turned on if:

    -   The skill was previously turned on, and then turned off again.
    -   An admin has adjusted roles for the skill.
    For more information, see [Now Assist skills, agents, and agentic workflows on by default](../../now-assist-skills/concept/now-assist-skills-on-by-default.md).


Before activating a document intelligence skill in Now Assist, the following applications and their respective plugins must be installed.

-   Now Assist

    For more information, see [Install Now Assist plugins](../../now-assist-admin/task/install-now-assist-feature-plugins.md).

-   Document Intelligence

    For more information, see [Install Document Intelligence](install-document-intelligence.md).

-   Now Assist in Document Intelligence

    For more information, see [Install Now Assist plugins](../../now-assist-admin/task/install-now-assist-feature-plugins.md).


Role required: admin

## About this task

Now Assist in Document Intelligence skills are now turned on by default. If a skill was previously turned on and then turned off, or if an administrator has adjusted roles for the skill, perform the steps in this task to reactivate the skill.

This task doesn’t apply to the Multimodal chat skill. The multimodal chat skill is used to enable chat responses about the content of uploaded documents and images. It is only used on the server side by the document and visual insights AI agent and by the question answering capability in Now Assist in Virtual Agent. This skill doesn’t require configuration in the Now Assist Admin console.

## Procedure

1.  Navigate to **All** &gt; **Now Assist Admin** &gt; **Skills**.

2.  In the workflow list, select **Platform** &gt; **Other**.

3.  In thelist of Platform skills, select **Activate skill** for the document intelligenceskill that you want to activate.

    For more information on document intelligence skills, see [Exploring Now Assist in Document Intelligence](../concept/docintel-exploring-now-assist.md).

    The guided use case setup opens.

4.  Create a use case.

    1.  To create a new use case, follow the steps in [Set up a use case for Now Assist in Document Intelligence](set-up-use-case-for-now-assist-document-intelligence.md).

    2.  Select **Save and continue**.

5.  Define access.

    1.  Define a different access control list \(ACL\) for the skill.

        An ACL enables you to restrict who is able to access and execute the skill to only users with the correct role.

        1.  Select the **Edit** icon \(![Edit icon.](../image/icon-docintel-edit.png)\) for **Roles**.
        2.  Select an option.

<table id="table_vbc_vcf_hhc"><thead><tr><th>

Option

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Any authenticated user

</td><td>

As long as a user is logged in, they can access and execute the skill.

</td></tr><tr><td>

Select roles

</td><td>

Select the roles that a user must have to execute the skill.

 **Note:** If you select multiple roles, a user must only have one of the roles to execute the skill.

</td></tr></tbody>
</table>        3.  Select **Apply**.
    2.  Select **Save and continue**.

6.  Review and activate.

    1.  Review the configuration selections you’ve made for the skill.

    2.  Select **Back** to return to a previous step and make a change.

    3.  Select **Activate**.


## Result

The skill is active and available to the selected user roles.

**Parent Topic:**[Configuring Now Assist in Document Intelligence](../concept/docintel-configuring-now-assist.md)

**Related topics**  


[Set up a use case for Now Assist in Document Intelligence](set-up-use-case-for-now-assist-document-intelligence.md)

[Turn on Full automation mode for a use case](turn-on-full-automation-for-document-extraction-na.md)

[Change the language models for a use case](change-llm-for-use-case.md)

[Edit a use case in Now Assist in Document Intelligence](edit-now-assist-document-intelligence-use-case.md)

[Make a copy of a use case in Now Assist in Document Intelligence](make-copy-of-now-assist-document-intelligence-use-case.md)

[Deactivate a use case in Now Assist in Document Intelligence](deactivate-now-assist-document-intelligence-use-case.md)

[Delete a use case in Now Assist in Document Intelligence](delete-now-assist-document-intelligence-use-case.md)

