---
title: Configure the Data visualization component instance
description: Configure the Data visualization component instance so that your users can embed it on their website to display information in the form of single score, pie chart, donut chart, or semi-donut chart directly from any ServiceNow table.
locale: en-US
release: australia
product: Customer Self-service and Omnichannel Engagement
classification: customer-self-service-and-omnichannel-engagement
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Data visualization component, Configure web components, Web Embeddables, Set up self-service, Configure, Customer Service Management]
---

# Configure the Data visualization component instance

Configure the Data visualization component instance so that your users can embed it on their website to display information in the form of single score, pie chart, donut chart, or semi-donut chart directly from any ServiceNow table.

## Before you begin

You must have the following setup to configure the Data visualization component instance:

-   Enable Web Embeddables in your instance. For more information, see [Activate Web Embeddables](act-web-embeddables.md).
-   [Set up a custom URL as the instance URL](set-up-custom-url.md).
-   Authenticate the ServiceNow components using OpenID Connect \(OIDC\) or non OIDC authentication. For more information, see [Authenticate the ServiceNow components using OIDC](authenticate-sn-webcomponents-oidc.md) and [Non OIDC authentication for ServiceNow components](../concept/auth-sn-webcomponents-non-oidc.md).

Role required: sn\_embeddable\_core.emb\_admin

## Procedure

1.  Navigate to **All** &gt; **Web Embeddables** &gt; **Homepage**.

2.  In the homepage, select Create module or use the existing module.

    For more information on creating a new module, see [Create a module](../concept/create-we-module.md).

3.  On the module page, in the Components tab, add a Data visualization component instance to an existing or a new group.

    For more information on creating a group and then adding a component instance, see [Create a group and add a component instance](we-create-group-and-add-comp-instance.md).

4.  Configure the Data visualization component instance properties.

    -   The Preview tab displays real-time data according to choices set in the component properties.
    -   For a description of the component properties related to the Data visualization component instance, see [Component properties for the Data visualization](../reference/we-data-viz-comp-prop.md).
5.  Select the **CORS rules** tab to configure the CORS rules.

    For more information about configuring CORS rules, see [Configure CORS \(Cross-Origin Resource Sharing\) rules before embedding ServiceNow components](configure-cors-for-web-components.md).

6.  Select the **Components** tab.

    If a message appears about the application scope, change the scope to **Web Components for Customer Service** to be able to edit the record.

7.  Select **Get embed code**.

    A pop-up window appears to display both Global code and Component code.

8.  In the Global code tab, review the generated code and select the **Copy global code**.

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

9.  In the Component Code tab, slide the **Enable event handler** toggle switch to handle events triggered by the user interactions on the website.

    **Note:** Enabling the event handler also modifies the component code. For more information on event handlers in Web Embeddables, see [Event handler in the Data visualization component](../reference/we-data-viz-event-handler.md).

