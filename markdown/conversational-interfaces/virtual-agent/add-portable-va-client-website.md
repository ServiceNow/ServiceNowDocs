---
title: Add the portable Virtual Agent chat widget to a third-party website
description: To use the portable chat widget for Virtual Agent on third-party web pages, add the necessary code to your web page.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/conversational-interfaces/virtual-agent/add-portable-va-client-website.html
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 7
keywords: [Add, portable, Virtual Agent, chat widget, third-party]
breadcrumb: [Adding Virtual Agent to your web page, Configure, Virtual Agent, Conversational Interfaces]
---

# Add the portable Virtual Agent chat widget to a third-party website

To use the portable chat widget for Virtual Agent on third-party web pages, add the necessary code to your web page.

## Before you begin

[Configure the portable Virtual Agent chat widget](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/virtual-agent/configure-portable-va-web-client.md) before completing this topic's steps.

For more information, review the [How to embed Virtual Agent in an external site](https://www.servicenow.com/community/virtual-agent-nlu-articles/how-to-embed-virtual-agent-in-an-external-site-updated-for-tokyo/ta-p/2308092) article on the ServiceNow Community site.

**Note:** Interactive view and the ability to move and drag the chat window are currently unavailable in embedded enhanced chat.

Role required: virtual\_agent\_admin or admin

## About this task

Both enhanced and standard chat code is included in this topic. Review the beginning of each step to confirm you're implementing the applicable chat experience's steps.

## Procedure

1.  Enhanced chat only: Verify that your enhanced chat assistant is linked to a portal in **Conversational Interfaces** &gt; **Assistant Designer** &gt; **\[Assistant name\]**.

    You can link to either a placeholder portal or an applicable portal. The portal suffix, for example, `esc`, is required for the following step.

2.  Enhanced chat only: Import and instantiate this script reference to the page header to create a ServiceNow chat instance on your external page header:

    **Note:** In the script reference example, `site1.example.com` refers to the URL for your ServiceNow instance.

    ```
    <script type="module" > 
         import {EnhancedChat} from "https://site1.example.com/uxasset/externals/embedded-enhanced-chat/index.jsdbx?sysparm_substitute=false"; 
         var chat = new EnhancedChat ({ instance: https://site1.example.com, portal:<portal-suffix> }); 
       </script> 
    ```

    **Tip:** If your organization uses a custom domain name, input the custom domain name as the instance property, rather than the ServiceNow domain name, to verify that browser results are consistent among multiple browsers.

    -   **JSON configuration schema**

        ```
        instance: <string> - required. Origin of your ServiceNow instance, e.g.
            'https://yourco.service-now.com'.
        portal: <string> - required. ServiceNow portal suffix (e.g. 'esc', 'sp', or a
            custom portal's suffix). Sent as the embed URL's `portal_suffix` param.
        manageNowLogin: <boolean> - default false. When true, listens for the iframe's
            SESSION_CREATED (unauthenticated) and SESSION_LOGGED_OUT postMessages and
            redirects the *host page* to the instance's SSO login when either fires.
        showSupportAndSettingsMenu: <boolean> - default false. Shows the chat's built-in
            support/settings menu.
        context: <object> - flat map of sysparm-style query params appended as-is to the
            embed URL, e.g. { skip_load_history: 1, sysparm_debug: true }. Keys/values are
            not validated or transformed - sent through with String(value).
        pinnable: <boolean> - default true. Shows/hides the header's pin button, which
            docks the panel full-height along the screen edge (position: 'pinned').
        expandable: <boolean> - default true. Shows/hides the header's expand button,
            which blows the panel up into a centered modal (position: 'modal').
        position: <'modal' | 'pinned' | undefined> - initial docking state of the panel.
            Leave undefined for the default floating panel. Also changes at runtime when a
            visitor clicks the pin/expand buttons (see Events, below) - this is docking
            state, not which side of the screen the launcher sits on (there's currently no
            config for that; the launcher is fixed bottom-right).
        container: <HTMLElement> - default document.body. Where the widget's root element
            is appended.
        title: <string> - default 'Now Assist'. Header title text and the iframe's
            accessible title.
        
        unread: <object> - unread-message badge and proactive nudges. See "Unread
            messages and proactive nudges" below for what this does and its limits.
            enabled: <boolean> - default true. Set false to disable all of it.
            notificationSoundUrl: <string> - URL of a chime played when a new unread
                message arrives. No sound plays if omitted; there's no bundled default.
        
        branding: <object> - colors accept any valid CSS color value (hex, rgb(), a named
            color, etc), not just rgb tuples or hex codes. Grouped by which part of the
            widget each field paints, so it's always explicit whether a color applies to
            just the launcher button, just the chat panel, just its header, or both.
            launcher: <object> - the always-visible floating button that opens/closes
                the panel.
                bgColor: <string> - background color, default state (default: a
                    green-to-blue gradient; set this to any solid color to replace it).
                bgColorHover: <string> - background color on hover. The button also
                    scales up slightly on hover (not configurable).
                bgColorActive: <string> - background color while pressed/active.
                color: <string> - icon color, default state.
                colorHover: <string> - icon color on hover.
                colorActive: <string> - icon color while pressed/active.
                openIcon: <string> - URL of a custom icon for the closed state (default: a sparkle).
                sizeMultiplier: <number> - scales the button and its icon uniformly
                    (default is a 60px button with a 24px icon).
            panel: <object> - the chat panel/window itself, not including its header.
                bgColor: <string> - background color.
                border: <string> - full CSS `border` shorthand, e.g. '1px solid #d1d5db'.
                    Whole-property override, not separate color/width/style fields.
                shadow: <string> - full CSS `box-shadow` value, e.g.
                    '0 4px 12px rgba(0,0,0,0.2)'.
            header: <object> - the header bar inside the panel (title, and its
                expand/pin/close buttons).
                iconColor: <string> - title icon color.
                titleIcon: <string> - URL of a custom title icon (default: a sparkle).
                buttonColor: <string> - expand/pin/close buttons' icon color, default
                    state.
                buttonColorActive: <string> - buttons' icon color while aria-pressed
                    (i.e. the expand button when position is 'modal', or the pin
                    button when position is 'pinned').
                buttonBgColorHover: <string> - buttons' background on hover.
                buttonBgColorActive: <string> - buttons' background while aria-pressed.
                expandIcon: <string> - URL of a custom icon for the expand button,
                    default state.
                collapseIcon: <string> - URL of a custom icon for the expand button,
                    expanded (position: 'modal') state.
                pinIcon: <string> - URL of a custom icon for the pin button, default
                    state.
                pinnedIcon: <string> - URL of a custom icon for the pin button, pinned
                    (position: 'pinned') state.
            closeIcon: <string> - URL of a custom icon shared by the launcher's open
                state and the header's close button (both mean "close this widget").
            focusRing: <string> - full CSS `box-shadow` value for the focus-visible ring,
                shared by both the launcher and header buttons.
        
        offsetX: <number> - default 25. Distance in pixels the widget is offset from its
            default right edge.
        offsetY: <number> - default 25. Distance in pixels the widget is offset from its
            default bottom edge.
        
        zIndex: <number> - default 1000. Stacking order of the widget while not in modal
            position.
        modalZIndex: <number> - default 4000. Stacking order while position is 'modal'.
        modalWidth: <string> - default '95vw'. Any valid CSS size (e.g. '900px', '80%').
        modalHeight: <string> - default '85vh'. Any valid CSS size.
        
        translations: <object> - overrides for the widget's built-in English aria-labels.
            Every button in the widget is icon-only, so these are its accessible names, not
            visible tooltip text.
            openLabel: <string> - launcher, closed state. Default 'Open chat'.
            closeLabel: <string> - launcher opened state, and the header's close button.
                Default 'Close chat'.
            pinLabel: <string> - header's pin button, default state. Default 'Pin'.
            unpinLabel: <string> - header's pin button, pinned state. Default 'Unpin'.
            expandLabel: <string> - header's expand button, default state. Default
                'Expand'.
            contractLabel: <string> - header's expand button, expanded state. Default
                'Contract'.
        ```

3.  Standard chat only:Import and instantiate this script reference to the page header to create a ServiceNow chat instance on your external page header:

    **Note:** In the script reference example, `site1.example.com` refers to the URL for your ServiceNow instance.

    ```
    <script type="module" >
          import ServiceNowChat from "https://site1.example.com/uxasset/externals/now-requestor-chat-popover-app/index.jsdbx?sysparm_substitute=false";
          var chat = new ServiceNowChat({ instance: "https://site1.example.com/", });
        </script>
    ```

    **Tip:** If your organization uses a custom domain name, input the custom domain name as the instance property, rather than the ServiceNow domain name, to verify that browser results are consistent among multiple browsers.

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


**Parent Topic:**[Use the portable chat widget to add Virtual Agent to your web page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/virtual-agent/use-portable-va-web-client.md)

