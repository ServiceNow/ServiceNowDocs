---
title: Configure Agent Chat in a portal
description: Your end users can initiate and maintain an Agent Chat conversation in any portal page. Write a script to pass portal-specific data to Agent Chat. For example, pass the name of your knowledge base to a Virtual Agent conversation.You can change the color and images that are used in the Agent Chat button in your portal.If you are upgrading from a previous release, your portal implementation may include the Virtual Agent Service Portal widget. Migrate widget options to the Agent Chat in Service Portal configuration and remove all instances of the widget to enable your users to initiate and maintain an Agent Chat conversation in any portal page. Use the spContextManager class in a widget client script to pass dynamic page data to Agent Chat. For example, pass the number of approvals in the Approvals widget to Agent Chat when a user initiates a conversation from the Service Portal homepage.If your portal includes a Live Chat link in the header menu, you can remove it by updating the widget's option schema.
locale: en-US
release: zurich
product: Service Portal
classification: service-portal
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 8
keywords: [Configure, Agent Chat, portal, Virtual Agent, com.glide.interaction.awa, AWA, Advanced Work Assignment]
breadcrumb: [Create a portal, Configuring Service Portal, Service Portal, Configure UIs and portals, Configure user experiences]
---

# Configure Agent Chat in a portal

Your end users can initiate and maintain an Agent Chat conversation in any portal page. Write a script to pass portal-specific data to Agent Chat. For example, pass the name of your knowledge base to a Virtual Agent conversation.

## Before you begin

Role required: admin

