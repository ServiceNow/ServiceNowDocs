---
title: Configure the Knowledge article view component instance
description: Configure the Knowledge article view component instance so that your users can embed it on their website to access knowledge articles from their website directly.
locale: en-US
release: australia
product: Customer Self-service and Omnichannel Engagement
classification: customer-self-service-and-omnichannel-engagement
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Knowledge article view component, Configure web components, Configure Web Embeddables, Set up self-service, Configure, Customer Service Management]
---

# Configure the Knowledge article view component instance

Configure the Knowledge article view component instance so that your users can embed it on their website to access knowledge articles from their website directly.

## Before you begin

You must have the following setup to configure the Knowledge article view component instance:

-   Enable Web Embeddables in your instance. For more information, see [Activate Web Embeddables](act-web-embeddables.md).
-   [Set up a custom URL as the instance URL](set-up-custom-url.md).
-   Authenticate the ServiceNow components using OpenID Connect \(OIDC\) or non OIDC authentication. For more information, see [Authenticate the ServiceNow components using OIDC](authenticate-sn-webcomponents-oidc.md) and [Non OIDC authentication for ServiceNow components](../concept/auth-sn-webcomponents-non-oidc.md).

Role required: sn\_embeddable\_core.emb\_admin

## Procedure

1.  Navigate to **All** &gt; **Web Embeddables** &gt; **Homepage**.

2.  In the homepage, select Create module or use the existing module.

    For more information on creating a new module, see [Create a module](../concept/create-we-module.md).

3.  On the module page, in the Components tab, add a Knowledge article view component instance to an existing or a new group.

    For more information on creating a group and then adding a component instance, see [Create a group and add a component instance](we-create-group-and-add-comp-instance.md).

4.  Toggle the **Show static preview** option to see a visual representation of a component when a live preview isn’t available.

    **Note:** When enabled, any changes to the global or component properties don't appear in the Preview tab in real-time.

5.  Configure the Knowledge article view component instance properties.

    -   The Preview tab displays real-time data according to choices set in the component properties.
    -   For a description of the component properties related to the Knowledge Article component instance, see [Component properties for the Knowledge article view](../reference/we-know-article-view-comp-prop.md).
6.  Select the **CORS rules** tab to configure the CORS rules.

    For more information about configuring CORS rules, see [Configure CORS \(Cross-Origin Resource Sharing\) rules before embedding ServiceNow components](configure-cors-for-web-components.md).

7.  Select the **Components** tab.

    If a message appears about the application scope, change the scope to **Web Components for Customer Service** to be able to edit the record.

8.  Select **Get embed code**.

    A pop-up window appears to display both Global code and Component code.

9.  In the Global code tab, review the generated code and select the **Copy global code**.

    The global code only must be added once to your third-party webpage.

    ```
    import { init, login, logout, startGuestSession } from 'https://demo.servicenow.com/uxasset/externals/sn_embeddable_core/index.jsdbx';
    
    await init({
        theme: 'fad87d2ca304121029a4d1aed31e610f',  /* sys_id of the theme to use for the embeddable components in your website */
        baseURL: 'https://demo.servicenow.com', /* Base URL of the instance to be used for the embeddable components in your website */
        authCallback: getTokenCallBack, /* Function which returns the auth token for the current user, required for auth setup */
        module: '591800ffc1243610f87714367ed47c6a', /* Demo module */
        pageName: document.title, /* Uses the browser's document title as the page name in User analytics experience */
        guestTokenCallback: getGuestJWTTokenCallBack, /* Function which returns the guest token for the current user, required for guest validation setup */
        cacheComponents: [] /* Pre-caches resources for improved performance. Update component list as per your usage */
    });
    
    function getTokenCallBack() {
        var idToken; /* Get the id token for the current user */
        return Promise.resolve(idToken);
    }
    
    function getGuestJWTTokenCallBack() {
        var guestToken; /* Get the guest token for the current user */
        return Promise.resolve(guestToken);
    }
    
    /* Uncomment below function to handle guest session */
    // await startGuestSession();
    
    /* Uncomment below functions to handle login and logout once the user logs into your website */
    // await login();
    // await logout();
    ```

