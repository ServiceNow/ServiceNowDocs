---
title: Configure link analysis for entity records in Investigative Case Management
description: As an admin, you can set up link analysis used to visualize the relationship between multiple components of a case.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/government-industry/psds-config-icm-entity-link-anaylsis.html
release: brazil
topic_type: task
last_updated: "2026-03-10"
reading_time_minutes: 3
breadcrumb: [Entity Management, Investigative Case Management, Playbooks and Solutions, Configure agent workspaces, Configure, Public Sector Digital Services \(PSDS\)]
---

# Configure link analysis for entity records in Investigative Case Management

As an admin, you can set up link analysis used to visualize the relationship between multiple components of a case.

## About this task

Link Analysis is a shared, prebuilt graph visualization component that lives in the `sn-configurable-comps` plugin, that renders an interactive node/edge graph, per-node info cards, node taglines, status chips, and search — for any ServiceNow table. Use this plugin in Investigative Case Management to visualize the relationships between multiple entities, evidence, tasks, and related cases as an interactive knowledge graph, surfacing hidden connections and blind spots.

An interactive knowledge graph renders all entities, evidence, tasks, and related cases; blue dotted lines show direct case relationships and gray solid lines show entity-to-entity links. Any node can be set as the home node to instantly re-map the network, and the view exports to PDF or PowerPoint for case reviews and handoffs.

## Before you begin

Before you begin, verify that

-   The `com.sn-configurable-comps` \(scope `sn_config_comps`\) plugin is installed on your instance.
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

7.  
## Result

The link analysis is now set up, and the relationship between each entity can be viewed with a graph.

