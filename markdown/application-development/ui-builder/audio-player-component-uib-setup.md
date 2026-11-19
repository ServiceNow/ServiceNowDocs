---
title: Audio Player component setup
description: The Audio Player component to embed sound content into a web page document.Configure the audio file location and player behavior such as looping with these properties.Enable the user to mute, autoplay, or loop audio on the Audio Player component.Select event handlers to configure the actions \(events\) provided with the Audio Player component.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/audio-player-component-uib-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 5
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Audio Player component setup

The Audio Player component to embed sound content into a web page document.

## Before you begin

This task assumes you have placed the component on the page and are ready to configure the properties and events. For instructions on accessing and using features in UI Builder, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

**Note:** This document describes the latest component functionality. Go to the store to make sure you have the latest version of the component.

Role required: admin or ui\_builder\_admin

## Procedure

1.  Define a label for your Audio Player that differentiates it from other components in the content tree.

    A label makes finding the component easier in a large list of components. For instructions on using the content tree, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md).

    \[Omitted image "audio-player-content-tree.png"\] Alt text: Audio Player in content tree.

2.  Select the Audio Player component, using one of these methods:

    -   Click anywhere within the component.
    -   Select the Audio Player label you created for your component in the content tree.
    The property fields appear in the **Config** tab in the setup panel on the right.


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## Audio Player component properties

Configure the audio file location and player behavior such as looping with these properties.

To configure the properties, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Creates dynamic property values from multiple sources. Sources include state variables \(@state\), URL variables \(@context\), or data resource payloads \(@data\). For details, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-data-resources.md).
-   **Scripting**: Creates a scripted property value. For details on scripted values, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).

<table id="table_hqk_1hf_yrb"><thead><tr><th>

Field

</th><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Audio file URLs

</td><td>

sources

</td><td>

A JSON array of URLs for audio content. The browser chooses the first source that it supports. The URLs can be a full URL, a file on the instance, or embedded data.Examples:

-   Full URL: `["https://file-examples-com.github.io/uploads/2017/11/file_example_MP3_700KB.mp3"]`
-   From instance: `[\"connect_alert.mp3\"]`
-   Embedded data: `["data:audio/mp3;base64,//....<data hash>...]`

</td></tr><tr><td>

Muted

</td><td>

muted

</td><td>

When true, audio is silent. To give the user the choice of muting the audio, set the value in a client state parameter. See "Set up UI controls for mute, autoplay, and loop."Default: false

</td></tr><tr><td>

Autoplay

</td><td>

autoplay

</td><td>

When true, plays the audio content automatically when it loads. To give the user the choice of autoplaying the audio, set the value in a client state parameter. See "Set up UI controls for mute, autoplay, and loop."**Note:** The audio player does not begin to autoplay until a user interacts with it.

 Default: false

</td></tr><tr><td>

Loop

</td><td>

loop

</td><td>

When true, the audio content automatically repeats when it reaches the end. To give the user the choice of looping the audio, set the value in a client state parameter. See "Set up UI controls for mute, autoplay, and loop."Default: false

</td></tr></tbody>
</table>## Set up UI controls for mute, autoplay, and loop

Enable the user to mute, autoplay, or loop audio on the Audio Player component.

### Before you begin

You configure a Checklist component as part of this procedure. Consider opening the reference for that component in another browser tab.

Role required: ui\_builder\_admin

### Procedure

1.  In the UI Builder, open the page that contains the Audio Player component.

2.  On that page, set the Muted, Autoplay, and Loop client state parameters.

    \[Omitted image "audio-player-client-state-parms.png"\] Alt text: The Muted, Autoplay, and Loop client state parameters.

3.  Bind the client state parameters to the Mute, Autoplay, and Loop properties of the Audio Player component.

    \[Omitted image "audio-player-data-bindings.png"\] Alt text: Data bindings for the Muted, Autoplay, and Loop properties.

    For more information, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).

4.  Add a Checklist component to the page.

5.  In the **check box items** property of the Checklist, add an item for each of the Audio Player properties.

    The following JSON defines a check box for the Mute and Loop properties, but not Autoplay.

    ```
    [{"order":0,"checked":false,"itemId":"Muted","label":"Muted","link":{"text":"","url":""}},
    {"order":2,"checked":false,"itemId":"Loop","label":"Loop","link":{"text":"","url":""}}]
    ```

6.  Write a client script to serve as the event handler.

    ```
    /**
    * @param {params} params
    * @param {api} params.api
    * @param {any} params.event
    * @param {any} params.imports
    * @param {ApiHelpers} params.helpers
    */
    function handler({api, event, helpers, imports}) {
        const {checked, itemId} = event.payload;
        api.setState(itemId, checked);  
    }
    ```

    For more information, see [Define and bind client scripts to components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/define-client-scripts.md).

7.  Select the client script as the NOW\_CHECKLIST\#ITEM\_CLICKED event handler.

    \[Omitted image "audio-player-checklist-event-handler.png"\] Alt text: The ITEM\_CLICKED event on a Checklist component showing a client script selected.


### Audio Player in runtime

The following Next Experience runtime page shows an Audio Player component. The component opens a file at a full URL. There is a Checklist component under the Audio Player. A user can use the Checklist component to mute or loop the audio.

\[Omitted image "audio-player-with-buttons.png"\] Alt text: Audio Player in runtime.

**Note:** The Audio Player does not begin to autoplay until a user interacts with it.

## Audio Player component events

Select event handlers to configure the actions \(events\) provided with the Audio Player component.

The Events tab shows the events used by the Loader component. To view the available events, select **+ Add event mapping**. Select the event in the list to add one or more event handlers.

### Event handlers

Event handlers work with data resources to link the Audio Player actions to the data you want to display to your users. Select the event in the list to add one or more event handlers.

For instructions on adding event handlers to an event, see [Configure an event handler](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/event-handler.md).

The Audio Player events are only meant to notify that an event has happened. They do not have payloads.

### Event descriptions

|Event|Description|
|-----|-----------|
|Audio has started|Dispatched when playback or streaming has started because of autoplay. Toggles off the pause.|
|Audio has paused|Dispatched when playback or streaming has paused.|
|Audio has ended|Dispatched when playback or streaming has ended.|

