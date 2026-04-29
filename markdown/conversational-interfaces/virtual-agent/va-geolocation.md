---
title: Using geolocation in Virtual Agent
description: Topic authors can include a pre-built topic block called Geolocation in conversations with users. The Geolocation topic block retrieves the latitude and longitude coordinates of the user's location.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Maximizing code reuse with topic blocks, Exploring other Virtual Agent features, Build and deploy, Virtual Agent, Conversational Interfaces]
---

# Using geolocation in Virtual Agent

Topic authors can include a pre-built topic block called Geolocation in conversations with users. The Geolocation topic block retrieves the latitude and longitude coordinates of the user's location.

Topic authors can add this topic block to larger conversation flows. With the user's permission, the topic block retrieves the user's latitude and longitude location coordinates. Knowing these coordinates can help topic authors respond to customer requests or issues faster and more efficiently.

For example, you may need to send a technician to a customer site to resolve an incident. To quickly respond to the customer, you need to know which technicians are located nearby so you can dispatch the appropriate technician for the customer's location.

For general information about how geolocation is used on the ServiceNow platform, see [Geolocation](https://www.servicenow.com/docs/access?context=c_Geolocation&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

## Share location details

The first time a user, such as a field technician, uses the Geolocation topic block in a conversation, they are asked if they would like to share details about their location.

![The chatbot asks, "Would you like to share your location?" Choices are No and Yes.](../images/va-geolocation-approval.png)

<table id="table_epl_33n_xrb"><thead><tr><th>

User choice

</th><th>

Topic block response

</th></tr></thead><tbody><tr><td>

Yes

</td><td>

The topic block sends the user's latitude and longitude coordinates from the server to the user's device.If users want to allow the ServiceNow instance to access their location, users may then see operating system-specific or browser-specific prompts. Examples of such prompts include the following:

-   Allow \(always\)
-   Allow \(one time only\)
-   Block \(don't allow\)

 Depending on the user's response, they may see this prompt one or more times, or they may never see it.

</td></tr><tr><td>

No

</td><td>

The topic block does not retrieve user coordinates and displays a relevant error message for the topic author to resolve. The error is logged as an output parameter. For details, see [Geolocation topic block parameters](../reference/va-platform-topicblocks.md#geolocation-topic-block-properties).

</td></tr></tbody>
</table>## Modify the Geolocation topic block

If you are a topic author or an admin, you can modify the Geolocation topic block flow, as applicable. Simply duplicate the topic block and rename it. You can then use it as needed in the larger conversation flow you're designing.

The Geolocation topic block properties sheet lets topic authors specify the input and output mappings. You can also customize the prompt using data pills or scripts. For example, you can include an explanation or reason for asking the question. For information about using data pills and scripts, see [Assistant Designer controls](virtual-agent-controls.md).

![The value of the permissionPrompt string is "Would you like to share your location?"](../images/va-geolocation-user-prompt.png "Share location prompt in the Geolocation topic block properties")

Use the input mappings to customize how Virtual Agent asks users for permission to share their location. The response is passed to the topic block.

Use the output mappings to specify the variables that are returned from the topic block in the conversation.

![Geolocation output mapping parameters include latitude, longitude, errormessage, errortype, and status.](../images/va-geolocation-output-parameters.png "Output mapping properties in the Geolocation topic block")

All the variables are selected by default. Keep the default choices, or select the variables you want returned from the topic block. At a minimum, you should select the latitude and longitude coordinates. However, error messages, error type, and status details could be useful when resolving problems. The output mappings you select are stored as variables on the server.

![Geolocation topic block results read, "This is what I got back," followed by the latitude and longitude, an OK status, and no error.](../images/va-geolocation-results.png "Geolocation topic block results")

For more information about the Geolocation topic block properties, see [Geolocation topic block parameters](../reference/va-platform-topicblocks.md#geolocation-topic-block-properties).

