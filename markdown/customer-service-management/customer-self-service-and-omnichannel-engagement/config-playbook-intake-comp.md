---
title: Configure the Playbook intake component instance
description: Configure the Playbook intake component instance so that your users can embed it on their website and submit cases using playbook guided experience from their website directly.
locale: en-US
release: australia
product: Customer Self-service and Omnichannel Engagement
classification: customer-self-service-and-omnichannel-engagement
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Playbook intake component, Configure web components, Web Embeddables, Set up self-service, Configure, Customer Service Management]
---

# Configure the Playbook intake component instance

Configure the Playbook intake component instance so that your users can embed it on their website and submit cases using playbook guided experience from their website directly.

## Before you begin

You must have the following setup to configure the Playbook intake component instance:

-   Enable Web Embeddables in your instance. For more information, see [Activate Web Embeddables](act-web-embeddables.md).
-   [Set up a custom URL as the instance URL](set-up-custom-url.md).
-   Authenticate the ServiceNow components using OpenID Connect \(OIDC\) or non OIDC authentication. For more information, see [Authenticate the ServiceNow components using OIDC](authenticate-sn-webcomponents-oidc.md) and [Non OIDC authentication for ServiceNow components](../concept/auth-sn-webcomponents-non-oidc.md).

Role required: sn\_embeddable\_core.emb\_admin

## Procedure

1.  Navigate to **All** &gt; **Web Embeddables** &gt; **Homepage**.

2.  In the homepage, select Create module or use the existing module.

    For more information on creating a new module, see [Create a module](../concept/create-we-module.md).

3.  On the module page, in the Components tab, add a Playbook intake component instance to an existing or a new group.

    For more information on creating a group and then adding a component instance, see [Create a group and add a component instance](we-create-group-and-add-comp-instance.md).

4.  Toggle the **Show static preview** option to see a visual representation of a component when a live preview isn’t available.

    **Note:** When enabled, any changes to the global or component properties don't appear in the Preview tab in real-time.

5.  Configure the Playbook intake component instance properties.

    -   The Preview tab displays real-time data according to choices set in the component properties.
    -   For a description of the component properties related to the Playbook intake component instance, see [Component properties for the Playbook intake](../reference/we-playbook-intake-comp-prop.md).
6.  Select the **CORS rules** tab to configure the CORS rules.

    For more information about configuring CORS rules, see [Configure CORS \(Cross-Origin Resource Sharing\) rules before embedding ServiceNow components](configure-cors-for-web-components.md).

7.  Select the **Components** tab.

    If a message appears about the application scope, change the scope to **Web Components for Customer Service** to be able to edit the record.

8.  Select the **Get embed code**.

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

10. In the Component Code tab, slide the **Enable event handler** toggle switch to handle events triggered by the user interactions on the website.

    **Note:** Enabling the event handler also modifies the component code. For more information on event handlers in Web Embeddables, see [Event handler in the Playbook intake component](../reference/we-playbook-intake-event-handler.md).

