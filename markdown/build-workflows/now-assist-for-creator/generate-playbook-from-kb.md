---
title: Generate a playbook from a knowledge base article
description: Use an existing knowledge base article to generate a playbook using AI. The stages and activities are automatically populated based on the article content.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/build-workflows/now-assist-for-creator/generate-playbook-from-kb.html
release: zurich
product: Now Assist for Creator
classification: now-assist-for-creator
topic_type: task
last_updated: "2026-06-24"
reading_time_minutes: 3
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Playbook generation from a KB article, Playbook generation, ServiceNow Otto for Creator, Build workflows]
---

# Generate a playbook from a knowledge base article

Use an existing knowledge base article to generate a playbook using AI. The stages and activities are automatically populated based on the article content.

## Before you begin

Verify that the ServiceNow Otto for Creator plugin is installed and the **Playbook Generation with KB** skill is active.

**Note:** The skill is available in **Admin** &gt; **Now Assist Admin** &gt; **Now Assist Skills** &gt; **Creator**. If you don't see **Creator** under **Now Assist Skills**, the plugin is not installed.

\[Omitted image "now-assist-creator-skills.png"\] Alt text: Now assist for creator skills page.

For information about installing ServiceNow Otto for Creator, see [Install ServiceNow Otto for Creator](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/build-workflows/now-assist-for-creator/install-now-assist-for-creator.md).

Verify that the knowledge base article describes a process with steps. Articles that contain only definitions or reference information can't be used to generate a playbook.

Role required: playbook\_author.

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  From the **New** drop-down menu, select **Playbook**.

3.  On the **Create with AI** tab, fill in the following fields.

    \[Omitted image "playbook-from-kb-otto.png"\] Alt text: Create a playbook from a KB article using AI.

<table id="id_ik5_54x_rjc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**Type**

</td><td>

Type of the playbook you want to create.Select **Standard playbook** for most day to day processes.

</td></tr><tr><td>

**Playbook name**

</td><td>

Unique, user-facing name for your playbook. This name also appears to agents and fulfillers during runtime.

</td></tr><tr><td>

**Application**

</td><td>

Application scope that you want your playbook to run in. Selecting **Global** lets your playbook run in any application scope. For more information, see Application scope.**Important:** You can't change the application scope of a playbook after you've generated a preview for it.

</td></tr><tr><td>

**Describe the playbook using these inputs**

</td><td>

Directions for the playbook that you want to create.-   **Image**

Attach a high quality, clear image of the process. You can compliment the image with text instructions as well. For example, if you attach an image of a flow chart, you can add additional information about the process as text directions.

-   **Knowledge Article**

Select a knowledge article based on which you want to generate a playbook. Additionally, you can add **Now Assist instructions** to compliment the knowledge base article.

-   **Instructions only**

Provide only text instructions to generate the playbook.

    -   Describe each stage and activity in as much detail as you can.

    -   Specify the order that stages and activities run in.

    -   Specify if any stages or activities run at the same time.

</td></tr><tr><td>

**Execution type**

</td><td>

The type of playbook you want to create.-   **Record driven**

The playbook is tied to a record. It is triggered on demands, or automatically based on the record operations. Any data that comes from the playbook will also be stored on that record.

-   **Standalone**

Single session playbook that don't store data to a record. These must be manually triggered or called from another playbook.

</td></tr><tr><td>

**Parent table**

</td><td>

In case of a record driven playbook, the table where the record resides. This option is not relevant for a standalone playbook.

</td></tr><tr><td>

**Additional properties**

</td><td>

Option to allow the playbook to be publicly accessible. Once embedded it is set to available to unauthenticated users, as long as there aren’t additional restrictions preventing the user from accessing the playbook. **Note:** Playbooks must be tied to a public parent table for unauthenticated users to see it in runtime.

</td></tr></tbody>
</table>    **Tip:**

    \[Omitted image "playbook-kb-otto.png"\] Alt text: Select KB article and provide optional text instructions.

    Use the **Knowledge article reference** drop-down list or the look up icon \[Omitted image "playbook-kb-browse.png"\] Alt text: Browse KB articles. to find and select the knowledge article. You can select the preview icon \[Omitted image "playbook-kb-preview.png"\] Alt text: Preview the selected KB article. to view the selected knowledge article in a new tab. Add additional instructions in the **Describe what you want** text field.

4.  Select **Generate playbook preview**.

    The generated playbook preview displays stages and activities identified from the article content. Each activity includes a description derived from the article content.

5.  Review the generated playbook preview for accuracy.

    If the generated playbook doesn't meet your requirements, rephrase your prompt and select **Regenerate preview**.

6.  If you're ready to generate your playbook, select **Save and edit playbook**.


## What to do next

After you generate the playbook, test and activate the playbook from the header.

**Related topics**  


[Playbook generation from a knowledge base article](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/build-workflows/now-assist-for-creator/playbook-generation-from-kb.md)

[Generate a playbook from text or image](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/build-workflows/now-assist-for-creator/generate-a-playbook-outline.md)

