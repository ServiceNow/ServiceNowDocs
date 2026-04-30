---
title: Example custom Discovery probe and sensor: populate a CI with text file values
description: This custom Discovery probe helps you if you need to read a text file from a Windows computer and populate a CI in the CMDB with the values from the file.
locale: en-US
release: xanadu
product: Discovery
classification: discovery
topic_type: task
last_updated: "2025-09-16"
reading_time_minutes: 2
breadcrumb: [Discovery probes and sensors, Discovery, ITOM Visibility, IT Operations Management]
---

# Example custom Discovery probe and sensor: populate a CI with text file values

This custom Discovery probe helps you if you need to read a text file from a Windows computer and populate a CI in the CMDB with the values from the file.

## Before you begin

Role required: admin

## About this task

In this example the user wanted to read files created by BGinfo.

**Note:** When you have completed the probe and sensor, place the probe in the appropriate Windows classifier at **Discovery Definition** &gt; **CI Classification** &gt; **Windows**.

## Procedure

1.  Navigate to **Discovery Definition** &gt; **Probes**, and then click **New**.

2.  Complete the following fields:

    -   Name: Unique and descriptive name for the probe
    -   Probe type: Select **Probe**.
    -   Description: Describe the function of this probe.
    -   Used by Discovery: Select this check box
    -   ECC queue topic: This is name of the probe the MID server is to run. In this example, we use WMIRunner.
    -   ECC queue name: In this example, we use the descriptive name WMI: BGInfo files.
3.  Right-click in the header bar and select **Save** from the context menu.

4.  Select the Probe Parameters tab in the Probe form, and then click **New**.

5.  Enter `WMI_GetFiles.js` as the Name of this parameter.

6.  Copy the script below into the Script field and edit as needed.

7.  Click **Submit**.

    ```
    
    //
     // Use ServiceNow WMIAPI to gather stats
     //
     var CMD_RETRIES = 3;
     var scanner = getScanner();
     if (scanner) {
       var output = "";
       for(var i = 0; i < CMD_RETRIES; i++) {
          output = scanner.winExec("%SystemRoot%\\system32\\cmd.exe /C type \\\"C:\\Information Systems\\BgInfo\\*.txt\\\"");
          if (output)
             break;
       }
       scanner.appendToRoot("output", output);
     }
    ```

8.  Navigate to **Discovery Definition** &gt; **Sensors**, and then click **New**.

    Complete the following fields:

    -   Name: Use the same name as the matching probe. In this example, we use Windows - Get BGInfo files.
    -   Reacts to probe: The name of the probe created in the previous procedure: Windows - Get BGInfo files
    -   Sensor type: Select the type of sensor to create - in this example Sensor.
    -   Description: Describes the function of this sensor.
    -   Script: Copy the script below into the Script field and edit as needed.
    -   Sensor type: Determines how the answer from the probe is processed - in this example JavaScript.
9.  Click **Submit**.

    ```
     
     
    new DiscoverySensor({ data: {}, process: function(result) { 
     
            this.parseOutput(result.output);
            this.update(this.data);
        },
     
     parseOutput: function(output) {
            var currentFile;
            var files = {};
     
     if (output.startsWith("<wmi")) {
                var bgout = new XMLHelper(output).toObject();
                if (!bgout)
                    return;
     
     output = bgout.output;
            }
     
     var lines = output.split(/\n/);
     
     for(var i = 0; i < lines.length; i++) {
                var line = lines[i];
                if (line.startsWith("C:\\Information Systems\\BgInfo\\")) {
                    currentFile = line.substr(30);
                    files[currentFile] = "";
                } else if (currentFile) {
                    var newLine = line.trim();
                    if (newLine)
                        files[currentFile] += (files[currentFile]? "\n&nbsp;" : "") + newLine;
                }
            }
     
     this.data['u_jack_id'] = files['JackID.txt'];
     this.data['warranty_expiration'] = files['Warranty.txt'];
     this.data['po_number'] = files['Ponum.txt'];},
     type: "DiscoverySensor"
     
     });
    
    ```


**Parent Topic:**[Discovery probes and sensors](../../../product/discovery/concept/c_DiscoveryProbesAndSensors.md)

