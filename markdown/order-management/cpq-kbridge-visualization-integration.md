---
title: Integrating kBridge visualization
description: Integrate kBridge for real-time 3D visualization. Sync configuration inputs with visual updates to enhance user experience.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Integrating CPQ with visualization tools, CPQ with other apps, Integrate, Sales Customer Relationship Management]
---

# Integrating kBridge visualization

Integrate kBridge for real-time 3D visualization. Sync configuration inputs with visual updates to enhance user experience.

CPQ supports several different 3D visualization options in the end-user configuration experience. CPQ can be implemented to use kBridge as a visualization component that is updated in real time in the CPQ UI as the user changes configuration inputs \(one-way communication\). In addition, bidirectional \(two-way\) communication may be defined so that user manipulations of the graphic update CPQ configuration fields.

The following video shows how to integrate CPQ with kBridge for real-time updates:

[KBridge Integration Setup Demo](https://www.youtube.com/watch?v=X4sxdRtz_v4)

The integration between CPQ and kBridge is set up in the CPQ blueprint layout definition. The layout definition:

-   defines where the kBridge visualization component will be rendered on the CPQ UI
-   specifies the kBridge connection
-   identifies the CPQ field or set data to be sent

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

## CPQ data

-   `eventFields`: Mapping of CPQ fields to kBridge
-   `eventSets`: Mapping of CPQ sets to kBridge
-   `eventProductPickers`: Mapping of CPQ product pickers to kBridge
-   `setActiveTriggers`: CPQ set triggers
-   `listenerFields`: For two-way data communication involving one or more CPQ sets, this object specifies the CPQ text field variable name to which a JSON representation of the set\(s\), manipulated in the kBridge visualization by the user, will be returned to CPQ. The Admin must define a rule that parses the content of the listenerFields and populates the appropriate set inputs.

    **Note:**

    -   If a blueprint/layout has `eventFields` but not `listenerFields`, every event field has two-way communication.
    -   If a listener field is added to the blueprint or layout, all event fields will communicate only from CPQ to kBridge.
    -   Event sets and event product pickers pass information only from CPQ to kBridge, and not from kBridge to CPQ.
    -   From a data standpoint, event sets and event product pickers data are passed the same way to kBridge \(in an array of objects\).

## Layout size

-   `height`: element height in layout, value is in pixels
-   `width`: element width in layout, value is in pixels

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

-   `name` corresponds to the field or rule name in kBridge.
-   `refChain` corresponds to the model path of this object in kBridge.

## Reference

For a discussion of features available among supported visualization applications in integration with CPQ, see [Visualization Integrations: An Overview](https://logikio.atlassian.net/wiki/spaces/CS/pages/1615462425/Visualization+Integrations+An+Overview).

