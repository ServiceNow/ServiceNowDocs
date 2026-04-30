---
title: On classification script objects for Discovery
description: Use an On classification script in a process classifier to customize an application record. This kind of script is used in a process classifiers.
locale: en-US
release: xanadu
product: Discovery
classification: discovery
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Create a Discovery process classification, Discovery classifiers, Configuring Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# On classification script objects for Discovery

Use an On classification script in a process classifier to customize an application record. This kind of script is used in a process classifiers.

## Renaming the default application name

By default, application names are in this format: `<name of the process classifer>@<the name of the computer CI where the process resides>;`

For example, for a MySQL server running on a computer called machineA, the application is named `mysql@machineA`.

You can use the **On classification script** field in the [process classifier record](../task/t_CreateAProcessClassification.md) to change the default application name to match your business needs. For example, the following script changes the default application name to include a suffix after the process classifier:

```
var computerName = g_sensor.deviceGR.name;
var processClassiferName = g_classification.name;
current.name = processClassiferName + "999" + "@" + computerName;
```

In this example, the name of the application record becomes `mysql999@machineA`.

Another common technique is to set the application name based on the name, command, and parameter variables. For example, an Eclipse process might have the following values in these variables:

<table id="table_kdz_jgv_1q"><tbody><tr><td>

name

</td><td>

"eclipse"

</td></tr><tr><td>

command

</td><td>

"/glide/eclipse/Eclipse.app/Contents/MacOS/eclipse"

</td></tr><tr><td>

parameter

</td><td>

"-psn\_0\_1884620"

</td></tr></tbody>
</table>If an Eclipse application runs on a computer called machineA, ServiceNow names the application eclipse@machineA. The following script appends the parameter value as part of the application name.

```
var computerName = g_sensor.deviceGR.name;
var processClassiferName = g_classification.name;
current.name = processClassiferName + parameters + "@" + computerName;
```

In this example, the name of the application record becomes eclipse-psn\_0\_1884620@machineA.

Sometimes it is useful to pass values to the triggered probes in the process classification. You can do this by creating a custom script that defines a name/value pair for the `g_probe_parameters` object. For example:

```
g_probe_parameters['processCommand'] = command;
```

In this example, when a classification record triggers a probe, the script passes the probe a parameter called `processCommand` with the value of the `command` variable.

## Script objects

Use these objects in the script:

|Script object|Description|
|-------------|-----------|
|current|Points to a JavaScript object with its \[property:value\] pair to update the application record. \(It is not an actual GlideRecord object of the application.\)|
|g\_sensor|Points to the running process sensor class. This object contains a deviceGR object, which points to the computer CI record on which the process resides.|
|g\_classification|Points to the process classifier record itself.|
|name|Points to the process name.|
|command|Points to the process command.|
|parameters|Points to the process parameters.|
|g\_probe\_parameters|A JavaScript object that will allow parameter passing to the triggered probes.|

**Related topics**  


[Create a Discovery process handler](../task/t_CreateAProcessHandler.md)

