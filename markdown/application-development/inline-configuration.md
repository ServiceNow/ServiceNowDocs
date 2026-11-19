---
title: Inline configuration
description: Inline configuration turns a property a developer declares in code into something a customer admin can change on a live page, without a code change or a redeploy. An author picks one of four modes per property, and the framework stores and reads back the resulting values.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/application-development/inline-configuration.html
release: australia
topic_type: concept
last_updated: "2026-09-29"
reading_time_minutes: 5
keywords: [Inline configuration, Four configuration modes, External config with @externalConfig, Custom URL with inline-simple, Self-config with inline-auto, Custom component in the props pane, How configuration is stored, sys\_aix\_configuration, sys\_user\_preference, REST surface, Server-side resolution, Related]
breadcrumb: [Configure experiences, Lux Development, Building pro-code applications, Developing your application, Building applications]
---

# Inline configuration

Inline configuration turns a property a developer declares in code into something a customer admin can change on a live page, without a code change or a redeploy. An author picks one of four modes per property, and the framework stores and reads back the resulting values.

The mechanics of declaring a property are in [Configurable properties for Lux experiences](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/configurable-properties.md); what the admin sees is in .

## Four configuration modes

An author picks a mode per property, or per widget for self-config, in increasing order of effort. A single widget can mix modes: some properties on the standard popover, others deep-linked or self-configured.

|Order|Mode|Declared with|What the admin gets|Where data saves|
|-----|----|-------------|-------------------|----------------|
|1|Independent config|`@config` on a field|The value field in the framework props pane, plus a lock toggle|`sys_aix_configuration`|
|2|External config|`@externalConfig` on the class|Same pane, plus a link out to a list, record, or URL|The author's own table|
|3|Custom URL|`static configMode = 'inline-simple'`|Pane stays; a button opens an author-supplied URL full-screen in an iframe|Wherever the linked tool saves; not through the framework|
|4|Self-config|`static configMode = 'inline-auto'`|Nothing framework-drawn; the widget renders its own editor|`sys_aix_configuration`, through the framework's save pipeline|

Mode 1 applies to most properties. Only complex widgets \(list, form, action bar, data visualization\) need one of the others.

## External config with @externalConfig

A class-level decorator with no effect on resolution, storage, or the priority stack. It only injects a link into the config panel, so the admin has a quick path to related platform data: assignment group rules, SLA definitions, approval policies.

```
@customElement('some-tag')
@externalConfig({
  key: 'incidentData',
  list: {table: 'incident', fixedFilter: 'active=true'}
})
class SomeElement extends AIUXElement {}
```

Three variants: `list: {table, fixedFilter}`, `record: {table, sysId, view}`, or `link: {url}`.

## Custom URL with inline-simple

For complex platform configuration where full self-config is not feasible. The widget's configuration lives in an external platform tool, opened in an iframe.

```
@customElement('my-component')
export class MyComponent extends AIUXElement {
  static configMode = 'inline-simple';

  provideConfigDeepLinking() {
    return {
      label: 'Configure Incident List',
      url: `${window.location.origin}/incident_list.do`
    };
  }
}
```

Two requirements: the `configMode` static \(a plain property, not a decorator\) and an override of `provideConfigDeepLinking()`, which is a no-op on `AIUXElement` by default. Return a single `{label, url}`, an array of them for several buttons, or `null` for none. The editor renders one link-icon button per entry on the element's outline.

**Warning:** Configuration set inside the opened URL is not returned to the widget. The framework does not receive or store values from the linked tool.

## Self-config with inline-auto

For widgets when a flat property form can't express the change: drag-and-drop layouts, a widget toolbox, a canvas, or curating an ordered collection. The framework delegates edit mode only; the UI, the affordances, and the autosave behavior are the author's.

```
class SnLayoutRenderer extends AIUXElement {
  static configMode = 'inline-auto';

  // The framework calls this when config mode opens.
  openConfigEditor({fieldValues, onChange, onSave, onClose}) {
    this._inlineConfig = {onChange, onSave, onClose};
    this._editMode = true;
  }

  closeConfigEditor() {
    this._editMode = false;
  }

  _persistChange(key, value) {
    this._inlineConfig?.onChange(key, structuredClone(value));
  }
}
```

|Callback|Direction|What it does|
|--------|---------|------------|
|`fieldValues`|in|Current resolved value per `selfConfigSchema` key, admin and user layers applied|
|`onChange(key, value)`|out|Stage a pending edit. Safe to call repeatedly; pass a clone, not a live reference.|
|`onSave()`|out|Persist all staged edits and exit config mode|
|`onClose()`|out|Exit, discarding anything unsaved|

On open, the editor scans the DOM to collect every configurable entry. Self-config widgets are handed their own editor instead of the standard per-property popover everyone else gets.

Self-config does not bypass the priority stack. The framework writes values to the admin layer through the same save path the props pane uses. The widget owns the editing UI, not the storage.

## Custom component in the props pane

Not a fifth mode. A bespoke component is injected into the standard props pane, keeping the familiar surface while still saving to `sys_aix_configuration`. Source marks this as available on request only. It also instructs authors to consult the configuration product and UX owners first, so the injected UI stays consistent with the rest of the configuration surface.

## How configuration is stored

## sys\_aix\_configuration

Extends `sys_metadata`, indexed on `(page_path, tag)`, and backs every admin layer.

|Column|Notes|
|------|-----|
|`page_path`|Required: matches the request's page path|
|`experience_path`|Required: matches the experience basename|
|`tag`|Required: the top-level element's custom-element name|
|`name`|Required: the full storage key|
|`value`|JSON, validated at write time|
|`condition`|Optional GlideScript, evaluated server-side|
|`order`|Evaluation order for conditional rows; default 100|
|`personalization_disallowed`|Blocks the user preference from applying; default false|
|`sys_domain` / `sys_domain_path`|Standard domain separation|

The `name` column encodes the element's position in the component tree: `propKey` for a top-level property, `header.propKey` or `header.badge.propKey` for a nested one. See [Configurable properties for Lux experiences](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/configurable-properties.md) for how an id chain produces that key.

## sys\_user\_preference

No schema changes. User layers use dot-separated keys:

-   Scoped: `aix.config.{pageId}.{tag}.{instanceId}.{name}`
-   Global: `aix.config-global.{tag}.{name}`

**Related topics**  


[Configuration model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/configuration-model.md)

[Configurable properties for Lux experiences](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/configurable-properties.md)

[admin-experience]

[Regions and the wrapper contract](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/regions-and-the-wrapper-contract.md)

