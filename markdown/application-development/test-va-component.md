---
title: Test a component for Virtual Agent
description: Test your Virtual Agent custom component before deploying it to your instance.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Develop a component for Virtual Agent, Create custom components using ServiceNow CLI, Builder library, Developing your application, Building applications]
---

# Test a component for Virtual Agent

Test your Virtual Agent custom component before deploying it to your instance.

## Before you begin

-   Set up your environment. For instructions, see the [ServiceNow® Developer Site](https://developer.servicenow.com/dev.do#!/reference/next-experience/xanadu/cli/getting-started).
-   Set up your component project. For instructions, see the [ServiceNow® Developer Site](https://developer.servicenow.com/dev.do#!/reference/next-experience/xanadu/cli/cli)
-   Develop your component. For instructions, see the [ServiceNow® Developer Site](https://servicenow.com/docs/bundle/xanadu-application-development/page/build/components/task/develop-component.html)
-   [Add properties to communicate with Virtual Agent](add-va-properties.md)

Role required: virtual\_agent\_admin or admin

## About this task

Virtual Agent components must be tested within the Virtual Agent client chat to ensure that the component responds correctly to user input. You can set properties in your component project to test your component in a mock Virtual Agent test client tool.

## Procedure

1.  Add a dependency on the test client tool to your component project.

    1.  Open the `<component-name>/package.json` file in your component project.

    2.  Add `"@servicenow/sdk-ci": "1.0.8"` and `"@servicenow/library-translate": "^18.0.0"` to the `devDependencies` object.

    Here is an example `package.json` file with the correct dependencies.

    ```
    "dependencies": {
        "@servicenow/ui-renderer-snabbdom": "australia",
        "@servicenow/library-translate": "^18.0.0",
        "@servicenow/now-button": "australia",
        "@servicenow/now-dropdown": "australia",
        "@servicenow/sass-generic": "australia",
        "@servicenow/cli-archetype": "australia",
        "@servicenow/sdk-ci": "1.0.8"
    }
    ```

2.  Add sample properties to use as the initial state of the component in your test.

    1.  Add a `<component-name>/example/sampleProps.json` file with initial properties to render in your test.

    Here is an example `sampleProps.json` file with initial properties set for a slider component.

    ```
    {	
    	"label": "How many penguins do you want to buy?",
    	"defaultValue": 10,
    	"sliderMin": 20,
    	"sliderMax": 80,
    	"unitName": "penguins",
    	"unitIcon": "https://image.flaticon.com/icons/svg/141/141836.svg"  
    }
    ```

3.  Update the `example.js` file to open the component through the test client tool using the sample properties that you created.

    1.  Open the `<component-name>/example/element.js` file in your component project.

    2.  Add statements to import `@servicenow/sdk-ci` and the sample properties file you created.

    3.  Add the following statement, replacing `<component-name>` with your component's name to create the test tool with initial data from your sample properties.

        ```
        const el = document.createElement('tool-ci-custom-control-tester');
        el.componentTagName="<component-name>";
        el.initialExampleData=sampleProps;
        document.body.appendChild(el);
        ```

    Here is an example `example.js` file that opens the component using the test client tool.

    ```
    import '../src/now-chat-control-slider';
    
    import '@servicenow/sdk-ci';
    
    import sampleProps from './sampleProps.json';
    
    const el = document.createElement('tool-ci-custom-control-tester');
    el.componentTagName="<component-name>";
    el.initialExampleData=sampleProps;
    document.body.appendChild(el);
    ```

4.  Run the development server command to view your component in a test browser.

    ```
    $ snc ui-component develop [--entry entry --open --port port --host host]
    ```

    Pass in values for these parameters.

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

    The component opens in the test client tool. You can see the initial data provided in the **Custom Control JSON Input Data** field and the component's output in the **Custom Control Return Data** field.


## What to do next

If your component is working as expected, deploy it to your instance. For instructions, see the [ServiceNow® Developer Site](https://developer.servicenow.com/dev.do#!/reference/next-experience/xanadu/cli/development-flow).

After developing the component and deploying it to your instance, add it to Virtual Agent Designer using a custom control and definition. For more information, see [Virtual Agent custom controls](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/virtual-agent/custom-controls.md).

**Parent Topic:**[Develop a component for Virtual Agent](../concept/va-components.md)

**Related topics**  


[Create custom components using ServiceNow CLI](../concept/custom-components.md)

