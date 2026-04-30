---
title: Query a GraphQL schema from a component
description: Access record data in a component by querying your scripted GraphQL schema.
locale: en-US
release: zurich
product: Web Services
classification: web-services
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Querying data using GraphQL, Additional integration resources, Web services, API implementation, API implementation and reference]
---

# Query a GraphQL schema from a component

Access record data in a component by querying your scripted GraphQL schema.

## Before you begin

Role required: admin

1.  [Create a GraphQL schema](build-graphql-scripted-schema.md#).
2.  [Test GraphQL APIs with GraphQL Explorer](test-gql-schema.md).
3.  [Disable introspective queries in your production environment](../reference/graphql-properties.md).
4.  [Create a custom component](https://www.servicenow.com/docs/access?context=custom-components&version=zurich&pubname=zurich-application-development&ft:locale=en-US).

## Procedure

1.  Navigate to your component directory.

2.  Define the query in your component's `index.js` file.

    -   **Remove introspective queries**

        Do not use introspective queries for components deployed in a production environment.

    -   **Include applicable namespaces**

        Include both the application and schema namespaces in the query.

    -   **Defer slow-responding fields**

        You can apply the `@defer` query directive to a fragment to delay the processing of one or more slow-responding fields. Deferring slow-responding fields allows the query to return other fields first.

        **Warning:** Avoid applying this query directive indiscriminately as it can also cause performance degradations. Conduct performance testing to determine which fields can be deferred for better performance.

    **Note:**

    ```
    const incidentQuery = `query ($sys_id: String!) {
        query (sys_id: $sys_id) {
            incident {
                _results {
                    sys_id {
                        displayValue
                    }
                }
            }
        }
    }`;
    ```

3.  Add the following line to the top of the script to import the createGraphQLEffect API into your component.

    ```
    import {createGraphQLEffect} from '@servicenow/ui-effect-graphql';
    ```

4.  Call the query using the `createGraphQLEffect` API. To learn more about this API, see the [Developer Site](https://developer.servicenow.com/dev.do#!/guide/sandiego/now-experience/ui-framework/api-reference/effect-graphql).

5.  Create action handlers to manage the result of the query.

    ```
    actionHandlers: {
       [DATA_FETCH_REQUESTED]: dataFetchHandler,
       [DATA_FETCH_STARTED]: ({updateState}) => updateState({loading: true}),
       [DATA_FETCH_SUCCEEDED]: ({action, updateState}) => updateState({data: action.payload}),
       [DATA_FETCH_FAILED]: () => { /* handle network error */ },
     }
    ```


## Example

This example shows a complete component including the query, the GraphQL API call, and action handlers to manage the response.

```
import {createCustomElement} from '@servicenow/ui-core';
import snabbdom from '@servicenow/ui-renderer-snabbdom';
import {createGraphQLEffect} from '@servicenow/ui-effect-graphql';

const GQL_QUERY = `
query query ($active: Boolean) {
    now {
        mySchema (active: $active) {
            myField {
                value
            }
         }
    }
}`;
  
const DATA_FETCH_REQUESTED = 'DATA_FETCH_REQUESTED';
const DATA_FETCH_STARTED = 'DATA_FETCH_STARTED';
const DATA_FETCH_SUCCEEDED = 'DATA_FETCH_SUCCEEDED';
const DATA_FETCH_FAILED = 'DATA_FETCH_FAILED';
  
const dataFetchHandler = createGraphQLEffect(GQL_QUERY, {
  variableList: ['active'],
  startActionType: DATA_FETCH_STARTED,    // gql http request started
  successActionType: DATA_FETCH_SUCCEEDED // gql request succeeded with result
  errorActionType: DATA_FETCH_FAILED      // gql http network request error (actual schema / server errors will succeed with error objects
});

const component = createCustomElement('now-component', {
  renderer: {type: snabbdom},
  view(state) {
    if(state.loading)
      return <div>Loading...</div>;

    if(!state.data)
      return <div>No Data</div>;

    return <div>My value: {state.data.data.now.mySchema.myField.value}</div>;
  },
  actionHandlers: {
   [DATA_FETCH_REQUESTED]: dataFetchHandler,
   [DATA_FETCH_STARTED]: ({updateState}) => updateState({loading: true}),
   [DATA_FETCH_SUCCEEDED]: ({action, updateState}) => updateState({data: action.payload}),
   [DATA_FETCH_FAILED]: () => { /* handle network error */ },
  }
});
```

**Parent Topic:**[Query record data using the GraphQL API framework](../concept/scripted-graph-ql.md)

