---
title: Input workflow activity
description: The Input activity creates a phone menu by presenting a list of options on a Notify call.
locale: en-US
release: xanadu
product: Notify
classification: notify
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Notify workflow activities, Reference, Notify, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Input workflow activity

The **Input** activity creates a phone menu by presenting a list of options on a Notify call.

## Input Variables

Input variables determine the initial behavior of the activity.

<table id="table_pgm_tfy_jr"><thead><tr><th>

Variable

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number of digits

</td><td>

Specify the maximum number of digits the caller can enter. A caller can enter fewer digits than the maximum and press the **Finish key** to complete the entry.

</td></tr><tr><td>

Finish key

</td><td>

Specify the key a caller can press on their phone when finished selecting a menu option.

</td></tr><tr><td>

Timeout \(in seconds\)

</td><td>

Specify the amount of time to wait before closing the menu automatically when the caller does not select a menu option.

</td></tr><tr><td>

Advanced

</td><td>

Select this check box to use a script to build the phone menu, instead of using the activity conditions.

</td></tr><tr><td>

Script

</td><td>

Define the script to build the phone menu. The script must specify an **answer** variable as a JavaScript object with the following format:```
 answer = {
  “1": {
      “play”: “https://some_url.com/options/one.mp3“,
      “myCustomData”: “some data here”
  },
  “2”: {
      “play”: “https://some_url.com/options/two.mp3”,
      “myCustomData”: “some other data here”
  },
“3”: {
      “speak”: “type 3 to speak to a representative”,
      “language”: “en-US”,
      “myCustomData”: “some more data here”
  }
};
```

 The script may specify either a text-to-speech string and language code using the **speak** attribute or URL of the music to be played using the **play** attribute. You can also add optional attributes to store related information, such as **myCustomData** in the example above.

 **Note:** The script object continues to support **say** attribute for backward compatibility.

</td></tr></tbody>
</table>## Conditions

The conditions determine the transition that comes after this activity.

The **input** activity does not specify any conditions by default. You must define conditions to build the phone menu. Each condition is one option on the phone menu. Notify reads the text from each condition **Name** to the caller, up to 100 characters per condition.

You can specify a language for each condition by prefixing the message with the language code, in the format **xx-XX:&lt;Message&gt;**. For example, add **fr-CA:** for Canadian French. Available languages are stored on the Notify Language \[notify\_language\] table.

The condition that the activity transitions through depends on the digits entered by the caller. Set the condition **Condition** value to **parseInt\(workflow.scratchpad.digits\) == &lt;expected digits&gt;**. For example, to transition through a condition when the caller presses the number 3, set the **Condition** to **parseInt\(workflow.scratchpad.digits\) == 3**.

You can add an error condition to this activity. The activity transitions through the error condition if the advanced script returns an invalid value, or if the text to say for a condition is empty.

## Scratchpad Entries

The activity uses the workflow scratchpad to write persistent values.

<table id="table_o2s_wgy_jr"><thead><tr><th>

Entry

</th><th>

Description

</th></tr></thead><tbody><tr><td>

workflow.scratchpad.digits

</td><td>

The digits entered by the caller, as a string.

</td></tr><tr><td>

workflow.scratchpad.menu&lt;activity name&gt;

</td><td>

The entire **answer** variable, if using the advanced script option. You can access this menu from other activities after this activity successfully executes.For example, if the activity name is `choices`, you can access values from the menu using

```
var previousActivity = "choices";
var choicesMenu = workflow.scratchpad.menu[previousActivity];
var menuItem = choicesMenu[workflow.scratchpad.digits];  // Selects the menu item based on the caller's input.
var selectedValue = menuItem.myCustomData; //get the custom data for the selected menu item. 
```

</td></tr></tbody>
</table>**Parent Topic:**[Notify workflow activities](../concept/c_NotifyActivities.md)

