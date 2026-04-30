---
title: Integrating kBridge visualization
description: Integrate kBridge for real-time 3D visualization. Sync configuration inputs with visual updates to enhance user experience.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2025-09-16"
reading_time_minutes: 3
breadcrumb: [Integrating ServiceNow CPQ with visualization tools, ServiceNow CPQ with other apps, Integrate, Sales Customer Relationship Management]
---

# Integrating kBridge visualization

Integrate kBridge for real-time 3D visualization. Sync configuration inputs with visual updates to enhance user experience.

ServiceNow CPQ supports several different 3D visualization options in the end-user configuration experience. ServiceNow CPQ can be implemented to use kBridge as a visualization component that is updated in real time in the ServiceNow CPQ UI as the user changes configuration inputs \(one-way communication\). In addition, bidirectional \(two-way\) communication may be defined so that user manipulations of the graphic update ServiceNow CPQ configuration fields.

The following video shows how to integrate ServiceNow CPQ with kBridge for real-time updates:

[KBridge Integration Setup Demo](https://www.youtube.com/watch?v=X4sxdRtz_v4)

The integration between ServiceNow CPQ and kBridge is set up in the ServiceNow CPQ blueprint layout definition. The layout definition:

-   defines where the kBridge visualization component will be rendered on the ServiceNow CPQ UI
-   specifies the kBridge connection
-   identifies the ServiceNow CPQ field or set data to be sent

To create a kBridge component, the `kbridge` layout component type can be added in the “type” column of the layout CSV file. Additional properties for the integration are set in the “value” column.

This sample layout CSV file demonstrates the use of the kBridge component and parameter inputs. See row 12.

[kBridge\_setsv2-layoutCSV](https://docs.google.com/spreadsheets/d/1AqYC6enIGexuzgEC8e89GsVtd6lnRhUje0BiTkt2Uzs/edit?usp=sharing)

## JSON value template

```
scriptUrl: string,
appUrl: string,
token: string,
sessionStartup: object
eventFields: object
eventSets: object
eventProductPickers: object
setActiveTriggers: array
listenerFields: object
height: number
width: number
```

## kBridge connection

-   scriptUrl: URL for kBridge script
-   appUrl: URL for kBridge app
-   token: Auth token from kBridge
-   sessionStartup: Additional kBridge startup information; work with kBridge, your implementer or kBridge administrator to determine the appropriate values to pass in this parameter for your kBridge setup

## ServiceNow CPQ data

-   eventFields: Mapping of ServiceNow CPQ fields to kBridge
-   eventSets: Mapping of ServiceNow CPQ sets to kBridge
-   eventProductPickers: Mapping of ServiceNow CPQ product pickers to kBridge
-   setActiveTriggers: ServiceNow CPQ set triggers
-   listenerFields: For 2-way data communication involving one or more ServiceNow CPQ sets, this object specifies the ServiceNow CPQ text field variable name to which a JSON representation of the set\(s\), manipulated in the kBridge visualization by the user, will be returned to ServiceNow CPQ. The Admin must define a rule that parses the content of the listenerFields and populates the appropriate set inputs.

    **Note:**

    -   If a blueprint/layout only has eventFields but not listenerFields, every eventField has 2-way communication.
    -   If a listenerField is added to the blueprint/layout, all eventFields will only communicate from ServiceNow CPQ to kBridge.
    -   eventSets and eventProductPickers only pass information from ServiceNow CPQ to kBridge, not the other way around.
    -   From a data standpoint, eventSets and eventProductPickers data are passed the same way to kBridge \(in an array of objects\).

## Layout size

-   height: element height in layout, value is in pixels
-   width: element width in layout, value is in pixels

## Example JSON values

```
{
  scriptUrl: 'http://script.location';,
  appUrl: 'http://app.script.location';,
  token: 'abc-123-def-456',
  sessionStartup: {
    type: 'model',
    revisionId: '1234-5678-90'
  },
  eventFields: {
    field1: { name: 'field-1', refChain: 'world.application.model' },
    field2: { name: 'field-2', refChain: 'world.application.model' },
    field3: { name: 'field-3', refChain: 'world.application.model' }
  },
  eventSets: {
    set1: { name: 'set-1', refChain: 'world.application.model' },
  },
  eventProductPickers: {
    picker1: { name: 'picker-1', refChain: 'world.application.model' },
  },
  setActiveTriggers: ['set.set2.triggerBoolean'],
  listenerFields: { 
    listenerFieldName: { name: 'logikTestSet', refChain: 'world.application.model' }
  },
  height: 800,
  width: 1200,
}
```

-   name: corresponds to the field or rule name in kBridge.
-   refChain: corresponds to the model path of this object in kBridge.

## Content security policy settings

The ServiceNow CPQ application will need to be configured to accept the traffic from the kBridge application. Please log a case with ServiceNow CPQ support, describe your intent to integrate kBridge with the ServiceNow CPQ UI, and request that your ServiceNow CPQ server CSP settings be configured to accommodate traffic to and from the kBridge environment.

## Reference

For a discussion of features available among supported visualization applications in integration with ServiceNow CPQ, see [Visualization Integrations: An Overview](https://logikio.atlassian.net/wiki/spaces/CS/pages/1615462425/Visualization+Integrations+An+Overview).

