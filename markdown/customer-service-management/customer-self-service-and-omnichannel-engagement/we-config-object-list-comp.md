---
title: Configure the Object list component instance
description: Configure the Object list component instance so that your user can embed it on their website to display information from any ServiceNow table. The component allows you to configure column selection, filtering, sorting, and pagination options.
locale: en-US
release: australia
product: Customer Self-service and Omnichannel Engagement
classification: customer-self-service-and-omnichannel-engagement
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Object list component, Configure web components, Web Embeddables, Set up self-service, Configure, Customer Service Management]
---

# Configure the Object list component instance

Configure the Object list component instance so that your user can embed it on their website to display information from any ServiceNow table. The component allows you to configure column selection, filtering, sorting, and pagination options.

## Before you begin

You must have the following setup to configure the Object list component instance:

-   Enable Web Embeddables in your instance. For more information, see [Activate Web Embeddables](act-web-embeddables.md).
-   [Set up a custom URL as the instance URL](set-up-custom-url.md).
-   Authenticate the ServiceNow components using OpenID Connect \(OIDC\) or non OIDC authentication. For more information, see [Authenticate the ServiceNow components using OIDC](authenticate-sn-webcomponents-oidc.md) and [Non OIDC authentication for ServiceNow components](../concept/auth-sn-webcomponents-non-oidc.md).

Role required: sn\_embeddable\_core.emb\_admin

## Procedure

1.  Navigate to **All** &gt; **Web Embeddables** &gt; **Homepage**.

2.  In the homepage, select Create module or use the existing module.

    For more information on creating a new module, see [Create a module](../concept/create-we-module.md).

3.  On the module page, in the Components tab, add a Object list component instance to an existing or a new group.

    For more information on creating a group and then adding a component instance, see [Create a group and add a component instance](we-create-group-and-add-comp-instance.md).

4.  Toggle the **Show static preview** option to see a visual representation of a component when a live preview isn’t available.

    **Note:** When enabled, any changes to the global or component properties don't appear in the Preview tab in real-time.

5.  Configure the Object list component instance properties.

    -   The Preview tab displays real-time data according to choices set in the component properties.
    -   For a description of the component properties related to the Object list component instance, see [Component properties for the Object list](../reference/we-object-list-comp-prop.md).
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

    **Note:** Enabling the event handler also modifies the component code. For more information on event handlers in Web Embeddables, see [Event handlers in the Object list component](../reference/we-event-handlers-object-list.md).

11. In the Component code tab, review the generated code and select the **Copy component code**.

    This generated code also includes event handlers.

    ```
    <!--  
        Module: Demo module
        Group: Group 1
        Instance: Object list 1
    -->
    <sn-embedx-object-list
    	type="default"
    	table="sn_customerservice_case"
    	action-config="6316ec1355dd422a8ebfdeb6336b1179"
    	child-records-per-load="10"
    	max-cell-characters="500"
    	records-per-page='[10,20,50]'
    	visible-page-range="5"
    	footer-text="View All"
    	max-top-records="20"
    	header-size="md">
    </sn-embedx-object-list>
    <!--
    	The component also includes the following additional properties:
    	hide-header
    	hide-record-count
    	hide-search
    	hide-filters
    	disable-column-selection
    	hide-actions
    	max-columns-displayed
    	hide-record-links
    	show-reference-record-links
    	disable-column-highlighting
    	shade-alternate-rows
    	hide-child-record-count
    	disable-quick-edit
    	disable-cell-wrapping
    	disable-cell-editing
    	hide-errors
    	limit-records-fetched
    	hide-page-size-control
    	disable-cell-filtering
    	disable-column-sorting
    	disable-column-filtering
    	disable-column-grouping
    	show-condition-builder
    	hide-refresh-button
    	disable-title-wrap
    	disable-column-resizing
    	disable-column-drag-and-drop
    	disable-row-drag-and-drop
    	expand-groups-by-default
    	hide-toggle-all-groups-button
    	hide-when-empty
    	edit-query
    	default-filter
    	columns
    	list-view
    	nest-by
    	default-group-by
    	list-title
    	subtitle
    	highlighted-value-config
    -->
    
    <script type="module">
    	import { getEmbeddables, setEvents, setProperties } from 'https://demo.servicenow.com/uxasset/externals/sn_embeddable_core/index.jsdbx';
    	
    	const snEmbedxObjectList = document.querySelector('sn-embedx-object-list');
    
    	/* Uncomment this code to set Object list properties using URL parameters.
    
    	// Get the table, query, view or nestby from the URL parameters to dynamically set the component properties. For related list, get sysRecordID to use it in filter.
    	const currentURL = new URL(window.location.href);
    	const urlParams = new URLSearchParams(currentURL.search);
    	const tableName = urlParams.get('emb_table');
    	const filter = urlParams.get('emb_filter');
    	const view = urlParams.get('emb_view');
    	const nestby = urlParams.get('emb_nestby');
    	const sysRecordId = urlParams.get('emb_recordid');
    
    	// Update the table, filter, view or nestby properties of the component
    	setProperties(snEmbedxObjectList, {
    		table: tableName,
    		editQuery: filter || '<fieldname>=' + sysRecordId,
    		listView: view,
    		nestBy: nestby
    	});
    */
    
    	getEmbeddables(["sn-embedx-object-list"]);
    
    	const eventHandlers = {
    		'SN_EMBEDX_OBJECT_LIST#FOOTER_LINK_SELECTED' : (e) => {
    			// This event is dispatched when footer link is selected
    			var {table, view, edit_query, nest_by} = e.detail.payload;
    	// the logic to construct the URL for the Record View component. Add your portal URL here.
    	const objectListURL = '/objectlist?emb_table=' + table + '&emb_query=' + edit_query + '&emb_view=' + view + '&emb_nestby=' + nest_by;
    	// Open the Record List component in the same tab
    	open(objectListURL, '_self');
    		},
    		'SN_EMBEDX_OBJECT_LIST#COMPONENT_ERROR' : (e) => {
    			// This event is dispatched when a property validation or internal error occurs.
    			var {errorMessage, errorType} = e.detail.payload;
    			console.log(errorMessage, errorType);
    		},
    		'SN_EMBEDX_OBJECT_LIST#RECORD_SELECTED' : (e) => {
    			// This event is dispatched when a record is selected.
    			var {table, record_sys_id} = e.detail.payload;
    
    			var RecordViewURL;
    			if(table == 'sn_customerservice_case'){
    				RecordViewURL = '/caseview?emb_table=' + table + '&emb_recordid=' + record_sys_id;
    			} else {
    				RecordViewURL = '/recordview?emb_table=' + table + '&emb_recordid=' + record_sys_id;
    			}
    			open(RecordViewURL, '_self');
    		},
    		'SN_EMBEDX_OBJECT_LIST#COMPONENT_READY' : (e) => {
    			// This event is dispatched when a component is ready and usable.
    		}
    	};
    
    	setEvents(snEmbedxObjectList, eventHandlers);
    </script>
    
    ```


## Result

The global and component codes are ready to be shared with the third-party administrator to embed the Object list component instance on their third-party website.

## What to do next

[Embed the Object list component on the third-party website](we-embed-object-list-comp-on-thirdparty-web.md)

**Related topics**  


[Component properties for the Object list](../reference/we-object-list-comp-prop.md)

[Event handlers in the Object list component](../reference/we-event-handlers-object-list.md)

[Sample code for the Object list component](../reference/we-object-list-sample-code.md)

