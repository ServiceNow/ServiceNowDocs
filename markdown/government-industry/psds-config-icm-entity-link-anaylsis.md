---
title: Configure link analysis for entity records in Investigative Case Management
description: As an admin, you can set up link analysis used to visualize the relationship between multiple components of a case.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/government-industry/psds-config-icm-entity-link-anaylsis.html
release: brazil
topic_type: task
last_updated: "2026-03-10"
reading_time_minutes: 8
breadcrumb: [Entity Management, Investigative Case Management, Playbooks and Solutions, Configure agent workspaces, Configure, Public Sector Digital Services \(PSDS\)]
---

# Configure link analysis for entity records in Investigative Case Management

As an admin, you can set up link analysis used to visualize the relationship between multiple components of a case.

## About this task

Link Analysis is a shared, prebuilt graph visualization component that lives in the `sn-configurable-comps` plugin, that renders an interactive node/edge graph, per-node info cards, node taglines, status chips, and search — for any ServiceNow table. Use this plugin in Investigative Case Management to visualize the relationships between multiple entities, evidence, tasks, and related cases as an interactive knowledge graph, surfacing hidden connections and blind spots.

An interactive knowledge graph renders all entities, evidence, tasks, and related cases; blue dotted lines show direct case relationships and gray solid lines show entity-to-entity links. Any node can be set as the home node to instantly re-map the network, and the view exports to PDF or PowerPoint for case reviews and handoffs.

It provides the node and edge graph, info cards, status chips, search, and context menus. You supply only a config provider script include that describes your data model, a registration record, and a page placement.

## Before you begin

Before you begin, verify that

-   The Configurable Components `com.sn-configurable-comps` \(scope `sn_config_comps`\) plugin is installed on your instance.
-   You have a "home" table, the record that users will view when they open the graph \(e.g., the case table\)
-   You have entity tables configured, and have linked the tables that connect them

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Task Relationships** &gt; **Relationship Types** to define your graph ID.

    Pick a unique string that identifies your graph. This does not need to be a real sys\_id.

    For example, if you choose `myapp-case-graph` as your graph id, ICM will use the sys\_id of its sys\_meta\_graph record.

    **Note:** This string is the `graphSysId` that scopes your entire configuration. Two teams using the same `graphSysId` will automatically merge their configurations into one graph.

2.  Create a Script Include in your app scope that extends `sn_config_comps.NodeMapConfigProvider`.

    ```
    var MyAppNodeMapConfigProvider = Class.create();
    MyAppNodeMapConfigProvider.prototype = Object.extendsObject(
        sn_config_comps.NodeMapConfigProvider,
        {
            MY_GRAPH_ID: 'myapp-case-graph',
    
            getConfig: function(graphSysId) {
                // CRITICAL: Guard on graphSysId
                if (graphSysId !== this.MY_GRAPH_ID) {
                    return { nodeTypes: {}, relationships: [], directRelationships: [] };
                }
    
                return {
                    nodeTypes: { /* ... */ },
                    relationships: [ /* ... */ ],
                    directRelationships: [ /* ... */ ],
                    iconMap: { /* ... */ },
                    defaultIcon: 'gear-fill',
                    captionConfig: { /* ... */ },
                    statusColorMap: { /* ... */ },
                    statusConfig: { /* ... */ },
                    edgeLabelConfig: { /* ... */ },
                };
            },
    
            type: 'MyAppNodeMapConfigProvider'
        }
    );
    
    ```

    **Note:** The `graphSysId` guard \(the "if" at the top\) must be included. Without it, your nodes will inject into every graph on the instance.

3.  Define node types with one entry per logical node type.

    Each entry describes one kind of node on your graph.

    ```
    nodeTypes: {
        myapp_case: {
            tables: ['myapp_case'],
            baseTable: 'myapp_case',
            primaryLabelField: 'short_description',
            secondaryLabelField: 'state',
            secondaryLabelFallbackText: 'Case',
            iconMap: { myapp_case: 'folder-outline' },
            colorMap: { myapp_case: 'blue' },
            cardHeadings: { myapp_case: 'short_description' },
            fieldConfig: {
                assigned_to: { label: 'Assigned to', valueType: 'text-link' },
                priority: { label: 'Priority' },
            },
        },
        myapp_person: {
            tables: ['myapp_person'],
            baseTable: 'myapp_person',
            primaryLabelField: 'name',
            secondaryLabelFallbackText: 'Person',
            iconMap: { myapp_person: 'user-outline' },
            colorMap: { myapp_person: 'green' },
            cardHeadings: { myapp_person: 'name' },
            fieldConfig: {
                email: { label: 'Email', valueType: 'text-link' },
                phone: { label: 'Phone' },
            },
        },
    },
    
    ```