-   Activate the Glide Virtual Agent \(com.glide.cs.chatbot\) or the Agent Chat \(com.glide.interaction.awa\) plugin. You can activate the Glide Virtual Agent plugin only if you have a subscription.

    **Note:** For information about using Now Assist in Virtual Agent in portals, see [Configuring assistants overview](https://www.servicenow.com/docs/access?context=configure-now-assist-va&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US).


## Procedure

1.  Navigate to **All** &gt; **Service Portal** &gt; **Agent Chat**.

    The Service Portal Agent Chat Configurations \[sp\_agent\_chat\_config\] table opens.

2.  Select **New**.

3.  Complete the form.

<table id="table_g4z_ldq_zgb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Active

</td><td>

Select to make the configuration active.

</td></tr><tr><td>

Name

</td><td>

Enter a unique name for the configuration record.

</td></tr><tr><td>

Portals

</td><td>

Select the portals in which you would like to use the specified chat configuration. If no portal is selected, the configuration applies to all portals in the system.

</td></tr><tr><td>

Application

</td><td>

Read-only application scope for the record.

</td></tr><tr><td>

Public

</td><td>

Select to make Agent Chat available to users before they log in.

</td></tr><tr><td>

Roles

</td><td>

Select the roles a user must have to use Agent Chat. If you don't select a role, Agent Chat is available to all users regardless of their role.

</td></tr><tr><td>

Order

</td><td>

Enter a number indicating the order that the configurations should run. Only one configuration applies per portal. If there are multiple configurations on a portal, the system runs the first configuration found from lowest to highest.

</td></tr><tr><td>

Server script

</td><td>

Write a script that passes page and widget data to an Agent Chat conversation when a user initiates the conversation. For example, pass a field to the chat conversation to enable Agent Chat to access the value. Data passed in this script is available to every page in the portal associated with this record. This script has access to the [GlideSPScriptable](https://www.servicenow.com/docs/access?context=c_GlideSPScriptableScopedAPI&version=zurich&pubname=zurich-api-reference&ft:locale=en-US) API.

 **Note:** The portal suffix, page ID, and language are automatically available to Agent Chat and do not require a custom script. Sys ID and table are automatically available to Agent Chat when they are present in the URL.

 This example returns an object containing the list of catalogs associated with the portal to the current conversation.

 ```
(function ($sp) {    
   return {        
      catalogs: $sp.getValue(‘catalogs’) 
   };
})($sp);
```

 When Agent Chat opens in an `iframe` HTML element, the list of catalogs is included in the `iframe` URL. Parameters from this field override any conflicting page data passed to Agent Chat.

</td></tr></tbody>
</table>4.  Select **Submit**.


## Result

Users can initiate and maintain an Agent Chat conversation from any page in the selected portal.

**Parent Topic:**[Create a portal](create-a-portal.md)

## Customize the Agent Chat button

You can change the color and images that are used in the Agent Chat button in your portal.

### Before you begin

If you plan to replace one or both of the images that are used in the Agent Chat button, upload the images to your instance. For more information on uploading an image, see [Storing images in the database](../../../administer/navigation-and-ui/concept/c_StoringImagesInTheDatabase.md).

Role required: sp\_admin or admin

### About this task

You can configure the following elements of the Agent Chat button:

-   The image to indicate that the chat window is open
-   The image to indicate that the chat window is closed
-   The button background color

These elements are determined in the portal theme. To customize the Agent Chat button, update the relevant SCSS variables in the portal theme record. For more information, see [Set up your bot's branding](https://www.servicenow.com/docs/access?context=ac-configure-chat-branding&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US).

**Note:** If you change the web client Virtual Agent button icon while the system property \[sys\_property\] table value **com.glide.cs.advanced-chat.popover** is set to `true`, set the web client Virtual Agent chat button to the same size as the original button icon, otherwise the icon is displayed oversize.

### Procedure

1.  Navigate to **All** &gt; **Service Portal** &gt; **Themes**.

2.  Open a theme record.

3.  In the **CSS variables** field, add the following variables:

<table id="table_sqr_fcd_qkb"><thead><tr><th>

Variable

</th><th>

Description

</th></tr></thead><tbody><tr><td>

`$sp-agent-chat-btn-close`

</td><td>

Image to indicate that the chat window is closed. Use an image URL that contains:-   Your instance address
-   The name of the Image \[db\_image\] record to reference
For example, to reference the `tack-icon.png` image in the database, enter the following:```
$sp-agent-chat-btn-close: url("https://<instance-name>.service-now.com/tack-icon.png");
```

 ![The image URL references tack-icon.png in the Agent Chat button](../image/sp-chat-close.png)

To use the default image, remove the variable.

</td></tr><tr><td>

`$sp-agent-chat-btn-open`

</td><td>

Image to indicate that the chat window is open. Use an image URL that contains:-   Your instance address
-   The name of the Image \[db\_image\] record to reference
For example, to reference the `book-icon.png` image in the database, enter the following:```
$sp-agent-chat-btn-open: url("https://<instance-name>.service-now.com/book-icon.png");
```

 ![The image URL references book-icon.png in the Agent Chat button](../image/sp-chat-open.png)

To use the default image, remove the variable.

</td></tr><tr><td>

`$sp-agent-chat-bg`

</td><td>

Button background color. Use a Hex code to set the color. For example, to use red, enter the following:```
$sp-agent-chat-bg: #ff0000;
```

 ![Red background color](../image/red-chat-icon.png)

To use the default background color, remove the variable.

</td></tr></tbody>
</table>4.  Click **Update**.


## Migrate from the Virtual Agent Service Portal widget

If you are upgrading from a previous release, your portal implementation may include the Virtual Agent Service Portal widget. Migrate widget options to the Agent Chat in Service Portal configuration and remove all instances of the widget to enable your users to initiate and maintain an Agent Chat conversation in any portal page.

### Before you begin

Role required: \(admin or none\)

### Procedure

1.  Record instance options and delete instances of the Virtual Agent Service Portal widget.

    1.  Locate each instance of the Virtual Agent Service Portal widget and open the instance options.

    2.  Record the values.

    3.  Delete the widget instance.

2.  If your widget instance included a color instance option, add the color variable to the portal theme record.

    1.  Navigate to **Service Portal** &gt; **Themes**.

    2.  Open the theme record for the portal.

    3.  In the **CSS variables** field, add the `$sp-agent-chat-bg` variable and set the value to the desired color.

        ```
        $sp-agent-chat-bg: #ff0000
        ```

3.  If your widget instance options included URL parameters, add them to the Service Portal Agent Chat Configurations form **Server script** field.

    **Note:** The portal suffix, page ID, and language are automatically available to Agent Chat and do not require a custom script. Sys ID and table are automatically available to Agent Chat when they are present in the URL.

    1.  Navigate to the record in the Service Portal Agent Chat Configurations \[sp\_agent\_chat\_config\] table for the desired portal.

    2.  In the **Server script** field, write a custom script to pass the parameters to Agent Chat.

        This example returns the value of the chat\_queue field to the current conversation.

        ```
        (function ($sp) {    
        	return {        
        		chat_queue: $sp.getValue('chat_queue')    
        	};
        })($sp);
        ```


### Result

Widget instances are removed from individual portal pages. Instead, the portal applies the Service Portal Agent Chat Configurations record to every portal page.

## Pass page data to Agent Chat

Use the spContextManager class in a widget client script to pass dynamic page data to Agent Chat. For example, pass the number of approvals in the Approvals widget to Agent Chat when a user initiates a conversation from the Service Portal homepage.

### Before you begin

Role required: admin

Examine the widget to understand how data is passed to the widget client script. To make data available to Agent Chat, you must pass it to the spContextManager service. You can then access the data in a Virtual Agent topic using the `vaContext` object. For more information about using context variables in Virtual Agent scripts, see [Virtual Agent scripts](https://www.servicenow.com/docs/access?context=virtual-agent-scripts&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US).

### Procedure

1.  Open the widget in the widget editor.

2.  Update the widget client script.

    1.  Inject the spContextManager service into the widget client script function.

    2.  Pass variables to Agent Chat using the spContextManager API.

    This example passes `approval_count` to Agent Chat. When a user initiates a conversation from the Service Portal homepage, the system appends `&sysparm_approval_count=5` to the Agent Chat `iframe` URL.

    ```
    function ($scope, spContextManager) {
    
       spContextManager.addContext('agent-chat', {
          'approval_count': 5       
       });
    };
    ```

    Keys passed to this API are unique per page. For example, if the `'agent-chat'` key is already initialized by another widget on the page through the addContext\(\) method, you must use the updateContextForKey\(\) method to update the key's data.. For more information about the spContextManager class, see [spContextManager](https://www.servicenow.com/docs/access?context=spContextManagerAPI&version=zurich&pubname=zurich-api-reference&ft:locale=en-US).

3.  Click **Save.**

4.  Use Service Portal data in a Virtual Agent topic.

    1.  Navigate to **Virtual Agent** &gt; **Designer** and open the topic in which you would like to use Service Portal data.

    2.  Click **Edit Topic Flow**.

    3.  Configure the topic as needed.

        In a script field, use the `vaContext` object to access the context variable passed from the Service Portal.

        For more information about creating a Virtual Agent topic, see [Create a Virtual Agent topic](https://www.servicenow.com/docs/access?context=create-virtual-agent-topic&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US).

        For example, this script accesses the value of the `approval_count` variable in the Approvals widget.

        ```
        (function execute() {
            return "Your approval count is: " + vaContext.approval_count;
        })()
        
        ```

    4.  Save and publish the topic.


### Result

Agent Chat can access the variables when an end user initiates a conversation from the Service Portal page.

![Agent Chat displays the value of the variable.](../image/agent-chat-client.png)

## Remove Live Chat link from the header menu

If your portal includes a Live Chat link in the header menu, you can remove it by updating the widget's option schema.

### Before you begin

Role required: admin

### About this task

Adding the **Chat Queue** field to a portal record adds the Live Chat link to the portal's header menu. If you integrate your portal with Agent Chat, the Live Chat link is no longer needed.

### Procedure

1.  In the Service Portal configuration page, navigate to **Portal Tables** &gt; **Instance with Menu**.

2.  Open the record for your portal's header menu.

    For example, open **SP Header Menu** if using the base system portal.

3.  In the **Additional options, JSON format** field, add the following JSON key-value pair.

    ```
    “enable_live_chat”: {
        “displayValue”: “false”,
        “value”: false
    }
    ```

    The final JSON looks like this.

    ```
    {
        “enable_cart”: {
            “displayValue”: “true”,
            “value”: true
        },
         “enable_wishlist”: {
           “displayValue”: “true”,
             “value”: true
         },
        “enable_live_chat”: {
          “displayValue”: “false”,
            “value”: false
        }
    }
    ```

4.  Click **Update**.


### Result

When you navigate to the portal, **Live Chat** does not appear in the header menu.

