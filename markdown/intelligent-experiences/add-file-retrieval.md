---
title: Add a file upload to an AI agent
description: Upload files for analysis by an AI agent in AI Agent Studio to grant your AI agent access to specialized knowledge.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2025-02-10"
reading_time_minutes: 1
breadcrumb: [Add a tool to an AI agent, Create an AI agent, Now Assist AI agents, Enable AI experiences]
---

# Add a file upload to an AI agent

Upload files for analysis by an AI agent in AI Agent Studio to grant your AI agent access to specialized knowledge.

## Before you begin

Role required: sn\_aia.admin

## Procedure

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage** &gt; **AI agents**.

2.  Open the AI agent that you want to add a file upload to and navigate to the Add tools and information section.

3.  In the Add tool drop-down list, select **File upload**.

4.  On the form, fill in the fields.

<table><thead><tr><th>

Fields

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name that you want to specify for your file upload.

</td></tr><tr><td>

Description

</td><td>

Description of the file upload and what it’s going to do to assist your AI agent.**Note:** This description is sent to the large language model \(LLM\).

</td></tr><tr><td>

Execution mode

</td><td>

Mode of execution for your selected file upload:-   **Supervised**: Inputs from your live agent are required during the execution of this uploaded file while the AI agent runs.
-   **Autonomous**: Doesn't require any input from your live agent during the execution of this uploaded file while the AI agent runs.


</td></tr><tr><td>

Display output

</td><td>

Permission to display the output of the execution in the Now Assist panel or in Virtual Agent:-   **Yes**
-   **No**


</td></tr><tr><td>

Processing message

</td><td>

Message to display to users when the tool is running.

</td></tr><tr><td>

Output transformation strategy

</td><td>

Style for the LLM to present the results. -   None
-   Concise
-   Paragraph
-   Verbose
-   Summary for search results


</td></tr><tr><td>

Attachments

</td><td>

For analysis by an AI agent, attach up to 5 files with a maximum size of 5 MB each in these file formats: PDF, DOCX, or TXT formats.**Note:** A user who interacts with the AI agent with the file upload tool can see the information contained within the files.

</td></tr></tbody>
</table>5.  Select **Add**.

    A file upload is added to the AI agent.


**Parent Topic:**[Add a tool to an AI agent](../concept/add-tool-aia.md)

