---
title: Use Generative AI Controller with Virtual Agent Designer
description: Use Generative AI Controller capabilities inside Virtual Agent topics to draft knowledge articles.
locale: en-US
release: xanadu
product: Generative AI Controller
classification: generative-ai-controller
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Using Generative AI Controller, Generative AI Controller, Now Assist, Enable AI experiences]
---

# Use Generative AI Controller with Virtual Agent Designer

Use Generative AI Controller capabilities inside Virtual Agent topics to draft knowledge articles.

## Before you begin

You must enable the capabilities for Virtual Agent Designer first. For more information, see [Enable a generative AI capability in Virtual Agent Designer](enable-generative-ai-controller-for-virtual-agent.md).

Role required: admin

## About this task

This example uses the Generate Content capability of the Generative AI Controller to draft knowledge article content from a Virtual Agent conversation.

For more information on tracking Generative AI Controller usage, see [Monitoring Now Assist usage](https://www.servicenow.com/docs/access?context=monitoring-now-assist-usage&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

## Procedure

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Virtual Agent** &gt; **Designer**.

2.  Create a topic by selecting the Create card.

3.  Enter a unique name for the topic.

    More topic options can be configured, such as Natural Language Understanding \(NLU\) model or access restrictions.

    This example uses `KB Article Generation` as the topic name.

4.  Select **Create**.

5.  Create a user input node between Start and End by dragging the **User Input** &gt; **Text** component from the Components panel.

6.  Enter a node name on the info panel on the canvas.

    In this example, the node name is `KB Article Content Request`.

    ![Topic flow with the KB Article Content Request.](../image/new-topic-content-node.png)

7.  In the prompt field, enter a message to display to the user.

    Because the user supplies the topic for the knowledge base \(KB\) article content, the prompt in this example is `What topic would you like to see a Knowledge Base article about?`.

8.  Add User Input nodes to fill in all required fields.

    **Note:** To create a record successfully, all required fields must have a value. The next steps describe how to fill in the required fields for a KB article. If your form has no required fields, you don't need to add any User Input nodes.

    1.  Add another **User Input** &gt; **Text** node and name it `Article Title Request`.

    2.  Add a prompt for the required `Article title` field such as `What should the title of the Knowledge Article be?`.

        ![Topic flow with two nodes, KB Article Content Request and Article Title Request.](../image/new-topic-second-node.png)

9.  On the Components panel, scroll down until you see the Capabilities section and drag the Generate Content action next in the Topic flow.

10. In the Info panel, name the node.

    The node name that is used in the example is `AI KB Generator`.

    ![Flow with Generate Content node.](../image/new-topic-ai-node.png)

11. Open up the data pill selector by selecting the data pill icon \(![Data pill icon.](../image/icon-variable-reference-picker.png)\) next to the topic field.

    ![Topic flow with datapill menu open for Topic.](../image/new-topic-ai-node-datapill-menu.png)

12. Use the text that was created in the interaction by selecting the **Input Variables** &gt; **Response** variable.

    ![Completed node with the prompt value filled in](../image/new-topic-ai-node-complete.png)

13. Drag the **Utilities** &gt; **Record Action** component from the Components panel after the Generate Content node.

    ![Flow with Update Record subflow added.](../image/new-topic-update-record-node.png)

14. Enter a name for the node.

    For this example, the node name is `Create KB Article`.

15. Fill in the other required fields.

    1.  For the Action type, select whether you want to create a record or update an existing one.

        In this example, the Action type is `Create a record`.

    2.  Select the table for the new or updated record.

        This example uses the Knowledge \(kb\_knowledge\) table.

16. Under Field, select the **Add Field** button to open the Field Values window.

17. Set a field value by selecting **Add Field Value**.

    ![Add field value modal with Add Field Value highlighted.](../image/new-topic-add-field-values-modal.png)

18. Select the field that you would like to update from the list.

    You can add as many fields as you like. In this example, the fields are `Article body`, `Knowledge base`, and `Short description`.

19. Select the data pill icon to open the data pill selection menu.

    ![Datapill picker open in the Add Fields modal.](../image/new-topic-add-field-values-datapill-modal.png)

20. For the `Article body` field, select `Input Variables`&lt; `Response` to use the response that is generated by the Generate Content node.

21. For the `Knowledge base` field, select `Knowledge` or your preferred category.

22. For the `Short description` field, select the data pill icon and add **Input Variables** &gt; **Article Title Request**, or the name of the user input node that is prompting for a title.

    ![All field values completed.](../image/new-topic-add-fields-modal-complete.png)

23. Save your field selections and close the Field Values window by selecting **Save**.

24. Save the topic by selecting **Save**.


## What to do next

This example topic creates simple knowledge articles. Use additional user input, such as context and background information, for more complex articles.

**Note:** Review any generated content before you publish. See [AI Limitations](../concept/exploring-generative-ai-controller.md) for more details.

