---
title: Deploy a component to an instance
description: Deploy your component to display in your instance as an application plugin.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Create custom components using ServiceNow CLI, Builder library, Developing your application, Building applications]
---

# Deploy a component to an instance

Deploy your component to display in your instance as an application plugin.

## Before you begin

-   [Set up your environment](set-up-environment.md)
-   [Set up your project](setup-component-project.md)
-   [Develop a component](develop-component.md)

## Procedure

1.  Deploy the component to your instance.

    1.  Open your system's command-line tool and execute this command.

        ```
        $ snc ui-component deploy [--open --force]
        ```

        Pass in values for these arguments.

<table id="table_ck1_qzt_vkb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

open

</td><td>

When true, opens the default browser and navigates to UI Builder in your instance. Default: false

</td></tr><tr><td>

force

</td><td>

Deploys component changes and overwrites any existing component records. Default: false.

</td></tr></tbody>
</table>        ```
        $ snc ui-component deploy --open
        ```


## What to do next

Navigate to your instance and add your component to a modal or a landing page in Agent Workspace, or to Virtual Agent. For Agent Workspace, see [rendering a Now component in a modal](https://www.servicenow.com/docs/access?context=declarative-actions-landing&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US) or [creating custom landing pages for workspaces](https://www.servicenow.com/docs/access?context=c_set-up-configurable-workspace&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US). For Virtual Agent, see [Virtual Agent custom controls](https://www.servicenow.com/docs/access?context=custom-controls&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US).

**Parent Topic:**[Create custom components using ServiceNow CLI](../concept/custom-components.md)

**Related topics**  


[Create custom components using ServiceNow CLI](../concept/custom-components.md)

