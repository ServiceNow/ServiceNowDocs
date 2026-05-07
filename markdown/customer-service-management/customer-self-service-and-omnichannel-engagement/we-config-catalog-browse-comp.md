---
title: Configure the Catalog browse component instance
description: Configure the Catalog browse component instance so that your user can embed it on their website to browse and search catalog items from different catalogs and categories.
locale: en-US
release: australia
product: Customer Self-service and Omnichannel Engagement
classification: customer-self-service-and-omnichannel-engagement
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Catalog browse component, Configure web components, Web Embeddables, Set up self-service, Configure, Customer Service Management]
---

# Configure the Catalog browse component instance

Configure the Catalog browse component instance so that your user can embed it on their website to browse and search catalog items from different catalogs and categories.

## Before you begin

You must have the following setup to configure the Catalog browse component instance:

-   Enable Web Embeddables in your instance. For more information, see [Activate Web Embeddables](act-web-embeddables.md).
-   [Set up a custom URL as the instance URL](set-up-custom-url.md).
-   Authenticate the ServiceNow components using OpenID Connect \(OIDC\) or non OIDC authentication. For more information, see [Authenticate the ServiceNow components using OIDC](authenticate-sn-webcomponents-oidc.md) and [Non OIDC authentication for ServiceNow components](../concept/auth-sn-webcomponents-non-oidc.md).

Role required: sn\_embeddable\_core.emb\_admin

## Procedure

1.  Navigate to **All** &gt; **Web Embeddables** &gt; **Homepage**.

2.  In the homepage, select Create module or use the existing module.

    For more information on creating a new module, see [Create a module](../concept/create-we-module.md).

3.  On the module page, in the Components tab, add a Catalog browse component instance to an existing or a new group.

    For more information on creating a group and then adding a component instance, see [Create a group and add a component instance](we-create-group-and-add-comp-instance.md).

4.  Toggle the **Show static preview** option to see a visual representation of a component when a live preview isn’t available.

    **Note:** When enabled, any changes to the global or component properties don't appear in the Preview tab in real-time.

5.  Configure the Catalog browse component instance properties.

    -   The Preview tab displays real-time data according to choices set in the component properties.
    -   For a description of the component properties related to the Catalog browse component, see [Component properties for the Catalog browse](../reference/we-catalog-browse-comp-prop.md).
6.  Select the **CORS rules** tab to configure the CORS rules.

    For more information about configuring CORS rules, see [Configure CORS \(Cross-Origin Resource Sharing\) rules before embedding ServiceNow components](configure-cors-for-web-components.md).

7.  Select **Components** tab.

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

    **Note:** Enabling the event handler also modifies the component code. For more information on event handlers in Web Embeddables, see [Event handlers in the Catalog browse component](../reference/we-event-handlers-catalog-browse.md).

11. In the Component code tab, review the generated code and select the **Copy component code**.

    This generated code also includes event handlers.

    ```
    <!--  
        Module: Demo module
        Group: Group 1
        Instance: Catalog browse 1
    -->
    <sn-embedx-catalog-browse selection-type="catalog"></sn-embedx-catalog-browse>
    <!--
    	The component also includes the following additional properties:
    	select-catalogs
    	select-categories
    	hide-price
    	hide-navigation-panel
    	hide-popular-requests
    	hide-recent-requests
    -->
    
    <script type="module">
    	import { getEmbeddables, setEvents, setProperties } from 'https://demo.servicenow.com/uxasset/externals/sn_embeddable_core/index.jsdbx';
    	
    	const snEmbedxCatalogBrowse = document.querySelector('sn-embedx-catalog-browse');
    
    	getEmbeddables(["sn-embedx-catalog-browse"]);
    
    	const eventHandlers = {
    		'CATALOG_BROWSE#COMPONENT_READY' : (e) => {
    			// This event is dispatched when a component is ready and usable.
    		},
    		'CATALOG_BROWSE#CATALOG_ITEM_SELECTED' : (e) => {
    			// This event is dispatched when a catalog item is selected.
    			var {catalog_item_details} = e.detail.payload;
    			// Logic to construct the URL based on the catalog item details
    			let redirectURL;
    			const type = catalog_item_details.type;
    
    			if (type === 'catalog_item' || type === 'record_producer') {
    				redirectURL = '/catalog_form?emb_recordid=' + catalog_item_details.sys_id;
    			} else if (type === 'content_item') {
    				const content_type = catalog_item_details.content_type;
    				if (content_type === 'kb') {
    					redirectURL = '/article_view?emb_recordid=' + catalog_item_details.kb_article;
    				} else if (content_type === 'external') {
    					redirectURL = catalog_item_details.url;
    				} else if (content_type === 'dynamic') {
    					const dynamicContentItemDetails = catalog_item_details.dynamicContentItemDetails;
    					// Check for 'Playbook' dynamic content type
    					if(dynamicContentItemDetails.dynamicContentType === 'c0e6a71443923110f6669c7385b8f20a')
    						redirectURL = '/playbook_intake?emb_playbook_title=' + dynamicContentItemDetails.content.title + '&emb_table=' + dynamicContentItemDetails.content.table + '&emb_record_generator=' + dynamicContentItemDetails.content.query + '&emb_playbook_experience=' + dynamicContentItemDetails.content.playbook_experience;
    				}
    			}
    			// Redirect to the respective component page
    			open(redirectURL, '_self');
    		},
    		'CATALOG_BROWSE#COMPONENT_EMPTY' : (e) => {
    			// This event is dispatched when a component has nothing to display.
    		},
    		'CATALOG_BROWSE#COMPONENT_ERROR' : (e) => {
    			// This event is dispatched when a component encounters an error.
    			var {errorMessage, errorType} = e.detail.payload;
    			console.log(errorMessage, errorType);
    		}
    	};
    
    	setEvents(snEmbedxCatalogBrowse, eventHandlers);
    </script>
    
    ```


## Result

The global and component codes are ready to be shared with the third-party administrator to embed the Catalog browse component instance on their third-party website.

## What to do next

[Embed the Catalog browse component on the third-party website](we-embed-catalog-browse-on-third-party-web.md)

**Related topics**  


[Component properties for the Catalog browse](../reference/we-catalog-browse-comp-prop.md)

[Event handlers in the Catalog browse component](../reference/we-event-handlers-catalog-browse.md)

[Sample code for the Catalog browse component](../reference/we-catalog-browse-samp-code.md)

