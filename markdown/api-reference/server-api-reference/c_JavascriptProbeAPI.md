---
title: JavascriptProbe - Global
description: The JavascriptProbe script include provides methods for using the JavascriptProbe on the MID Server.Creates an instance of the JavascriptProbe.Adds a parameter with the specified value to the probe.Creates the probe for the current MID server, puts it on the output queue, and sets its state to "ready".Adds a script to the probe.Sets the name of the JavascriptProbeSets the source of the probe.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# JavascriptProbe- Global

The JavascriptProbe script include provides methods for using the JavascriptProbe on the MID Server.

Use these methods in server scripts to send a probe to the MID Server For more information, see [Create a JavaScript Probe activity](https://www.servicenow.com/docs/access?context=t_CreateAJavaScriptProbeActivity&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## JavascriptProbe - JavascriptProbe\(String midServer\)

Creates an instance of the JavascriptProbe.

|Name|Type|Description|
|----|----|-----------|
|midServer|String|The MID server name|

The following example shows how to use an instance of JavascriptProbe.

```
var jspr = new JavascriptProbe('midserver_name');

var func = function () {
    // Java FileWriter class of java.io package. FileWriter is write data in character.
    var FileWriter = Packages.java.io.FileWriter;

    // Constructs a FileWriter object given a file name.
    var file = new FileWriter("TestMessage.txt");

    // Gets the parameter from the ECC queue payload.
    var message = probe.getParameter("message");

    // Write the message to a file.
    file.write(message);

    // Close the FileWriter.
    file.close();
    file = null;
}

// Add parameter to pass to MIDServer.
jspr.addParameter('message', 'ServiceNow Message');

// Set the script to be executed by the MIDServer as a string
jspr.setJavascript('(' + func.toString() + ')();');

// Send to MIDServer. The MIDServer will execute the Script immediately.
jspr.create();
```

## JavascriptProbe - addParameter\(String name, String value\)

Adds a parameter with the specified value to the probe.

|Name|Type|Description|
|----|----|-----------|
|name|String|The parameter name|
|value|String|The parameter's value|

|Type|Description|
|----|-----------|
|void| |

```
var jspr = new JavascriptProbe('msserv');
jspr.setName('jsprobe100');
jspr.setSource('jspr_source');
jspr.addParameter('support_feat', 'yes');
```

## JavascriptProbe - create\(\)

Creates the probe for the current MID server, puts it on the output queue, and sets its state to "ready".

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|void| |

```
var jspr = new JavascriptProbe('msserv');
jspr.setName('jsprobe100');
jspr.setSource('jspr_source');
jspr.setJavascript('jspr_script');
jspr.create();
```

## JavascriptProbe - setJavascript\(String script\)

Adds a script to the probe.

|Name|Type|Description|
|----|----|-----------|
|script|String|The script to add to the probe|

|Type|Description|
|----|-----------|
|void| |

```
var jspr = new JavascriptProbe('msserv');
jspr.setName('jsprobe100');
jspr.setSource('jspr_source');
jspr.setJavascript('jspr_script');
```

## JavascriptProbe - setName\(String name\)

Sets the name of the JavascriptProbe

|Name|Type|Description|
|----|----|-----------|
|name|String|The name to give the JavascriptProbe.|

|Type|Description|
|----|-----------|
|void| |

```
var jspr = new JavascriptProbe('msserv');
jspr.setName('jsprobe100');
```

## JavascriptProbe - setSource\(String ip\)

Sets the source of the probe.

|Name|Type|Description|
|----|----|-----------|
|ip|String|The IP address of the target probe.|

|Type|Description|
|----|-----------|
|void| |

```
var jspr = new JavascriptProbe('msserv');
jspr.setName('jsprobe100');
jspr.setSource('100.100.100.1');
```

