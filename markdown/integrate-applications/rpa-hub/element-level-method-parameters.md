---
title: Element level method parameters
description: These parameters pass custom specifications to the elements in various applications such as Java, Google Chrome , Windows , and Mainframe. Based on the specifications, the applications return an output. The process is a part of a Robotic Process Automation .
locale: en-US
release: yokohama
product: RPA Hub
classification: rpa-hub
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Connectors, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Data and Automation]
---

# Element level method parameters

These parameters pass custom specifications to the elements in various applications such as Java, Google Chrome, Windows, and Mainframe. Based on the specifications, the applications return an output. The process is a part of a Robotic Process Automation.

|Parameter|Description|Mandatory?|
|---------|-----------|----------|
|Return \(Boolean\)|Returns the Boolean response to whether the rules in the MATCH RULES section matched. The responses are True or False.|Not applicable|
|ClearExistingValue|Clears or retains existing value in a field after accepting a Boolean response of True or False.|No|
|TypeDelay|Delays the execution of the SendKeys method in terms of seconds. Specify the seconds.|No|
|Value \(String\)|Accepts keys, combination of keys, or special keys to trigger their specific actions. For example, **CTRL+A** selects all text.|Yes|
|Return \(String\)|Returns a list of actions you can perform on an element.|Not applicable|
|Return|Returns the Boolean response on whether the action was successful.|Not applicable|
|Action \(String\)|Option to indicate the action to be performed on the method.|Yes|
|Keys \(String\)|Accepts keys, combination of keys, or special keys to trigger their specific actions. For example, **CTRL+A** selects all text.|No|
|Return \(Boolean\)|Boolean response to whether the Click method was successful.|Not applicable|

**Parent Topic:**[Connectors](../concept/connectors.md)