10. In the Component code tab, review the generated code and select the **Copy component code**.

    The generated component code also includes configurations for event handlers and a donut chart.

    ```
    <!--  
        Module: Demo module
        Group: Group 1
        Instance: Data visualization 1
    -->
    <sn-embedx-visualization-donut
    	sort-by="value"
    	data-labels-type="value"
    	data-sources='[{"allowRealTime":true,"dataCategories":["trend","group","simple"],"filterQuery":"active=true^sys_updated_onONLast 7 days@javascript:gs.beginningOfLast7Days()@javascript:gs.endOfLast7Days()","id":"dGFibGVzbl9jdXN0b21lcnNlcnZpY2VfY2FzZTE3MjU0MjYxODczODc=","isDatabaseView":false,"label":"Case","preferredVisualizations":["d24d53f60350de7a652caf3188a46ed2"],"reportSourceSysId":null,"sourceType":"table","tableOrViewName":"sn_customerservice_case"}]'
    	metrics='[{"aggregateFunction":"COUNT","axisId":"primary","dataSource":"dGFibGVzbl9jdXN0b21lcnNlcnZpY2VfY2FzZTE3MjU0MjYxODczODc=","id":"ZEdGaWJHVnpibDlqZFhOMGIyMWxjbk5sY25acFkyVmZZMkZ6WlRFM01qVTBNall4T0Rjek9EYz0xNzI1NDI2MTg4NjYx","numberFormat":{"customFormat":false}}]'
    	group-by='[{"disableRanges":false,"groupBy":[{"dataSource":"dGFibGVzbl9jdXN0b21lcnNlcnZpY2VfY2FzZTE3MjU0MjYxODczODc=","groupByField":"state","isChoice":true,"isPaBucket":false,"isRange":false}],"hideZeroValues":true,"maxNumberOfGroups":"ALL","numberOfGroupsBasedOn":"NO_OF_GROUP_BASED_ON_PER_METRIC","showOthers":false}]'
    	additional-group-by-config='[{"id":"state","label":"State"},{"id":"account","label":"Account"}]'
    	truncation-type="end"
    	show-register
    	register-position="bottom"
    	register-orientation="horizontal"
    	legend-horizontal-alignment="center"
    	ranges-config='null'
    	color-config='null'
    	show-header
    	header-color='null'
    	title-color='null'
    	sort-by-order="desc"
    	empty-state-illustration="no-data"
    	empty-state-heading="No data available."
    	empty-state-heading-level="3"
    	empty-state-content="There are no scores available for the selected criteria. Contact your admin for more info."
    	empty-state-alignment="vertical-centered"
    	number-of-periods="3"
    	period="M"
    	user-info='"@context.session.user"'
    	shared-context='null'
    	colors='{}'>
    </sn-embedx-visualization-donut>
    <!--
    	The component also includes the following additional properties:
    	show-border
    	drilldown-label
    	show-data-labels
    	max-label-size
    	show-register-on-same-line
    	show-register-value
    	legend-max-item-width
    	legend-expand-to-fit
    	show-register-percentage
    	wrap-title
    	show-header-separator
    	header-title
    	description
    	refresh-request
    	show-additional-group-by-selector
    	show-metric-label
    	show-total-value
    	enable-click-and-stay
    	show-data-table
    	enable-custom-empty-state
    	apply-date-range
    	show-absolute-period
    	score-type
    	start-time
    	end-time
    	use-current-date-for-end
    	show-extended-error-messages
    	auto-aggregate-periods
    -->
    
    <script type="module">
    	import { getEmbeddables, setEvents, setProperties } from 'https://demo.servicenow.com/uxasset/externals/sn_embeddable_core/index.jsdbx';
    	
    	const snEmbedxVisualizationDonut = document.querySelector('sn-embedx-visualization-donut');
    
    	getEmbeddables(["sn-embedx-visualization-donut"]);
    
    	const eventHandlers = {
    		'NOW_VIS_WRAPPER#PROPERTY_OVERRIDE' : (e) => {
    			// Dispatched when the visualization overrides its property. For example when the user selects a different group by from the alternative group by selection
    			var {properties} = e.detail.payload;
    			console.log(properties);
    		},
    		'NOW_VIS_WRAPPER#SELECTED' : (e) => {
    			// Dispatched when the user selects/de-selects element on data visualizations, typically to filter other content on the page
    			var {title, type, isSelected, params, data} = e.detail.payload;
    			console.log(title, type, isSelected, params, data);
    		},
    		'NOW_VIS_WRAPPER#CLICKED' : (e) => {
    			// Dispatched when the visualization is clicked
    			var {title, type, params, data} = e.detail.payload;
    			console.log(title, type, params, data);
    		}
    	};
    
    	setEvents(snEmbedxVisualizationDonut, eventHandlers);
    </script>
    
    ```


## Result

The global and component codes are ready to be shared with the third-party administrator to embed the Data visualization component instance on their third-party website.

## What to do next

[Embed the Data visualization component instance on the third-party website](embed-data-viz-comp.md)

**Related topics**  


[Component properties for the Data visualization](../reference/we-data-viz-comp-prop.md)

[Event handler in the Data visualization component](../reference/we-data-viz-event-handler.md)

[Sample code for the Data visualization component](../reference/we-data-viz-sample-code.md)