4.  Define the relationships between entities via a many-to-many via join table.

    ```
    relationships: [
        {
            table: 'myapp_case_person_link',    // the join/link table
            label: 'Related to',
            a: { col: 'case', type: 'myapp_case' },       // column referencing source
            b: { col: 'person', type: 'myapp_person' },    // column referencing target
        },
    ],
    
    ```

    **Note:** If your link table is shared across multiple parent records \(for example, if every case uses the same link table\), add the following **scopeField** and **scopeType** values to prevent cross-record edge leaks:

    -   rel.scopeField = `case`
    -   rel.scopeType = `myapp_case`
5.  Define the directRelationships via an FK.

    ```
    directRelationships: [
        {
            fromType: 'myapp_task',
            toType: 'myapp_case',
            fkField: 'parent_case',    // FK column on myapp_task pointing at myapp_case
            label: 'Belongs to',
        },
    ],
    
    ```

6.  Define the top-level visual configuration.

    ```
    // Node bubble icons (filled variants)
    iconMap: {
        myapp_case: 'folder-fill',
        myapp_person: 'user-fill',
        myapp_task: 'clipboard-check-fill',
    },
    defaultIcon: 'gear-fill',
    
    // Card captions
    captionConfig: {
        myapp_case: { field: 'number' },
        myapp_person: { field: 'role', fallbackText: 'Person' },
    },
    
    // Status chips
    statusConfig: {
        myapp_person: { field: 'status' },
    },
    statusColorMap: {
        myapp_person: {
            1: { name: 'Active', color: 'positive', icon: 'activity-fill' },
            2: { name: 'Inactive', color: 'low', icon: 'ban-outline' },
        },
    },
    
    // Edge labels
    edgeLabelConfig: {
        default: { field: 'relationship_type' },
    },
    
    ```

7.  Embed the Component in UI Builder.

    1.  Navigate to **UI Builder** and navigate to your workspace record page.

    2.  Open a new tab.

    3.  Ensure the scope is set to **sn\_config\_comps**, and search the component palette for Link Analysis default.

    4.  Place the compenent onto the page you wish for the link analysis component to appear.

    5.  Add the following properties to the page context.

<table id="table_mdc_tfm_1lc"><thead><tr><th>

Property

</th><th>

Bind To

</th><th>

Description

</th></tr></thead><tbody><tr><td>

table

</td><td>

Page param: table name

</td><td>

The home record's table \(e.g., "myapp\_case"\)

</td></tr><tr><td>

sysID

</td><td>

Page param: record sys\_id

</td><td>

The home record's sys\_id

</td></tr><tr><td>

graphSysId

</td><td>

Static string: your MY\_GRAPH\_ID value

</td><td>

Must match the constant in your Config Provider

</td></tr><tr><td>

maxLevels

</td><td>

Static number: 2

</td><td>

How many relationship hops \(1, 2, or 3\)

</td></tr></tbody>
</table>8.  Choose a unique graph ID string, for example `myapp-case-graph`.

    This value is the `graphSysId` that scopes your configuration. It does not need to be a real sys\_id. Two teams that use the same value merge their configurations into one graph.

9.  In your application scope, create a script include that extends `sn_config_comps.NodeMapConfigProvider`.

    Use the following skeleton.

    ```
    var MyAppNodeMapConfigProvider = Class.create();
    MyAppNodeMapConfigProvider.prototype = Object.extendsObject(
        sn_config_comps.NodeMapConfigProvider,
        {
            MY_GRAPH_ID: 'myapp-case-graph',
    
            getConfig: function(graphSysId) {
                if (graphSysId !== this.MY_GRAPH_ID) {
                    return { nodeTypes: {}, relationships: [], directRelationships: [] };
                }
                return {
                    nodeTypes: { /* ... */ },
                    relationships: [ /* ... */ ],
                    directRelationships: [ /* ... */ ],
                    iconMap: { /* ... */ },
                    defaultIcon: 'gear-fill',
                    captionConfig: { /* ... */ },
                    statusColorMap: { /* ... */ },
                    statusConfig: { /* ... */ },
                    edgeLabelConfig: { /* ... */ }
                };
            },
    
            type: 'MyAppNodeMapConfigProvider'
        }
    );
    ```

