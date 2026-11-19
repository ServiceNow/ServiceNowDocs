---
title: Configurable properties for Lux experiences
description: A property becomes configurable and visible in the props pane when you add a decorator to it. The decorator's options set the field type that the props pane renders, and also set the storage key that the resolved value is read back from.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/application-development/configurable-properties.html
release: australia
topic_type: reference
last_updated: "2026-09-29"
reading_time_minutes: 9
keywords: [Configurable properties, @config decorator, @config options, Field types, Grouping a crowded panel, Conditional fields \(dependsOn\), Configuration ids for nested components, Storage key format, Config service methods, Configuration modes, Actions \(@action\), Related]
breadcrumb: [Configure experiences, Lux Development, Building pro-code applications, Developing your application, Building applications]
---

# Configurable properties for Lux experiences

A property becomes configurable and visible in the props pane when you add a decorator to it. The decorator's options set the field type that the props pane renders, and also set the storage key that the resolved value is read back from.

## @config decorator

```
import {AIUXElement, config} from '@servicenow/aiux-components-core';
import {customElement} from 'lit/decorators.js';
import {html} from 'lit';

@customElement('my-widget')
export default class MyWidget extends AIUXElement {
  @config({
    label: 'Display Density',
    description: 'Controls how compact the widget appears',
    group: 'Appearance',
    type: 'select',
    choices: [
      {value: 'compact', label: 'Compact'},
      {value: 'normal', label: 'Normal'},
      {value: 'comfortable', label: 'Comfortable'}
    ]
  })
  density = 'normal'; // ← the developer default

  render() {
    return html`<div class="widget density-${this.density}">…</div>`;
  }

  _onDensityChange(e) {
    this.updateConfig('density', e.detail.value);
  }
}
```

The decorator does three things:

1.  Registers metadata. The `label`, `description`, `group`, `choices`, and `type` you pass go into the component's manifest. The props pane auto-generates the settings UI from it, and AIEL reads the same manifest.
2.  Turns the field into a getter: `get density() { return this.aiuxConfigData?.density ?? 'normal'; }`. The `this.aiuxConfigData` object is populated from the `aiux-config-data` attribute on the element, which carries the fully-resolved payload for this user.
3.  Makes your initial value the bottom layer: the developer default, used when no other layer has a value.

Two constraints that produce silent bugs if you miss them:

-   Never assign to a `@config` field. The statement `this.density = 'compact'` is a no-op, because the field is a getter. Use `this.updateConfig('density', 'compact')`, or `setPersonalization` or `setConfigValue` from the config service.
-   Never combine `@config` with a parent-controlled `@property()`. The getter reads from `aiuxConfigData`, and a parent setting the same attribute conflicts with it. Use `@state()`, or no Lit decorator at all, for the backing field.

## @config options

|Option|Type|Description|
|------|----|-----------|
|`label` \(required\)|string|Name shown in the config UI, and the name AIEL uses to expose the property.|
|`description`|string|Longer explanation, rendered as tooltip text.|
|`group`|string \(default `"General"`\)|Groups related settings in the panel. See [Grouping a crowded panel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/configurable-properties.md).|
|`order`|number|Sort position within the group; lower values appear first.|
|`choices`|`{value, label}[]`|A closed set of values. Renders a select; combine with `multi: true` for a multi-select.|
|`type`|string|Explicit field type. Takes priority over the legacy constructor flags. See [Field types](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/configurable-properties.md).|
|`table`|string|Required with `type: 'reference-picker'`; the table to search.|
|`min` / `max` / `step`|number|Constraints for number fields.|
|`rows` / `maxlength` / `minlength` / `placeholder`|number or string|Options for textarea and string fields. `rows` defaults to 3.|
|`pattern`|string|Regex validation for string and URL inputs.|
|`dependsOn`|object|Conditional visibility. See [Conditional fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/configurable-properties.md).|
|`list`|`{table, query?, view?, columns?}`|Renders a pencil button opening a list iframe modal. Use with `type: Array`; the stored value is the resulting ordered record set.|

## Field types

