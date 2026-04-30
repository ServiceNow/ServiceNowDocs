---
title: Virtual Agent Designer user input controls
description: Use the collection of input controls provided by Virtual Agent Designer to prompt and capture information from the user in a conversation.
locale: en-US
release: yokohama
product: Virtual Agent
classification: virtual-agent
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 6
breadcrumb: [Virtual Agent Designer interface reference, Virtual Agent reference, Virtual Agent, Conversational Interfaces]
---

# Virtual Agent Designer user input controls

Use the collection of input controls provided by Virtual Agent Designer to prompt and capture information from the user in a conversation.

## Common input control properties

In addition to [data pills and condition controls](../concept/virtual-agent-controls.md), each input control has the following common properties:

-   **Input variable for the user response**

    Each control stores the user response in an input variable that is accessible from other controls within the same topic using the `getValue` and `getDisplayValue` methods. The variable name is based on the name that you assign to the input control. For example, if you assign the name `First prompt` to an input control, the variable name is `first_prompt`. The variable name is lowercase, with an underscore character instead of a space. For more information on these methods, see [Virtual Agent scripts](../concept/virtual-agent-scripts.md).

    ![The Variable name field is populated automatically under Text input.](../images/va-text-input-node-var-name.png "The Variable name field is populated automatically")


## Large Language Model \(LLM\) user input controls

The following user input controls are supported in LLM topics when you create an LLM Virtual Agent topic. LLM user inputs include the following.

-   [Input Collector](va-ai-data-collector.md)
-   [Text input](va-text-input.md)
-   [Static Choice list](va-static-choicelist.md)
-   [Dynamic Choice list](va-reference-choicelist.md)
-   [Boolean input](va-boolean-user-input.md)
-   [Date Time input](va-date-time-input.md)
-   [Carousel input](va-carousel-input.md)

**Note:** Avoid placing more than five user input controls in a single LLM topic, or more than five in a single Input Collector. Excessive user input controls can overwhelm the LLM and may lead to inaccurate or unexpected responses.

## Natural Language Understanding \(NLU\) entity properties

-   ****

    If NLU is enabled, the following properties are displayed in the property sheet for the **Text**, **Static Choice**, **Dynamic Choice**, **Boolean**, **Date Time**, and **Carousel** input controls. To view or enable these properties, go to the Advanced options section.

    -   **NLU entity**: The entity that corresponds to the input variable for the control. You select the entity from the list of entities associated with the topic intent, as defined in the NLU model that you’re using for the topic. When Virtual Agent recognizes the entity value in user utterances and if the value meets the entity prediction confidence threshold, then Virtual Agent extracts the value. The value is stored in the input variable for the node. This storing action is called slot filling. Slot filling recognizes when multiple values for the same NLU entity occur in a conversation. Users are prompted with a list to confirm which node value to select when multiple nodes are tied to the same NLU entity. This property is available only for NLU topic discovery.

        ![Slide the NLU entity toggle to select an NLU topic when topic discovery is enabled.](../images/va-user-input-nlu-entity-property.png "NLU entity property")

    -   **Enable NLU to switch topics**: Enables NLU prediction for the node. If enabled, users can enter text to answer questions, regardless of the type of input control being used. Virtual Agent uses this utterance to match another existing intent, letting the user switch topics. To enable this property on a node, navigate to **Advanced options** &gt; **Topic switching**.

        ![Under Advanced options - Topic switching, slide the Enable NLU to switch topics toggle to switch topics property.](../images/va-user-input-topic-switching.png "Enable NLU to switch topics property")

-   **Default value**

    An input prompt can have a preset value that you define. This value can be either a string or a script that returns a string. This property is in the Advanced options section.

    ![Default value property under Advanced options to predefine a value for user input.](../images/va-user-input-default-value.png "Default value property")

-   **Confirmation messages**

    These bot response messages signal the end of the node interaction and ask the users to confirm their response. This property is in the Advanced options section.

    ![Confirmation messages properties under Advanced options for input completion and default value confirmations.](../images/va-user-input-confirmation-messages.png "Confirmation messages properties")


-   **[Input Collector user input control](va-ai-data-collector.md)**  
Use the Input Collector control to gather data for use by Now Assist in conversations that use large language model \(LLM\) topic discovery.
-   **[Text user input control](va-text-input.md)**  
The Text user input control in a Virtual Agent topic prompts the user for a text string.
-   **[Static Choice user input control](va-static-choicelist.md)**  
Use the Static Choice user input control in a Virtual Agent topic to list predefined choices available to the user. You can select only one item from a choice list.
-   **[Grouped Choice user input control](va-grouped-choice-user-input.md)**  
Use the Grouped Choice user input control in a Virtual Agent topic to list multiple groups of choices in one message.
-   **[Dynamic Choice user input control](va-reference-choicelist.md)**  
Use the Dynamic Choice user input control in a Virtual Agent topic to dynamically create a list of available choices for your users. Create these choices by querying a table or by using a script to dynamically create them.
-   **[Boolean user input control](va-boolean-user-input.md)**  
Use the Boolean user input control in a Virtual Agent topic to present a Yes/No prompt to the user.
-   **[Date Time user input control](va-date-time-input.md)**  
Use the Date Time user input control in a Virtual Agent topic to enable the user to select a calendar date, time \(hours and minutes\), or both.
-   **[File Picker user input control](va-file-picker.md)**  
Use the File Picker user input control in a Virtual Agent topic to prompt a user to upload an image or any file type. After the user uploads an image file, the image appears immediately in the Virtual Agent client.
-   **[Carousel user input control](va-carousel-input.md)**  
Use the Carousel user input control in a Virtual Agent topic to present a prompt and a horizontal series of labeled images. The user can select a single item from the carousel.
-   **[Secure Text user input control](va-secure-text.md)**  
The Secure Text control provides a means to encrypt sensitive information provided as simple text or other formats. Use this control to encrypt sensitive information in topics that use large language model \(LLM\) discovery.

**Parent Topic:**[Virtual Agent Designer interface reference](../concept/vad-reference.md)

