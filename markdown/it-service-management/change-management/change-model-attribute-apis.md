---
title: Change model attribute API methods
description: Use these server-side and client-side methods to check which change model attributes are present for a change request in its current state.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/change-management/change-model-attribute-apis.html
release: brazil
product: Change Management
classification: change-management
topic_type: reference
last_updated: "2026-09-30"
reading_time_minutes: 3
keywords: [change model attributes, ChangeRequest API, hasStateAttribute, getStateAttributes]
breadcrumb: [Change model attributes, Create a Change model, Configure, Change Management, IT Service Management]
---

# Change model attribute API methods

Use these server-side and client-side methods to check which change model attributes are present for a change request in its current state.

## Server-side methods

The ChangeRequest API provides these methods for use in business rules, UI actions, and other server-side scripts.

|Method|Description|
|------|-----------|
|hasStateAttribute|Returns `true` if the attribute with the specified name is assigned to the current state of the change request.|
|modelContainsAttribute\(name\)|Returns true if the attribute with the specified name is contained anywhere in the model. Useful when introducing an attribute and you want to preserve existing behavior for models without the attribute.|

## Server-side example

The following example loads a change request and checks its state attributes.

```javascript
var changeGr = new GlideRecord("change_request");
changeGr.get("<sys_id>");

var changeRequest = new ChangeRequest(changeGr);
gs.info(changeRequest.getStateAttributes());
gs.info(changeRequest.hasStateAttribute("allow_ci_modification"));
```

For a change request in a state that has both attributes, the output includes both attribute names and `true` for each attribute.

## Client-side methods

A client-side Change Model object is available on the Change Request form for client scripts.

|Method|Description|
|------|-----------|
|hasStateAttribute\(name\)|Returns true if the attribute with the specified name is assigned to the current state of the change request.|
|containsAttribute\(name\)|Returns true if the attribute with the specified name is contained anywhere in the model. Useful when introducing an attribute and you want to preserve existing behavior for models without the attribute.|

The functions can be found in the change\_model object on the scratchpad.

## Example: Enforce the Allow CI Modification attribute

The base system enforces the Allow CI Modification attribute with a client script and a business rule that use these methods. Together, they keep the original CI modification behavior for models that don't use the attribute and apply the attribute for models that do. You can follow the same pattern to add support for a custom attribute.

**Client script: Change model: Read only CI**

This client script makes the **Configuration item** field read-only unless the current state has the Allow CI Modification attribute. If no state in the model has the attribute, the field stays editable in the initial state only. The script runs when the value of the **State** field changes, so the form always matches the change model.

```javascript
function onChange(control, oldValue, newValue, isLoading, isTemplate) {
    var ALLOW_CI_MODIFICATION = "allow_ci_modification";

    // Retrieve the Change Model API and data from the scratchpad
    if (!g_scratchpad.change_model)
        return;

    var model = g_scratchpad.change_model;

    // Check if the field should be read only based on if the model contains the state and if the "allow_ci_modification" attribute has been added to the state
    var isReadOnly = model.containsAttribute(ALLOW_CI_MODIFICATION) ?
            !model.hasStateAttribute(ALLOW_CI_MODIFICATION) : g_form.getValue(model.field) + "" !== model.initial_state;

    g_form.setReadOnly("cmdb_ci", isReadOnly);
}
```

**Business rule: Change Model: Read only CI**

This business rule prevents changes to the configuration item on a change request unless the current or previous state has the Allow CI Modification attribute. If no state in the model has the attribute, the configuration item can still change in the initial state. The business rule runs when the configuration item changes on a change request that has a change model.

```javascript
(function executeRule(current, previous /*null when async*/) {
    var ALLOW_CI_MODIFICATION = "allow_ci_modification";

    var changeRequest = new ChangeRequest(current);
    var preChangeRequest = new ChangeRequest(previous);
    var modelContainsAttribute = changeRequest.modelContainsAttribute(ALLOW_CI_MODIFICATION);

    // If the attribute isn't enabled preserve original 'initial state' CI changes
    if (!modelContainsAttribute && (changeRequest.isInitialState() || prevChangeRequest.isInitialState()))
        return;

    // If the current state has the attribute allow the CI to be modified
    if (changeRequest.hasStateAttribute(ALLOW_CI_MODIFICATION))
        return;

    // If the previous state has the attribute also allow the CI to be modified
    if (new ChangeRequest(previous).hasStateAttribute(ALLOW_CI_MODIFICATION))
        return;

    // Otherwise, if it's a new record (no previous record) use the model to lookup the attribute on the intial state
    var changeModel = new ChangeModel(new ChangeRequest(current).getModel());
    if (current.isNewRecord() && changeModel.hasStateAttribute(changeRequest.getInitialState(), ALLOW_CI_MODIFICATION))
        return;

    // Abort the modification
    gs.addErrorMessage(gs.getMessage("Configuration item cannot change for Change Requests in this state"));
    current.setAbortAction(true);
})(current, previous);
```

**Parent Topic:**[Change model attributes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/change-management/change-model-attributes.md)

