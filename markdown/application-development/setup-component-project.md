---
title: Set up your project
description: Create the component project and the set of files required to develop a component. You can connect to your instance and create an application scope for your component, or you can reserve a scope to verify later.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Create custom components using ServiceNow CLI, Builder library, Developing your application, Building applications]
---

# Set up your project

Create the component project and the set of files required to develop a component. You can connect to your instance and create an application scope for your component, or you can reserve a scope to verify later.

## Before you begin

[Set up your environment](set-up-environment.md).

## Procedure

1.  Create a folder for your project and point your system's command-line tool to the folder.

2.  Create the component project and all the files required to build a component.

    1.  From the folder you created, execute this command.

        ```
        $ snc ui-component project [--name name --description description --scope scope --offline]
        ```

        Pass in values for these arguments.

<table id="table_bkt_yyt_vkb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

name

</td><td>

Required. The project name. Must be a valid and unique npm package name.

</td></tr><tr><td>

description

</td><td>

The project description to be available in the npm registry and the plugins list in your instance.

</td></tr><tr><td>

scope

</td><td>

Suggested application scope to assign to this project and its components. If provided, the instance validates the name. Use the namespace identifier guidelines for application development on the instance. For more information, see [Application scope](../../applications/concept/c_ApplicationScope.md). Maximum: 18 characters.

 Case: snake case.

 Default: `x_customerprefix_componentname`, where:

-   `customerprefix` is the value in the **glide.appcreator.company.code** system property on your instance.
-   `componentname` is the value provided in the component's `name` parameter when you created the project.
 Alternatively, you can add a value to the `scopeName` parameter in the `now-ui.json` file. For more information, see [Change a component's application scope](change-scope.md).

</td></tr><tr><td>

offline

</td><td>

When true, creates and scaffolds a component while disconnected from your instance. Skips validation of the given scope name. Default: `false`.

</td></tr></tbody>
</table>        ```
        $ snc ui-component project --name @myorg/movie-quotes --description 'A web component that prints movie quotes.'
        ```

        ```
        $ snc ui-component project --name @myorg/hello-world --scope x_myorg_helloworld --offline
        ```

3.  Run the following command to install the npm dependencies.

    ```
    npm install
    ```


## What to do next

[Develop a component](develop-component.md).

**Parent Topic:**[Create custom components using ServiceNow CLI](../concept/custom-components.md)

**Related topics**  


[Create custom components using ServiceNow CLI](../concept/custom-components.md)