10. In the Component Code tab, slide the **Enable event handler** toggle switch to handle events triggered by the user interactions on the webpage.

    **Note:** Enabling the event handler also modifies the component code. For more information on event handlers in Web Embeddables, see [Event handler in the Knowledge article view component](../reference/we-know-article-view-event-handler.md).

11. In the Component code tab, review the generated code and select the **Copy component code**.

    This generated code also includes event handlers.

    ```
    <!--  
        Module: Demo module
        Group: Group 1
        Instance: Knowledge article view 1
    -->
    <sn-embedx-kb-article-view record-id="9d25b5b8dbd92200d75270f5bf96198b"></sn-embedx-kb-article-view>
    <!--
    	The component also includes the following additional properties:
    	hide-header
    	hide-language-selector
    	hide-author-information
    	hide-reading-time
    	hide-last-updated
    	hide-view-count
    	hide-average-rating
    	hide-attachments
    	hide-helpful-option
    	hide-article-rating
    	disable-displaying-latest-article-version
    	hide-errors
    	hide-notifications
    -->
    
    <script type="module">
    	import { getEmbeddables, setEvents, setProperties } from 'https://demo.servicenow.com/uxasset/externals/sn_embeddable_core/index.jsdbx';
    	
    	const snEmbedxKbArticleView = document.querySelector('sn-embedx-kb-article-view');
    
    	getEmbeddables(["sn-embedx-kb-article-view"]);
    
    	const eventHandlers = {
    		'SN_EMBEDX_KNOWLEDGE_ARTICLE_VIEW#BACK_BUTTON_CLICKED' : (e) => {
    			// Event for back button clicked on mobile variant of knowledge article view.
    			//Redirect to the knowledge browse page
    			open('/knowledgebrowse', '_self');
    		},
    		'SN_EMBEDX_KNOWLEDGE_ARTICLE_VIEW#RATING_CLICKED' : (e) => {
    			// This event is dispatched when rating is provided for the article
    			var {rating} = e.detail.payload;
    			console.log(rating);
    		},
    		'SN_EMBEDX_KNOWLEDGE_ARTICLE_VIEW#LANGUAGE_DROPDOWN_CLICKED' : (e) => {
    			// This event is dispatched when language dropdown selection is clicked
    			var {articleID} = e.detail.payload;
    
    			// Set properties for the knowledge article view
    			setProperties(snEmbedxKbArticleView, {recordId: articleID});
    			
    		},
    		'SN_EMBEDX_KNOWLEDGE_ARTICLE_VIEW#NOTIFICATION_LINK_CLICKED' : (e) => {
    			// This event is dispatched when link present on notification has been clicked
    			var {table, sys_id} = e.detail.payload;
    
    			if(table == 'kb_knowledge') {
    				// Set properties for the knowledge article view
    				setProperties(snEmbedxKbArticleView, {recordId: sys_id});
    			}
    		},
    		'SN_EMBEDX_KNOWLEDGE_ARTICLE_VIEW#COMPONENT_READY' : (e) => {
    			// This event is dispatched when a component is ready and usable.
    		},
    		'SN_EMBEDX_KNOWLEDGE_ARTICLE_VIEW#COMPONENT_ERROR' : (e) => {
    			// This event is dispatched when a property validation or internal error occurs.
    			var {errorMessage, errorType} = e.detail.payload;
    			console.log(errorMessage, errorType);
    		},
    		'SN_EMBEDX_KNOWLEDGE_ARTICLE_VIEW#LINK_CLICKED' : (e) => {
    			// This event is dispatched when a record link has been clicked inside article body
    			var {table, sys_id} = e.detail.payload;
    			console.log(table, sys_id);
    		}
    	};
    
    	setEvents(snEmbedxKbArticleView, eventHandlers);
    </script>
    
    ```


## Result

The global and component codes are ready to be shared with the third-party administrator to embed the Knowledge article view component instance on their third-party website.

## What to do next

[Embed the Knowledge article view component instance on the third-party website](embed-know-article-view-comp.md)

**Related topics**  


[Component properties for the Knowledge article view](../reference/we-know-article-view-comp-prop.md)

[Event handler in the Knowledge article view component](../reference/we-know-article-view-event-handler.md)

[Sample code for the Knowledge article view component](../reference/we-know-article-view-sample-code.md)

