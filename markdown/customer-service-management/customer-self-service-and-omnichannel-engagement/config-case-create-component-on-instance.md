---
title: Configure the Case create component instance
description: Configure the Case create component instance so that your users can embed it within their website to address any issues related to product and services from their website directly.
locale: en-US
release: australia
product: Customer Self-service and Omnichannel Engagement
classification: customer-self-service-and-omnichannel-engagement
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Case create component, Configure web components, Configure Web Embeddables, Set up self-service, Configure, Customer Service Management]
---

# Configure the Case create component instance

Configure the Case create component instance so that your users can embed it within their website to address any issues related to product and services from their website directly.

## Before you begin

You must have the following setup to configure the Case create component:

-   Enable Web Embeddables in your instance. For more information, see [Activate Web Embeddables](act-web-embeddables.md).
-   [Set up a custom URL as the instance URL](set-up-custom-url.md).
-   Authenticate the ServiceNow components using OpenID Connect \(OIDC\) or non OIDC authentication. For more information, see [Authenticate the ServiceNow components using OIDC](authenticate-sn-webcomponents-oidc.md) and [Non OIDC authentication for ServiceNow components](../concept/auth-sn-webcomponents-non-oidc.md).

Role required: sn\_embeddable\_core.emb\_admin

## Procedure

1.  Navigate to **All** &gt; **Web Embeddables** &gt; **Homepage**.

2.  In the homepage, select Create module or use the existing module.

    For more information on creating a new module, see [Create a module](../concept/create-we-module.md).

3.  On the module page, in the Components tab, add a Case create component instance to an existing or a new group.

    For more information on creating a group and then adding a component instance, see [Create a group and add a component instance](we-create-group-and-add-comp-instance.md).

4.  Toggle the **Show static preview** option to see a visual representation of a component instance when a live preview isn’t available.

    **Note:** When enabled, any changes to the global or component properties don't appear in the Preview tab in real-time.

5.  Configure the Case create component instance properties.

    -   The Preview tab displays real-time data according to choices set in the component properties.
    -   For a description of the component properties related to the Case create component instance, see [Component properties for the Case create](../reference/comp-properties-case-create.md).
6.  Select the **CORS rules** tab to configure the CORS rules.

    For more information about configuring CORS rules, see [Configure CORS \(Cross-Origin Resource Sharing\) rules before embedding ServiceNow components](configure-cors-for-web-components.md).

7.  Select the **Components** tab.

    If a message appears about the application scope, change the scope to **Web Components for Customer Service** to be able to edit the record.

8.  Select the **Get embed code**.

    A pop-up window appears to display both Global code and Component code.

9.  In the Global code tab, review the generated code and select the **Copy global code**.

    The global code must only be added once to your third-party webpage.

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

    **Note:** Enabling the event handler also modifies the component code. For more information on event handlers in Web Embeddables, see [Event handlers in the Case create component](../reference/we-case-create-event-handlers.md).

11. In the Component code tab, review the generated code and select the **Copy component code**.

    This generated code also includes event handlers.

    ```
    <!--  
        Module: Demo module
        Group: Group 1
        Instance: Case create 1
    -->
    <sn-embedx-case-form
    	sys-id="de45c412c312310015519f2974d3ae1b"
    	confirmation-text="Case submitted successfully!"
    	confirmation-sub-text="Estimated resolution in 24 hours"
    	reference-number-label="Reference Number :"
    	primary-button-label="View details"
    	secondary-button-label="Browse services">
    </sn-embedx-case-form>
    <!--
    	The component also includes the following additional properties:
    	hide-reference-number
    	hide-primary-button
    	hide-secondary-button
    	hide-record-created-confirmation
    	hide-errors
    	hide-notifications
    -->
    
    <script type="module">
    	import { getEmbeddables, setEvents, setProperties } from 'https://demo.servicenow.com/uxasset/externals/sn_embeddable_core/index.jsdbx';
    	
    	const snEmbedxCaseForm = document.querySelector('sn-embedx-case-form');
    
    	/* Uncomment this code for the default behaviour of the Case create component.
    
    	// Get the record producer record id from the current URL.
    	// Optionally, get query to pre fill the form.
    	const currentURL = new URL(window.location.href);
    	const urlParams = new URLSearchParams(currentURL.search);
    	const product = urlParams.get('emb_product');
    	// Update the sysId of the component property.
    	// Optionally, update the prefill fields property
    	const prefillConfig = {
    		product: product
    	};
    	setProperties(snEmbedxCaseForm,{
    		prefillFields: prefillConfig
    	});
    */
    
    	getEmbeddables(["sn-embedx-case-form"]);
    
    	const eventHandlers = {
    		'SN_EMBEDX_CASE_FORM#COMPONENT_ERROR' : (e) => {
    			// This event is dispatched when a property validation or internal error occurs.
    			var {errorMessage, errorType} = e.detail.payload;
    			console.log(errorMessage, errorType);
    		},
    		'SN_EMBEDX_CASE_FORM#COMPONENT_READY' : (e) => {
    			// This event is dispatched when a component is ready and usable.
    		},
    		'SN_EMBEDX_CASE_FORM#BUTTON_CLICKED' : (e) => {
    			// This event is dispatched if any button is clicked on the confirmation message.
    			var {table, record_sys_id, button_variant} = e.detail.payload;
    			var primaryURL =  '/caseview'; // Replace with the URL of the case view page
    			var secondaryURL = '/browse'; // Replace with the URL of the secondary page
    
    			if(button_variant == 'primary') {
    				// Construct the URL for the Case View component with URL parameters
    				const caseViewURL = primaryURL+'?emb_table='+table+'&emb_recordid='+record_sys_id;
    				open(caseViewURL,'_self'); // Open case record when primary button is clicked
    			}
    			else {
    				// Open the Case View component in the same tab
    				open(secondaryURL,'_self');
    			}
    		},
    		'SN_EMBEDX_CASE_FORM#RECORD_CREATION_SUCCEEDED' : (e) => {
    			// This event is dispatched if the record was successfully created.
    			var {table, record_sys_id} = e.detail.payload;
    			console.log(table, record_sys_id);
    		},
    		'SN_EMBEDX_CASE_FORM#RECORD_CREATION_FAILED' : (e) => {
    			// This event is dispatched if the record creation has failed.
    		},
    		'SN_EMBEDX_CASE_FORM#COMPONENT_NOTIFICATION_SENT' : (e) => {
    			// This event is dispatched when the component provides a notification for the end user.
    			var {items} = e.detail.payload;
    			console.log(items);
    		}
    	};
    
    	setEvents(snEmbedxCaseForm, eventHandlers);
    </script>
    
    ```


## Result

The global and component codes are ready to be shared with the third-party administrator to embed the Case create component instance on their third-party website.

## What to do next

[Embed the Case create component instance on the third-party website](embed-case-create-component-on-third-party-website.md)

**Related topics**  


[Component properties for the Case create](../reference/comp-properties-case-create.md)

[Event handlers in the Case create component](../reference/we-case-create-event-handlers.md)

[Sample code for the Case create component](../reference/we-case-create-sample-code.md)