|`type`|Field rendered|Extra options|
|------|--------------|-------------|
|`'string'` \(fallback\)|Text input|`maxlength`, `minlength`, `placeholder`, `pattern`|
|`'url'`|URL input|same as string|
|`'textarea'`|Textarea|`rows`, `maxlength`, `minlength`, `placeholder`|
|`Boolean`|Toggle switch| |
|`Number`|Number input|`min`, `max`, `step`|
|`choices[]` without `multi`|Drop-down list|`choices` required|
|`'select-multi'`|Multi-select|`choices` required|
|`'datetime'`|Date and time picker|`hideTime` renders date-only|
|`'color'`|Color swatch picker|`choices` optional; defaults to a built-in palette|
|`'reference-picker'`|Single record typeahead|`table` required|
|`'table-picker'`|Table name typeahead|`items` optionally pre-seeds the list|
|`'table-reference'`|Two-step: pick table, then record| |
|`'role-picker'`|Role typeahead over `sys_user_role`|`items` optionally pre-seeds the list|
|`'condition-builder'`|Condition builder modal|`tableName` fixes the table; omit for a dynamic picker|
|`'custom'`|Author-supplied element|`component` required: the element tag name. Pilot.|

Values come out of storage as JSON strings, and `type` drives the coercion.

```
@config({label: 'Show SLA Fields', type: 'boolean'})
showSlaFields = true;

@config({label: 'Page Size', type: 'number', min: 5, max: 100, step: 5})
pageSize = 20;

@config({label: 'Default Assignment Group', type: 'reference-picker', table: 'sys_user_group'})
defaultGroup = '';

@config({label: 'Notes', type: 'textarea', rows: 5, placeholder: 'Enter notes…'})
notes = '';
```

Legacy constructor flags \(`referencePicker: true` with `table`, `tablePicker: true`, `tableReference: true`, `rolePicker: true`\): resolve to the equivalent string `type` values for backward compatibility. Use the explicit string `type` in new code; the explicit string type value is used when both are set.

## Grouping a crowded panel

Give each property a `group` id, and optionally declare `static configGroups` to control order and labels:

```
class MyWidget extends AIUXElement {
  static configGroups = [
    {id: 'text', label: 'Text fields'},
    {id: 'selection', label: 'Selection fields'},
    {id: 'data', label: 'Data fields', defaultExpanded: false}
  ];

  @config({label: 'Title', type: String, group: 'text'})
  title;
}
```

Groups render in the declared order, or in first-appearance order if you omit `configGroups`. Each group's `defaultExpanded` defaults to `true`. Properties with no group, or with a group id not listed, render ungrouped after the accordions.

Grouping earns its keep when the pane is crowded. What matters is how far an admin has to navigate to reach the property they configure most often, not the number of groups.

## Conditional fields \(dependsOn\)

A field can declare that it appears only when a sibling satisfies a condition.

|Mode|Schema|Shown when|
|----|------|----------|
|exists|`dependsOn: {key: 'parentProp'}`|Parent value is non-empty|
|equals|`dependsOn: {key: 'parentProp', value: 'exact'}`|Parent strictly equals `value`|
|one-of|`dependsOn: {key: 'parentProp', value: ['a', 'b']}`|Parent is in the array|

```
@config({
  label: 'Temperature',
  type: Number,
  dependsOn: {key: 'cookingMethod', value: ['grill', 'oven']}
})
temperature;
```

When a parent value changes, any field whose condition is no longer satisfied resets to its default, and the cascade propagates transitively. Circular `dependsOn` chains are detected at decoration time and logged as an error rather than thrown. The circular segment is silently ignored, which can produce unexpected auto-clear behavior.

## Configuration ids for nested components

A page's resolved payload is one flat object with dot-namespaced keys: `"other.button.density": "compact"`. A component gets its slice of that payload by carrying a configuration id.

In a region template, write the attribute.

```
// regions/home/body.js
export default () => region`
  <row>
    <column span=${8}><stat-card aiux-config-id="stat-card-1" /></column>
  </row>
`;
```

The `aiux-config-id` attribute is the one region-DSL editor attribute the runtime does not consume and drop. It compiles to exactly the binding a hand-written `elementId(host, 'stat-card-1')` on `aiux-config-data` produces, and that directive stamps `data-aiux-element-id` on the rendered element. So the widget becomes an ordinary configuration entry: stored in `sys_aix_configuration` under `<id>.<prop>`, read back by the same `@config` getter, reset by the same call.

Three rules apply to the attribute:

-   It must be a non-empty string. A bare `aiux-config-id` with no value throws, because the value is used both as a DOM id and as an `aiuxConfigData` key prefix.
-   It is valid only on a widget tag, not on `row` or `column`.
-   Without it, the widget cannot be configured at all: see [Placing Lux widgets in regions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/placing-widgets-in-regions.md) for what that looks like to an admin.

