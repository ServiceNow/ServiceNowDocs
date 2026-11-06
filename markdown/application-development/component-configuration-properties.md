---
title: Component configuration properties
description: Properties in the now-ui.json file that define a component's scope, dependencies, actions, properties, and UI Builder and analytics settings.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/application-development/component-configuration-properties.html
release: australia
topic_type: reference
last_updated: "2026-10-26"
reading_time_minutes: 5
breadcrumb: [UI component CLI extension reference, UI component CLI extension, Building pro-code applications, Developing your application, Classic app development, Building applications]
---

# Component configuration properties

Properties in the now-ui.json file that define a component's scope, dependencies, actions, properties, and UI Builder and analytics settings.

## Top-level properties

The now-ui.json file is at the root of each Next Experience UI Framework project.

|Property|Description|
|--------|-----------|
|components|Object that contains the configuration for each component exported by the target package. Object keys correspond to the exported components.|
|scopeName|Scope name that the platform reserves for the component's application. Limited to 18 characters, and must use snake case. If you don't provide a scope name, the platform generates one.|

## Component properties

Each component is exported with the createCustomElement function from the @servicenow/ui-core module. Use this function directly, without wrapping it in helper functions. Direct use enables automatic metadata extraction.

|Property|Description|
|--------|-----------|
|components.\[component-name\]|Configuration for one component. The component name must match the name that the page uses and the name passed to the createCustomElement function.|
|components.\[component-name\].actions|Array of objects that describe every action the component emits. Action names must be unique for each component.|
|components.\[component-name\].innerComponents|Array of strings that lists the components that this component depends on to render. Listing an extra dependency has no negative effect. Omitting a needed dependency prevents the component from rendering correctly. Include transient dependencies, which the build process doesn't infer.|
|components.\[component-name\].properties|Array of objects that describe every custom property the component supports.|
|components.\[component-name\].requiredSysProps|Array of strings that lists the system properties the component requires.|
|components.\[component-name\].requiredTranslationKeys|Array of strings that lists the translation keys the component requires that aren't part of the component.|
|components.\[component-name\].slots|Array of strings that lists the slots of the component.|

## Action properties

|Property|Description|
|--------|-----------|
|name|String. Name of the Next Experience UI Framework action that the component dispatches.|
|description|String. Short description of what the action does or how it's used.|
|label|String. Human-readable name of the dispatched action.|
|payload|Array of objects that describe the payload details of the action.|

## Custom property properties

|Property|Description|
|--------|-----------|
|name|String. Name of the property, as the Next Experience UI Framework code consumes it.|
|label|String. Human-readable name of the property, shown in the UI Builder toolbox when applicable.|
|description|String. Short description of what the property does or how it's used.|
|readOnly|Boolean. Setting that prevents editing the property in the UI Builder context. Default is false.|
|required|Boolean. Setting that requires a value for the property. Default is false.|
|defaultValue|String or Boolean. Value used when no value is provided.|
|fieldType|String. Data type of the property value.|
|typeMetadata|Object. Additional configuration for types that need it, such as reference properties and choice lists.|
|selectable|Boolean. Setting that allows other components to point to this property and map it to their local properties.|

## UI Builder properties

Adding the uiBuilder object makes the component appear in the UI Builder toolbox.

|Property|Description|
|--------|-----------|
|uiBuilder.label|String. Name of the component in the UI Builder toolbox.|
|uiBuilder.icon|String. Name of the icon that appears in the toolbox for this component.|
|uiBuilder.description|String. Short description of the component's functionality.|
|uiBuilder.associatedTypes|Array. Location in the UI Builder toolbox where the component appears.|
|uiBuilder.internalComponent|Boolean. Setting that limits the component to internal use.|
|uiBuilder.category|String. Category of the component.|
|uiBuilder.scriptedConfigPolicy|String. Path to a JavaScript file that further configures the component's configuration panel in UI Builder.|
|uiBuilder.configLayout|String. Configuration for the component's configuration panel in UI Builder.|
|uiBuilder.tileIcon|String. Path to an SVG file that appears as the icon for this component in the toolbox.|
|uiBuilder.searchFacets|Array. Search tags for categorizing the component.|
|uiBuilder.externalConfigSources|Array of objects. External sources of configuration for the component.|

## Analytics properties

Adding the parMetadata object makes the component appear in Platform Analytics, including Visualization Designer, Dashboards, and Component Builder.

