---
title: Configure Lens launcher using scripted screen
description: Configure a ServiceNow AI Lens launcher button with scripted screen.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-12-08"
reading_time_minutes: 1
breadcrumb: [Configure Lens launcher button, Configuring Now Assist for Mobile, Now Assist for Mobile, Mobile Platform]
---

# Configure Lens launcher using scripted screen

Configure a ServiceNow AI Lens launcher button with scripted screen.

The following example adds a button instance to the “top-icon” location of the scripted screen. The highlighted portions indicate the updates needed in an existing scripted screen to add the ServiceNow AI Lens Launcher button.

![new script additions highlighted in yellow](../image/na-lens-launcher-scripted-screen.png "Lens launcher configured with scripted screen")

```
(function ScriptedScreen(input, result) {
var builder = new sn_scripted_screen.ParameterScreenBuilder("scripted_screen_incident", "Edit Incident Scr");
builder.nextLabel = gs.getMessage("Next");
builder.previousLabel = gs.getMessage("Previous");
builder.cancelLabel = gs.getMessage("Cancel");
builder.submitLabel = gs.getMessage("Submit");
var variableBuilder = new sn_scripted_screen.VariableBuilder("v_short_description", "db_field");
variableBuilder.addAttribute("FieldName", "short_description");

var buttonInstanceBuilder = new sn_scripted_screen.ButtonInstanceBuilder("a719743e0f703210e83019e800d1b29d", "Lens Launcher", "top_icon");
buttonInstanceBuilder.icon = "76d03b43ff6c721057e9ffffffffff1f";

var inputBuilder = new sn_scripted_screen.InputBuilder("short_description", "string", "Short Descrition");
inputBuilder.autofillVariable(variableBuilder);
builder.addInput(inputBuilder);
builder.addButtonInstance(buttonInstanceBuilder);
builder.addVariable(variableBuilder);
builder.presentationStyle = "screen";
builder.advancedPagination = "true";
result.screenBuilder = builder;
return result;
})(input, result);

```

In this example, `a719743e0f703210e83019e800d1b29d` is the sys\_id of the **sys\_sg\_button** of type **lens\_launcher**. The button must be created declaratively.

`76d03b43ff6c721057e9ffffffffff1f` is the sys\_id of the **sys\_sg\_icon**.

**PresentationStyle** should be **screen** to support a button instance on an input form screen or scripted screen.

The third parameter in `ButtonInstanceBuilder()` is the location. The location can be either `top_icon` or `top`.

**Parent Topic:**[Configure Lens launcher button](configure-lens-launcher-button.md)

