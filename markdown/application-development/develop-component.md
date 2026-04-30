---
title: Develop a component
description: Add your component code and test it using a local development server.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Create custom components using ServiceNow CLI, Builder library, Developing your application, Building applications]
---

# Develop a component

Add your component code and test it using a local development server.

## Before you begin

-   [Set up your environment](set-up-environment.md)
-   [Set up your project](setup-component-project.md)

## About this task

For a tutorial on developing a counter component, visit the [Developer Site](https://developer.servicenow.com/dev.do#!/guide/sandiego/now-experience/ui-framework/examples/counter).

## Procedure

1.  In your project directory, navigate to `src/<component-name>/index.js`.

    This is the primary code file for a component.

2.  Add your component code.

    This example shows a sample Hello World component.

    ```
    import {createCustomElement} from '@servicenow/ui-core';
    import snabbdom from '@servicenow/ui-renderer-snabbdom';
    import styles from './styles.scss';
    
    const view = (state, {updateState}) => {
    	return (
    		<div>Hello World!</div>
    	);
    };
    
    createCustomElement('hello-world', {
    	renderer: {type: snabbdom},
    	view,
    	styles
    });
    ```

    To develop a component for Virtual Agent, add specific properties and actions to interact with the Virtual Agent client interface. The properties required depend on the type of component you are creating. For more information, see [Develop a component for Virtual Agent](../concept/va-components.md) for more information.

3.  Add inner components.

    An inner component is a component included in another component. For example, a card component might include a separate button component. The button component becomes an inner component that you must import, install, and define in the card component project.

    1.  Install the inner component package by executing the install command using your system's command-line tool:

        ```
        npm install @servicenow/<now-inner-button> 
        ```

    2.  Add an import statement to the top of your `index.js` file:

        ```
        import '@servicenow/<now-inner-button>’;
        ```

    3.  Use the inner component in your `index.js` file:

        ```
        <now-inner-button label="Click Me" />
        ```

    4.  List the inner component in the `components.[component-name].innerComponents` array in the `now-ui.json` configuration file.

        ```
        {
          "components": {
            "now-chart-timeseries": {
              "innerComponents": [
                "now-inner-button"
              ],
        ```

4.  Run the development server command to view your component in a test browser.

    ```
    $ snc ui-component develop [--entry entry --open --port port --host host]
    ```

    Pass in values for these arguments.

<table id="table_lnx_bzt_vkb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

entry

</td><td>

Path to the test module in your component project. Default: `example/index.js`.

</td></tr><tr><td>

open

</td><td>

Opens the default browser and navigates to the test page. Default: false.

</td></tr><tr><td>

port

</td><td>

Port where the development server runs. Default: 8081.

</td></tr><tr><td>

host

</td><td>

Host address to use if you want your local development server to be accessible externally by others. Typically set to `0.0.0.0`

</td></tr></tbody>
</table>    ```
    $ snc ui-component develop --entry example/hello.js --open --port 3000
    ```


## What to do next

[Deploy a component to an instance](deploy-to-instance.md).

**Parent Topic:**[Create custom components using ServiceNow CLI](../concept/custom-components.md)

**Related topics**  


[Create custom components using ServiceNow CLI](../concept/custom-components.md)

