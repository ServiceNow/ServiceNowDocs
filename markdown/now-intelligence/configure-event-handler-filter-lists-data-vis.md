---
title: Configure an event handler for a Filter component
description: On a technical dashboard, configure a special client script-based event handler for a Filter component so it can be followed by any Lists or Data Visualizations. It is not necessary to configure an event handler for filters on inline dashboards.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Technical dashboards, Dashboards, Platform Analytics experience, Platform Analytics]
---

# Configure an event handler for a Filter component

On a technical dashboard, configure a special client script-based event handler for a Filter component so it can be followed by any Lists or Data Visualizations. It is not necessary to configure an event handler for filters on inline dashboards.

## Before you begin

This procedure assumes that the following tasks are complete:

1.  You have added the Filter component to the UI Builder page, as well as at least one Data Visualization or List component. The Filter can apply to multiple Data Visualizations or Lists.
2.  You have configured the filter to source and the data to filter, if applicable, for the Filter component. If the Filter component is supposed to filter a List, you have specified the table that the List component shows as data to filter.
3.  You have configured data sources for any Data Visualization components.
4.  You have specified a table for any List components.

Role required: ui\_builder\_admin, admin

## Procedure

1.  Open the relevant UI Builder page.

    This page may be a technical dashboard.

2.  Navigate to the UI Builder State section and add a state variable named *parFilters* of type JSON with a simple array initial value `[]`.

    For more information, see [Create and bind a client state parameter to a component](https://www.servicenow.com/docs/access?context=state-parameters&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US).

    ![Adding the parFilters client state parameter to a UIB page.](../../par-for-workspace/image/add-parFilters.png)

3.  Add a second state variable named *encodedQueries* of type JSON with initial value `{}`.

4.  Navigate to the Client Scripts section and create a custom script with a name such as "Apply PAR Filters" and the following content or a functional equivalent thereof:

    ```javascript
    function handler({ api, event, helpers, imports }) {
    	const mergePARFiltersV2 = imports["global.mergePARFilters"]().v2;
    	const { appliedFilters } = event.payload;
    	api.setState("parFilters", ({ currentValue, api }) => {
    		const { parFilters, encodedQueries } = mergePARFiltersV2(
    			currentValue,
    			appliedFilters
    		);
    		api.setState("encodedQueries", encodedQueries);
    		return parFilters;
    	});
    }
    ```

5.  In the Client Scripts section, open the **Client Script Includes** tab.

    ![The Client Script Includes tab of the Client Scripts pane on a UIB page.](../../par-for-workspace/image/client-script-includes.png)

6.  In the **Add a script include** field, select `mergePARFilters` and click **Add**.

    ![Adding the mergePARFilters script include.](../../par-for-workspace/image/add-mergePARFilters.png)

7.  Close the window for configuring data, client state, and client scripts.

8.  In the UI Builder, select the Filter component.

9.  Select the **Events** tab in the configuration panel and add the page script you have created, which in our example is Apply PAR Filters, as an event handler.

    ![Adding the Apply PAR Filters script as the Filter applied event handler.](../../par-for-workspace/image/add-apply-par-filters.png)

10. In the UI Builder, select a List component, if one exists.

11. Select **Edit fixed filter** and set this property \[fixedQuery\] as the dynamic binding expression `@state.encodedQueries.<list-datasource>`.

    Replace &lt;list-datasource&gt; with the data source for the List component. For example, if your List shows records from the Incident \[incident\] table, enter `@state.encodedQueries.incident`.

    ![In the fixed filter field on a List config panel, binding the fixedQuery property to the encodedQueries client state parameter.](../../par-for-workspace/image/configure-fixed-filter.png)

12. Repeat the previous two steps for any other List components.

13. Save the page.


**Parent Topic:**[Technical dashboards](../../performance-analytics/concept/technical-dashboards.md)