|Property|Description|
|--------|-----------|
|parMetadata.visibility|String. Designer where the component appears. Accepts dashboard\_designer, viz\_designer, or component\_designer.|
|parMetadata.supports\_standard\_props|Boolean. Setting that indicates the component conforms to PAR standard props. Default is false.|
|parMetadata.supports\_export|Boolean. Setting that indicates the component exports correctly and handles the printerFriendlyView property. Default is false.|
|parMetadata.use\_dashboard\_header|Boolean. Setting that makes the component use the dashboard header instead of its own. Default is false.|
|parMetadata.supports\_standard\_request|Boolean. Setting that enables dashboard data management. When set to true, the standard request properties in this table must be provided. Default is false.|
|parMetadata.standard\_request\_script\_type|String. Scripting language of the standard request. Accepts java or js.|
|parMetadata.data\_provider\_class\_name|String. Class name of the data provider. Used only when standard\_request\_script\_type is java.|
|parMetadata.standard\_request|String. JavaScript implementation of the standard request.|
|parMetadata.data\_field|String. Field that receives the data retrieved on behalf of the component.|

## now-ui.json file

```
{
  "components": {
    "snc-stock-tracker": {
      "actions": [
        {
          "name": "SEND_MESSAGE",
          "description": "Will send message in current language",
          "label": "Send message",
          "payload": [
            {
              "name": "value",
              "label": "Value",
              "description": "Description",
              "defaultValue": false
            }
          ]
        },
        {
          "name": "SEND_MESSAGE#BROAD_CAST",
          "label": "Send messages to many",
          "description": "Will send message in current language",
          "payload": [
            {
              "name": "value",
              "label": "Value",
              "description": "Description",
              "defaultValue": false
            }
          ]
        }
      ],
      "innerComponents": ["myco-bar", "myco-baz"],
      "uiBuilder": {
        "associatedTypes": ["global.core", "global.landing-page"],
        "label": "My Stock Tracker",
        "icon": "chat-fill",
        "description": "Stock Tracking component",
        "category": "stocks",
        "tileIcon": "./tile-icon/generic-tile-icon.svg",
        "searchFacets": ["global.stocks:global.tracking"]
      },
      "properties": [
        {
          "name": "backgroundColor",
          "label": "Background Color",
          "readOnly": false,
          "required": false,
          "defaultValue": "purple",
          "fieldType": "string",
          "description": "Description"
        },
        {
          "name": "table",
          "label": "table",
          "fieldType": "json",
          "required": true,
          "typeMetadata": {
            "schema": {
              "type": "array",
              "items": [
                { "name": "name" }
              ]
            }
          }
        },
        {
          "name": "from",
          "label": "from",
          "fieldType": "object",
          "required": true,
          "typeMetadata": {
            "schema": {
              "type": "object",
              "properties": {
                "country": { "type": "string" },
                "timezone": { "type": "string" },
                "id": { "nowUIType": "CustomType" }
              }
            }
          }
        },
        {
          "name": "search",
          "label": "Search type",
          "defaultValue": "list",
          "fieldType": "choice",
          "readOnly": false,
          "required": true,
          "selectable": false,
          "typeMetadata": {
            "choices": [
              { "label": "None", "value": "none" },
              { "label": "Contains", "value": "contains" }
            ],
            "schema": {
              "type": "string",
              "enum": ["none", "contains"]
            }
          }
        },
        {
          "name": "to",
          "label": "To",
          "defaultValue": "{}",
          "typeMetadata": {
            "schema": {
              "type": "object",
              "properties": {
                "start": { "anyOf": [{ "type": "string" }, { "type": "number" }] },
                "end": { "anyOf": [{ "type": "string" }, { "type": "number" }] },
                "type": { "type": "string" },
                "hasConflict": { "type": "boolean" },
                "tooltip": { "type": "string" }
              }
            }
          }
        }
      ],
      "requiredSysProps": ["abc.foo", "abc.bar"],
      "requiredTranslationKeys": ["T_FOO", "T_BAR"],
      "slots": ["slot-foo", "slot-bar"]
    },
    "snc-stock-seller": {
      "uiBuilder": {
        "associatedTypes": ["global.core", "global.landing-page"],
        "label": "My Stock Seller",
        "icon": "chat-fill",
        "description": "Stock selling component",
        "category": "stocks",
        "searchFacets": ["global.stocks:global.selling"]
      },
      "actions": [
        {
          "name": "SEND_MESSAGE",
          "description": "Will send message in current language",
          "label": "Send message",
          "payload": [
            {
              "name": "value",
              "label": "Value",
              "description": "Description",
              "defaultValue": false
            }
          ]
        }
      ],
      "properties": [
        {
          "name": "search",
          "label": "Search type",
          "defaultValue": "list",
          "fieldType": "choice",
          "readOnly": false,
          "required": true,
          "selectable": false,
          "typeMetadata": {
            "choices": [
              { "label": "None", "value": "none" },
              { "label": "Contains", "value": "contains" }
            ],
            "schema": {
              "type": "string",
              "enum": ["none", "contains"]
            }
          }
        }
      ]
    }
  },
  "scopeName": "x_snc_stock_track"
}
```

