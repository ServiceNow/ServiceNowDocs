---
title: Add the Portable Virtual Agent Chat Widget to a third-party website
description: To use the Portable Chat Widget for Virtual Agent on third-party web pages, add the necessary code to your web page.
locale: en-US
release: xanadu
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2024-11-14"
reading_time_minutes: 2
keywords: [Add, Portable, Virtual Agent, chat widget, third-party]
breadcrumb: [Configuring the portable Virtual Agent chat widget, Configuring Virtual Agent, Virtual Agent, Conversational Interfaces]
---

# Add the Portable Virtual Agent Chat Widget to a third-party website

To use the Portable Chat Widget for Virtual Agent on third-party web pages, add the necessary code to your web page.

## Before you begin

[Configure the Portable Virtual Agent chat widget](configure-portable-va-web-client.md) prior to completing this topic's steps.

For additional information, review the [How to embed Virtual Agent in an external site](https://www.servicenow.com/community/virtual-agent-nlu-articles/how-to-embed-virtual-agent-in-an-external-site-updated-for-tokyo/ta-p/2308092) article on the ServiceNow Community site.

Role required: virtual\_agent\_admin or admin

## Procedure

1.  Import and instantiate this script reference to the page header to create a ServiceNow chat instance on your external page header:

    **Note:** In the script reference example, site1.example.com refers to the URL for your ServiceNow instance.

    ```
    <script type="module" >
          import ServiceNowChat from "https://site1.example.com/uxasset/externals/now-requestor-chat-popover-app/index.jsdbx?sysparm_substitute=false";
          var chat = new ServiceNowChat({ instance: "https://site1.example.com/", });
        </script>
    ```

    **Tip:** If your organization uses a custom domain name, input the custom domain name as the instance property, rather than the ServiceNow domain name, to ensure that browser results are consistent among multiple browsers.

    -   **Example with configuration**

        ```
        const chat = new ServiceNowChat({
        	instance: 'https://site1.example.com',
        	context: {
        		skip_load_history: 1
        	},
        	branding: {
        		bgColor: '#333',
        		primaryColor: '#000',
        		hoverColor: '#EFEFEF',
        		activeColor: '#AAA',
        		openIcon: 'custom-open.svg',
        		closeIcon: 'custom-close.svg',
        		sizeMultiplier: 1.6
        	},
        	offsetX: 50,
        	offsetY: 50,
        	position: 'left',
        	translations: {
        		'Open dialog': 'Open chat',
        		'Open Chat. {0} unread message(s)': 'Click to open',
        		'Close chat.': 'Click to close',
        	},
        });
        ```

    -   **JSON configuration schema**

        ```
        {
            instance: <string> - url to your instance, must be of the same domain (sub-domain)
            context: <object> - sys_parm variables to pass into the iframe
            branding: <object> - branding settings
                  bgColor: <rgb|hex> - can take an rgb tuple, ie: '56,56,56' or a 3 or 6 hex color code, ie: #333 or #efefef.  background color of button
           	primaryColor: <rgb|hex> - font color
           	hoverColor: <rgb|hex> - hover background color of button
           	activeColor: <rgb|hex> - click / active background color of button
           	openIcon: <string> - name of the uploaded custom icon in settings
           	closeIcon: <string> - name of the uploaded custom icon in settings
           offsetX: <integer> - distance in pixels the button moves along the x-axis
           offsetY: <integer> - distance in pixels the button moves along the y-axis
           position: <enum: left|right> - position left or right side of screen
           translations: <object> - contains label mappings for translations or label changes
           	'Open dialog': <string> - replacement text for accessibility
           	'Open Chat. {0} unread messages(s)': <string> - replacement text for tooltip
           	'Close chat.': <string> - replacement text for tooltip
        }
        ```


**Parent Topic:**[Configuring the portable Virtual Agent chat widget](../concept/use-portable-va-web-client.md)