11. In the Component code tab, review the generated code and select the **Copy component code**.

    The generated component code also includes configurations for event handlers.

    ```
    <!--  
        Module: Demo module
        Group: Group 1
        Instance: Playbook intake 1
    -->
    <sn-embedx-playbook-intake
    	table="sn_onboarding_case"
    	sys-id="-1"
    	playbook-title="Create case with playbook"
    	stage-orientation="horizontal"
    	max-visible-stages="5"
    	activity-view-mode="focused"
    	playbook-experience="0d71033773f220109edbc1f52ff6a741"
    	record-generator="494435eb53a231103466ddeeff7b12e0"
    	confirmation-text="Case submitted successfully!"
    	confirmation-sub-text="Estimated resolution in 24 hours"
    	reference-number-label="Reference Number :"
    	primary-button-label="View details"
    	secondary-button-label="Browse services">
    </sn-embedx-playbook-intake>
    <!--
    	The component also includes the following additional properties:
    	hide-stages
    	hide-errors
    	hide-reference-number
    	hide-primary-button
    	hide-secondary-button
    	hide-record-created-confirmation
    	prefill-fields
    -->
    
    <script type="module">
    	import { getEmbeddables, setEvents, setProperties } from 'https://demo.servicenow.com/uxasset/externals/sn_embeddable_core/index.jsdbx';
    	
    	const snEmbedxPlaybookIntake = document.querySelector('sn-embedx-playbook-intake');
    
    	/* Uncomment this code for the default behaviour of the Playbook intake component.
    
    	// Get the table, playbook title, record generator and pre-fill fields from the current URL
    	const currentURL = new URL(window.location.href);
    	const urlParams = new URLSearchParams(currentURL.search);
    	const tableName = urlParams.get('emb_table');
    	const playbookTitle = urlParams.get('emb_playbook_title');
    	const recordGenerator = urlParams.get('emb_record_generator');
    	const prefillFields = urlParams.get('emb_prefill_fields');
    
    	// Update the properties of the componentProperties object
    	setProperties(snEmbedxPlaybookIntake,{table: tableName,recordGenerator:recordGenerator,playbookTitle:playbookTitle,prefillFields:prefillFields});
    	*/
    
    	getEmbeddables(["sn-embedx-playbook-intake"]);
    
    	const eventHandlers = {
    		'SN_EMBEDX_PLAYBOOK_INTAKE#COMPONENT_READY' : (e) => {
    			// This event is dispatched when a component is ready and usable.
    		},
    		'SN_EMBEDX_PLAYBOOK_INTAKE#COMPONENT_ERROR' : (e) => {
    			// This event is dispatched when a property validation or internal error occurs.
    			var {errorType, errorMessage} = e.detail.payload;
    			console.log(errorType, errorMessage);
    		},
    		'SN_EMBEDX_PLAYBOOK_INTAKE#RECORD_CREATION_SUCCEEDED' : (e) => {
    			// Dispatched when a record is created by a Record Generator Playbook.
    			var {table, sysId, number, playbook_experience_id, hide_record_creation} = e.detail.payload;
    			if(hide_record_creation){
    				var primaryURL =  '/caseview'; // Replace with the URL of the case view page
    
    				// Construct the URL for the Case View component with URL parameters
    				const caseViewURL = primaryURL + '?emb_table=' + table + '&emb_recordid=' + sysId + (playbook_experience_id === '98e09a560f2200102920c912d4767e1a' ? '' : '&emb_playbook_experience=' + playbook_experience_id);
    				open(caseViewURL,'_self'); // Open case record when record created confirmation is hidden
    			}
    		},
    		'SN_EMBEDX_PLAYBOOK_INTAKE#PRIMARY_BUTTON_CLICKED' : (e) => {
    			// This event is dispatched when primary button is clicked on the record created confirmation page.
    			var {table, record_sys_id, playbook_experience_id} = e.detail.payload;
    			var primaryURL =  '/caseview'; // Replace with the URL of the case view page
    
    			// Construct the URL for the Case View component with URL parameters
    			const caseViewURL = primaryURL + '?emb_table=' + table + '&emb_recordid=' + record_sys_id + (playbook_experience_id === '98e09a560f2200102920c912d4767e1a' ? '' : '&emb_playbook_experience=' + playbook_experience_id);
    			open(caseViewURL,'_self'); // Open case record when primary button is clicked
    			
    		},
    		'SN_EMBEDX_PLAYBOOK_INTAKE#SECONDARY_BUTTON_CLICKED' : (e) => {
    			// This event is dispatched when secondary button is clicked on the record created confirmation page.
    			var {table, record_sys_id} = e.detail.payload;
    			var secondaryURL =  '/browse'; // Replace with the URL of the secondary page
    
    			// Open the Case View component in the same tab
    			open(secondaryURL,'_self');
    			
    		}
    	};
    
    	setEvents(snEmbedxPlaybookIntake, eventHandlers);
    </script>
    
    ```


## Result

The global and component codes are ready to be shared with the third-party administrator to embed the Playbook intake component instance on their third-party website.

## What to do next

[Embed the Playbook intake component instance on the third-party website](embed-playbook-intake-comp.md)

**Related topics**  


[Component properties for the Playbook intake](../reference/we-playbook-intake-comp-prop.md)

[Event handler in the Playbook intake component](../reference/we-playbook-intake-event-handler.md)

[Sample code for the Playbook intake component](../reference/we-playbook-intake-sample-code.md)