Avoid `/` in an id. The id travels in a URL path segment when a reset is sent, where a slash either gets rejected or normalized back into a separator. Widgets the visual editor adds are stamped `<tag>__<nonce>` for this reason.

In a hand-written Lit template, call the function. The `elementId(this, 'id')` call is the underlying mechanism, and what you write when the parent is a plain Lit `render()` rather than a region:

```
import {AIUXElement, elementId, config} from '@servicenow/aiux-components-core';

@customElement('some-page')
class SomePage extends AIUXElement {
  @config({label: 'Greeting'})
  greeting = 'Hello there!';

  render() {
    return html`
      <h1>${this.greeting}</h1>
      <other-element aiux-config-data=${elementId(this, 'other')}></other-element>
    `;
  }
}
```

Either way, each element does exactly two things with its slice:

1.  Peels its own keys: assigns values whose key matches one of its own `@config` field names.
2.  Forwards subtrees: for every id it declares, slices all keys prefixed `id.`, strips the prefix, and passes the rest down.

So given `greeting`, `other.propA`, and `other.button.density`, the page keeps `greeting` and forwards the other two. A page author only needs to specify their direct children's ids; the child is responsible for slicing and forwarding to its own children. The id must be unique among siblings at that level, and a child absent from the payload gets an empty object, so its `@config` defaults take over.

## Storage key format

|Element|Stored key|
|-------|----------|
|Top-level page property|`propKey`|
|Direct child \(id chain `['header']`\)|`header.propKey`|
|Grandchild \(id chain `['header', 'badge']`\)|`header.badge.propKey`|

The `tag` column on the stored row is always the top-level element's custom-element name, not the child's.

## Config service methods

The config service is a module, not a DOM element, and it works on top-level element tag names; it does not work on nested children directly.

|Method|What it does|
|------|------------|
|`setConfigValue(tag, key, value, options)`|Change the admin-layer value. Optimistic: applies immediately, rolls back if the save fails.|
|`setPersonalization(tag, key, value, options)`|Change the user's own value, saved to `sys_user_preference`. Optimistic with rollback.|
|`resetConfig(tag, key, options)`|Clear the current value, falling back to the next lower layer. `{all: true}` clears every layer down to the developer default.|
|`resetPersonalization(tag, key)`|Clear this user's preference only.|

```
import {
  setPersonalization,
  resetPersonalization,
  resetConfig
} from '@servicenow/aiux-config-service';

await setPersonalization('itsm-incident-list', 'density', 'compact');
await resetPersonalization('itsm-incident-list', 'density');
await resetConfig('itsm-incident-list', 'density', {all: true});
```

## Configuration modes

`@config` is one of four modes a property or a whole widget can use, in increasing order of author effort.

|Order|Mode|Declared with|Editing UI|Saves to|
|-----|----|-------------|----------|--------|
|1|Independent config|`@config` on a field|The framework props pane: value field plus lock toggle per property|`sys_aix_configuration`|
|2|External config|`@externalConfig` on the class|Same pane, plus a link out to a list, record, or URL|The author's own table|
|3|Custom URL|`static configMode = 'inline-simple'`|Pane stays; a button opens an author-supplied URL in an iframe|Wherever that tool saves, not through the framework|
|4|Self-config|`static configMode = 'inline-auto'`|The widget renders its own editor, fully interactive|`sys_aix_configuration`, through the framework's save pipeline|

Mode 1 is the default unless the widget is genuinely complex: list, form, action bar, data visualization. Modes 3 and 4 are the path for those specific widget families.

Modes combine. The `configMode` static accepts a comma-separated list: `'inline-auto,inline-simple'`, and either mode can be paired with `@config` decorators on the same widget. The editor then shows both the deep-link button and the props-pane pencil on one outline. A widget can also declare multiple `@externalConfig` entries.

See [Inline configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/inline-configuration.md) for each mode in detail.

## Actions \(@action\)

`@action`, a decorator for exposing component methods as AI-invokable, shortcut-configurable actions, is design-stage only. Nothing described for it exists in the current codebase, and it has no entry in the customer-facing configuration documentation. Don't build against it.

**Related topics**  


[Configuration model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/configuration-model.md)

[Inline configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/inline-configuration.md)

[admin-experience]

