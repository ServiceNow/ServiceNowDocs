---
title: Configure the Case list component instance
description: Configure the Case list component instance so that your user can embed it on their website to access the list of all cases from their website directly.
locale: en-US
release: australia
product: Customer Self-service and Omnichannel Engagement
classification: customer-self-service-and-omnichannel-engagement
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Case list component, Configure web components, Configure Web Embeddables, Set up self-service, Configure, Customer Service Management]
---

# Configure the Case list component instance

Configure the Case list component instance so that your user can embed it on their website to access the list of all cases from their website directly.

## Before you begin

You must have the following setup to configure the Case list component instance:

-   Enable Web Embeddables in your instance. For more information, see [Activate Web Embeddables](act-web-embeddables.md).
-   [Set up a custom URL as the instance URL](set-up-custom-url.md).
-   Authenticate the ServiceNow components using OpenID Connect \(OIDC\) or non OIDC authentication. For more information, see [Authenticate the ServiceNow components using OIDC](authenticate-sn-webcomponents-oidc.md) and [Non OIDC authentication for ServiceNow components](../concept/auth-sn-webcomponents-non-oidc.md).

Role required: sn\_embeddable\_core.emb\_admin

## Procedure

1.  Navigate to **All** &gt; **Web Embeddables** &gt; **Homepage**.

2.  In the homepage, select Create module or use the existing module.

    For more information on creating a new module, see [Create a module](../concept/create-we-module.md).

3.  On the module page, in the Components tab, add a Case list component instance to an existing or a new group.

    For more information on creating a group and then adding a component instance, see [Create a group and add a component instance](we-create-group-and-add-comp-instance.md).

4.  Toggle the **Show static preview** option to see a visual representation of a component when a live preview isn’t available.

    **Note:** When enabled, any changes to the global or component properties don't appear in the Preview tab in real-time.

5.  Configure the Case list component instance properties.

    -   The Preview tab displays real-time data according to choices set in the component properties.
    -   For a description of the component properties related to the Case list component instance, see [Component properties for the Case list](../reference/component-properties-for-the-case-list.md).
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

    **Note:** Enabling the event handler also modifies the component code. For more information on event handlers in Web Embeddables, see [Event handler in the Case list component](../reference/we-case-list-event-handlers.md).

11. In the Component code tab, review the generated code and select the **Copy component code**.

    This generated code also includes event handlers.

    ```
    <!--  
        Module: Demo module
        Group: Group 1
        Instance: Case list 1
    -->
    <sn-embedx-case-list
    	table="sn_customerservice_case"
    	limit="20"
    	list-title="List of Cases"
    	query="state=10"
    	columns="number,short_description,sys_updated_on,state">
    </sn-embedx-case-list>
    <!--
    	The component also includes the following additional properties:
    	hide-header
    	hide-last-refreshed-text
    	hide-record-count
    	hide-search
    	hide-refresh
    	show-filters
    	hide-when-empty
    	disable-column-resizing
    	hide-errors
    	view
    -->
    
    <script type="module">
    	import { getEmbeddables, setEvents, setProperties } from 'https://demo.servicenow.com/uxasset/externals/sn_embeddable_core/index.jsdbx';
    	
    	const snEmbedxCaseList = document.querySelector('sn-embedx-case-list');
    
    	getEmbeddables(["sn-embedx-case-list"]);
    
    	const eventHandlers = {
    		'SN_EMBEDX_CASE_LIST#RECORD_SELECTED' : (e) => {
    			// This event is dispatched when a record is selected.
    			var {table, record_sys_id} = e.detail.payload;
    			// the logic to construct the URL for the Case View component. Add your portal URL here.
    			const caseViewURL = '/caseview?emb_table='+table+'&emb_recordid='+record_sys_id;
    			// Redirect to the Case View component page
    			open(caseViewURL,'_self');
    		},
    		'SN_EMBEDX_CASE_LIST#COMPONENT_READY' : (e) => {
    			// This event is dispatched when a component is ready and usable.
    		},
    		'SN_EMBEDX_CASE_LIST#COMPONENT_ERROR' : (e) => {
    			// This event is dispatched when a property validation or internal error occurs.
    			var {errorMessage, errorType} = e.detail.payload;
    			console.log(errorMessage, errorType);
    		}
    	};
    
    	setEvents(snEmbedxCaseList, eventHandlers);
    </script>
    
    ```


## Result

The global and component codes are ready to be shared with the third-party administrator to embed the Case list component instance on their third-party website.

## What to do next

[Embed the Case list component instance on the third-party website](embed-case-list-component-on-third-party-website.md)

**Related topics**  


[Component properties for the Case list](../reference/component-properties-for-the-case-list.md)

[Event handler in the Case list component](../reference/we-case-list-event-handlers.md)

[Sample code for the Case list component](../reference/we-case-list-sample-code.md)

