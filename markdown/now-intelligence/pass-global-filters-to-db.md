---
title: Pass global filters to the dashboard page template
description: Global filters are sent to the dashboard to serve as filters for the visualizations within the dashboard. These filters are merged with existing filters in the dashboard.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Creating Platform Analytics pages, Platform Analytics experience, Platform Analytics]
---

# Pass global filters to the dashboard page template

Global filters are sent to the dashboard to serve as filters for the visualizations within the dashboard. These filters are merged with existing filters in the dashboard.

## About this task

Global filters are filters that apply to visualizations on the target dashboard. These filters apply to all relevant data visualizations. The format of the value passed to globalFilter is the stringified form of \{encodedQueries: 'encoded-queries-string', filters: 'PAR-Filter'\}. Both encodedQueries and filters are transformed into Platform Analytics filters internally and merged with the existing filters on the dashboard.

Either `encodedQueries`, `filters`, or both can be specified. In the following example, equivalent `encodedQueries` and `filters` values both filter visualizations that show records from the Incident \[incident\] table based on a State field value of 1 or 2:

```
JSON.stringify({
    encodedQueries: {incident: 'stateIN1,2'},
    parFilters: [{ order: 0, apply_to: ['incident.state'], values: ['1', '2'] }]
})
```

Configure links to dashboards on UI Builder pages to open dashboards that are already filtered.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to the UI Builder page that you want to add a global filter to.

2.  Configure the behavior of the hyperlink or button \(or something else\) on the page to point to the dashboard with the specified sys\_ID.

    In this example, the sys\_ID is 1238.

    The showInfoMessage parameter, if true, shows the configured infoMessage on the linked dashboard when filters are passed.

    ```
    api.emit('NAV_ITEM_SELECTED', {
            route: 'dashboards',
            params: {
                sysId: '1238',
                unifiedFilters: JSON.stringify({
                    showInfoMessage: true, // default false
                    infoMessage: 'custom info message', // if not passed and if showInfoMessage is true then the default message is displayed
                    encodedQueries: {
                        incident: 'priority=1'
                    },
                })
            }
        });
    
    ```


**Parent Topic:**[Creating Platform Analytics pages in your own workspace](../../performance-analytics/concept/adding-analytics-center-to-ws.md)

**Related topics**  


[Create a Platform Analytics workspace from App Engine Studio](../../performance-analytics/concept/create-analytics-ws-aes.md)

[Add Platform Analytics pages to a configurable workspace](../../performance-analytics/task/add-analytics-center-to-experience.md#)

[Add a dashboard to a Dashboards page](../../performance-analytics/task/add-dashboard-to-workspace.md)

[Configure custom redirection from a dashboard component](../../performance-analytics/task/config-custom-redirection-from-db.md)

[Configure dashboard data broker](../../../build/component-uib-setup/task/configure-dashboard-data-broker.md)