10. Confirm that `getConfig()` returns an empty configuration when `graphSysId` does not match your graph ID.

    The engine calls `getConfig()` on every registered provider and merges the results. Without this guard, your nodes appear on every other graph on the instance.

11. In the `nodeTypes` object, add one entry for each kind of node on your graph.

    For each node type, set at least **tables**, **baseTable**, **primaryLabelField**, **iconMap**, **colorMap**, and **cardHeadings**. Use **fieldConfig** to choose the fields shown on the info card.

    ```
    nodeTypes: {
        myapp_case: {
            tables: ['myapp_case'],
            baseTable: 'myapp_case',
            primaryLabelField: 'short_description',
            secondaryLabelField: 'state',
            secondaryLabelFallbackText: 'Case',
            iconMap: { myapp_case: 'folder-outline' },
            colorMap: { myapp_case: 'blue' },
            cardHeadings: { myapp_case: 'short_description' },
            fieldConfig: {
                assigned_to: { label: 'Assigned to', valueType: 'text-link' },
                priority: { label: 'Priority' }
            }
        }
    }
    ```

12. Define how your node types connect.

    1.  For many-to-many connections through a join table, add an entry to `relationships`.

        ```
        relationships: [
            {
                table: 'myapp_case_person_link',
                label: 'Related to',
                a: { col: 'case', type: 'myapp_case' },
                b: { col: 'person', type: 'myapp_person' }
            }
        ]
        ```

        If the link table is shared across multiple parent records, also set **scopeField** and **scopeType** on the relationship. Otherwise, edges from one record appear on another record's graph.

    2.  For plain foreign-key connections, add an entry to `directRelationships`.

        ```
        directRelationships: [
            {
                fromType: 'myapp_task',
                toType: 'myapp_case',
                fkField: 'parent_case',
                label: 'Belongs to'
            }
        ]
        ```

13. Define the top-level visual settings: **iconMap** \(filled icon for each node\), **defaultIcon**, **captionConfig**, **statusConfig**, **statusColorMap**, and **edgeLabelConfig**.

    The **iconMap** inside a node type \(card tagline\), the top-level **iconMap** \(node bubble\), and **avatarIcon** \(card avatar\) are three separate settings. Keys in **statusColorMap** must be the raw choice values from **sys\_choice**, not the display text. An incorrect key produces an unstyled gray chip with no error.

14. Register the script include as an extension instance by creating a record in the **sys\_extension\_instance** table with the following values.

    |Field|Value|
    |-----|-----|
    |Active|true|
    |Order|100|
    |Point|`sn_config_comps.NodeMapConfigProvider`|
    |Script Include|Your `MyAppNodeMapConfigProvider` script include|

    If you use the Now SDK, define the same record in Fluent:

    ```
    Record({
        table: 'sys_extension_instance',
        data: {
            active: 'true',
            order: '100',
            point: 'sn_config_comps.NodeMapConfigProvider',
            script_include: '<sys_id of your script include>'
        }
    })
    ```

15. In UI Builder, open your workspace record page and add a new tab or open an existing tab.

16. In the component palette, search for **Link Analysis default** \(scope `sn_config_comps`\) and drag it onto the page.

17. Bind the component properties.

    |Property|Bind to|Description|
    |--------|-------|-----------|
    |table|Page parameter: table name|The table of the home record, for example `myapp_case`.|
    |sysId|Page parameter: record sys\_id|The sys\_id of the home record.|
    |graphSysId|Static string: your graph ID|Must match `MY_GRAPH_ID` in your config provider.|
    |maxLevels|Static number: `2`|The number of relationship hops to display: 1, 2, or 3.|

18. Open a record that has linked entities and go to the tab that contains Link Analysis.

    The home node appears at the center of the graph, and at least one related node and edge appear.

19. Select a node.

    The info card opens and shows the fields you configured.

20. Right-click a node.

    The context menu appears.

21. Open a graph page that belongs to a different team.

    Verify that your nodes do not appear. If they do, check the **graphSysId** guard in your config provider.


## Result

The link analysis is now set up, and the relationship between each entity can be viewed with a graph.

## What to do next

To change the graph, edit the script include on your dev instance and refresh the record page. Changes take effect immediately. Do not modify `LinkAnalysisUtilImpl`; file bugs against the sn-configurable-comps component instead.

