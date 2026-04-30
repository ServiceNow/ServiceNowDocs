---
title: Application level method parameters
description: These parameters pass custom specifications to the various applications such as Java, Google Chrome , Windows , and Mainframe. Based on the specifications, the applications return an output. The process is a part of a Robotic Process Automation .
locale: en-US
release: xanadu
product: RPA Hub
classification: rpa-hub
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Connectors, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Creating integrations with applications]
---

# Application level method parameters

These parameters pass custom specifications to the various applications such as Java, Google Chrome, Windows, and Mainframe. Based on the specifications, the applications return an output. The process is a part of a Robotic Process Automation.

|Parameter|Description|Mandatory?|
|---------|-----------|----------|
|Return \(Boolean\)|Returns the Boolean response to the request of setting an inactive window active. Successful operation returns True.|Not applicable|
|Form data|Returns the captured form element data.|Not applicable|
|MatchAllChildren|Option to indicate whether the method will match all elements of the application while the terminal session executes.|No|
|Action \(MouseAction\)|Action the mouse device will perform on the Java application.|No|
|Keys|Accepts keys, combination of keys, or special keys to trigger their specific actions. For example, **CTRL+A** selects all text.|Yes|
|Return \(Integer\)|Returns the integer value of the number of open Java application instances.|Not applicable|
|ClearExistingValue|Clears or retains existing value in a field after accepting a Boolean response of True or False.|No|
|Keys \(String\)|Shortcut keys that perform specific actions.|Yes|
|ClearExistingValues|Option to indicate whether the method will clear any existing value on the field in the Java application.|No|
|TypeDelay|Option to set any delay before the method operates.|No|
|xPos|Position of the Java application along the X-axis.|No|
|yPos|Position of the Java application along the Y-axis.|No|
|Width|Width of the Java application along the X-axis.|No|
|Height|Height of the Java application along the X-axis.|No|
|TypeDelay|Delays the execution of the SendKeys method in terms of seconds. Specify the seconds.|No|
|timeoutInSeconds|Time until which the method waits for the terminal session to execute. The method times out if the terminal session doesn't execute after the specified time.|No|
|Return \(Boolean\)|Returns the Boolean response to the WaitforCreate request. If the terminal session executes before the set timeout, the value is **True**.|Not applicable|
|Return \(Boolean\)|Boolean response to indicate whether a window or web page is ready to accept requests.|No|
|Timeout|Time after which the wait for elements to load will time out.|No|
|Return \(Boolean\)|Boolean response to indicate whether the method waited for the elements to load.|Not applicable|
|Return \(Boolean\)|Returns the Boolean response on whether all children elements matched.|Not applicable|
|Return \(Integer\)|Returns the integer value of the Microsoft Windows handle.|Not applicable|
|MatchAllChildren|Option to indicate whether the request will match all parameters of the window while it waits for the window to load.|No|
|Parameter|Parameter value for the JavaScript.|Yes|
|Return \(Bitmap\)|Returns the captured screenshot of the active Java application window in Bitmap format.|Not applicable|
|Return \(Boolean\)|Returns the boolean response to whether a Java application is active or available.|Not applicable|
|Field \(String\)|Returns the data in the form or text field.|Not applicable|
|MatchAllChildren|Option to indicate whether the method will match all elements of the application while the terminal session executes.|No|

**Parent Topic:**[Connectors](../concept/connectors.md)

