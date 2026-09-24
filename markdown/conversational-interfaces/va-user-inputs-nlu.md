---
title: \(Legacy\) Virtual Agent Designer user input controls for NLU
description: Use the collection of input controls provided by Virtual Agent Designer to prompt and capture information from the user in a conversation.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/conversational-interfaces/va-user-inputs-nlu.html
release: brazil
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 4
breadcrumb: [Virtual Agent Designer interface reference, NLU reference, \(Legacy\) Virtual Agent for NLU, Conversational Interfaces]
---

# \(Legacy\) Virtual Agent Designer user input controls for NLU

Use the collection of input controls provided by Virtual Agent Designer to prompt and capture information from the user in a conversation.

## Common input control properties

In addition to [data pills and condition controls](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/virtual-agent-controls.md), each input control has the following common properties:

-   **Input variable for the user response**

    Each control stores the user response in an input variable that is accessible from other controls within the same topic using the `getValue` and `getDisplayValue` methods. The variable name is based on the name that you assign to the input control. For example, if you assign the name `First prompt` to an input control, the variable name is `first_prompt`. The variable name is lowercase, with an underscore character instead of a space. For more information on these methods, see [Virtual Agent scripts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/virtual-agent-scripts.md).

    \[Omitted image "va-text-input-node-var-name.png"\] Alt text: The Variable name field is populated automatically under Text input.


## Natural Language Understanding \(NLU\) entity properties

If NLU is enabled, the following properties are displayed in the property sheet for the **Text**, **Static Choice**, **Dynamic Choice**, **Boolean**, **Date Time**, and **Carousel** input controls. To view or enable these properties, go to the Advanced options section.

-   **NLU entity**: The entity that corresponds to the input variable for the control. You select the entity from the list of entities associated with the topic intent, as defined in the NLU model that you’re using for the topic. When Virtual Agent recognizes the entity value in user utterances and if the value meets the entity prediction confidence threshold, then Virtual Agent extracts the value. The value is stored in the input variable for the node. This storing action is called slot filling. Slot filling recognizes when multiple values for the same NLU entity occur in a conversation. Users are prompted with a list to confirm which node value to select when multiple nodes are tied to the same NLU entity. This property is available only for NLU topic discovery.
-   **Enable NLU to switch topics**: Enables NLU prediction for the node. If enabled, users can enter text to answer questions, regardless of the type of input control being used. Virtual Agent uses this utterance to match another existing intent, letting the user switch topics. To enable this property on a node, navigate to **Advanced options** &gt; **Topic switching**.

Additional Advanced properties include:

-   **Default value**

    An input prompt can have a preset value that you define. This value can be either a string or a script that returns a string. This property is in the Advanced options section.

-   **Confirmation messages**

    These bot response messages signal the end of the node interaction and ask the users to confirm their response. This property is in the Advanced options section.


-   **[\(Legacy\) Text user input control for NLU](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/va-text-input-nlu.md)**  
The Text user input control in a Virtual Agent topic prompts the user for a text string.
-   **[\(Legacy\) Static Choice user input control](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/va-static-choicelist-nlu.md)**  
Use the Static Choice user input control in a Virtual Agent topic to list predefined choices available to the user. You can select only one item from a choice list.
-   **[\(Legacy\) Grouped Choice user input control](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/va-grouped-choice-user-input-nlu.md)**  
Use the Grouped Choice user input control in a Virtual Agent topic to list multiple groups of choices in one message.
-   **[\(Legacy\) Dynamic Choice user input control](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/va-reference-choicelist-nlu.md)**  
Use the Dynamic Choice user input control in a Virtual Agent topic to dynamically create a list of available choices for your users. Create these choices by querying a table or by using a script to dynamically create them.
-   **[\(Legacy\) Boolean user input control](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/va-boolean-user-input-nlu.md)**  
Use the Boolean user input control in a Virtual Agent topic to present a Yes/No prompt to the user.
-   **[\(Legacy\) Date Time user input control](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/va-date-time-input-nlu.md)**  
Use the Date Time user input control in a Virtual Agent topic to enable the user to select a calendar date, time \(hours and minutes\), or both.
-   **[\(Legacy\) File Picker user input control](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/va-file-picker-nlu.md)**  
Use the File Picker user input control in a Virtual Agent topic to prompt a user to upload an image or any file type. After the user uploads an image file, the image appears immediately in the Virtual Agent client.
-   **[\(Legacy\) Carousel user input control](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/va-carousel-input-nlu.md)**  
Use the Carousel user input control in a Virtual Agent topic to present a prompt and a horizontal series of labeled images. The user can select a single item from the carousel.

**Parent Topic:**[\(Legacy\) Virtual Agent Designer interface reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/vad-reference-nlu.md)

