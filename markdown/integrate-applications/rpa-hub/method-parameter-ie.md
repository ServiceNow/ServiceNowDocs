---
title: Parameters of the IE connector methods
description: Learn about the parameters of the Microsoft IE Connector \(Internet Explorer\) methods in RPA Desktop Design Studio.
locale: en-US
release: xanadu
product: RPA Hub
classification: rpa-hub
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [IE connector, Connectors, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Creating integrations with applications]
---

# Parameters of the IE connector methods

Learn about the parameters of the Microsoft IE Connector \(Internet Explorer\) methods in RPA Desktop Design Studio.

<table id="table_rfq_qpm_3rb"><thead><tr><th>

Parameter Name

</th><th>

Description

</th><th>

Mandatory?

</th></tr></thead><tbody><tr><td>

MatchAllChildren

</td><td>

Option to indicate in Boolean values whether before loading a screen, the method will match all the captured children screens and elements with the screen.

 You can find the children screens and elements under the MATCH CHILDREN section of the configuration window.

</td><td>

No

</td></tr><tr><td>

Return \(String\)

</td><td>

Returns the value.

</td><td>

Not applicable

</td></tr><tr><td>

Return \(String\)

</td><td>

Returns the URL of the web page or website.

</td><td>

Not applicable

</td></tr><tr><td>

Return \(String\)

</td><td>

Returns the title of the web page.

</td><td>

Not applicable

</td></tr><tr><td>

XPath

</td><td>

XPath value.

</td><td>

Yes

</td></tr><tr><td>

Return \(Bitmap\)

</td><td>

Returns the screenshot of the web page in Bitmap format.

</td><td>

Not applicable

</td></tr><tr><td>

Return \(Boolean\)

</td><td>

Boolean response to the request for setting focus on a window and making it active.

</td><td>

Not applicable

</td></tr><tr><td>

Form fields

</td><td>

Returns the data in the forms.

</td><td>

Not applicable

</td></tr><tr><td>

Return

</td><td>

Returns the page source of the web page.

</td><td>

Not applicable

</td></tr><tr><td>

Return \(Object\)

</td><td>

Returns the output as an object after executing the JavaScript.

</td><td>

Not applicable

</td></tr><tr><td>

url

</td><td>

URL of the file to download.

</td><td>

Yes

</td></tr><tr><td>

fileName

</td><td>

Name of the file to download.

</td><td>

Yes

</td></tr><tr><td>

Return \(Boolean\)

</td><td>

Boolean response to the request for file download.

</td><td>

Not applicable

</td></tr><tr><td>

Parameter

</td><td>

Value of the parameter you added when configuring the method.

</td><td>

No

</td></tr><tr><td>

Return \(Boolean\)

</td><td>

Boolean value to indicate whether the website or screen on the IE browser is ready to accept requests from methods.

</td><td>

Not applicable

</td></tr><tr><td>

Timeout

</td><td>

Time in seconds after which the request for wait times out.The default value is 30 seconds.

</td><td>

No

</td></tr><tr><td>

GetOuterHTML

</td><td>

Returns the outer HTML in a string format,

</td><td>

Not applicable

</td></tr><tr><td>

Return \(String\)

</td><td>

Returns the inner HTML of the element in a string.

</td><td>

Not applicable

</td></tr><tr><td>

Return \(String\)

</td><td>

Returns the URL of the element in a string format.

</td><td>

Not applicable

</td></tr><tr><td>

Return \(Boolean\)

</td><td>

Boolean response to whether the method waited for the screen to load.

</td><td>

Not applicable

</td></tr><tr><td>

Keys

</td><td>

Gives the keys that will operate on the web page open in the browser.

</td><td>

Yes

</td></tr><tr><td>

GetInnerText

</td><td>

Returns the inner HTML of the element in a string.

</td><td>

Not applicable

</td></tr><tr><td>

MatchAllChildren

</td><td>

Boolean option to indicate whether the method will match all children elements of the web page before sending keys.

</td><td>

No

</td></tr><tr><td>

TypeDelay

</td><td>

Delay before the method sends the request.

</td><td>

No

</td></tr><tr><td>

timeoutInSeconds

</td><td>

Time indicated in seconds before the request times out.

</td><td>

Yes

</td></tr><tr><td>

NoPrompt

</td><td>

Boolean option to indicate whether a prompt is passed through the method to print the web page.

</td><td>

Yes

</td></tr><tr><td>

matchAllChildren

</td><td>

Boolean option to indicate whether the method will match all children elements of the screen.

</td><td>

Not applicable

</td></tr><tr><td>

Return \(Boolean\)

</td><td>

Returns the Boolean response to the request of opening a web page.

</td><td>

Not applicable

</td></tr><tr><td>

URL

</td><td>

Address of a web page to open.

</td><td>

Yes

</td></tr><tr><td>

Return \(Boolean\)

</td><td>

Boolean response to the request to check whether a website or screen is open on the browser.

</td><td>

Not applicable

</td></tr><tr><td>

Return \(Boolean\)

</td><td>

Boolean response to indicate whether all children elements were matched.

</td><td>

Not applicable

</td></tr><tr><td>

XPath \(String\)

</td><td>

Option to provide the XPath that the method converts to string.

</td><td>

Yes

</td></tr><tr><td>

Return \(String\)

</td><td>

Returns the converted XPath as a String.

</td><td>

Not applicable

</td></tr></tbody>
</table>## Enter inputs for parameters

To enter inputs, see [Configure port properties](../task/configure-input-port-properties.md).

**Parent Topic:**[IE connector](../concept/internet-explorer-connector.md)

